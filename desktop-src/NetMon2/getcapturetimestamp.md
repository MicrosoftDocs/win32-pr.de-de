---
description: Die GetCaptureTimeStamp-Funktion gibt die Uhrzeit und das Datum zurück, zu der die Aufzeichnung mit der Aufzeichnung von Frames begonnen hat.
ms.assetid: a7120a7c-5031-4c71-a177-f08c41037b3c
title: GetCaptureTimeStamp-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 93ae1c94a5e83d0029aba4403ad4ba23db0f4006bb5b9be68cc469939e63c734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366635"
---
# <a name="getcapturetimestamp-function"></a>GetCaptureTimeStamp-Funktion

Die **GetCaptureTimeStamp-Funktion** gibt die Uhrzeit und das Datum zurück, zu der die Aufzeichnung mit der Aufzeichnung von Frames begonnen hat.

## <a name="syntax"></a>Syntax


```C++
LPSYSTEMTIME WINAPI GetCaptureTimeStamp(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hCapture* \[ In\]
</dt> <dd>

Handle für die Erfassung. Informationen zum Abrufen des Erfassungshandle finden Sie im Abschnitt "Hinweise" dieses **GetCaptureTimeStamp-Themas.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf eine [SYSTEMTIME-Struktur.](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **NULL.**

## <a name="remarks"></a>Hinweise

Die **GetCaptureTimeStamp-Funktion** gibt den Zeitpunkt zurück, zu dem der Netzwerkpaketanbieter (Network Packet Provider, NPP) mit dem Sammeln von Daten beginnt, nicht, wenn der Experte die Erfassung zur Analyse lädt.

Überschreiben Sie die Daten nicht in der **SYSTEMTIME-Struktur.** Die Daten sind Teil der Erfassung. Der Versuch, die Daten zu ändern, verursacht eine Zugriffsverletzung.

[*Experten*](e.md) und [*Parser*](p.md) können die **GetCaptureTimeStamp-Funktion** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systemtime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 

