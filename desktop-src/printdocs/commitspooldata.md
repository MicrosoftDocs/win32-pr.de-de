---
description: Die CommitSpoolData-Funktion benachrichtigt den Druckspooler, dass eine angegebene Datenmenge in eine angegebene Spooldatei geschrieben wurde und zum Rendern bereit ist.
ms.assetid: cb8899e0-2fdf-4928-adff-17ef5af39f63
title: CommitSpoolData-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommitSpoolData
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 90c5907f86f7586710e8a65e60874587491674f2dc4d73d0632279f8b1b3c119
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950500"
---
# <a name="commitspooldata-function"></a>CommitSpoolData-Funktion

Die **CommitSpoolData-Funktion** benachrichtigt den Druckspooler, dass eine angegebene Datenmenge in eine angegebene Spooldatei geschrieben wurde und zum Rendern bereit ist.

## <a name="syntax"></a>Syntax


```C++
HANDLE CommitSpoolData(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile,
       DWORD  cbCommit
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPrinter* \[ In\]
</dt> <dd>

Ein Handle für den Drucker, an den der Auftrag übermittelt wurde. Dies sollte dasselbe Handle sein, das zum Abrufen von *hSpoolFile* mit [**GetSpoolFileHandle verwendet wurde.**](getspoolfilehandle.md)

</dd> <dt>

*hSpoolFile* \[ In\]
</dt> <dd>

Ein Handle für die Spooldatei, die geändert wird. Beim ersten Aufruf von **CommitSpoolData** sollte dies dasselbe Handle sein, das von [**GetSpoolFileHandle zurückgegeben wurde.**](getspoolfilehandle.md) Nachfolgende Aufrufe von **CommitSpoolData** sollten das vom vorherigen Aufruf zurückgegebene Handle übergeben. Siehe Hinweise.

</dd> <dt>

*cbCommit* 
</dt> <dd>

Die Anzahl der Bytes, die an den Druckspooler übertragen wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, wird ein Handle an die Spooldatei zurückgegeben.

Wenn die Funktion fehlschlägt, wird INVALID \_ HANDLE \_ VALUE zurückgegeben.

## <a name="remarks"></a>Hinweise

Anwendungen, die einen Spoolerdruckauftrag übermitteln, können [**GetSpoolFileHandle**](getspoolfilehandle.md) aufrufen und dann daten direkt in das Spooldateihandle schreiben, indem [**sie WriteFile aufrufen.**](/windows/desktop/api/fileapi/nf-fileapi-writefile) Um den Druckspooler zu benachrichtigen, dass die Datei Daten enthält, die gerendert werden können, muss die Anwendung **CommitSpoolData** aufrufen und die Anzahl der verfügbaren Bytes bereitstellen.

Wenn **CommitSpoolData** mehrmals aufgerufen wird, muss jeder Aufruf das vom vorherigen Aufruf zurückgegebene Spooldateihand handle verwenden. Wenn keine daten mehr in die Spooldatei geschrieben werden, sollte [**CloseSpoolFileHandle**](closespoolfilehandle.md) für das Dateihandle aufgerufen werden, das durch den letzten Aufruf von **CommitSpoolData zurückgegeben wurde.**

Vor dem **Aufrufen von CommitSpoolData** müssen Anwendungen den Dateizeiger auf die Position festlegen, die sie hatte, bevor sie Daten in die Datei geschrieben hat. Beim Rendern der Daten in der Spoolerdatei wird der Spooler den Spooldateizeiger *cbCommit* bytes aus dem aktuellen Wert des Dateizeigers verschieben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool.drv</dt> </dl>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetSpoolFileHandle**](getspoolfilehandle.md)
</dt> <dt>

[**CloseSpoolFileHandle**](closespoolfilehandle.md)
</dt> </dl>

 

