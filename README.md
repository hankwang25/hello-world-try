# hello-world-try
#Just a try at Github
#compress size of pictures 压缩图片尺寸
from PIL import Image
import os.path
import glob
def convertjpg(jpgfile,outdir,width=1280,height=720):
    img=Image.open(jpgfile)   
    new_img=img.resize((width,height),Image.BILINEAR)   
    new_img.save(os.path.join(outdir,os.path.basename(jpgfile)))
for jpgfile in glob.glob("E:/pythonExercise/*.jpg"):
    convertjpg(jpgfile,"E:/pythonExercise")
