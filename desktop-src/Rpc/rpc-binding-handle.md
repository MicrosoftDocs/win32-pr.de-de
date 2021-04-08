---
title: RPC_BINDING_HANDLE (rpcdce. h)
description: Der Datentyp des RPC- \_ Bindungs Handles deklariert ein Bindungs handle, das Informationen enthält, die von der RPC-Lauf Zeit Bibliothek für den Zugriff auf Bindungs Informationen verwendet werden.
ms.assetid: 3e07d9e9-04d8-4f94-8104-cd0ee89a9407
keywords:
- RPC_BINDING_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e37d14bc5186f05815c10f538b0c90bdddd353
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743792"
---
# <a name="rpc_binding_handle"></a>RPC- \_ Bindungs \_ handle

Der Datentyp des **RPC- \_ Bindungs Handles** deklariert ein Bindungs handle, das Informationen enthält, die von der RPC-Lauf Zeit Bibliothek für den Zugriff auf Bindungs Informationen verwendet werden.


```C++
typedef I_RPC_HANDLE RPC_BINDING_HANDLE;
```



## <a name="remarks"></a>Bemerkungen

Die-Lauf Zeit Bibliothek verwendet Bindungs Informationen, um eine Client/Server-Beziehung einzurichten, die die Ausführung von Remote Prozedur aufrufen ermöglicht. Basierend auf dem Kontext, in dem ein Bindungs Handle erstellt wird, wird es als Server Bindungs handle oder Client Bindungs handle angesehen.

Ein Server Bindungs Handle enthält die Informationen, die für einen Client erforderlich sind, um eine Beziehung zu einem bestimmten Server herzustellen. Eine beliebige Anzahl von RPC-API-Lauf Zeit Routinen gibt ein Server Bindungs Handle zurück, das zum Ausführen eines Remote Prozedur Aufrufs verwendet werden kann.

Ein Client Bindungs Handle kann nicht verwendet werden, um einen Remote Prozedur aufzurufen. Die RPC-Lauf Zeit Bibliothek erstellt und stellt ein Client Bindungs Handle für eine aufgerufene Server Prozedur (auch als Server-Manager-Routine bezeichnet) als Parameter für den RPC- \_ Bindungs \_ handle bereit. Das Client Bindungs Handle enthält Informationen zum aufrufenden Client.

Die Funktionen **RpcBinding \** _ und _*rpcnsbinding \**_ geben den Statuscode RPC \_ S \_ falsch \_ an, \_ \_ Wenn eine Anwendung den falschen bindungshandlertyp bereitstellt.

Eine Anwendung kann ein einzelnes Bindungs Handle für mehrere Ausführungs Threads freigeben. Die RPC-Lauf Zeit Bibliothek verwaltet gleichzeitige Remote Prozedur Aufrufe, bei denen ein einzelnes Bindungs Handle verwendet wird. Die Anwendung ist jedoch für die Bindung der Parallelitäts Steuerung für Vorgänge zuständig, die ein Bindungs handle ändern. Diese Vorgänge umfassen die folgenden Routinen:

-   [_ *Rpcbindingfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)
-   [**Rpcbindingreset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)
-   [**Rpcbindingsetauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
-   [**Rpcbindingsetobject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

Wenn eine Anwendung z. b. ein Bindungs Handle für zwei Ausführungs Threads nutzt und den Bindungs handle-Endpunkt in einem der Threads durch Aufrufen von [**rpcbindingreset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)zurücksetzt, sind die Ergebnisse nicht definiert. Das Bindungs Handle im anderen Thread kann ebenfalls zurückgesetzt werden, oder der Vorgang kann fehlschlagen, oder der Prozess stürzt ab. Ein häufiger Fehler besteht darin, ein Bindungs Handle freizugeben, während ein-Vorgang ausgeführt wird. Dies stürzt normalerweise den aufrufenden Prozess ab.

Wenn Sie keine Parallelität möchten, können Sie eine Anwendung so entwerfen, dass eine Kopie eines Bindungs Handles durch Aufrufen von [**rpcbindingcopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy)erstellt wird. In diesem Fall hat ein Vorgang für das erste Bindungs Handle keine Auswirkung auf das zweite Bindungs handle.

Routinen, die ein Bindungs Handle als Parameter erfordern, zeigen den Datentyp **RPC- \_ Bindungs \_ handle** an. Bindungs handle-Parameter werden als Wert übermittelt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Rpcdce. h (Include RPC. h)</dt> </dl> |



 

 





