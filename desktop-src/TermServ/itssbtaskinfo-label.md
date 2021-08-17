---
title: ITsSbTaskInfo Label-Eigenschaft
description: Ruft die Bezeichnung ab, die den Zweck der Aufgabe beschreibt.
ms.assetid: 075de6a4-53b0-43b0-9bca-03bf312fff6e
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Bezeichnungseigenschaft
- Label-Eigenschaft Remotedesktopdienste , ITsSbTaskInfo-Schnittstelle
- ITsSbTaskInfo-Schnittstelle Remotedesktopdienste , Label-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Label
- ITsSbTaskInfo.get_Label
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2414dd83d44add4084a4176f575817875e933f9770039e49b02364bd8103cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138303"
---
# <a name="itssbtaskinfolabel-property"></a>ITsSbTaskInfo::Label-Eigenschaft

Ruft die Bezeichnung ab, die den Zweck der Aufgabe beschreibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Label(
  [out, retval] BSTR *pLabel
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein Zeiger auf einen **BSTR-Wert,** der die Bezeichnung enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





