---
description: Bricht einen registrierten warte Vorgang ab, der von der RegisterWaitForSingleObject-Funktion ausgegeben wurde.
ms.assetid: ea700e55-fce7-46cd-bb96-0c129b429d46
title: Unregisterwaitex-Funktion (threadpoollegacyapiset. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnregisterWaitEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-threadpool-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-threadpool-legacy-l1-1-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
ms.openlocfilehash: 30f5ad5f88bec9eb7eebff5a73d8f84f633cb249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865404"
---
# <a name="unregisterwaitex-function"></a>Unregisterwaitex-Funktion

Bricht einen registrierten warte Vorgang ab, der von der [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) -Funktion ausgegeben wurde.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI UnregisterWaitEx(
  _In_     HANDLE WaitHandle,
  _In_opt_ HANDLE CompletionEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*WaitHandle* \[ in\]
</dt> <dd>

Das Wait-Handle. Dieses Handle wird von der [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) -Funktion zurückgegeben.

</dd> <dt>

*CompletionEvent* \[ in, optional\]
</dt> <dd>

Ein Handle für das Ereignis Objekt, das signalisiert werden soll, wenn die Registrierung des warte Vorgangs aufgehoben wurde. Dieser Parameter kann **NULL** sein.

Wenn dieser Parameter ein **ungültiger \_ handle- \_ Wert** ist, wartet die Funktion auf den Abschluss aller Rückruf Funktionen, bevor Sie zurückgegeben wird.

Wenn dieser Parameter **null** ist, markiert die Funktion den Timer zum Löschen und wird sofort zurückgegeben. Die meisten Aufrufer sollten jedoch warten, bis die Rückruffunktion vollständig ist, damit Sie alle benötigten Bereinigungs Vorgänge ausführen können.

Wenn der Aufrufer dieses Ereignis bereitstellt und die Funktion erfolgreich ist oder die Funktion mit der Fehler-e/a **\_ \_ Ausstehend** ausfällt, schließen Sie das Ereignis erst, wenn es signalisiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Es ist nicht möglich, einen blockierenden Aufrufs von **unregisterwaitex** innerhalb einer Rückruffunktion für denselben warte Vorgang durchführen. Andernfalls wartet der Rückruf darauf, dass er abgeschlossen wird. Im Allgemeinen wird durch einen blockierenden Aufrufs von **unregisterwaitex** eine Abhängigkeit zwischen dem aktuellen Thread und dem Rückruf erstellt. Wenn Sie also einen blockierenden aufheben-Aufrufs bei einem anderen warte Vorgang ausführen möchten, müssen Sie sicherstellen, dass die Rückruf Funktionen nicht voneinander abhängen und dass der zweite warte Vorgang nicht auch einen blockierenden aufheben-Aufrufs für den ersten Vorgang ausführt.

Gehen Sie beim Erstellen eines **unregisterwaitex** -Aufrufs für einen persistenten Thread vorsichtig vor. Wenn der Warte Vorgang, dessen Registrierung aufgehoben wurde, mit dem **WT \_ executeinpersistentthread** erstellt wurde, kann ein Deadlock auftreten.

Nach dem nicht blockierenden Aufrufen von **unregisterwaitex** können keine neuen Rückruf Funktionen in eine Warteschlange eingereiht werden, die mit *WaitHandle* verknüpft sind. Möglicherweise gibt es jedoch ausstehende Rückruf Funktionen, die bereits in die Warteschlange eingereiht wurden.

Unter bestimmten Bedingungen tritt bei der Funktion ein **Fehler auf \_ , \_** Wenn *CompletionEvent* **null** ist. Dies weist darauf hin, dass ausstehende Rückruf Funktionen vorhanden sind. Diese Rückrufe werden entweder ausgeführt oder befinden sich in der Mitte der Ausführung.

Wenn *CompletionEvent* ein Handle für ein Ereignis ist, das vom Aufrufer bereitgestellt wird, ist es möglich, dass die Funktion erfolgreich ausgeführt wird, dass die Fehler-e/a **\_ \_ Ausstehend** ist oder mit einem anderen Fehlercode fehlschlägt. Wenn die Funktion erfolgreich ausgeführt wird oder wenn die Funktion fehlschlägt, wenn die Fehler-e/a aussteht, sollte der Aufrufer immer warten, bis das Ereignis signalisiert wird, um das Ereignis **\_ \_** Wenn die Funktion mit einem anderen Fehlercode fehlschlägt, müssen Sie nicht warten, bis das Ereignis signalisiert wird, um das Ereignis zu schließen.

**Windows XP:** Wenn *CompletionEvent* ein Handle für ein Ereignis ist, das vom Aufrufer bereitgestellt wird, und die Funktion mit dem **\_ \_ ausstehenden Fehler**-e/a-Vorgang fehlschlägt, sollte der Aufrufer warten, bis das Ereignis signalisiert wird, Dieses Verhalten hat sich seit Windows Vista geändert.

Um eine Anwendung zu kompilieren, die diese Funktion verwendet, definieren Sie **\_ Win32 \_ Winnt** als 0x0500 sein oder höher. Weitere Informationen finden Sie unter [Verwenden der Windows-Header](../winprog/using-the-windows-headers.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                                                                                                                                                                                                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                                                                                                                                                                                                                                                                           |
| Header<br/>                   | <dl> <dt>Threadpoollegacyapiset. h unter Windows 8 und Windows Server 2012 (Include Windows. h); </dt> <dt>Winbase. h unter Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP und Windows Server 2003 (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Von RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)
</dt> <dt>

[Synchronisierungsfunktionen](synchronization-functions.md)
</dt> <dt>

[Pooling von Threads](../procthread/thread-pooling.md)
</dt> </dl>

 

 
