# Problem
my problem encouted during my learing

matplotlib绘图时，中文显示乱码问题解决：

1. 查看matplotlib字体安装位置：
import matplotlib    
print(matplotlib.matplotlib_fname())

2. 下载字体，并将字体转到matplotlib字体目录下，一般位于/lib/python3.5/site-packages/matplotlib/mpl-data/fonts/ttf

3.删除字体缓存文件
rm /home/.cache/matplotlib

4.加入如下代码：
from pylab import mpl
mpl.rcParams['font.sans-serif']=['SimHei']
mpl.rcParams['axes.unicode_minus']=False

5.重启程序
