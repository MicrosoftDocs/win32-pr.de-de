---
description: Erstellt einen e/a-Abschluss Anschluss (Input/Output), ordnet ihn einem angegebenen Datei Handle zu oder erstellt einen e/a-Abschlussport, der noch keinem Datei Handle zugeordnet ist und die Zuordnung zu einem späteren Zeitpunkt zulässt.
ms.assetid: 40cb47fc-7b15-47f6-bee2-2611d4686053
title: Funktion "anateiocompletionport" (ioapi. h)
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
ms.openlocfilehash: b85ec931e740de192655ada091a990cd97180b6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360582"
---
# <a name="createiocompletionport-function"></a>Funktion "anateiocompletionport"

Erstellt einen e/a-Abschluss Anschluss (Input/Output), ordnet ihn einem angegebenen Datei Handle zu oder erstellt einen e/a-Abschlussport, der noch keinem Datei Handle zugeordnet ist und die Zuordnung zu einem späteren Zeitpunkt zulässt.

Wenn Sie eine Instanz eines geöffneten Datei Handles mit einem e/a-Abschlussport verknüpfen, kann ein Prozess eine Benachrichtigung über den Abschluss von asynchronen e/a-Vorgängen, die das Datei Handle betreffen, empfangen.

> [!Note]
>
> Der hier verwendete Begriff " *Datei Handle* " bezieht sich auf eine System Abstraktion, die einen überlappenden e/a-Endpunkt darstellt, nicht nur auf eine Datei auf dem Datenträger. Alle Systemobjekte, die überlappende e/a-Vorgänge unterstützen, z. b. Netzwerk Endpunkte, TCP-Sockets, Named Pipes und e-Mail-Slots, können als Datei Handles verwendet werden. Weitere Informationen finden Sie im Abschnitt "Hinweise".

 

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

*FILEHANDLE* \[ in\]
</dt> <dd>

Ein geöffnetes Datei Handle oder ein **ungültiger \_ handle- \_ Wert**.

Das Handle muss ein Objekt sein, das überlappende e/a unterstützt.

Wenn ein Handle bereitgestellt wird, muss es für überlappende e/a-Vervollständigung geöffnet worden sein. Beispielsweise müssen Sie das überlappende Flag für das **\_ Dateiflag \_** angeben, wenn [**Sie das Handle mithilfe der Funktion "**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) -Funktion" abrufen.

Wenn ein **ungültiger \_ handle- \_ Wert** angegeben wird, erstellt die Funktion einen e/a-Abschlussport, ohne ihn einem Datei Handle zuzuordnen. In diesem Fall muss der *existingcompletionport* -Parameter **null** sein, und der *completionkey* -Parameter wird ignoriert.

</dd> <dt>

*Existingcompletionport* \[ in, optional\]
</dt> <dd>

Ein Handle für einen vorhandenen e/a-Abschlussport oder **null**.

Wenn dieser Parameter einen vorhandenen e/a-Abschlussport angibt, ordnet die Funktion ihn dem Handle zu, das durch den *FILEHANDLE* -Parameter angegeben wird. Die-Funktion gibt bei erfolgreicher Ausführung das Handle des vorhandenen e/a-Abschlussports zurück. Es wird kein neuer e/a-Abschlussport erstellt.

Wenn dieser Parameter **null** ist, wird von der Funktion ein neuer e/a-Abschlussport erstellt und, wenn der *FILEHANDLE* -Parameter gültig ist, der neue e/a-Abschlussport zugeordnet. Andernfalls erfolgt keine Zuordnung von Datei Handles. Bei erfolgreicher Ausführung gibt die Funktion das Handle an den neuen e/a-Abschlussport zurück.

</dd> <dt>

*Completionkey* \[ in\]
</dt> <dd>

Der benutzerdefinierte Vervollständigungs Schlüssel pro handle, der in jedem e/a-abschlusspaket für das angegebene Datei Handle enthalten ist. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> <dt>

*Anzahl von concurrentthreads* \[ in\]
</dt> <dd>

Die maximale Anzahl von Threads, die das Betriebssystem für die gleichzeitige Verarbeitung von e/a-Abschluss Paketen für den e/a-Abschlussport zulassen kann. Dieser Parameter wird ignoriert, wenn der *existingcompletionport* -Parameter nicht **null** ist.

Wenn dieser Parameter NULL ist, lässt das System so viele gleichzeitig ausgeführten Threads zu, wie Prozessoren im System vorhanden sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert das Handle für einen e/a-Abschlussport:

-   Wenn der *existingcompletionport* -Parameter **null** war, ist der Rückgabewert ein neues handle.

-   Wenn der *existingcompletionport* -Parameter ein gültiger e/a-Abschluss Port Handle war, ist der Rückgabewert derselbe handle.

-   Wenn der *FILEHANDLE* -Parameter ein gültiges Handle war, ist dieses Datei Handle nun dem zurückgegebenen e/a-Abschlussport zugeordnet.

Wenn die Funktion fehlschlägt, ist der Rückgabewert **null**. Um erweiterte Fehlerinformationen abzurufen, müssen Sie die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion aufrufen.

## <a name="remarks"></a>Bemerkungen

Das e/a-System kann angewiesen werden, e/a-Abschluss Benachrichtigungs Pakete an e/a-Abschlussports zu senden, wo Sie in die Warteschlange gestellt werden. Diese Funktion wird **von der Funktion** "-Funktion" (Funktion) bereitstellt.

Ein e/a-Abschlussport und sein Handle sind dem Prozess zugeordnet, der ihn erstellt hat und der nicht zwischen Prozessen freigegeben werden kann. Ein einzelnes Handle kann jedoch zwischen Threads im gleichen Prozess freigegeben werden.

" **Kreateiocompletionport** " kann in drei verschiedenen Modi verwendet werden:

-   Erstellen Sie nur einen e/a-Abschlussport, ohne ihn einem Datei Handle zuzuordnen.
-   Ordnen Sie einen vorhandenen e/a-Abschlussport einem Datei Handle zu.
-   Führt sowohl die Erstellung als auch die Zuordnung in einem einzelnen-Befehl aus.

Um einen e/a-Abschlussport ohne Zuordnung zu erstellen, legen Sie den *FILEHANDLE* -Parameter auf **einen ungültigen \_ handle- \_ Wert**, den *existingcompletionport* -Parameter auf **null** und den *completionkey* -Parameter auf 0 (null) fest (Dies wird in diesem Fall ignoriert). Legen Sie den Parameter " *numofconcurrentthreads* " auf den gewünschten Parallelitäts Wert für den neuen e/a-Abschlussport oder NULL für den Standardwert (die Anzahl der Prozessoren im System) fest.

Das Handle, das im *FILEHANDLE* -Parameter übergeben wird, kann ein beliebiges Handle sein, das überlappende e/a unterstützt. In den meisten Fällen handelt es sich hierbei um ein Handle [**, das von der Funktion "**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " mit dem überlappenden Flag " **\_ Dateiflag \_** " geöffnet wird (z. b. Dateien, Postfächer und Pipes). Objekte, die von anderen Funktionen wie [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) erstellt werden, können auch einem e/a-Abschlussport zugeordnet werden. Ein Beispiel für die Verwendung von Sockets finden Sie unter [**Accept tex**](/windows/desktop/api/mswsock/nf-mswsock-acceptex). Ein Handle kann nur einem e/a-Abschlussport zugeordnet werden, und nachdem die Zuordnung erfolgt ist, bleibt das Handle diesem e/a-Abschlussport zugeordnet, bis er geschlossen wird.

Weitere Informationen zu e/a-Abschluss Port Theorie, Verwendung und zugehörigen Funktionen finden Sie unter e [/](i-o-completion-ports.md)a-Abschlussports.

Mehrere Datei Handles können einem einzelnen e/a-Abschlussport zugeordnet werden, indem **CreateIoCompletionPort** mehrmals mit dem gleichen e/a-Abschluss Port Handle im *existingcompletionport* -Parameter und einem anderen Datei Handle im *FILEHANDLE* -Parameter aufgerufen wird.

Verwenden Sie den *completionkey* -Parameter, um Ihre Anwendung zu unterstützen, welche e/a-Vorgänge abgeschlossen wurden. Dieser Wert wird nicht von " **kreateiocompletionport** " für funktionale Steuerelemente verwendet. Stattdessen wird Sie an das im *FILEHANDLE* -Parameter angegebene Datei Handle zum Zeitpunkt der Zuordnung mit einem e/a-Abschlussport angefügt. Dieser Vervollständigungs Schlüssel sollte für jedes Datei Handle eindeutig sein, und er begleitet das Datei Handle während des internen Beendigungs Warteschlangen Prozesses. Sie wird beim Eintreffen eines Vervollständigungs Pakets im [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktions Aufrufwert zurückgegeben. Der *completionkey* -Parameter wird auch von der [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) -Funktion verwendet, um Ihre eigenen speziellen Vervollständigungs Pakete in die Warteschlange zu stellen.

Nachdem eine Instanz eines geöffneten Handles einem e/a-Abschlussport zugeordnet ist, kann Sie nicht in der Funktion "read [**fileex**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) " oder " [**schreitefileex**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) " verwendet werden, da diese Funktionen über eigene asynchrone e/a-Mechanismen verfügen.

Es empfiehlt sich, ein Datei Handle, das einem e/a-Abschlussport zugeordnet ist, entweder mithilfe der Vererbung von Handles oder eines Aufrufes der [**dupligehandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) -Funktion nicht freizugeben. Mit diesen doppelten Handles ausgeführte Vorgänge generieren Abschluss Benachrichtigungen. Eine sorgfältige Überlegung wird empfohlen.

Der e/a-Abschluss Port Handle und jedes Datei Handle, das diesem bestimmten e/a-Abschlussport zugeordnet ist, werden als *Verweise auf den e/* a-Abschlussport bezeichnet. Der e/a-Abschlussport wird freigegeben, wenn keine Verweise mehr vorhanden sind. Daher müssen alle diese Handles ordnungsgemäß geschlossen werden, um den e/a-Abschlussport und seine zugeordneten Systemressourcen freizugeben. Nachdem diese Bedingungen erfüllt sind, schließen Sie den e/a-Abschluss Port handle, indem Sie die [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion aufrufen.

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
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[UWP-Apps für Windows XP-Desktop-Apps \|\]<br/>                                                                                                                                                                                                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 \[ -Desktop-Apps \| UWP-apps\]<br/>                                                                                                                                                                                                                                              |
| Header<br/>                   | <dl> <dt>Ioapi. h (Include Windows. h); </dt> <dt>Winbase. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



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

[Windows Sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

**Funktionen**
</dt> <dt>

[**Akzeptex**](/windows/desktop/api/mswsock/nf-mswsock-acceptex)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**Duplialisiehandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatus usex**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**' PostQueuedCompletionStatus '**](postqueuedcompletionstatus.md)
</dt> <dt>

[**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

