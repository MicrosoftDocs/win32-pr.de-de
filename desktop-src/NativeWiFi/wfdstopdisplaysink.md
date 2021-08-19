---
description: Beendet den Miracast Senkenmodus, deaktiviert die Auffindbarkeit und deaktiviert die Registrierung des Rückrufs.
ms.assetid: 38AE60CB-F601-4C03-A725-9B802341B84B
title: WFDDisplaySinkStop-Funktion (Wfdsink.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStopDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: a5e2da91e29535c1e2fd9553a2b6ec2bb0008e61f33cd55ebcda2746b93eb657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797930"
---
# <a name="wfddisplaysinkstop-function"></a>WFDDisplaySinkStop-Funktion

Beendet den Miracast Senkenmodus, deaktiviert die Auffindbarkeit und deaktiviert die Registrierung des Rückrufs. Ihre App sollte dies einmal beim Herunterfahren aufrufen.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI WFDStopDisplaySink(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS.

## <a name="remarks"></a>Hinweise

Es wird erwartet, dass Ihre App die Blockierung aller ausgeführten Rückrufe aufgehoben hat, bevor **WFDStopDisplaySink** aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows 10<br/>                                                                      |
| Ende des Supports (Server)<br/>    | Windows Server 2016<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl>       |
| Bibliothek<br/>                  | <dl> <dt>Wifidisplay.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



 

 




