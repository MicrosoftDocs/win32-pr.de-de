---
title: Itssbtarget Farmname (Eigenschaft)
description: Ruft den Namen der Farm ab, mit der dieses Ziel verknüpft ist, oder legt ihn fest.
ms.assetid: 83e168ae-f985-40f9-912b-496c0695f82a
ms.tgt_platform: multiple
keywords:
- Farmname-Eigenschaft Remotedesktopdienste
- Farmname-Eigenschaft Remotedesktopdienste, itssbtarget-Schnittstelle
- Itssbtarget-Schnittstelle Remotedesktopdienste, Farmname-Eigenschaft
- Farmname-Eigenschaft Remotedesktopdienste, itssbtargetex-Schnittstelle
- Itssbtargetex-Schnittstelle Remotedesktopdienste, Farmname-Eigenschaft
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
ms.openlocfilehash: b94f86b2cf0ec257be9fe9b801e6fceae364a46e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718318"
---
# <a name="itssbtargetfarmname-property"></a>Itssbtarget:: Farmname-Eigenschaft

Ruft den Namen der Farm ab, mit der dieses Ziel verknüpft ist, oder legt ihn fest.

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

Eine **BSTR** -Variable, die den Namen der Farm enthält.

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

 

 





