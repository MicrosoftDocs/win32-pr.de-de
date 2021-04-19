---
description: Ruft mehrere Vervollständigungs Port Einträge gleichzeitig ab.
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: GetQueuedCompletionStatus usex-Funktion (ioapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetQueuedCompletionStatusEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: d45471cc066e6de7cb388036e06e727fe828a532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353937"
---
# <a name="getqueuedcompletionstatusex-function"></a>GetQueuedCompletionStatus usex-Funktion

Ruft mehrere Vervollständigungs Port Einträge gleichzeitig ab. Er wartet auf den Abschluss ausstehender e/a-Vorgänge, die dem angegebenen Abschlussport zugeordnet sind.

Um die e/a-Abschluss Pakete einzeln aus der Warteschlange zu entfernen, verwenden Sie die [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI GetQueuedCompletionStatusEx(
  _In_  HANDLE             CompletionPort,
  _Out_ LPOVERLAPPED_ENTRY lpCompletionPortEntries,
  _In_  ULONG              ulCount,
  _Out_ PULONG             ulNumEntriesRemoved,
  _In_  DWORD              dwMilliseconds,
  _In_  BOOL               fAlertable
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Completionport* \[ in\]
</dt> <dd>

Ein Handle für den Abschlussport. Um einen Abschlussport zu erstellen, verwenden Sie die Funktion " [**kreateiocompletionport**](createiocompletionport.md) ".

</dd> <dt>

*lpcompletionportentries* \[ vorgenommen\]
</dt> <dd>

Bei der Eingabe verweist auf ein vorab zugeordneter Array von überlappenden [**\_ Eintrags**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) Strukturen.

Bei der Ausgabe empfängt ein Array von [**überlappenden \_ Eintrags**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) Strukturen, die die Einträge enthalten. Die Anzahl der Array Elemente wird von *ulnumentriesremoved* bereitgestellt.

Die Anzahl von Bytes, die während der einzelnen e/a-Vorgänge übertragen werden, der Abschluss Schlüssel, der angibt, für welche Datei die einzelnen e/As aufgetreten sind, und die überlappende Struktur Adresse, die in den einzelnen ursprünglichen e/a-Vorgängen verwendet wird, werden im *lpcompletionportentries*

</dd> <dt>

*ulcount* \[ in\]
</dt> <dd>

Die maximale Anzahl der zu entfernenden Einträge.

</dd> <dt>

*ulnumentriesentfernt* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der tatsächlich entfernten Einträge empfängt.

</dd> <dt>

*dwmillisekunden* \[ in\]
</dt> <dd>

Die Anzahl der Millisekunden, die der Aufrufer warten soll, bis ein abschlusspaket am Abschlussport angezeigt wird. Wenn ein Vervollständigungs Paket nicht innerhalb der angegebenen Zeit angezeigt wird, tritt bei der Funktion ein Timeout auf, und es wird **false** zurückgegeben.

Wenn *dwMilliseconds* **unendlich** (0xFFFFFFFF) ist, tritt für die Funktion kein Timeout auf. Wenn *dwMilliseconds* gleich 0 (null) ist und kein e/a-Vorgang zum Entfernen der Warteschlange vorhanden ist, tritt für die Funktion sofort ein Timeout ein.

</dd> <dt>

*falertable* \[ in\]
</dt> <dd>

Wenn dieser Parameter **false** ist, wird die Funktion erst zurückgegeben, wenn der Timeout Zeitraum abgelaufen ist oder ein Eintrag abgerufen wird.

Wenn der-Parameter den Wert **true** hat und keine Einträge verfügbar sind, führt die Funktion eine warterattabellenwartezeit aus. Der Thread gibt zurück, wenn das System eine e/a-Abschluss Routine oder APC in die Warteschlange für den Thread fügt und der Thread die Funktion ausführt.

Eine Vervollständigungs Routine wird in die Warteschlange eingereiht, wenn die Funktion "read [**fileex**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) " oder " [**schreitefileex**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) ", in der Sie angegeben wurde, abgeschlossen wurde und der aufrufende Thread der Thread ist, der den Vorgang initiiert Ein APC wird in die Warteschlange eingereiht, wenn [**queueuserapc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc)aufgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (**true**) zurück, wenn erfolgreich, andernfalls 0 (**false**).

Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ordnet einen Thread dem angegebenen Abschlussport zu. Einem Thread kann höchstens ein Abschlussport zugeordnet werden.

Diese Funktion gibt **true** zurück, wenn mindestens ein ausstehender e/a-Vorgang abgeschlossen ist. es ist jedoch möglich, dass bei mindestens einem e/a-Vorgang ein Fehler aufgetreten ist. Beachten Sie, dass es für den Benutzer dieser Funktion ist, die Liste der zurückgegebenen Einträge im *lpcompletionportentries* -Parameter zu überprüfen, um zu bestimmen, welche von Ihnen mögliche fehlgeschlagene e/a-Vorgänge entsprechen, indem Sie den Status des **lpoverllapp** -Elements in jedem überlappenden [**\_ Eintrag**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry)betrachten.

Diese Funktion gibt **false** zurück, wenn kein e/a-Vorgang aus der Warteschlange entfernt wurde. Dies bedeutet in der Regel, dass bei der Verarbeitung der Parameter für diesen Befehl ein Fehler aufgetreten ist oder dass der *completionport* -Handle geschlossen oder anderweitig ungültig ist. Die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion stellt erweiterte Fehlerinformationen bereit.

Wenn beim Aufrufen von " [**GetQueuedCompletionStatus usex**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) " ein Fehler auftritt, weil das zugeordnete Handle geschlossen ist, gibt die Funktion " **false** " zurück, und " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " gibt einen Fehler zurück, der **\_ abgebrochen \_ \_** wurde

Server Anwendungen können mehrere Threads aufweisen, die die Funktion **GetQueuedCompletionStatus usex** für denselben Abschlussport aufrufen. Wenn e/a-Vorgänge durchgeführt werden, werden Sie in der Reihenfolge für die erstmaligen Ausführung in die Warteschlange dieses Ports eingereiht. Wenn ein Thread aktiv auf diesen-Befehl wartet, schließt mindestens eine in der Warteschlange befindliche Anforderung den-Befehl nur für diesen Thread aus.

Weitere Informationen zu e/a-Abschluss Port Theorie, Verwendung und zugehörigen Funktionen finden Sie unter e [/](i-o-completion-ports.md)a-Abschlussports.

In Windows 8 und Windows Server 2012 wird diese Funktion von den folgenden Technologien unterstützt.



| Technologie                                           | Unterstützt      |
|------------------------------------------------------|----------------|
| Server Message Block-Protokoll (SMB) 3,0<br/>   | Ja<br/> |
| SMB 3,0 transparent Failover (TFO)<br/>        | Ja<br/> |
| SMB 3,0 mit Dateifreigaben mit horizontaler Skalierung (also)<br/>   | Ja<br/> |
| Freigegebenes Clustervolume Datei System (csvfs)<br/> | Ja<br/> |
| Robustes Dateisystem (Resilient File System, ReFS)<br/>              | Ja<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                                                                                                                                                                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]<br/>                                                                                                                                                                                                             |
| Header<br/>                   | <dl> <dt>Ioapi. h (Include Windows. h); </dt> <dt>Winbase. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übersichts Themen**
</dt> <dt>

[Dateiverwaltungsfunktionen](file-management-functions.md)
</dt> <dt>

[E/a-Abschlussports](i-o-completion-ports.md)
</dt> <dt>

[Verwenden der Windows-Header](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

**Funktionen**
</dt> <dt>

[**Connectnamedpipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
</dt> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**GetQueuedCompletionStatus usex**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**Lockfileex**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[**' PostQueuedCompletionStatus '**](postqueuedcompletionstatus.md)
</dt> <dt>

[**Transactnamedpipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
</dt> <dt>

[**WaitCommEvent**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> </dl>

 

