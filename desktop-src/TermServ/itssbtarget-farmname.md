---
title: Eigenschaft "ITsSbTarget FarmName"
description: Ruft den Namen der Farm ab, mit der dieses Ziel verbunden ist, oder gibt diesen an.
ms.assetid: 83e168ae-f985-40f9-912b-496c0695f82a
ms.tgt_platform: multiple
keywords:
- FarmName-Remotedesktopdienste
- FarmName-Eigenschaft Remotedesktopdienste , ITsSbTarget-Schnittstelle
- ITsSbTarget-Schnittstelle Remotedesktopdienste , FarmName-Eigenschaft
- FarmName-Eigenschaft Remotedesktopdienste , ITsSbTargetEx-Schnittstelle
- ITsSbTargetEx-Schnittstelle Remotedesktopdienste , FarmName-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbTarget.FarmName
- ITsSbTarget.get_FarmName
- ITsSbTarget.put_FarmName
- ITsSbTargetEx.FarmName
- ITsSbTargetEx.get_FarmName
- ITsSbTargetEx.put_FarmName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b1c36a1a44f38dac11a7e474d7fefb80a09948
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988293"
---
# <a name="itssbtargetfarmname-property"></a>ITsSbTarget::FarmName -Eigenschaft

Ruft den Namen der Farm ab, mit der dieses Ziel verbunden ist, oder gibt diesen an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_FarmName(
  [in]          BSTR Val
);

HRESULT get_FarmName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine **BSTR-Variable,** die den Namen des landwirtschaftlichen Betriebs enthält.

## <a name="requirements"></a>Anforderungen




| Anforderung | Wert |
|--------|-------|
| Unterstützte Mindestversion (Client)<br /> | Nicht unterstützt<br /> | 
| Unterstützte Mindestversion (Server)<br /> | Windows Server 2012<br /> | 
| IDL<br /> | <dl><dt>Sbtsv.idl</dt></dl> | 
| IID<br /> | IID_ITsSbTarget ist wie:<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 auf Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





