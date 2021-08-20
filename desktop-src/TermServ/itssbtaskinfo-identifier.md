---
title: ITsSbTaskInfo-Bezeichnereigenschaft
description: Ruft eine GUID ab, die vom Task-Agent als eindeutiger Bezeichner verwendet wird.
ms.assetid: 96b41588-d634-4cdd-aacc-0456b8e47c3b
ms.tgt_platform: multiple
keywords:
- Bezeichnereigenschaft Remotedesktopdienste
- Bezeichnereigenschaft Remotedesktopdienste , ITsSbTaskInfo-Schnittstelle
- ITsSbTaskInfo-Schnittstelle Remotedesktopdienste , Identifier-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Identifier
- ITsSbTaskInfo.get_Identifier
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43eb5b0495b9f258f3b82df8657f104cbea0555a46f61e6a133be8f765081a07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128079"
---
# <a name="itssbtaskinfoidentifier-property"></a>ITsSbTaskInfo::Identifier -Eigenschaft

Ruft eine GUID ab, die vom Task-Agent als eindeutiger Bezeichner verwendet wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Identifier(
  [out, retval] BSTR *pIdentifier
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf einen **BSTR-Wert,** der die GUID empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





