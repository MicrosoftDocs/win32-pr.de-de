---
description: Die getpropbyid-Methode des Item-Objekts verwendet die ID einer Item-Eigenschaft, um ihren Wert zurückzugeben.
ms.assetid: 00f7a91c-fd55-4016-a932-f710045a14b8
title: Item. getpropbyid-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 54eb329d51005893b89a9fd28f160ff616e682df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353473"
---
# <a name="itemgetpropbyid-method"></a>Item. getpropbyid-Methode

Die **getpropbyid** -Methode des [**Item**](-wia-item.md) -Objekts verwendet die ID einer Item-Eigenschaft, um ihren Wert zurückzugeben.

## <a name="syntax"></a>Syntax


```JScript
retVal = Item.GetPropById(
  Id
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Typ: **[wiaitempropertyid](-wia-wiaitempropertyid.md)**

Gibt die ID der Eigenschaft an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **Variant**

Diese Methode gibt den Wert der Eigenschaft zurück, die durch *ID* angegeben wird.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, um den Wert einer Element Eigenschaft aus der ID zu suchen. Eine Liste der Eigenschaften-IDs finden Sie unter [Eigenschaften konstanter Definitionen von WIA](-wia-wia-property-constant-definitions.md). Weitere Informationen zu den Eigenschaften selbst finden Sie unter [WIA Property Konstanten](-wia-wia-property-constants.md).

Fügen Sie für Microsoft Visual Basic-Anwendungen einen Verweis auf die Typbibliothek "Windows-Abbild Erfassung 1,01" hinzu. Die folgenden Konstanten, die in dieser Datei definiert sind, sind nur für Stamm Elemente (Geräte Elemente) gültig:

``` syntax
const FirmwareVersion = 1026
const ConnectStatus = 1027
const DeviceTime = 1028
const PicturesTaken = 2050
const PicturesRemaining = 2051
const ExposureMode = 2052
const ExposureCompensation = 2053
const ExposureTime = 2054
const FNumber = 2055
const FlashMode = 2056
const FocusMode = 2057
const FocusManualDist = 2058
const ZoomPosition = 2059
const PanPosition = 2060
const TiltPostion = 2061
const TimerMode = 2062
const TimerValue = 2063
const PowerMode = 2064
const BatteryStatus = 2065
const Dimension = 2070
const HorizontalBedSize = 3074
const VerticalBedSize = 3075
const HorizontalSheetFeedSize = 3076
const VerticalSheetFeedSize = 3077
const SheetFeederRegistration = 3078
const HorizontalBedRegistration = 3079
const VerticalBedRegistraion = 3080
const PlatenColor = 3081
const PadColor = 3082
const FilterSelect = 3083
const DitherSelect = 3084
const DitherPatternData = 3085
const DocumentHandlingCapabilities = 3086
const DocumentHandlingStatus = 3087
const DocumentHandlingSelect = 3088
const DocumentHandlingCapacity = 3089
const HorizontalOpticalResolution = 3090
const VerticalOpticalResolution = 3091
const EndorserCharacters = 3092
const EndorserString = 3093
const ScanAheadPages = 3094
const MaxScanTime = 3095
const Pages = 3096
const PageSize = 3097
const PageWidth = 3098
const PageHeight = 3099
const Preview = 3100
const TransparencyAdapter = 3101
const TransparecnyAdapterSelect = 3102
```

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird veranschaulicht, wie die **getpropbyid** -Methode verwendet wird, um einen Eigenschafts Wert abzurufen.


```JScript
<SCRIPT LANGUAGE="VBScript">
const DeviceType = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    objRootItem=objDeviceInfo.Create()
    objSelectedItems=objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItem
    PropValue = objItem.GetPropById(DeviceType)
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4,90 oder höher)</dt> </dl> |



 

 




