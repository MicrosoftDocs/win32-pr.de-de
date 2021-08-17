---
description: Bricht einen registrierten Wartevorgang ab, der von der RegisterWaitForSingleObject-Funktion ausgegeben wird.
ms.assetid: ea700e55-fce7-46cd-bb96-0c129b429d46
title: UnregisterWaitEx-Funktion (Threadpoollegacyapiset.h)
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
ms.openlocfilehash: 4181aa43cb0c2844f99b7ad81b448271366eb2925740c25d400f891389efb129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765522"
---
# <a name="unregisterwaitex-function"></a>UnregisterWaitEx-Funktion

Bricht einen registrierten Wartevorgang ab, der von der [**RegisterWaitForSingleObject-Funktion**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) ausgegeben wird.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI UnregisterWaitEx(
  _In_     HANDLE WaitHandle,
  _In_opt_ HANDLE CompletionEvent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*WaitHandle* \[ In\]
</dt> <dd>

Das Wait-Handle. Dieses Handle wird von der [**RegisterWaitForSingleObject-Funktion**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) zurückgegeben.

</dd> <dt>

*CompletionEvent* \[ in, optional\]
</dt> <dd>

Ein Handle für das Ereignisobjekt, das signalisiert werden soll, wenn die Registrierung des Wartevorgangs aufgehoben wurde. Dieser Parameter kann **NULL** sein.

Wenn dieser Parameter **INVALID \_ HANDLE \_ VALUE** ist, wartet die Funktion, bis alle Rückruffunktionen abgeschlossen sind, bevor sie zurückgegeben wird.

Wenn dieser Parameter **NULL** ist, markiert die Funktion den Timer für den Löschvorgang und gibt sofort zurück. Die meisten Aufrufer sollten jedoch warten, bis die Rückruffunktion abgeschlossen ist, damit sie alle erforderlichen Bereinigungen durchführen können.

Wenn der Aufrufer dieses Ereignis bereitstellt und die Funktion erfolgreich ist oder die Funktion mit **ERROR \_ IO \_ PENDING** fehlschlägt, schließen Sie das Ereignis erst, wenn es signalisiert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

## <a name="remarks"></a>Bemerkungen

Sie können keinen blockierenden Aufruf von **UnregisterWaitEx** innerhalb einer Rückruffunktion für denselben Wartevorgang vornehmen. Andernfalls wartet der Rückruf auf den Abschluss des Rückrufs. Im Allgemeinen wird durch einen blockierenden Aufruf von **UnregisterWaitEx** eine Abhängigkeit zwischen dem aktuellen Thread und dem Rückruf erstellt. Um also einen blockierenden Unregister-Aufruf für einen anderen Wartevorgang auszuführen, müssen Sie sicherstellen, dass die Rückruffunktionen nicht voneinander abhängen und dass der zweite Wartevorgang nicht auch einen blockierenden Aufruf der Nichtregistrierung für den ersten Vorgang ausführt.

Seien Sie vorsichtig, wenn Sie einen blockierenden **UnregisterWaitEx-Aufruf** für einen persistenten Thread vornehmen. Wenn der nicht registrierte Wartevorgang mit **WT \_ EXECUTEINPERSISTENTTHREAD** erstellt wurde, kann ein Deadlock auftreten.

Nach dem nicht blockierenden Aufruf von **UnregisterWaitEx** können keine neuen Rückruffunktionen, die *WaitHandle* zugeordnet sind, in die Warteschlange eingereiht werden. Es kann jedoch sein, dass Rückruffunktionen bereits in der Warteschlange für Arbeitsthreads stehen.

Unter bestimmten Umständen schlägt die Funktion mit **ERROR \_ IO \_ PENDING fehl,** wenn *CompletionEvent* **NULL** ist. Dies gibt an, dass ausstehende Rückruffunktionen vorhanden sind. Diese Rückrufe werden entweder ausgeführt oder befinden sich in der Ausführung.

Wenn *CompletionEvent* ein Handle für ein vom Aufrufer bereitgestelltes Ereignis ist, ist es möglich, dass die Funktion erfolgreich ist, mit **ERROR IO \_ \_ PENDING** fehlschlägt oder mit einem anderen Fehlercode fehlschlägt. Wenn die Funktion erfolgreich ist oder die Funktion mit **ERROR \_ IO \_ PENDING** fehlschlägt, sollte der Aufrufer immer warten, bis das Ereignis signalisiert wird, um das Ereignis zu schließen. Wenn die Funktion mit einem anderen Fehlercode fehlschlägt, müssen Sie nicht warten, bis das Ereignis signalisiert wird, um das Ereignis zu schließen.

**Windows XP:** Wenn *CompletionEvent* ein Handle für ein vom Aufrufer bereitgestelltes Ereignis ist und die Funktion mit **ERROR IO \_ \_ PENDING** fehlschlägt, sollte der Aufrufer warten, bis das Ereignis signalisiert wird, um das Ereignis zu schließen. Dieses Verhalten hat sich ab Windows Vista geändert.

Um eine Anwendung zu kompilieren, die diese Funktion verwendet, definieren Sie **\_ WIN32 \_ WINNT** als 0x0500 oder höher. Weitere Informationen finden Sie unter [Verwenden der Windows Header.](../winprog/using-the-windows-headers.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                                                                                                                                                                                                                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                                                                                                                                                                                                                                                                           |
| Header<br/>                   | <dl> <dt>Threadpoollegacyapiset.h für Windows 8 und Windows Server 2012 (einschließlich Windows.h);</dt> <dt>WinBase.h auf Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP und Windows Server 2003 (einschließlich Windows.h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Registerwaitforsingleobject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)
</dt> <dt>

[Synchronisierungsfunktionen](synchronization-functions.md)
</dt> <dt>

[Pooling von Threads](../procthread/thread-pooling.md)
</dt> </dl>

 

 
