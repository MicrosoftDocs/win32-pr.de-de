---
description: Markiert ausstehende synchrone E/A-Vorgänge, die vom angegebenen Thread ausgegeben werden, als abgebrochen.
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
title: CancelSynchronousIo-Funktion (IoAPI.h)
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
ms.openlocfilehash: 1bdae4682bcbabb09778bdf5f5d3421c16af17587eda72813c9103eb16f7037f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582550"
---
# <a name="cancelsynchronousio-function"></a>CancelSynchronousIo-Funktion

Markiert ausstehende synchrone E/A-Vorgänge, die vom angegebenen Thread ausgegeben werden, als abgebrochen.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CancelSynchronousIo(
  _In_ HANDLE hThread
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hThread* \[ In\]
</dt> <dd>

Ein Handle für den Thread.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.

Wenn die Funktion fehlschlägt, ist der Rückgabewert 0 (null). Um erweiterte Fehlerinformationen zu erhalten, rufen Sie die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

Wenn diese Funktion keine Anforderung zum Abbrechen finden kann, ist der Rückgabewert 0 (null), und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt **ERROR NOT FOUND \_ \_ zurück.**

## <a name="remarks"></a>Hinweise

Der Aufrufer muss über das [Thread \_ terminate-Zugriffsrecht](/windows/desktop/ProcThread/thread-security-and-access-rights) verfügen.

Wenn für den angegebenen Thread ausstehende E/A-Vorgänge ausgeführt werden, markiert die **CancelSynchronousIo-Funktion** sie für den Abbruch. Die meisten Arten von Vorgängen können sofort abgebrochen werden. Andere Vorgänge können bis zum Abschluss fortgesetzt werden, bevor sie tatsächlich abgebrochen werden und der Aufrufer benachrichtigt wird. Die **CancelSynchronousIo-Funktion** wartet nicht, bis alle abgebrochenen Vorgänge abgeschlossen sind. Weitere Informationen finden Sie unter [E/A-Vervollständigungs-/Abbruchrichtlinien.](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx)

Der abgebrochene Vorgang wird mit einem von drei Status abgeschlossen. Sie müssen den Abschlussstatus überprüfen, um den Abschlussstatus zu bestimmen. Die drei Status sind:

-   **Der Vorgang wurde normal abgeschlossen.** Dies kann auch auftreten, wenn der Vorgang abgebrochen wurde, da die Abbrichtanforderung möglicherweise nicht innerhalb der Zeit zum Abbrechen des Vorgangs übermittelt wurde.
-   **Der Vorgang wurde abgebrochen.** Die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt **ERROR OPERATION \_ \_ ABORTED zurück.**
-   **Der Vorgang ist mit einem anderen Fehler fehlgeschlagen.** Die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt den relevanten Fehlercode zurück.

In Windows 8 und Windows Server 2012 wird diese Funktion von den folgenden Technologien unterstützt.



| Technologie                                           | Unterstützt      |
|------------------------------------------------------|----------------|
| Server Message Block (SMB) 3.0-Protokoll<br/>   | Ja<br/> |
| SMB 3.0 Transparent Failover (TFO)<br/>        | Ja<br/> |
| SMB 3.0 mit Dateifreigaben mit aufskalieren (SO)<br/>   | Ja<br/> |
| Freigegebenes Clustervolume Dateisystem (CsvFS)<br/> | Ja<br/> |
| Robustes Dateisystem (Resilient File System, ReFS)<br/>              | Ja<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                                                                                                                                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                                                                                                                                    |
| Header<br/>                   | <dl> <dt>IoAPI.h (include Windows.h);</dt> <dt>WinBase.h auf Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista (einschließlich Windows.h)</dt> </dl> |
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

[Synchrone und asynchrone E/A](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

