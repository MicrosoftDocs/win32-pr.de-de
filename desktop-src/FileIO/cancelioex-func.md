---
description: Markiert alle ausstehenden E/A-Vorgänge für das angegebene Dateihandle. Die Funktion bricht nur E/A-Vorgänge im aktuellen Prozess ab, unabhängig davon, welcher Thread den E/A-Vorgang erstellt hat.
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
title: CancelIoEx-Funktion (IoAPI.h)
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
ms.openlocfilehash: 3726bf221073f33d87481d7a6bb6f2f4fd459812616975fba38d9a9a8f0334ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582610"
---
# <a name="cancelioex-function"></a>CancelIoEx-Funktion

Markiert alle ausstehenden E/A-Vorgänge für das angegebene Dateihandle. Die Funktion bricht nur E/A-Vorgänge im aktuellen Prozess ab, unabhängig davon, welcher Thread den E/A-Vorgang erstellt hat.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CancelIoEx(
  _In_     HANDLE       hFile,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFile* \[ In\]
</dt> <dd>

Ein Handle für die Datei.

</dd> <dt>

*lpOverlapped* \[ in, optional\]
</dt> <dd>

Ein Zeiger [](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) auf eine OVERLAPPED-Datenstruktur, die die für asynchrone E/A verwendeten Daten enthält.

Wenn dieser Parameter **NULL** ist, werden alle E/A-Anforderungen für den *hFile-Parameter* abgebrochen.

Wenn dieser Parameter nicht **NULL** ist, werden nur die spezifischen E/A-Anforderungen, die für die Datei mit der angegebenen lpOverlapped-Überlappungsstruktur ausgegeben wurden, als abgebrochen markiert. Das bedeutet, dass Sie eine oder mehrere Anforderungen abbrechen können, während die [**CancelIo-Funktion**](cancelio.md) alle ausstehenden Anforderungen für ein Dateihandle abbricht. 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null. Der Abbruchvorgang für alle ausstehenden E/A-Vorgänge, die vom aufrufenden Prozess für das angegebene Dateihandle ausgegeben wurden, wurde erfolgreich angefordert. Die Anwendung darf die [**OVERLAPPED-Struktur,**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) die den abgebrochenen E/A-Vorgängen zugeordnet ist, erst wiederverwenden oder freigeben, wenn sie abgeschlossen ist. Der Thread kann die [**GetOverlappedResult-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) verwenden, um zu bestimmen, wann die E/A-Vorgänge selbst abgeschlossen wurden.

Wenn die Funktion fehlschlägt, ist der Rückgabewert 0 (null). Um erweiterte Fehlerinformationen abzurufen, rufen Sie die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

Wenn diese Funktion keine Anforderung zum Abbrechen finden kann, ist der Rückgabewert 0 (null), und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt **ERROR NOT FOUND \_ \_ zurück.**

## <a name="remarks"></a>Hinweise

Mit **der CancelIoEx-Funktion** können Sie Anforderungen in anderen Threads als dem aufrufenden Thread abbrechen. Die [**CancelIo-Funktion**](cancelio.md) bricht nur Anforderungen im gleichen Thread ab, der die **CancelIo-Funktion** aufgerufen hat. **CancelIoEx** bricht nur ausstehende E/A für das Handle ab. Der Zustand des Handles wird nicht geändert. Dies bedeutet, dass Sie sich nicht auf den Zustand des Handles verlassen können, da Sie nicht wissen können, ob der Vorgang erfolgreich abgeschlossen oder abgebrochen wurde.

Wenn für das angegebene Dateihandle ausstehende E/A-Vorgänge ausgeführt werden, markiert die **CancelIoEx-Funktion** diese für den Abbruch. Die meisten Arten von Vorgängen können sofort abgebrochen werden. andere Vorgänge können bis zum Abschluss fortgesetzt werden, bevor sie tatsächlich abgebrochen werden und der Aufrufer benachrichtigt wird. Die **CancelIoEx-Funktion** wartet nicht auf den Abschluss aller abgebrochenen Vorgänge.

Wenn das Dateihandle einem Abschlussport zugeordnet ist, wird ein E/A-Abschlusspaket nicht in die Warteschlange des Ports eingereiht, wenn ein synchroner Vorgang erfolgreich abgebrochen wurde. Bei asynchronen Vorgängen, die noch ausstehen, stellt der Abbruchvorgang ein E/A-Abschlusspaket in die Warteschlange.

Der abgebrochene Vorgang wird mit einem von drei Status abgeschlossen. Sie müssen den Abschlussstatus überprüfen, um den Abschlussstatus zu bestimmen. Die drei Status sind:

-   Der Vorgang wurde normal abgeschlossen. Dies kann auch auftreten, wenn der Vorgang abgebrochen wurde, da die Abbruchanforderung möglicherweise nicht rechtzeitig übermittelt wurde, um den Vorgang abzubrechen.
-   Der Vorgang wurde abgebrochen. Die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt **ERROR OPERATION \_ \_ ABORTED zurück.**
-   Der Vorgang ist mit einem weiteren Fehler fehlgeschlagen. Die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den relevanten Fehlercode zurück.

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

[**CancelIo**](cancelio.md)
</dt> <dt>

[**CancelSynchronousIo**](cancelsynchronousio-func.md)
</dt> <dt>

[Abbrechen ausstehender E/A-Vorgänge](canceling-pending-i-o-operations.md)
</dt> <dt>

[Dateiverwaltungsfunktionen](file-management-functions.md)
</dt> <dt>

[Synchrone und asynchrone E/A](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

