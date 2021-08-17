---
title: RpcTryExcept (Rpc.h)
description: Die RpcTryExcept-Anweisung stellt eine strukturierte Ausnahmebehandlung für RPC-Anwendungen bereit.
ms.assetid: 3addb367-4bdc-4c11-bf4d-b5b94da45b26
keywords:
- RpcTryExcept RPC
topic_type:
- apiref
api_name:
- RpcTryExcept
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c7a73ca80eb342b9a23fcaa4b922afe8d19f00e1f22ab82f8c6027ecc43d76d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925967"
---
# <a name="rpctryexcept"></a>RpcTryExcept

Die **RpcTryExcept-Anweisung** stellt eine strukturierte Ausnahmebehandlung für RPC-Anwendungen bereit. Wenn eine der Programmanweisungen in **RpcTryExcept** eine Ausnahme verursacht, werden die Anweisungen im [**RpcExcept-Codeblock**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) ausgeführt. Alle **RpcTryExcept-Anweisungen** müssen durch die [**RpcEndExcept-Anweisung**](/previous-versions/aa375629(v=vs.80)) beendet werden.

Weitere Informationen finden Sie unter [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).

**Windows Vista und höhere Versionen von Windows:**[**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) wird für die strukturierte Ausnahmebehandlung für die gängigsten Ausnahmen als Alternative zu benutzerdefinierten Filtern mit [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)empfohlen.  

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Rpc.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)
</dt> <dt>

[**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)
</dt> <dt>

[**RpcTryFinally**](rpctryfinally.md)
</dt> </dl>

 

