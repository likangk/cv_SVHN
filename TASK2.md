### 数据读取
``` class SVHNDataset(Dataset):
def __init__(self, img_path, img_label, transform=None):
self.img_path = img_path self.img_label = img_label if transform is not None:
self.transform = transform else:
self.transform = None def __getitem__(self, index):
img = Image.open(self.img_path[index]).convert('RGB') if self.transform is not None:
img = self.transform(img)
```
### 数据扩充函数
1. transforms.CenterCrop 
2. transforms.ColorJitter 
3. transforms.FiveCrop
4. transforms.Grayscale 
5. transforms.Pad 
6. transforms.RandomAffine
7. transforms.RandomCrop 
8. transforms.RandomHorizontalFlip
9. transforms.RandomRotation 
10. transforms.RandomVerticalFlip 
在baseline上测试数据扩充的效果

### 还有一部分pytorch的练习在另一台电脑上，明天加进本笔记
