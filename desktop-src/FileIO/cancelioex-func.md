---
description: Markiert alle ausstehenden e/a-Vorgänge für das angegebene Datei handle. Die-Funktion bricht nur e/a-Vorgänge im aktuellen Prozess ab, unabhängig davon, welcher Thread den e/a-Vorgang erstellt hat.
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
title: CancelIoEx-Funktion (ioapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIoEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3de44762ad9a230a9d8cc410c4ba3ae7c2d9964e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358398"
---
# <a name="cancelioex-function"></a>CancelIoEx-Funktion

Markiert alle ausstehenden e/a-Vorgänge für das angegebene Datei handle. Die-Funktion bricht nur e/a-Vorgänge im aktuellen Prozess ab, unabhängig davon, welcher Thread den e/a-Vorgang erstellt hat.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CancelIoEx(
  _In_     HANDLE       hFile,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFile* \[ in\]
</dt> <dd>

Ein Handle für die Datei.

</dd> <dt>

*lpoverlgetauscht* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Datenstruktur, die die Daten enthält, die für asynchrone e/a verwendet werden.

Wenn dieser Parameter **null** ist, werden alle e/a-Anforderungen für den *hFile* -Parameter abgebrochen.

Wenn dieser Parameter nicht **null** ist, werden nur die spezifischen e/a-Anforderungen, die für die Datei mit der *angegebenen über* Lapp enden überlappenden Struktur ausgegeben wurden, als abgebrochen markiert. Dies bedeutet, dass Sie eine oder mehrere Anforderungen abbrechen können, während die [**CancelIo**](cancelio.md) -Funktion alle ausstehenden Anforderungen eines Datei Handles abbricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null. Der Abbruch Vorgang für alle ausstehenden e/a-Vorgänge, die vom aufrufenden Prozess für das angegebene Datei Handle ausgegeben wurden, wurde erfolgreich angefordert. Die Anwendung darf die [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur, die den abgebrochenen e/a-Vorgängen zugeordnet ist, nicht freigeben oder wieder verwenden, bis Sie abgeschlossen sind. Der Thread kann die [**gedeverlappedresult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) -Funktion verwenden, um zu bestimmen, wann die e/a-Vorgänge selbst abgeschlossen wurden.

Wenn die Funktion fehlschlägt, ist der Rückgabewert 0 (null). Um erweiterte Fehlerinformationen abzurufen, müssen Sie die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion aufrufen.

Wenn diese Funktion eine abzubrechende Anforderung nicht finden kann, ist der Rückgabewert 0 (null), und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den **Fehler " \_ nicht \_ gefunden**" zurück.

## <a name="remarks"></a>Bemerkungen

Die **CancelIoEx** -Funktion ermöglicht es Ihnen, Anforderungen in anderen Threads als dem aufrufenden Thread abzubrechen. Die [**CancelIo**](cancelio.md) -Funktion bricht nur Anforderungen im gleichen Thread ab, der die **CancelIo** -Funktion aufgerufen hat. **CancelIoEx** bricht nur ausstehende e/a-Vorgänge für das Handle ab, ändert den Zustand des Handles nicht. Dies bedeutet, dass Sie sich nicht auf den Zustand des Handles verlassen können, weil Sie nicht wissen, ob der Vorgang erfolgreich abgeschlossen wurde oder abgebrochen wurde.

Wenn für das angegebene Datei Handle ausstehende e/a-Vorgänge ausgeführt werden, markiert die Funktion **CancelIoEx** Sie für den Abbruch. Die meisten Vorgänge können sofort abgebrochen werden. andere Vorgänge können fortgesetzt werden, bevor Sie tatsächlich abgebrochen werden, und der Aufrufer wird benachrichtigt. Die **CancelIoEx** -Funktion wartet nicht, bis alle abgebrochenen Vorgänge beendet sind.

Wenn das Datei Handle einem Abschlussport zugeordnet ist, wird ein e/a-abschlusspaket nicht in die Warteschlange des Ports eingereiht, wenn ein synchroner Vorgang erfolgreich abgebrochen wurde. Für asynchrone Vorgänge, die noch ausstehen, fügt der Abbruch Vorgang ein e/a-abschlusspaket in die Warteschlange ein.

Der Vorgang, der abgebrochen wird, wird mit einem von drei Status abgeschlossen. Sie müssen den Abschluss Status überprüfen, um den Abschluss Status zu ermitteln. Die drei Status lauten:

-   Der Vorgang wurde normal abgeschlossen. Dies kann auch auftreten, wenn der Vorgang abgebrochen wurde, da die Abbruch Anforderung möglicherweise nicht rechtzeitig übermittelt wurde, um den Vorgang abzubrechen.
-   Der Vorgang wurde abgebrochen. Die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt einen **\_ \_ abgebrochenen Fehler Vorgang** zurück.
-   Der Vorgang ist mit einem weiteren Fehler fehlgeschlagen. Die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt den relevanten Fehlercode zurück.

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

[**CancelIo**](cancelio.md)
</dt> <dt>

[**CancelSynchronousIo**](cancelsynchronousio-func.md)
</dt> <dt>

[Abbrechen von ausstehenden e/a-Vorgängen](canceling-pending-i-o-operations.md)
</dt> <dt>

[Dateiverwaltungsfunktionen](file-management-functions.md)
</dt> <dt>

[Synchrone und asynchrone e/a](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

