---
description: Die Funktion wiaadddevice Ruft die Benutzeroberfläche des Assistenten zum Installieren von Scanner und Kameras auf. Dies entspricht der Ausführung von &\# 0034; rundll32.exe STI \_ci.dll AddDevice&\# 0034; von der Eingabeaufforderung aus.
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: Wiaadddevice-Funktion (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaAddDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 694265f0a59096a5a6a58ccbf4e43c92e21fe9b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751752"
---
# <a name="wiaadddevice-function"></a>Wiaadddevice-Funktion

Die Funktion **wiaadddevice** Ruft die Benutzeroberfläche des Assistenten zum Installieren von Scanner und Kameras auf. Dies entspricht der Ausführung von "rundll32.exe STI \_ci.dll AddDevice" an der Eingabeaufforderung.

## <a name="syntax"></a>Syntax


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion sollte mit Administrator Anmelde Informationen aufgerufen werden. Bei der Ausführung unter der Benutzerkontensteuerung (LUA) sollte der Prozess erhöht werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Installwiadevice**](-wia-installwiadevice.md)
</dt> </dl>

 

 




