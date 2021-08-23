---
title: ITsSbClientConnection-Domäneneigenschaft
description: Ruft einen Wert ab, der den Domänennamen des Remotedesktopverbindung (RDC) angibt.
ms.assetid: 628f450d-10f4-4405-8d7c-ae58c72c2755
ms.tgt_platform: multiple
keywords:
- Domäneneigenschafts-Remotedesktopdienste
- Domäneneigenschaft Remotedesktopdienste , ITsSbClientConnection-Schnittstelle
- ITsSbClientConnection-Schnittstelle Remotedesktopdienste , Domäneneigenschaft
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Domain
- ITsSbClientConnection.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc99724eb419e831e65f402299aa1603be07ab2ab5a88e0ba9b056492514865
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511510"
---
# <a name="itssbclientconnectiondomain-property"></a>ITsSbClientConnection::D omain-Eigenschaft

Ruft einen Wert ab, der den Domänennamen des Remotedesktopverbindung (RDC) angibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Domain(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine **BSTR-Variable,** die den Domänennamen des RDC-Clients enthält. Wenn Sie die Verwendung der Zeichenfolge abgeschlossen haben, geben Sie sie frei, indem Sie die [**SysFreeString-Funktion**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

