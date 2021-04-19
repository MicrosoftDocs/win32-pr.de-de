---
description: Sammlung von "de viceinfo"-Objekten, die alle auf dem Computer installierten Geräte darstellen.
ms.assetid: 2f124188-2b66-46cc-9b26-bfef3709a1af
title: WIA. Devices (Eigenschaft)
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
ms.openlocfilehash: d03aa0b7e73d5dfbc6449816f3b64147e51db882
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356533"
---
# <a name="wiadevices-property"></a>WIA. Devices (Eigenschaft)

Sammlung von " [**de viceinfo**](-wia-deviceinfo.md) "-Objekten, die alle auf dem Computer installierten Geräte darstellen. Schreibgeschützt.

> [!Note]  
> Diese Auflistung ist 0-basiert.

 

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Wia.Devices
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="examples"></a>Beispiele

Das folgende Beispiel veranschaulicht die Verwendung der **Geräte** Auflistung zum Auflisten der Geräte in einem System.


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
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4,90 oder höher)</dt> </dl> |



 

 




