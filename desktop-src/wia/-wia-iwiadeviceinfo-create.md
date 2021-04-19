---
description: Die Create-Methode des DeviceInfo-Objekts stellt eine Verbindung mit dem durch das deviceInfo-Objekt angegebenen Windows-Abbild Erfassungsgerät (WIA) her und gibt ein Element Objekt zurück, das das Gerät darstellt.
ms.assetid: 57f3698c-3f9f-4775-8b53-a65a5591aa3d
title: Deviceingefo. Create-Methode
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
ms.openlocfilehash: 1efc36ea8794de4b64c9af616320b09d547f6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372881"
---
# <a name="deviceinfocreate-method"></a>Deviceingefo. Create-Methode

Die **Create** -Methode des [**deviceInfo**](-wia-deviceinfo.md) -Objekts stellt eine Verbindung mit dem durch das **deviceInfo** -Objekt angegebenen Windows-Abbild Erfassungsgerät (WIA) her und gibt ein [**Element**](-wia-item.md) Objekt zurück, das das Gerät darstellt.

## <a name="syntax"></a>Syntax


```JScript
retVal = DeviceInfo.Create()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **iwiadispatchitem**

Diese Methode gibt das [**Item**](-wia-item.md) -Objekt zurück, das das erstellte Gerät darstellt.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Create** -Methode, um eine Verbindung mit einem WIA-Hardware Gerät zu erstellen, nachdem Sie die [**Geräte**](-wia-iwia-devices.md) Sammlung aufgelistet haben. Die-Methode gibt ein [**Item**](-wia-item.md) -Objekt zurück, das das Gerät darstellt (ein root-Element).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **Create** -Methode veranschaulicht.


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
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4,90 oder höher)</dt> </dl> |



 

 




