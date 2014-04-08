# DrawView
Subclass of UIView that supports drawing.

# Basic Usage
Using CocoaPods

	pod "DrawView"

In the storyboard under the views Identity Inspector set the view class to ```DrawView```. 

![](readmeassets/screen_shot_1.png)

In the implementation file you can setup the drawing view. 

	[drawingView setBackgroundColor:[UIColor whiteColor]];
	[drawingView strokeColor:[UIColor blackColor]];

# Usage
## Drawing Existing Paths
You can draw either a existing ```UIBezierPath``` or ```CGPathRef``` by calling either of the following methods respectively.

	- (void)drawBezier:(UIBezierPath *)path;
	- (void)drawPath:(CGPathRef)path;

## Animating Path
To animate the current path in the draw view simply call
	
	- (void)animatePath;

![](readmeassets/animation.gif)

## Debugging Drawing
To debug the path simply set ```debugBox``` to ```true```. This will add a grey box around the bounds of the current path.

![](readmeassets/screen_shot_2.png)