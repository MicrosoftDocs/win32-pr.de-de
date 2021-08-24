---
description: Ruft mehrere Abschlussporteinträge gleichzeitig ab.
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: GetQueuedCompletionStatusEx-Funktion (IoAPI.h)
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
ms.openlocfilehash: f81bc0c997e3637fa941cb5a23f6394ba1f585566c8d633cadb00c9fd75ac805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696120"
---
# <a name="getqueuedcompletionstatusex-function"></a>GetQueuedCompletionStatusEx-Funktion

Ruft mehrere Abschlussporteinträge gleichzeitig ab. Er wartet, bis ausstehende E/A-Vorgänge, die dem angegebenen Abschlussport zugeordnet sind, abgeschlossen sind.

Verwenden Sie die [**GetQueuedCompletionStatus-Funktion,**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) um E/A-Vervollständigungspakete einzeln aus der Klammer zu nehmen.

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

*CompletionPort* \[ In\]
</dt> <dd>

Ein Handle für den Abschlussport. Verwenden Sie zum Erstellen eines Abschlussports die [**CreateIoCompletionPort-Funktion.**](createiocompletionport.md)

</dd> <dt>

*lpCompletionPortEntries* \[ out\]
</dt> <dd>

Zeigt bei der Eingabe auf ein vorab zugeordnetes Array von [**OVERLAPPED \_ ENTRY-Strukturen.**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry)

Empfängt bei der Ausgabe ein Array von [**OVERLAPPED \_ ENTRY-Strukturen,**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) die die Einträge enthalten. Die Anzahl der Arrayelemente wird von *ulNumEntriesRemoved* bereitgestellt.

Die Anzahl der während jeder E/A übertragenen Bytes, der Vervollständigungsschlüssel, der angibt, in welcher Datei jede E/A aufgetreten ist, und die überlappende Strukturadresse, die in jeder ursprünglichen E/A verwendet wird, werden alle im *lpCompletionPortEntries-Array* zurückgegeben.

</dd> <dt>

*ulCount* \[ In\]
</dt> <dd>

Die maximale Anzahl von Einträgen, die entfernt werden sollen.

</dd> <dt>

*ulNumEntriesRemoved* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der tatsächlich entfernten Einträge empfängt.

</dd> <dt>

*dwMilliseconds* \[ In\]
</dt> <dd>

Die Anzahl von Millisekunden, die der Aufrufer warten möchte, bis ein Abschlusspaket am Abschlussport angezeigt wird. Wenn ein Vervollständigungspaket nicht innerhalb der angegebenen Zeit angezeigt wird, tritt für die Funktion ein Time out auf und gibt **FALSE** zurück.

Wenn *dwMilliseconds* **auf INFINITE** (0xFFFFFFFF) festgelegt ist, tritt für die Funktion nie ein Time out auf. Wenn *dwMilliseconds* 0 (null) ist und kein E/A-Vorgang zum Aussetzen aus der Klammer vorhanden ist, tritt für die Funktion sofort ein Time out auf.

</dd> <dt>

*fAlertable* \[ In\]
</dt> <dd>

Wenn dieser Parameter **FALSE** ist, gibt die Funktion erst dann zurück, wenn der Time out-Zeitraum abgelaufen ist oder ein Eintrag abgerufen wurde.

Wenn der Parameter **TRUE** ist und keine Einträge verfügbar sind, führt die Funktion eine warnungsfähige Wartezeit aus. Der Thread gibt zurück, wenn das System eine E/A-Abschlussroutine oder APC in die Warteschlange des Threads einreiht und der Thread die Funktion ausführt.

Eine Abschlussroutine wird in die Warteschlange eingereiht, wenn die [**ReadFileEx-**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) oder [**WriteFileEx-Funktion,**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) in der sie angegeben wurde, abgeschlossen wurde und der aufrufende Thread der Thread ist, der den Vorgang initiiert hat. Ein APC wird in die Warteschlange eingereiht, wenn Sie [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc)aufrufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 **(TRUE)** zurück, andernfalls 0 **(FALSE).**

Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ordnet einen Thread dem angegebenen Abschlussport zu. Ein Thread kann höchstens einem Abschlussport zugeordnet werden.

Diese Funktion gibt **TRUE** zurück, wenn mindestens eine ausstehende E/A abgeschlossen ist, aber es ist möglich, dass ein oder mehrere E/A-Vorgänge fehlgeschlagen sind. Beachten Sie, dass es dem Benutzer dieser Funktion obliegt, die Liste der zurückgegebenen Einträge im *lpCompletionPortEntries-Parameter* zu überprüfen, um zu bestimmen, welche von ihnen allen möglichen fehlgeschlagenen E/A-Vorgängen entsprechen, indem der Status im **lpOverlapped-Member** in jedem [**OVERLAPPED \_ ENTRY-Element**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry)betrachtet wird.

Diese Funktion gibt **FALSE** zurück, wenn kein E/A-Vorgang aus der Klammer genommen wurde. Dies bedeutet in der Regel, dass beim Verarbeiten der Parameter für diesen Aufruf ein Fehler aufgetreten ist oder dass das *CompletionPort-Handle* geschlossen wurde oder anderweitig ungültig ist. Die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) stellt erweiterte Fehlerinformationen bereit.

Wenn bei einem Aufruf von [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) ein Fehler auftritt, weil das zugeordnete Handle geschlossen ist, gibt die Funktion **FALSE** zurück, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt **ERROR ABANDONED WAIT \_ \_ \_ 0** zurück.

Serveranwendungen können über mehrere Threads verfügen, die die **GetQueuedCompletionStatusEx-Funktion** für denselben Abschlussport aufrufen. Wenn E/A-Vorgänge abgeschlossen sind, werden sie in der Reihenfolge des ersten In-First-Out-Vorgangs an diesem Port in die Warteschlange eingereiht. Wenn ein Thread aktiv auf diesen Aufruf wartet, schließt eine oder mehrere Anforderungen in der Warteschlange den Aufruf nur für diesen Thread ab.

Weitere Informationen zur E/A-Abschlussport-Theorie, -Verwendung und zugehörigen Funktionen finden Sie unter [E/A-Abschlussports.](i-o-completion-ports.md)

In Windows 8 und Windows Server 2012 wird diese Funktion von den folgenden Technologien unterstützt.



| Technologie                                           | Unterstützt      |
|------------------------------------------------------|----------------|
| Server Message Block (SMB) 3.0-Protokoll<br/>   | Ja<br/> |
| Transparentes SMB 3.0-Failover (TFO)<br/>        | Ja<br/> |
| SMB 3.0 mit Dateifreigaben mit aufskalieren (SO)<br/>   | Ja<br/> |
| Freigegebenes Clustervolume File System (CsvFS)<br/> | Ja<br/> |
| Robustes Dateisystem (Resilient File System, ReFS)<br/>              | Ja<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Vista-Desktop-Apps \| UWP-Apps\]<br/>                                                                                                                                                                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für Server \[ 2008-Desktop-Apps \|\]<br/>                                                                                                                                                                                                             |
| Header<br/>                   | <dl> <dt>IoAPI.h (include Windows.h);</dt> <dt>WinBase.h auf Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista (einschließlich Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Übersichtsthemen**
</dt> <dt>

[Dateiverwaltungsfunktionen](file-management-functions.md)
</dt> <dt>

[E/A-Abschlussports](i-o-completion-ports.md)
</dt> <dt>

[Verwenden der Windows-Header](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

**Funktionen**
</dt> <dt>

[**ConnectNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
</dt> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> <dt>

[**TransactNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
</dt> <dt>

[**WaitCommEvent**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> </dl>

 

