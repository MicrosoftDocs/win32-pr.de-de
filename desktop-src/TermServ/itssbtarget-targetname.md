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
# <a name="itssbtargettargetname-property"></a><span data-ttu-id="c8b5c-108">Itssbtarget:: TargetName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c8b5c-108">ITsSbTarget::TargetName property</span></span>

<span data-ttu-id="c8b5c-109">Gibt den Namen des Ziels an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="c8b5c-109">Specifies or retrieves the name of the target.</span></span>

<span data-ttu-id="c8b5c-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c8b5c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b5c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8b5c-111">Syntax</span></span>


```C++
HRESULT put_TargetName(
  [in]          BSTR Val
);

HRESULT get_TargetName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="c8b5c-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c8b5c-112">Property value</span></span>

<span data-ttu-id="c8b5c-113">Eine **BSTR** -Variable, die den Zielnamen angibt.</span><span class="sxs-lookup"><span data-stu-id="c8b5c-113">A **BSTR** variable that specifies the target name.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8b5c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8b5c-114">Remarks</span></span>

<span data-ttu-id="c8b5c-115">Diese Eigenschaft war vor Windows Server 2012 schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c8b5c-115">This property was read-only prior to Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8b5c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8b5c-116">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8b5c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8b5c-117">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="c8b5c-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c8b5c-118">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8b5c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8b5c-119">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="c8b5c-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c8b5c-120">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c8b5c-121">IDL</span><span class="sxs-lookup"><span data-stu-id="c8b5c-121">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="c8b5c-122"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="c8b5c-122"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8b5c-123">IID</span><span class="sxs-lookup"><span data-stu-id="c8b5c-123">IID</span></span><br/></td>
<td><span data-ttu-id="c8b5c-124">IID_ITsSbTarget ist definiert als:</span><span class="sxs-lookup"><span data-stu-id="c8b5c-124">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="c8b5c-125">16616ecc-272d-411d-b324-126893033856</span><span class="sxs-lookup"><span data-stu-id="c8b5c-125">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="c8b5c-126">e85e10ea-db0b-4752-b456-5sd5840901c0 unter Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c8b5c-126">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="c8b5c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8b5c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8b5c-128">**Itssbtargetex**</span><span class="sxs-lookup"><span data-stu-id="c8b5c-128">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="c8b5c-129">**Itssbtarget**</span><span class="sxs-lookup"><span data-stu-id="c8b5c-129">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





