---
description: Erstellt einen E/A-Abschlussport (Input/Output, E/A) und ordnet ihn einem angegebenen Dateihandle zu, oder erstellt einen E/A-Abschlussport, der noch keinem Dateihandle zugeordnet ist, sodass die Zuordnung zu einem späteren Zeitpunkt möglich ist.
ms.assetid: 40cb47fc-7b15-47f6-bee2-2611d4686053
title: CreateIoCompletionPort-Funktion (IoAPI.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateIoCompletionPort
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 6612c3087841aa0c13f131581f8a05c29403e4fccf81bd6f0dc338b1dd9e42a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083160"
---
# <a name="createiocompletionport-function"></a>CreateIoCompletionPort-Funktion

Erstellt einen E/A-Abschlussport (Input/Output, E/A) und ordnet ihn einem angegebenen Dateihandle zu, oder erstellt einen E/A-Abschlussport, der noch keinem Dateihandle zugeordnet ist, sodass die Zuordnung zu einem späteren Zeitpunkt möglich ist.

Durch das Zuordnen einer Instanz eines geöffneten Dateihandle zu einem E/A-Abschlussport kann ein Prozess eine Benachrichtigung über den Abschluss asynchroner E/A-Vorgänge empfangen, die dieses Dateihandle betreffen.

> [!Note]
>
> Der hier verwendete Begriff *Dateihandle* bezieht sich auf eine Systemabstraktion, die einen überlappende E/A-Endpunkt darstellt, nicht nur eine Datei auf dem Datenträger. Alle Systemobjekte, die überlappende E/A unterstützen, z. B. Netzwerkendpunkte, TCP-Sockets, Named Pipes und E-Mail-Slots, können als Dateihandles verwendet werden. Weitere Informationen finden Sie im Abschnitt "Hinweise".

 

## <a name="syntax"></a>Syntax


```C++
HANDLE WINAPI CreateIoCompletionPort(
  _In_     HANDLE    FileHandle,
  _In_opt_ HANDLE    ExistingCompletionPort,
  _In_     ULONG_PTR CompletionKey,
  _In_     DWORD     NumberOfConcurrentThreads
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FileHandle* \[ In\]
</dt> <dd>

Ein geöffnetes Dateihandle oder **INVALID \_ HANDLE \_ VALUE**.

Das Handle muss für ein Objekt sein, das überlappende E/A unterstützt.

Wenn ein Handle bereitgestellt wird, muss es für die überlappende E/A-Vervollständigung geöffnet worden sein. Sie müssen z. B. das **FLAG FILE \_ FLAG \_ OVERLAPPED** angeben, wenn Sie die [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) verwenden, um das Handle abzurufen.

Wenn **INVALID \_ HANDLE \_ VALUE** angegeben wird, erstellt die Funktion einen E/A-Abschlussport, ohne ihn einem Dateihandle zuzuordnen. In diesem Fall muss der *ExistingCompletionPort-Parameter* **NULL** sein, und der *CompletionKey-Parameter* wird ignoriert.

</dd> <dt>

*ExistingCompletionPort* \[ in, optional\]
</dt> <dd>

Ein Handle für einen vorhandenen E/A-Abschlussport oder **NULL.**

Wenn dieser Parameter einen vorhandenen E/A-Abschlussport angibt, ordnet die Funktion ihn dem durch den *FileHandle-Parameter* angegebenen Handle zu. Die Funktion gibt bei Erfolg das Handle des vorhandenen E/A-Abschlussports zurück. Es wird kein neuer E/A-Abschlussport erstellt.

Wenn dieser Parameter **NULL** ist, erstellt die Funktion einen neuen E/A-Abschlussport und ordnet ihn dem neuen E/A-Abschlussport zu, wenn der *FileHandle-Parameter* gültig ist. Andernfalls erfolgt keine Zuordnung des Dateihandle. Die Funktion gibt bei Erfolg das Handle an den neuen E/A-Abschlussport zurück.

</dd> <dt>

*CompletionKey* \[ In\]
</dt> <dd>

Der benutzerdefinierte Vervollständigungsschlüssel pro Handle, der in jedem E/A-Vervollständigungspaket für das angegebene Dateihandle enthalten ist. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

*NumberOfConcurrentThreads* \[ In\]
</dt> <dd>

Die maximale Anzahl von Threads, die das Betriebssystem zur gleichzeitigen Verarbeitung von E/A-Abschlusspaketen für den E/A-Abschlussport zulassen kann. Dieser Parameter wird ignoriert, wenn der *ExistingCompletionPort-Parameter* nicht **NULL** ist.

Wenn dieser Parameter 0 (null) ist, lässt das System so viele gleichzeitig ausgeführte Threads zu, wie Prozessoren im System vorhanden sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert das Handle für einen E/A-Abschlussport:

-   Wenn der *ExistingCompletionPort-Parameter* **NULL** war, ist der Rückgabewert ein neues Handle.

-   Wenn der *ExistingCompletionPort-Parameter* ein gültiges E/A-Abschlussporthandle war, entspricht der Rückgabewert dem gleichen Handle.

-   Wenn der *FileHandle-Parameter* ein gültiges Handle war, ist dieses Dateihandle jetzt dem zurückgegebenen E/A-Abschlussport zugeordnet.

Wenn die Funktion fehlschlägt, ist der Rückgabewert **NULL.** Um erweiterte Fehlerinformationen abzurufen, rufen Sie die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Hinweise

Das E/A-System kann angewiesen werden, E/A-Abschlussbenachrichtigungspakete an E/A-Abschlussports zu senden, wo sie in die Warteschlange eingereiht werden. Die **CreateIoCompletionPort-Funktion** stellt diese Funktionalität bereit.

Ein E/A-Abschlussport und sein Handle sind dem Prozess zugeordnet, der ihn erstellt hat, und können nicht zwischen Prozessen aufgeteilt werden. Ein einzelnes Handle kann jedoch zwischen Threads im gleichen Prozess aufgeteilt werden.

**CreateIoCompletionPort** kann in drei verschiedenen Modi verwendet werden:

-   Erstellen Sie nur einen E/A-Abschlussport, ohne ihn einem Dateihandle zuzuordnen.
-   Ordnen Sie einem Dateihandle einen vorhandenen E/A-Abschlussport zu.
-   Führen Sie die Erstellung und Zuordnung in einem einzigen Aufruf aus.

Um einen E/A-Abschlussport ohne Zuordnung zu erstellen, legen Sie den *FileHandle-Parameter* auf **INVALID HANDLE \_ \_ VALUE,** den *ExistingCompletionPort-Parameter* auf **NULL** und den *CompletionKey-Parameter* auf 0 (in diesem Fall ignoriert) fest. Legen Sie den *Parameter NumberOfConcurrentThreads* auf den gewünschten Parallelitätswert für den neuen E/A-Abschlussport oder null für den Standardwert (die Anzahl der Prozessoren im System) fest.

Das im *FileHandle-Parameter* übergebene Handle kann ein beliebiges Handle sein, das überlappende E/A unterstützt. In der Regel handelt es sich dabei um ein Handle, das von der [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) mit dem **FLAG FILE FLAG \_ \_ OVERLAPPED** geöffnet wird (z. B. Dateien, E-Mail-Slots und Pipes). Objekte, die von anderen Funktionen wie [**Sockets**](/windows/desktop/api/winsock2/nf-winsock2-socket) erstellt werden, können auch einem E/A-Abschlussport zugeordnet werden. Ein Beispiel für die Verwendung von Sockets finden Sie unter [**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex). Ein Handle kann nur einem E/A-Abschlussport zugeordnet werden, und nachdem die Zuordnung vorgenommen wurde, bleibt das Handle diesem E/A-Abschlussport zugeordnet, bis es geschlossen wird.

Weitere Informationen zur E/A-Abschlussport-Theorie, -Verwendung und zugehörigen Funktionen finden Sie unter [E/A-Abschlussports.](i-o-completion-ports.md)

Mehrere Dateihandles können einem einzelnen E/A-Abschlussport zugeordnet werden, indem **CreateIoCompletionPort** mehrmals mit dem gleichen E/A-Abschlussporthandle im *ExistingCompletionPort-Parameter* und einem anderen Dateihandle im *FileHandle-Parameter* aufgerufen wird.

Verwenden Sie den *CompletionKey-Parameter,* um Ihrer Anwendung zu helfen, nachzuverfolgen, welche E/A-Vorgänge abgeschlossen wurden. Dieser Wert wird nicht von **CreateIoCompletionPort** für das funktionale Steuerelement verwendet. stattdessen wird es an das Dateihandle angefügt, das im *FileHandle-Parameter* zum Zeitpunkt der Zuordnung zu einem E/A-Abschlussport angegeben ist. Dieser Vervollständigungsschlüssel sollte für jedes Dateihandle eindeutig sein und das Dateihandle während des internen Abschlusswarteschlangenprozesses begleitet. Sie wird im [**GetQueuedCompletionStatus-Funktionsaufruf**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) zurückgegeben, wenn ein Abschlusspaket eingeht. Der *CompletionKey-Parameter* wird auch von der [**PostQueuedCompletionStatus-Funktion**](postqueuedcompletionstatus.md) verwendet, um Ihre eigenen speziellen Vervollständigungspakete in die Warteschlange zu stellen.

Nachdem eine Instanz eines geöffneten Handles einem E/A-Abschlussport zugeordnet wurde, kann sie nicht in der [**ReadFileEx-**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) oder [**WriteFileEx-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) verwendet werden, da diese Funktionen über eigene asynchrone E/A-Mechanismen verfügen.

Es ist am besten, ein Dateihandle, das einem E/A-Abschlussport zugeordnet ist, nicht mithilfe der Handlevererbung oder eines Aufrufs der [**DuplicateHandle-Funktion**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) freizugeben. Vorgänge, die mit solchen doppelten Handles ausgeführt werden, generieren Vervollständigungsbenachrichtigungen. Es wird eine sorgfältige Überlegung empfohlen.

Das E/A-Abschlussporthandle und jedes Dateihandle, das diesem bestimmten E/A-Abschlussport zugeordnet ist, werden als *Verweise auf den E/A-Abschlussport* bezeichnet. Der E/A-Abschlussport wird freigegeben, wenn keine Verweise mehr darauf vorhanden sind. Daher müssen alle diese Handles ordnungsgemäß geschlossen werden, um den E/A-Abschlussport und die zugehörigen Systemressourcen freizugeben. Wenn diese Bedingungen erfüllt sind, schließen Sie das E/A-Abschlussporthandle, indem Sie die [**CloseHandle-Funktion**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) aufrufen.

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
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[XP-Desktop-Apps \| UWP-Apps\]<br/>                                                                                                                                                                                                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows UWP-Apps für \[ Server 2003-Desktop-Apps \|\]<br/>                                                                                                                                                                                                                                              |
| Header<br/>                   | <dl> <dt>IoAPI.h (include Windows.h);</dt> <dt>WinBase.h auf Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP (einschließlich Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



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

[Windows Sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

**Funktionen**
</dt> <dt>

[**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> <dt>

[**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

