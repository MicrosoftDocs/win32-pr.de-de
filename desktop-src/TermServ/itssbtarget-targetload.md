---
title: ITsSbTarget TargetLoad (Eigenschaft)
description: Ruft die relative Last auf einem Ziel ab.
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- TargetLoad-Remotedesktopdienste
- TargetLoad-Remotedesktopdienste , ITsSbTarget-Schnittstelle
- ITsSbTarget-Schnittstelle Remotedesktopdienste , TargetLoad-Eigenschaft
- TargetLoad-Remotedesktopdienste , ITsSbTargetEx-Schnittstelle
- ITsSbTargetEx-Schnittstelle Remotedesktopdienste , TargetLoad-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetLoad
- ITsSbTarget.get_TargetLoad
- ITsSbTargetEx.TargetLoad
- ITsSbTargetEx.get_TargetLoad
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d6d4839f60ef4b4af33498658bd78bf234c14f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482346"
---
# <a name="itssbtargettargetload-property"></a>ITsSbTarget::TargetLoad (Eigenschaft)

Ruft die relative Last auf einem Ziel ab. Dieser Wert basiert auf der Anzahl der vorhandenen und ausstehenden Sitzungen. Standardmäßig hat eine ausstehende Sitzung den gleichen Wert wie eine vorhandene Sitzung.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zahl, die die relative Last auf einem Ziel darstellt.

## <a name="remarks"></a>Hinweise

Die Gewichtung einer ausstehenden Sitzung relativ zu einer aktiven Sitzung kann durch Festlegen des Werts des *LB \_ ConnectionEstablishmentPenalty-Parameters* für den Verbindungsbroker geändert werden. Dieser Parameter befindet sich unter dem **Registrierungsschlüssel HKLM \\ System \\ CurrentControlSet \\ Services \\ Tssdis \\ Parameters.** Der Standardwert 1 gibt an, dass ausstehende Sitzungen die gleiche Gewichtung wie aktive Sitzungen haben.

Diese Eigenschaft ist auf Windows Server 2012 R2 mit [KB3091411](https://support.microsoft.com/kb/3091411) verfügbar, das in der [**ITsSbTargetEx-Schnittstelle installiert**](itssbtargetex.md) ist.

## <a name="requirements"></a>Anforderungen




| | | Mindestens unterstützter Client<br /> | Keine unterstützt<br /> | | Unterstützter Mindestserver<br /> | Windows Server 2016<br /> | | IDL<br /> | <dl><dt>Sbtsv.idl</dt></dl> | | IID<br /> | IID_ITsSbTarget ist wie:<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 auf Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





