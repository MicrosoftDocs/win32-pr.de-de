---
title: Itssbsession-Domänen Eigenschaft
description: Ruft den Domänen Namen des Benutzers ab.
ms.assetid: bbb9a805-7270-4555-8fee-130a46bc3903
ms.tgt_platform: multiple
keywords:
- Domänen Eigenschaft Remotedesktopdienste
- Domänen Eigenschaft Remotedesktopdienste, itssbsession-Schnittstelle
- Itssbsession-Schnittstelle Remotedesktopdienste, Domain-Eigenschaft
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
ms.openlocfilehash: 4501413888d17a70610160117df3ad03fde73b76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339598"
---
# <a name="itssbsessiondomain-property"></a>Itssbsession::D omain-Eigenschaft

Ruft den Domänen Namen des Benutzers ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Domain(
  [out, retval] BSTR *domain
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf eine **BSTR** -Variable, die den Domänen Namen des Benutzers empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itssbsession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





