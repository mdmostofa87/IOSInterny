//
//  ViewController.swift
//  ScrollView
//
//  Created by MacBook Air on 29/12/19.
//  Copyright © 2019 MacBook Air. All rights reserved.
//

import UIKit

class ViewController: UIViewController,UIScrollViewDelegate {
    override func viewDidLoad() {
        super.viewDidLoad()
        ScrollView.delegate = self
        setupScroll()
    }
    

    @IBOutlet weak var ScrollView: UIScrollView!
    
    @IBOutlet weak var PageControl: UIPageControl!
    var contentWidth : CGFloat = 0.0
    
    func setupScroll(){
    for image in 0...3 {
    let imageToDisplay = UIImage(named:"\(image).png")
    let imageView = UIImageView(image:imageToDisplay)
        let xCoordinate = view.frame.midX+view.frame.width*CGFloat(image)
        contentWidth += view.frame.width
        ScrollView.addSubview(imageView)
        imageView.frame = CGRect(x:xCoordinate - 50, y:(view.frame.height/2) - 50, width:250, height:250)
        }
        ScrollView.contentSize = CGSize(width:contentWidth, height:view.frame.height)
    }
    
    func scrollViewDidScroll(_ scrollView: UIScrollView) {
        print(scrollView.contentOffset)
        
        PageControl.currentPage = Int(scrollView.contentOffset.x/CGFloat(414))
    }
    
}

