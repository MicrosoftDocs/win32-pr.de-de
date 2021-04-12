---
title: RPC_NS_HANDLE (rpcnsi. h)
description: Der RPC \_ -NS-Datentyp \_ definiert ein Name-Service-handle.
ms.assetid: d9c2a376-4972-4f16-aa8d-f0e43d5ddb8d
keywords:
- RPC_NS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e72ee694e08be1b30a75dc1f5b986619043d592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518719"
---
# <a name="rpc_ns_handle"></a>RPC- \_ NS- \_ handle

Der RPC- **\_ NS \_** -Datentyp definiert ein Name-Service-handle.


```C++
typedef void* RPC_NS_HANDLE;
```



## <a name="remarks"></a>Bemerkungen

Ein Name-Dienst-Handle ist eine nicht transparente Variable mit Informationen, die von der RPC-Lauf Zeit Bibliothek verwendet werden, um die folgenden RPC-Daten aus der Name-Service-Datenbank zurückzugeben:

-   Server Bindungs Handles
-   UUIDs von Ressourcen, die von Serverprofil Mitgliedern angeboten werden
-   Gruppenmitglieder

Der Gültigkeitsbereich eines Namensdienst Handles erfolgt über die entsprechende "Done"-Routine.

Anwendungen sind verantwortlich für die Parallelitäts Steuerung von Name-Service-Handles über Threads hinweg.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Rpcnsi. h (Include RPC. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[**Rpcnsbindingimportdone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone)
</dt> <dt>

[**Rpcnsbindingimportnext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)
</dt> <dt>

[**Rpcnsbindinglookupbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[**Rpcnsbindinglookupdone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone)
</dt> <dt>

[**Rpcnsbindinglookupnext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)
</dt> </dl>

 

 





