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
# <a name="itssbtargettargetload-property"></a><span data-ttu-id="2ba88-108">Itssbtarget:: targetload-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2ba88-108">ITsSbTarget::TargetLoad property</span></span>

<span data-ttu-id="2ba88-109">Ruft die relative Auslastung eines Ziels ab.</span><span class="sxs-lookup"><span data-stu-id="2ba88-109">Retrieves the relative load on a target.</span></span> <span data-ttu-id="2ba88-110">Dieser Wert basiert auf der Anzahl der vorhandenen und ausstehenden Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="2ba88-110">This value is based on the number of existing and pending sessions.</span></span> <span data-ttu-id="2ba88-111">Standardmäßig hat eine ausstehende Sitzung denselben Wert wie eine vorhandene Sitzung.</span><span class="sxs-lookup"><span data-stu-id="2ba88-111">By default a pending session has the same value as an existing session.</span></span>

<span data-ttu-id="2ba88-112">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2ba88-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ba88-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ba88-113">Syntax</span></span>


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a><span data-ttu-id="2ba88-114">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2ba88-114">Property value</span></span>

<span data-ttu-id="2ba88-115">Eine Zahl, die die relative Auslastung eines Ziels darstellt.</span><span class="sxs-lookup"><span data-stu-id="2ba88-115">A number representing the relative load on a target.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ba88-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ba88-116">Remarks</span></span>

<span data-ttu-id="2ba88-117">Die Gewichtung einer ausstehenden Sitzung in Relation zu einer aktiven Sitzung kann geändert werden, indem der Wert des *lb- \_ connectionmenshmentpenalty* -Parameters für den Verbindungs Broker festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="2ba88-117">The weight of a pending session relative to an active session can be changed by setting the value of the *LB\_ConnectionEstablishmentPenalty* parameter for the Connection Broker.</span></span> <span data-ttu-id="2ba88-118">Dieser Parameter befindet sich unter dem Registrierungsschlüssel "**HKLM \\ System \\ CurrentControlSet \\ Services \\ Tssdis \\ para** meters".</span><span class="sxs-lookup"><span data-stu-id="2ba88-118">This parameter is located under the **HKLM\\System\\CurrentControlSet\\Services\\Tssdis\\Parameters** registry key.</span></span> <span data-ttu-id="2ba88-119">Der Standardwert 1 gibt an, dass ausstehende Sitzungen dieselbe Gewichtung aufweisen wie aktive Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="2ba88-119">The default value of 1 specifies that pending sessions have the same weight as active sessions.</span></span>

<span data-ttu-id="2ba88-120">Diese Eigenschaft ist auf Windows Server 2012 R2 mit installiertem [KB3091411](https://support.microsoft.com/kb/3091411) in der [**itssbtargetex**](itssbtargetex.md) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2ba88-120">This property is available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbTargetEx**](itssbtargetex.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ba88-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ba88-121">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ba88-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ba88-122">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="2ba88-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2ba88-123">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ba88-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ba88-124">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="2ba88-125">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2ba88-125">Windows Server 2016</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ba88-126">IDL</span><span class="sxs-lookup"><span data-stu-id="2ba88-126">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="2ba88-127"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="2ba88-127"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ba88-128">IID</span><span class="sxs-lookup"><span data-stu-id="2ba88-128">IID</span></span><br/></td>
<td><span data-ttu-id="2ba88-129">IID_ITsSbTarget ist definiert als:</span><span class="sxs-lookup"><span data-stu-id="2ba88-129">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="2ba88-130">16616ecc-272d-411d-b324-126893033856</span><span class="sxs-lookup"><span data-stu-id="2ba88-130">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="2ba88-131">e85e10ea-db0b-4752-b456-5sd5840901c0 unter Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2ba88-131">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="2ba88-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ba88-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ba88-133">**Itssbtargetex**</span><span class="sxs-lookup"><span data-stu-id="2ba88-133">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="2ba88-134">**Itssbtarget**</span><span class="sxs-lookup"><span data-stu-id="2ba88-134">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





