# LYSDatePicker

当前最高版本:0.0.2

LYSDatePicker is mainly to adapt to the scenes that need to choose the date in daily development. The bottom layer is mainly implemented by UIPickerView and UIDatePicker components. Since this is just released, there may be bugs in the middle of use, so you need to ask for it, I will try to fix it.

![iOS技术群群二维码](https://github.com/LIYANGSHUAI/LYSDatePicker/blob/master/resource/iOS技术群群二维码.JPG)

使用方法:(目前支持iOS 8.0以上)

其实这个插件我没有在iOS 8.0以下测过,自我认为应该没有使用那些iOS 8之前和之后有改动的API,但是我在集成Cocoapods时,选的支持环境是iOS 8以上,如果要在iOS 8以下使用,直接拷贝文件到项目即可

为了方便大家引入,我加入了Cocoapods管理,使用终端 pod search LYSDatePicker

不出意外的情况下,会查出

```objc
-> LYSDatePicker (版本号)
I hope everyone will give me some advice during the process of use. I want to
go further.
pod 'LYSDatePicker', '~> 版本号'
- Homepage: https://github.com/LIYANGSHUAI/LYSDatePicker
- Source:   https://github.com/LIYANGSHUAI/LYSDatePicker.git
- Versions: 版本列表 [master repo]
(END)
```

直接粘贴: pod 'LYSDatePicker', '~> 版本号'

Here is the usage scenario I thought of as much as possible, as a reference

![效果图](https://github.com/LIYANGSHUAI/LYSDatePicker/blob/master/resource/目录.png)
![效果图](https://github.com/LIYANGSHUAI/LYSDatePicker/blob/master/resource/系统(时间).png)
![效果图](https://github.com/LIYANGSHUAI/LYSDatePicker/blob/master/resource/系统(日期).png)
![效果图](https://github.com/LIYANGSHUAI/LYSDatePicker/blob/master/resource/系统(日期和时间).png)
![效果图](https://github.com/LIYANGSHUAI/LYSDatePicker/blob/master/resource/自定义(时间).png)
![效果图](https://github.com/LIYANGSHUAI/LYSDatePicker/blob/master/resource/自定义(时间12小时).png)
![效果图](https://github.com/LIYANGSHUAI/LYSDatePicker/blob/master/resource/自定义(日期).png)
![效果图](https://github.com/LIYANGSHUAI/LYSDatePicker/blob/master/resource/自定义(日期和星期).png)
![效果图](https://github.com/LIYANGSHUAI/LYSDatePicker/blob/master/resource/自定义(日期和时间).png)
![效果图](https://github.com/LIYANGSHUAI/LYSDatePicker/blob/master/resource/自定义(日期和时间和星期).png)
![效果图](https://github.com/LIYANGSHUAI/LYSDatePicker/blob/master/resource/自定义(年和日期).png)
![效果图](https://github.com/LIYANGSHUAI/LYSDatePicker/blob/master/resource/自定义(年和日期和时间).png)
![效果图](https://github.com/LIYANGSHUAI/LYSDatePicker/blob/master/resource/自定义(年和日期和时间和星期).png)
![效果图](https://github.com/LIYANGSHUAI/LYSDatePicker/blob/master/resource/自定义(年和日期和星期).png)
![效果图](https://github.com/LIYANGSHUAI/LYSDatePicker/blob/master/resource/自定义(年和日期和时间和星期12小时).png)


```objc
LYSDatePicker *pickerView = [[LYSDatePicker alloc] initWithFrame:CGRectMake(0, 100, CGRectGetWidth(self.view.frame), 256) type:(LYSDatePickerTypeSystem)];
pickerView.date = [NSDate date];
pickerView.headerView.headerBar = self.headerBar;
pickerView.delegate = self;
pickerView.dataSource = self;
[self.view addSubview:pickerView];
```

```objc
pickerView.datePickerMode = LYSDatePickerModeTime;
```

```objc
pickerView.datePickerMode = LYSDatePickerModeDate;
```
