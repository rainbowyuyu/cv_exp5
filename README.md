# cv_exp5  
计算机视觉实验5  

![logo](logo.png)

## 单文档一键化实验操作，分步调试实现  

这个相当于是计算机视觉中比较基础的操作。如果想体验更完整的功能，可以参考 YOLO 的文档；本实验较为基础，按照 README 文档一步步调试即可。  
YOLO 详细参考 [Ultralytics](https://github.com/ultralytics/yolov5)。  

> **注意**：模型在 CPU 上运行时间较长。如果没有服务器租赁经验，这里直接提供模型，在 `./saved_models` 中，但准确率较低（batch size=32, epoch=5, acc=0.91），供大家随意使用。  

---

## 相较于老师版本的改进和修正  

1. **分步实现**：清晰化文件分支，单文档实现。  
2. **更新 GPU 检测代码**：自动检测是否支持 GPU 运算。  
3. **添加自动分类的 JSON 函数**：便于生成分类文件。  
4. **添加数据集的自动划分代码**：支持数据集自动划分为训练集和验证集。  
5. **修正 classes 分支的列表层数**：确保数据格式正确。  
6. **删除模型训练的延迟参数**：优化模型训练过程。  
7. **改进 reload 弃用函数**：避免调用已弃用的 API。  

---

## 详细使用方法  

1. 安装依赖：  
   ```bash
   pip install -r requirements.txt
   ```

   -加入按照时有什么数据包不成功，建议新建一个conda环境
   ```bash
   conda create -n [env-name] [python-version]
   conda activate [env-name]
   pip install -r requirements.txt
   ```
   
3. 注意事项：
- 根据实际情况调整 CUDA 和 cuDNN 的版本。
- 分步操作时，需要调整 mode 参数以及文件路径

3. 模式选择：
-  0  -- 一键化操作  
-   1  -- 分类已生成  
-   2  -- 完成数据集划分  
-   3  -- 分步可视化  
-   4  -- 完成模型训练  
-   5  -- 完成预测

## 大致最终文件结构
base  
├── evaluate  
├── Plant_leave_diseases_dataset_with_augmentation  
├── saved_models  
├── train  
├── val  
├── categories.json  
├── cv_exp5.ipynb  
