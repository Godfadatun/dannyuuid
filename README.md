# dannyuuid.js

This is a simple cdn i built after searching all of the internet for code or plugin that could get you your device details using javascript anyway i found this 
npm package from https://github.com/biggora/device-uuid/

he really helped me out so i decided to convert it into a cdn so we can all use it on the fly without any node_modules

<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/Godfadatun/dannyuuid/device-uuid.js"></script>


automatically create not browser depended uuid:

    var uuid = new DeviceUUID().get();

as a result example:

    e9dc90ac-d03d-4f01-a7bb-873e14556d8e

custom device uuid generation:

var du = new DeviceUUID().parse();
    var dua = [
        du.language,
        du.platform,
        du.os,
        du.cpuCores,
        du.isAuthoritative,
        du.silkAccelerated,
        du.isKindleFire,
        du.isDesktop,
        du.isMobile,
        du.isTablet,
        du.isWindows,
        du.isLinux,
        du.isLinux64,
        du.isMac,
        du.isiPad,
        du.isiPhone,
        du.isiPod,
        du.isSmartTV,
        du.pixelDepth,
        du.isTouchScreen
    ];
    var uuid = du.hashMD5(dua.join(':'));

##module provides details such as the following:

{
  "isMobile":false,
  "isDesktop":true,
  "isBot":false,
  .....
  "browser":"Chrome",
  "version":"17.0.963.79",
  "os":"Windows 7",
  "platform":"Microsoft Windows",
  "source":"Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/535.11 (KHTML, like Gecko) Chrome/17.0.963.79..."
}

for further info check https://github.com/biggora
