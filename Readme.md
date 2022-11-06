# psych-engine-fps 
 
how to add psych engine fps to your game!!!  

1. Drag and Drop the folder and the file into the folder called "source".

2. Go into Main.hx and remove this code. 

		#if !mobile
		addChild(new FPS(10, 3, 0xFFFFFF));
		#end 
		 
		 
4. paste the fps var next to skip splash
```
public static var fpsVar:FPS;
```       

5. Paste this new FPS into Main.hx  
 
		#if !mobile
		fpsVar = new FPS(10, 3, 0xFFFFFF);
		addChild(fpsVar);
		Lib.current.stage.align = "tl";
		Lib.current.stage.scaleMode = StageScaleMode.NO_SCALE;
		if(fpsVar != null) {
			fpsVar.visible = ClientPrefs.showFPS;
		}
		#end

4. import this code on Main.hx 
	import openfl.display.StageScaleMode;
	import ClientPrefs; 
      
Now you add psych engine fps into your engine!!! 

# Credits  
- [Psych engine](https://github.com/ShadowMario/FNF-PsychEngine) - For da fps
