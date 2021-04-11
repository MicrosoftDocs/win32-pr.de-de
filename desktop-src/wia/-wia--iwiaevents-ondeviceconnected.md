---
description: Das Ereignis tritt auf, wenn ein neues Hardware Gerät für Windows-Abbild Beschaffung (WIA) verbunden ist.
ms.assetid: 327a29b8-581c-41b5-bea7-068bec95e653
title: WIA. onabviceconnected-Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceConnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 952b738e8afa0850bd67bab1206382e96419513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216061"
---
# <a name="wiaondeviceconnected-event"></a>WIA. onabviceconnected-Ereignis

Das Ereignis tritt auf, wenn ein neues Hardware Gerät für Windows-Abbild Beschaffung (WIA) verbunden ist.

## <a name="syntax"></a>Syntax


```JScript
Wia.OnDeviceConnected(
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

WIA benachrichtigt das Skript oder die Anwendung immer dann, wenn ein neues Hardware Gerät mit dem Computer verbunden ist. Implementieren Sie die **objwia** \_ **ondeviceconnected ()** -Unterroutine, damit das Skript oder die Anwendung auf die Geräte Verbindung reagieren kann.

Beispielsweise kann es sein, dass ein Skript die [**Geräte**](-wia-iwia-devices.md) Sammlung aktualisiert, wenn ein neues Gerät installiert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4,90 oder höher)</dt> </dl> |



 

 




