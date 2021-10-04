# Action_Cube_XiaoxinSGSIs

> 仅支持Android R
>
> 支持自定义精简功能
>
> 当前版本: [v11](https://github.com/xiaoxindada/SGSI-build-tool/tree/11)
>
> 注意：如果提示失败并在 下载ROM... 时出现 Error: Process completed with exit code 127. 系服务器网络问题，请重试

## 快速开始

1. Fork此仓库
   
   首次使用时，你需要先**Fork此仓库**，然后再进行参数配置

2. 配置参数

   假设你此时已经Fork本仓库并进入自己的仓库，点击菜单中 **Actions - 左栏All workflows下的SGSI_Build - 右侧 Run workflow 灰色按钮 - 填写相应参数**

   |说明               |Name       |Value(按你自己的需求填写)                                                 |
   |:------:           |:------:   | :------------------------:                                               |
   |待制作包链接       |ROM_URL    |https://hugeota.d.miui.com/21.9.28/miui_DAVINCI_21.9.28_48aa8cdf69_11.0.zip|
   |待制作包名称       |ZIP_NAME   |miui_DAVINCI_21.9.28_48aa8cdf69_11.0.zip                                   |
   |待制作包种类       |OS_TYPE    |miui                                                                      |
   |打包名称           |REPACK_NAME|MIUI＿SGSI.zip                                                                  |

3. 开始制作
   
   点击Run workflow绿色按钮即可开始制作

## 个性化配置

1. 自定义精简功能
   
   修改apps_clean文件夹下对应系统的精简脚本，请自行参照修改

2.关于Prepare-app

   每次跑sgsi时回自动生成Prepare-app.zip
   prepare-app.zip里包含用vendor修bug的文件夹，因为是自动化所
   以需要大家解压自己筛选，用于补驱动,所以文件不加筛选对自己的
   vendor乱补几乎不会成功。

## 后续步骤

由于wetransfer限制，制作后的SGSI若超过**2GB**则**无法上传**，因此本Action将自动根据制作后的SGSI大小选择**直接上传**/**分卷上传**

若以分卷方式上传，请下载每个分卷后手动合卷解压

```
下载完用cat命令合并，例如
cat MIUI_GSI.zip00 MIUI_GSI.zip01 MIUI_GSI.zip02 >MIUI_GSI.tar.gz  #合并
tar xzvf MIUI_GSI.tar.gz                                           #解压

## 版权与致谢

本项目受https://github.com/xiaoxindada/SGSI-build-action   和   https://github.com/XayahSuSuSu/Action-SGSI-build    项目启发。
感谢[xiaoxindada](https://github.com/xiaoxindada)的开源。
