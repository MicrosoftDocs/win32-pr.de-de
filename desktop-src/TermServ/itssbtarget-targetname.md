---
title: Itssbtarget TargetName-Eigenschaft
description: Gibt den Namen des Ziels an oder ruft ihn ab.
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- TargetName-Eigenschaft Remotedesktopdienste
- TargetName-Eigenschaft Remotedesktopdienste, itssbtarget-Schnittstelle
- Itssbtarget-Schnittstelle Remotedesktopdienste, TargetName-Eigenschaft
- TargetName-Eigenschaft Remotedesktopdienste, itssbtargetex-Schnittstelle
- Itssbtargetex-Schnittstelle Remotedesktopdienste, TargetName-Eigenschaft
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
ms.openlocfilehash: 7dce949abee4ca00184a2b784ab154dbd75b9de6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038167"
---
# <a name="itssbtargettargetname-property"></a>Itssbtarget:: TargetName-Eigenschaft

Gibt den Namen des Ziels an oder ruft ihn ab.

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

Eine **BSTR** -Variable, die den Zielnamen angibt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft war vor Windows Server 2012 schreibgeschützt.

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
<td>Windows Server 2012<br/></td>
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

 

 





