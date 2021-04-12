---
description: Das Ereignis tritt auf, wenn ein neues Hardware Gerät für die Windows-Abbild Erfassung (WIA) getrennt ist.
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: WIA. ondevicedevi-Ereignis
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
ms.openlocfilehash: 45652f3c447c1dd0f59b0470823782c6ba635cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216060"
---
# <a name="wiaondevicedisconnected-event"></a>WIA. ondevicedevi-Ereignis

Das Ereignis tritt auf, wenn ein neues Hardware Gerät für die Windows-Abbild Erfassung (WIA) getrennt ist.

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

## <a name="remarks"></a>Bemerkungen

WIA benachrichtigt das Skript oder die Anwendung immer dann, wenn ein Hardware Gerät vom Computer getrennt wird. Implementieren Sie die **objwia** \_ **ondevicedevi()** -Unterroutine, damit das Skript oder die Anwendung auf die Trennung des Geräts reagieren kann.

Beispielsweise möchten Sie möglicherweise ein Skript aktualisieren, um die [**Geräte**](-wia-iwia-devices.md) Sammlung zu aktualisieren, wenn ein Gerät vom Computer entfernt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4,90 oder höher)</dt> </dl> |



 

 




