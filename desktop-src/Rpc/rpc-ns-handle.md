---
title: RPC_NS_HANDLE (Rpcnsi.h)
description: Der Datentyp RPC \_ NS \_ HANDLE definiert ein Name-Dienst-Handle.
ms.assetid: d9c2a376-4972-4f16-aa8d-f0e43d5ddb8d
keywords:
- RPC_NS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7612671b03f507bc2e722520fa775e0e999d0f1456ebfcefa971bba27b65dbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926284"
---
# <a name="rpc_ns_handle"></a>\_RPC-NS-HANDLE \_

Der Datentyp **RPC \_ NS \_ HANDLE** definiert ein Name-Dienst-Handle.


```C++
typedef void* RPC_NS_HANDLE;
```



## <a name="remarks"></a>Hinweise

Ein Name-Service-Handle ist eine nicht transparente Variable, die Informationen enthält, die von der RPC-Laufzeitbibliothek verwendet werden, um die folgenden RPC-Daten aus der name-service-Datenbank zurückzugeben:

-   Serverbindungshandles
-   UUIDs von Ressourcen, die von Mitgliedern des Serverprofils angeboten werden
-   Gruppenmitglieder

Der Bereich eines Namensdiensthandle stammt von einer "Begin"-Routine über die entsprechende "Done"-Routine.

Anwendungen sind für die parallele Steuerung von Name-Dienst-Handles über Threads hinweg verantwortlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Rpcnsi.h (include Rpc.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone)
</dt> <dt>

[**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)
</dt> <dt>

[**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[**RpcNsBindingLookupDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone)
</dt> <dt>

[**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)
</dt> </dl>

 

 





