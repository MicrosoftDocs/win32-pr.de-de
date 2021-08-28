---
title: ITsSbTarget TargetName-Eigenschaft
description: Gibt den Namen des Ziels an oder ruft den Namen ab.
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- TargetName-Eigenschaft Remotedesktopdienste
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
ms.openlocfilehash: 971ae66d162464c49d7eb4206f1fbddf206707c2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467867"
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

## <a name="remarks"></a>Hinweise

Diese Eigenschaft war vor Windows Server 2012 schreibgeschützt.

## <a name="requirements"></a>Anforderungen




| | | Mindestens unterstützter Client<br /> | None supported (Keine unterstützt)<br /> | | Unterstützter Mindestserver<br /> | Windows Server 2012<br /> | | IDL<br /> | <dl><dt>Sbtsv.idl</dt></dl> | | IID<br /> | IID_ITsSbTarget wird wie folgt definiert:<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 auf Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





