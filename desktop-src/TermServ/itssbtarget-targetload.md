---
title: ITsSbTarget TargetLoad-Eigenschaft
description: Ruft die relative Last auf einem Ziel ab.
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- TargetLoad-Eigenschaft Remotedesktopdienste
- TargetLoad-Eigenschaft Remotedesktopdienste , ITsSbTarget-Schnittstelle
- ITsSbTarget-Schnittstelle Remotedesktopdienste , TargetLoad-Eigenschaft
- TargetLoad-Eigenschaft Remotedesktopdienste , ITsSbTargetEx-Schnittstelle
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
ms.openlocfilehash: 3c367e9c00caff78bb3e64263c1622de45fa6e640e78d88239e1ed25a6f68558
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989860"
---
# <a name="itssbtargettargetload-property"></a>ITsSbTarget::TargetLoad-Eigenschaft

Ruft die relative Last auf einem Ziel ab. Dieser Wert basiert auf der Anzahl vorhandener und ausstehender Sitzungen. Standardmäßig hat eine ausstehende Sitzung den gleichen Wert wie eine vorhandene Sitzung.

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

Die Gewichtung einer ausstehenden Sitzung relativ zu einer aktiven Sitzung kann durch Festlegen des Werts des *Parameters LB \_ ConnectionEstablishmentPenalty* für den Verbindungsbroker geändert werden. Dieser Parameter befindet sich unter dem **Registrierungsschlüssel HKLM \\ System \\ CurrentControlSet \\ Services \\ Tssdis \\ Parameters.** Der Standardwert 1 gibt an, dass ausstehende Sitzungen die gleiche Gewichtung wie aktive Sitzungen haben.

Diese Eigenschaft ist auf Windows Server 2012 R2 verfügbar, wobei [KB3091411](https://support.microsoft.com/kb/3091411) in der [**ITsSbTargetEx-Schnittstelle**](itssbtargetex.md) installiert ist.

## <a name="requirements"></a>Anforderungen



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Unterstützte Mindestversion (Client)<br/></td>
<td>Nicht unterstützt<br/></td>
</tr>
<tr class="even">
<td>Unterstützte Mindestversion (Server)<br/></td>
<td>Windows Server 2016<br/></td>
</tr>
<tr class="odd">
<td>Idl<br/></td>
<td><dl> <dt>Sbtsv.idl</dt> </dl></td>
</tr>
<tr class="even">
<td>IID<br/></td>
<td>IID_ITsSbTarget wird wie folgt definiert:
<ul>
<li>16616ECC-272D-411D-B324-126893033856</li>
<li>e85e10ea-db0b-4752-b456-5fd5840901c0 auf Windows Server 2008 R2</li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





