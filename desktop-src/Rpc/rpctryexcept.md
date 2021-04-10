---
title: Rpctryaußer (RPC. h)
description: Die rpctryaußer-Anweisung stellt eine strukturierte Ausnahmebehandlung für RPC-Anwendungen bereit.
ms.assetid: 3addb367-4bdc-4c11-bf4d-b5b94da45b26
keywords:
- Rpctryaußer RPC
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
ms.openlocfilehash: 0f5876a3fe0b33f96a5e10a9c712bdcadcbfca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104378"
---
# <a name="rpctryexcept"></a>Rpctryaußer

Die **rpctryaußer** -Anweisung stellt eine strukturierte Ausnahmebehandlung für RPC-Anwendungen bereit. Wenn eine der Programm Anweisungen in **rpctryaußer** eine Ausnahme auslöst, werden die Anweisungen im Code Block " [**rpcaußer**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) " ausgeführt. Alle **rpctryaußer** -Anweisungen müssen von der [**rpcendexcept**](/previous-versions/aa375629(v=vs.80)) -Anweisung beendet werden.

Weitere Informationen finden Sie unter [**rpcaußer**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).

**Windows Vista und höhere Versionen von Windows:**  [**rpcexceptionfilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) wird für die strukturierte Ausnahmebehandlung für die häufigsten Ausnahmen als Alternative zu benutzerdefinierten Filtern mit " [**rpcaußer**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)" empfohlen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>RPC. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rpcaußer**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)
</dt> <dt>

[**Rpcexceptionfilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)
</dt> <dt>

[**Rpctryschließlich**](rpctryfinally.md)
</dt> </dl>

 

