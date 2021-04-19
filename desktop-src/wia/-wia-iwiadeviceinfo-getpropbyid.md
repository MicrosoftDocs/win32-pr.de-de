---
description: Die getpropbyid-Methode des DeviceInfo-Objekts verwendet die ID einer Geräte Eigenschaft, um ihren Wert zurückzugeben.
ms.assetid: 9c68e6af-446c-4750-89e6-70862b23b296
title: Deviceingefo. getpropbyid-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: adbc8b6a29f97066c8dc5b2e45b7ddc5834f2b60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350238"
---
# <a name="deviceinfogetpropbyid-method"></a>Deviceingefo. getpropbyid-Methode

Die **getpropbyid** -Methode des [**deviceInfo**](-wia-deviceinfo.md) -Objekts verwendet die ID einer Geräte Eigenschaft, um ihren Wert zurückzugeben.

## <a name="syntax"></a>Syntax


```JScript
retVal = DeviceInfo.GetPropById(
  Id
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Typ: **[wiadeviceinf opropertyid](-wia-wiadeviceinfopropertyid.md)**

Gibt die ID der Eigenschaft an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **Variant**

Diese Methode gibt den Wert der Eigenschaft zurück, die durch *ID* angegeben wird.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, um den Wert einer Geräte Eigenschaft aus der ID zu suchen. Eine Liste der Eigenschaften-IDs finden Sie unter [Eigenschaften konstanter Definitionen von WIA](-wia-wia-property-constant-definitions.md). Weitere Informationen zu den Eigenschaften der Windows-Abbild Erfassung (WIA) selbst finden Sie unter [WIA Property Konstanten](-wia-wia-property-constants.md).

Fügen Sie für Microsoft Visual Basic-Anwendungen einen Verweis auf die Typbibliothek "Windows-Abbild Erfassung 1,01" hinzu. Die folgenden Konstanten, die in dieser Datei definiert sind, sind für diese Methode gültig:

``` syntax
const DeviceID = 2
const Manufacturer = 3
const Description = 4
const Type = 5
const Port = 6
const Name = 7
const Server = 8
const RemoteDevID = 9
const UIClassID = 10
```

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird veranschaulicht, wie die **getpropbyid** -Methode verwendet wird, um einen Eigenschafts Wert abzurufen.


```JScript
<SCRIPT LANGUAGE="VBScript">
const WIA_DIP_DEV_TYPE = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    PropValue = objDeviceInfo.GetPropById(WIA_DIP_DEV_TYPE)
Next
</SCRIPT>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4,90 oder höher)</dt> </dl> |



 

 




