---
description: Sammlung von DeviceInfo-Objekten, die alle auf dem Computer installierten Geräte darstellt.
ms.assetid: 2f124188-2b66-46cc-9b26-bfef3709a1af
title: Wia.Devices-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Devices
- SafeWia.Devices
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: b6cf843d92b5ce2260578b653a1163526b22fb735c01542d772b2687ca890dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208923"
---
# <a name="wiadevices-property"></a>Wia.Devices-Eigenschaft

Sammlung von [**DeviceInfo-Objekten,**](-wia-deviceinfo.md) die alle auf dem Computer installierten Geräte darstellt. Schreibgeschützt.

> [!Note]  
> Diese Auflistung ist 0-basiert.

 

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="examples"></a>Beispiele

Das folgende Beispiel veranschaulicht die Verwendung der Sammlung **Geräte** zum Aufzählen der Geräte auf einem System.


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    ! Do something with the DeviceInfo object
Next
</SCRIPT>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4.90 oder höher)</dt> </dl> |



 

 




