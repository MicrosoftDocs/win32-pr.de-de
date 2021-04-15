---
description: Die getcapturetimestamp-Funktion gibt das Datum und die Uhrzeit zurück, zu der die Erfassung mit dem Aufzeichnen von Frames begonnen hat
ms.assetid: a7120a7c-5031-4c71-a177-f08c41037b3c
title: Getcapturetimestamp-Funktion (Netmon. h)
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
ms.openlocfilehash: 855aa8b5432fd06bb25571fcb48c091dcfe502f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525139"
---
# <a name="getcapturetimestamp-function"></a>Getcapturetimestamp-Funktion

Die **getcapturetimestamp** -Funktion gibt das Datum und die Uhrzeit zurück, zu der die Erfassung mit dem Aufzeichnen von Frames begonnen hat

## <a name="syntax"></a>Syntax


```C++
LPSYSTEMTIME WINAPI GetCaptureTimeStamp(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hcapture* \[ in\]
</dt> <dd>

Handle für die Erfassung. Weitere Informationen zum Abrufen des Aufzeichnungs Handles finden Sie im Abschnitt "Hinweise" in diesem Thema zu **getcapturetimestamp** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf eine [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Struktur.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

Die **getcapturetimestamp** -Funktion gibt die Zeit zurück, zu der der Netzwerk Paketanbieter (NPP) mit dem Sammeln von Daten beginnt, nicht, wenn der Experte die Erfassung für die Analyse lädt.

Überschreiben Sie die Daten in der **SYSTEMTIME** -Struktur nicht. Die Daten sind Teil der Erfassung. Der Versuch, die Daten zu ändern, verursacht eine Zugriffsverletzung.

[*Experten*](e.md) und [*Parser*](p.md) können die **getcapturetimestamp** -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[System Time](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 

