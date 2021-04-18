---
description: Beendet den miracast-senkenmodus, deaktiviert die Auffindbarkeit und hebt die Registrierung des Rückrufs auf.
ms.assetid: 38AE60CB-F601-4C03-A725-9B802341B84B
title: WF-displaysink-Funktion (wsdsink. h)
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
ms.openlocfilehash: d1ebaa9920ca7d38cff22cef6383b37065faa2ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347294"
---
# <a name="wfddisplaysinkstop-function"></a>Wsddisplaysink-Funktion

Beendet den miracast-senkenmodus, deaktiviert die Auffindbarkeit und hebt die Registrierung des Rückrufs auf. Ihre APP sollte diese einmal beim Herunterfahren anrufen.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI WFDStopDisplaySink(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

## <a name="remarks"></a>Bemerkungen

Es wird erwartet, dass Ihre APP die Blockierung aller aktuell ausgeführten Rückrufe aufgehoben hat, bevor **wfdstopdisplaysink** aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows 10<br/>                                                                      |
| Ende des Supports (Server)<br/>    | Windows Server 2016<br/>                                                             |
| Header<br/>                   | <dl> <dt>WF-Senke. h</dt> </dl>       |
| Bibliothek<br/>                  | <dl> <dt>Wifdisplay. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



 

 




