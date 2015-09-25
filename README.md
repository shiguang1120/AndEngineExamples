# AndEngineExamples 导入资源是会报错

# 错误一：	Description Resource Path Location Type
	Type mismatch: cannot convert from void to AnimatedSprite BoundCameraExample.java /AndEngineExamples/src/org/andengine/examples line 220 Java Problem
 
#解决办法：
	final AnimatedSprite face = new AnimatedSprite(pX, pY, this.mBoxFaceTextureRegion, this.getVertexBufferObjectManager()).animate(100);  
#改为：
	final AnimatedSprite face = new AnimatedSprite(pX, pY, this.mBoxFaceTextureRegion, this.getVertexBufferObjectManager());  
	face.animate(100);  
 
 
# 错误二：Description Resource Path Location Type
	The constructor TextOptions(AutoWrap, float, float, HorizontalAlign) is undefined TextBreakExample.java /AndEngineExamples/src/org/andengine/examples line 106 Java Problem
 
#解决办法：
	this.mText = new Text(50, 40, this.mFont, "", 1000, new TextOptions(AutoWrap.LETTERS, AUTOWRAP_WIDTH, Text.LEADING_DEFAULT, HorizontalAlign.CENTER), vertexBufferObjectManager);  
#改为：
	this.mText = new Text(50, 40, this.mFont, "", 1000, new TextOptions(AutoWrap.LETTERS, AUTOWRAP_WIDTH,  HorizontalAlign.CENTER, Text.LEADING_DEFAULT), vertexBufferObjectManager);  
 
# 错误三：DrawMode cannot be resolved to a variable
 
#解决办法：
	import org.andengine.entity.primitive.vbo.DrawMode;  
#改为：
	import org.andengine.entity.primitive.DrawMode;  
 

