---
description: Markiert ausstehende synchrone e/a-Vorgänge, die vom angegebenen Thread ausgegeben werden, als abgebrochen.
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
title: CancelSynchronousIo-Funktion (ioapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelSynchronousIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3e0c1596603ef7c0d13362c2608cc59b88d366fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530005"
---
# <a name="cancelsynchronousio-function"></a>CancelSynchronousIo-Funktion

Markiert ausstehende synchrone e/a-Vorgänge, die vom angegebenen Thread ausgegeben werden, als abgebrochen.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CancelSynchronousIo(
  _In_ HANDLE hThread
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hThread* \[ in\]
</dt> <dd>

Ein Handle für den Thread.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.

Wenn die Funktion fehlschlägt, ist der Rückgabewert 0 (null). Um erweiterte Fehlerinformationen abzurufen, müssen Sie die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion aufrufen.

Wenn diese Funktion eine abzubrechende Anforderung nicht finden kann, ist der Rückgabewert 0 (null), und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den **Fehler " \_ nicht \_ gefunden**" zurück.

## <a name="remarks"></a>Bemerkungen

Der Aufrufer muss über das Zugriffsrecht " [Thread \_ Beenden](/windows/desktop/ProcThread/thread-security-and-access-rights) " verfügen.

Wenn für den angegebenen Thread ausstehende e/a-Vorgänge ausgeführt werden, markiert die Funktion " **CancelSynchronousIo** " Sie für den Abbruch. Die meisten Vorgänge können sofort abgebrochen werden. andere Vorgänge können fortgesetzt werden, bevor Sie tatsächlich abgebrochen werden, und der Aufrufer wird benachrichtigt. Die **CancelSynchronousIo** -Funktion wartet nicht, bis alle abgebrochenen Vorgänge beendet sind. Weitere Informationen finden Sie unter e [/a-Abschluss-/Abbruch Richtlinien](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).

Der Vorgang, der abgebrochen wird, wird mit einem von drei Status abgeschlossen. Sie müssen den Abschluss Status überprüfen, um den Abschluss Status zu ermitteln. Die drei Status lauten:

-   **Der Vorgang wurde normal abgeschlossen.** Dies kann auch auftreten, wenn der Vorgang abgebrochen wurde, da die Abbruch Anforderung möglicherweise nicht rechtzeitig übermittelt wurde, um den Vorgang abzubrechen.
-   **Der Vorgang wurde abgebrochen.** Die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt einen **\_ \_ abgebrochenen Fehler Vorgang** zurück.
-   **Der Vorgang ist mit einem weiteren Fehler fehlgeschlagen.** Die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt den relevanten Fehlercode zurück.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                                                                                                                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                                                                                                                                                                    |
| Header<br/>                   | <dl> <dt>Ioapi. h (Include Windows. h); </dt> <dt>Winbase. h unter Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CancelIo**](cancelio.md)
</dt> <dt>

[**CancelIoEx**](cancelioex-func.md)
</dt> <dt>

[Dateiverwaltungsfunktionen](file-management-functions.md)
</dt> <dt>

[Synchrone und asynchrone e/a](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

