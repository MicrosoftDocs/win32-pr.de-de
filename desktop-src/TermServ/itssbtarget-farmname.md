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
# <a name="itssbtargetfarmname-property"></a><span data-ttu-id="1e094-108">Itssbtarget:: Farmname-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1e094-108">ITsSbTarget::FarmName property</span></span>

<span data-ttu-id="1e094-109">Ruft den Namen der Farm ab, mit der dieses Ziel verknüpft ist, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="1e094-109">Retrieves or specifies the name of the farm to which this target is joined.</span></span>

<span data-ttu-id="1e094-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1e094-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e094-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e094-111">Syntax</span></span>


```C++
HRESULT put_FarmName(
  [in]          BSTR Val
);

HRESULT get_FarmName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="1e094-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1e094-112">Property value</span></span>

<span data-ttu-id="1e094-113">Eine **BSTR** -Variable, die den Namen der Farm enthält.</span><span class="sxs-lookup"><span data-stu-id="1e094-113">A **BSTR** variable that contains the farm name.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e094-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e094-114">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e094-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e094-115">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="1e094-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1e094-116">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e094-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e094-117">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="1e094-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1e094-118">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e094-119">IDL</span><span class="sxs-lookup"><span data-stu-id="1e094-119">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="1e094-120"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="1e094-120"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e094-121">IID</span><span class="sxs-lookup"><span data-stu-id="1e094-121">IID</span></span><br/></td>
<td><span data-ttu-id="1e094-122">IID_ITsSbTarget ist definiert als:</span><span class="sxs-lookup"><span data-stu-id="1e094-122">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="1e094-123">16616ecc-272d-411d-b324-126893033856</span><span class="sxs-lookup"><span data-stu-id="1e094-123">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="1e094-124">e85e10ea-db0b-4752-b456-5sd5840901c0 unter Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1e094-124">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="1e094-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e094-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e094-126">**Itssbtargetex**</span><span class="sxs-lookup"><span data-stu-id="1e094-126">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="1e094-127">**Itssbtarget**</span><span class="sxs-lookup"><span data-stu-id="1e094-127">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





