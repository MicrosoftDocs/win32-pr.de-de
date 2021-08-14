---
description: Das Ereignis tritt auf, wenn Windows WIA-Hardwaregerät (Image Acquisition) getrennt wird.
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: Wia.OnDeviceDisconnected-Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceDisconnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: b9d61d196e3a9a7471b9a1fb1ab86c3ba918427ccc5dd5060ffaabdf28f80871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442156"
---
# <a name="wiaondevicedisconnected-event"></a>Wia.OnDeviceDisconnected-Ereignis

Das Ereignis tritt auf, wenn Windows WIA-Hardwaregerät (Image Acquisition) getrennt wird.

## <a name="syntax"></a>Syntax


```JScript
Wia.OnDeviceDisconnected(
  Id
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Id* 
</dt> <dd>

Eine Zeichenfolge, die die ID des verbundenen Geräts enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

WIA benachrichtigt das Skript oder die Anwendung, wenn ein Hardwaregerät vom Computer getrennt ist. Implementieren Sie **die Unterroutine objWia** \_ **OnDeviceDisconnected(),** damit das Skript oder die Anwendung auf die Trennung der Geräteverbindung reagieren kann.

Sie möchten beispielsweise, dass ein Skript die [**Gerätesammlung**](-wia-iwia-devices.md) aktualisiert, wenn ein Gerät vom Computer entfernt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4.90 oder höher)</dt> </dl> |



 

 




