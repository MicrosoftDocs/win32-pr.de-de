---
title: ITsSbTarget TargetName-Eigenschaft
description: Gibt den Namen des Ziels an oder ruft den Namen ab.
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der TargetName-Eigenschaft
- TargetName-Eigenschaft Remotedesktopdienste , ITsSbTarget-Schnittstelle
- ITsSbTarget-Schnittstelle Remotedesktopdienste , TargetName-Eigenschaft
- TargetName-Eigenschaft Remotedesktopdienste , ITsSbTargetEx-Schnittstelle
- ITsSbTargetEx-Schnittstelle Remotedesktopdienste , TargetName-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetName
- ITsSbTarget.get_TargetName
- ITsSbTarget.put_TargetName
- ITsSbTargetEx.TargetName
- ITsSbTargetEx.get_TargetName
- ITsSbTargetEx.put_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da653b581c512e0397bb4c486d7c21d6844d41b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982593"
---
# <a name="itssbtargettargetname-property"></a>ITsSbTarget::TargetName-Eigenschaft

Gibt den Namen des Ziels an oder ruft den Namen ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_TargetName(
  [in]          BSTR Val
);

HRESULT get_TargetName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine **BSTR-Variable,** die den Zielnamen angibt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft war vor Windows Server 2012 schreibgeschützt.

## <a name="requirements"></a>Anforderungen




| Anforderung | Wert |
|--------|-------|
| Unterstützte Mindestversion (Client)<br /> | Nicht unterstützt<br /> | 
| Unterstützte Mindestversion (Server)<br /> | Windows Server 2012<br /> | 
| IDL<br /> | <dl><dt>Sbtsv.idl</dt></dl> | 
| IID<br /> | IID_ITsSbTarget ist wie folgt definiert:<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 auf Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





