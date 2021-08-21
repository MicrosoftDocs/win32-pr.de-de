---
title: ITsSbSession-Domäneneigenschaft
description: Ruft den Domänennamen des Benutzers ab.
ms.assetid: bbb9a805-7270-4555-8fee-130a46bc3903
ms.tgt_platform: multiple
keywords:
- Domäneneigenschaft Remotedesktopdienste
- Domäneneigenschaft Remotedesktopdienste , ITsSbSession-Schnittstelle
- ITsSbSession-Schnittstelle Remotedesktopdienste , Domäneneigenschaft
topic_type:
- apiref
api_name:
- ITsSbSession.Domain
- ITsSbSession.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52854f719830933c96bc130dbec4f0b15f1264344396382ad59099d4c37cf02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128305"
---
# <a name="itssbsessiondomain-property"></a>ITsSbSession::D omain-Eigenschaft

Ruft den Domänennamen des Benutzers ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Domain(
  [out, retval] BSTR *domain
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine **BSTR-Variable,** die den Domänennamen des Benutzers empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





