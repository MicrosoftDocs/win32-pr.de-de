---
description: Die Create-Methode des DeviceInfo-Objekts stellt eine Verbindung mit dem vom DeviceInfo-Objekt angegebenen wia-Gerät (Windows Image Acquisition) her und gibt ein Item-Objekt zurück, das das Gerät darstellt.
ms.assetid: 57f3698c-3f9f-4775-8b53-a65a5591aa3d
title: DeviceInfo.Create-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: bf0ff85733e71ce9425ae8176d9f6d0b97a3c85d0c4892145c112e6f42dd7036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670233"
---
# <a name="deviceinfocreate-method"></a>DeviceInfo.Create-Methode

Die **Create-Methode** des [**DeviceInfo-Objekts**](-wia-deviceinfo.md) stellt eine Verbindung mit dem vom **DeviceInfo-Objekt** angegebenen Windows Image Acquisition-Gerät her und gibt ein [**Item-Objekt**](-wia-item.md) zurück, das das Gerät darstellt.

## <a name="syntax"></a>Syntax


```JScript
retVal = DeviceInfo.Create()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **IWiaDispatchItem**

Diese Methode gibt das [**Item-Objekt**](-wia-item.md) zurück, das das erstellte Gerät darstellt.

## <a name="remarks"></a>Hinweise

Verwenden **Sie** die Create-Methode, um nach dem Aufzählen der Sammlung Geräte eine Verbindung mit einem [**WIA-Hardwaregerät**](-wia-iwia-devices.md) herzustellen. Die -Methode gibt ein [**Item-Objekt**](-wia-item.md) zurück, das das Gerät (ein Stammelement) darstellt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **Create-Methode** veranschaulicht.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objDeviceInfo.Create()
Next
</SCRIPT>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4.90 oder höher)</dt> </dl> |



 

 




