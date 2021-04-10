---
description: Die commitspooldata-Funktion benachrichtigt den Druck Spooler, dass eine angegebene Datenmenge in eine angegebene Spooldatei geschrieben wurde und zum Rendern bereit ist.
ms.assetid: cb8899e0-2fdf-4928-adff-17ef5af39f63
title: Commitspooldata-Funktion (winspool. h)
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
ms.openlocfilehash: fa90cb1344e7c087a601a74991598e509daed226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864760"
---
# <a name="commitspooldata-function"></a>Commitspooldata-Funktion

Die **commitspooldata** -Funktion benachrichtigt den Druck Spooler, dass eine angegebene Datenmenge in eine angegebene Spooldatei geschrieben wurde und zum Rendern bereit ist.

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

*hprinter* \[ in\]
</dt> <dd>

Ein Handle für den Drucker, an den der Auftrag übermittelt wurde. Dabei sollte es sich um das gleiche Handle handeln, das zum Abrufen von *hspoolfile* mit [**getspoolfilehandle**](getspoolfilehandle.md)verwendet wurde.

</dd> <dt>

*hspoolfile* \[ in\]
</dt> <dd>

Ein Handle für die Spooldatei, die geändert wird. Beim ersten Aufrufen von **commitspooldata** sollte dies das gleiche Handle sein, das von [**getspoolfilehandle**](getspoolfilehandle.md)zurückgegeben wurde. Nachfolgende Aufrufe von **commitspooldata** sollten das vom vorhergehenden-Aufruf zurückgegebene Handle übergeben. Siehe Hinweise.

</dd> <dt>

*cbcommit* 
</dt> <dd>

Die Anzahl der Bytes, die an den Druck Spooler übertragen wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird ein Handle für die Spooldatei zurückgegeben.

Wenn die Funktion fehlschlägt, wird ein ungültiger handle-Wert zurückgegeben \_ \_ .

## <a name="remarks"></a>Bemerkungen

Anwendungen, die einen spoolerdruckauftrag übermitteln, können [**getspoolfilehandle**](getspoolfilehandle.md) aufrufen und dann Daten direkt in das spooldateihandle schreiben, indem Sie " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile)" aufrufen. Um den Druck Spooler zu benachrichtigen, dass die Datei Daten enthält, die zum Rendern bereit sind, muss die Anwendung **commitspooldata** aufzurufen und die Anzahl der verfügbaren Bytes angeben.

Wenn **commitspooldata** mehrmals aufgerufen wird, muss jeder Aufruf das spooldateihandle verwenden, das vom vorherigen Aufruf zurückgegeben wurde. Wenn keine weiteren Daten in die Spooldatei geschrieben werden, sollte [**closespoolfilehandle**](closespoolfilehandle.md) für das Datei Handle aufgerufen werden, das durch den letzten Aufruf von **commitspooldata** zurückgegeben wurde.

Vor dem Aufrufen von **commitspooldata** müssen Anwendungen den Dateizeiger auf die Position festlegen, die vor dem Schreiben von Daten in die Datei aufgetreten ist. Beim Rendern der Daten in der spoolerdatei verschiebt der Druck Spooler den spooldateizeiger *cbcommit* Bytes aus dem aktuellen Wert des Dateizeigers.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Getspoolfilehandle**](getspoolfilehandle.md)
</dt> <dt>

[**Closespoolfilehandle**](closespoolfilehandle.md)
</dt> </dl>

 

