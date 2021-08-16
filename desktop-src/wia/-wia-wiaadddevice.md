---
description: Die WiaAddDevice-Funktion ruft die Benutzeroberfläche des Scanner- und Kamerainstallations-Assistenten auf. Dies entspricht der Ausführung von &\# 0034;rundll32.exe sti \_ci.dll AddDevice&\# 0034; über die Eingabeaufforderung.
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: WiaAddDevice-Funktion (Wia.h)
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
ms.openlocfilehash: 81dcff3cdca3459126751b12b86f1e11adc2b4fec8926f69211f0508253b64fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965399"
---
# <a name="wiaadddevice-function"></a>WiaAddDevice-Funktion

Die **WiaAddDevice-Funktion** ruft die Benutzeroberfläche des Scanner- und Kamerainstallations-Assistenten auf. Dies entspricht der Ausführung von "rundll32.exe sti \_ci.dll AddDevice" über die Eingabeaufforderung.

## <a name="syntax"></a>Syntax


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion sollte mit Administratoranmeldeinformationen aufgerufen werden. Bei der Ausführung unter Benutzerkontensteuerung (USER Account Control, LUA) sollte der Prozess mit erhöhten Rechten ausgeführt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**InstallWiaDevice**](-wia-installwiadevice.md)
</dt> </dl>

 

 




