---
title: Itssbtarget targetload-Eigenschaft
description: Ruft die relative Auslastung eines Ziels ab.
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- Targetload-Eigenschaft Remotedesktopdienste
- Targetload-Eigenschaft Remotedesktopdienste, itssbtarget-Schnittstelle
- Itssbtarget-Schnittstelle Remotedesktopdienste, targetload-Eigenschaft
- Targetload-Eigenschaft Remotedesktopdienste, itssbtargetex-Schnittstelle
- Itssbtargetex-Schnittstelle Remotedesktopdienste, targetload-Eigenschaft
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
ms.openlocfilehash: ddfc9be9805406ab76b166e2a34bc47a7f5e9ab5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718582"
---
# <a name="itssbtargettargetload-property"></a>Itssbtarget:: targetload-Eigenschaft

Ruft die relative Auslastung eines Ziels ab. Dieser Wert basiert auf der Anzahl der vorhandenen und ausstehenden Sitzungen. Standardmäßig hat eine ausstehende Sitzung denselben Wert wie eine vorhandene Sitzung.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a>Eigenschaftswert

Eine Zahl, die die relative Auslastung eines Ziels darstellt.

## <a name="remarks"></a>Bemerkungen

Die Gewichtung einer ausstehenden Sitzung in Relation zu einer aktiven Sitzung kann geändert werden, indem der Wert des *lb- \_ connectionmenshmentpenalty* -Parameters für den Verbindungs Broker festgelegt wird. Dieser Parameter befindet sich unter dem Registrierungsschlüssel "**HKLM \\ System \\ CurrentControlSet \\ Services \\ Tssdis \\ para** meters". Der Standardwert 1 gibt an, dass ausstehende Sitzungen dieselbe Gewichtung aufweisen wie aktive Sitzungen.

Diese Eigenschaft ist auf Windows Server 2012 R2 mit installiertem [KB3091411](https://support.microsoft.com/kb/3091411) in der [**itssbtargetex**](itssbtargetex.md) -Schnittstelle verfügbar.

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
<td>IDL<br/></td>
<td><dl> <dt>Sbtsv. idl</dt> </dl></td>
</tr>
<tr class="even">
<td>IID<br/></td>
<td>IID_ITsSbTarget ist definiert als:
<ul>
<li>16616ecc-272d-411d-b324-126893033856</li>
<li>e85e10ea-db0b-4752-b456-5sd5840901c0 unter Windows Server 2008 R2</li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itssbtargetex**](itssbtargetex.md)
</dt> <dt>

[**Itssbtarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





