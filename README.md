# TagListViewStoryboardBug

This project is intended to show a bug in the [TagListView](https://github.com/xhacker/TagListView) project. When TagListView is embedded in a UITableViewCell in a table that supports self-sizing cells (using UITableViewAutomaticDimension), the tag list view's behavior depends on the frame of the table view controller in the storyboard. If the controller's width in the storyboard is large, the tag list view miscalculates its own height and the cell is incorrectly sized. If the controller's width is small, then the tag view calculates its own height properly and the cell is correctly sized. This project provides a simple example.

When the view controller is the standard 600x600 in the storyboard, the tag list view is cut off:
![FatVC](https://github.com/UberJason/TagListViewStoryboardBug/blob/master/FatVC.png)
![WrongSize](https://github.com/UberJason/TagListViewStoryboardBug/blob/master/WrongSize.png)

When the view controller is reduced to 375x600 in the storyboard, the tag list view is correctly sized:
![ThinVC](https://github.com/UberJason/TagListViewStoryboardBug/blob/master/ThinVC.png)
![RightSize](https://github.com/UberJason/TagListViewStoryboardBug/blob/master/RightSize.png)
