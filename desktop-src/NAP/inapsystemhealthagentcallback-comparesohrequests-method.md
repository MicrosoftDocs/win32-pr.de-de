---
title: Inapsystemhealthagentcallback comparesohrequests-Methode (napsystemhealthagent. h)
description: Wird vom SHA zum Vergleichen von SoH-Anforderungen verwendet.
ms.assetid: 14ba189a-e745-44b0-b729-522087d4e08b
keywords:
- Comparesohrequests-Methode NAP
- Comparesohrequests-Methode NAP, inapsystemhealthagentcallback-Schnittstelle
- Inapsystemhealthagentcallback-Schnittstelle NAP, comparesohrequests-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.CompareSoHRequests
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6713f3de47cfbde6df67662f89ab3c094d0674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338551"
---
# <a name="inapsystemhealthagentcallbackcomparesohrequests-method"></a><span data-ttu-id="91653-106">Inapsystemhealthagentcallback:: comparesohrequests-Methode</span><span class="sxs-lookup"><span data-stu-id="91653-106">INapSystemHealthAgentCallback::CompareSoHRequests method</span></span>

> [!Note]  
> <span data-ttu-id="91653-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="91653-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="91653-108">Die **inapsystemhealthagentcallback:: comparesohrequests** -Methode wird vom SHA zum Vergleichen von SoH-Anforderungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="91653-108">The **INapSystemHealthAgentCallback::CompareSoHRequests** method is used by the SHA to compare SoH requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="91653-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="91653-109">Syntax</span></span>


```C++
HRESULT CompareSoHRequests(
  [in]  const SoHRequest *lhs,
  [in]  const SoHRequest *rhs,
  [out]       BOOL       *isEqual
);
```



## <a name="parameters"></a><span data-ttu-id="91653-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="91653-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91653-111">*LHS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91653-111">*lhs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91653-112">Ein Zeiger auf den [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) Links vom Vergleichs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="91653-112">A pointer to the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the left of the comparison operation.</span></span>

</dd> <dt>

<span data-ttu-id="91653-113">*RHS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91653-113">*rhs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91653-114">Ein Zeiger auf den [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) auf der rechten Seite des Vergleichs Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="91653-114">A pointer to the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the right of the comparison operation.</span></span>

</dd> <dt>

<span data-ttu-id="91653-115">*IsEqual* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="91653-115">*isEqual* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91653-116">Ein Zeiger auf einen **booleschen** Wert, der **true** ist, wenn *LHS* und *RHS* semantisch gleich sind, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="91653-116">A pointer to a **BOOL** that is **TRUE** if *lhs* and *rhs* are semantically equal, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91653-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91653-117">Return value</span></span>

<span data-ttu-id="91653-118">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="91653-118">This method can return one of these values.</span></span>



| <span data-ttu-id="91653-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="91653-119">Return code</span></span>                                                                               | <span data-ttu-id="91653-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91653-120">Description</span></span>                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="91653-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="91653-121"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="91653-122">Gibt die erfolgreiche Ausführung an.</span><span class="sxs-lookup"><span data-stu-id="91653-122">Indicates success.</span></span><br/>                         |
| <dl> <span data-ttu-id="91653-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="91653-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="91653-124">Die Methode wurde nicht vom SHA implementiert.</span><span class="sxs-lookup"><span data-stu-id="91653-124">The method was not implemented by the SHA.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="91653-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91653-125">Remarks</span></span>

<span data-ttu-id="91653-126">Diese Rückruf Methode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="91653-126">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="91653-127">Der SHA sollte die SoHs vergleichen und **true** zurückgeben, wenn die SoHs semantisch gleich sind.</span><span class="sxs-lookup"><span data-stu-id="91653-127">The SHA should compare the SoHs and return **TRUE** if the SoHs are semantically equal.</span></span> <span data-ttu-id="91653-128">Der NAPAgent verwendet diese Informationen, um zu bestimmen, ob ein SoH-Austausch aufgrund einer Änderung des Zustands des Client Computers initiiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="91653-128">The NapAgent uses this information to determine if an SoH exchange should be initiated due to change of state of the client machine.</span></span>

<span data-ttu-id="91653-129">Wenn SHAs inkrementelle IDs oder Zeitstempel in Ihrem SoH abgelegt haben, sind SoHs möglicherweise semantisch gleich (d. h., Sie können dieselben Integritäts Informationen vermitteln), Sie können jedoch Byte Weise ungleich sein.</span><span class="sxs-lookup"><span data-stu-id="91653-129">If SHAs have put incremental IDs or time-stamps into their SoH, then SoHs may be semantically equal (i.e. they may convey the same health information), but they may be byte-wise unequal.</span></span> <span data-ttu-id="91653-130">Diese Funktion sollte von SHAs implementiert werden, um die semantische Gleichheit von SoHs zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="91653-130">SHAs should implement this function to check for semantic equality of SoHs.</span></span>

<span data-ttu-id="91653-131">Wenn SHAs keine Zeitstempel oder IDs in ihren SoHs abgelegt haben, können Sie diese Funktion nicht implementieren und **E \_ notimpl** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="91653-131">If SHAs have not put any time-stamps or Ids into their SoHs, they may choose to not implement this function and return **E\_NOTIMPL**.</span></span> <span data-ttu-id="91653-132">In diesem Fall führt der NAPAgent einen Byte weisen Vergleich der [**sohrequests**](/windows/win32/api/naptypes/ns-naptypes-soh)durch.</span><span class="sxs-lookup"><span data-stu-id="91653-132">In this case, the NapAgent performs a byte-wise comparison on the [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="requirements"></a><span data-ttu-id="91653-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91653-133">Requirements</span></span>



| <span data-ttu-id="91653-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91653-134">Requirement</span></span> | <span data-ttu-id="91653-135">Wert</span><span class="sxs-lookup"><span data-stu-id="91653-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91653-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="91653-136">Minimum supported client</span></span><br/> | <span data-ttu-id="91653-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91653-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="91653-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="91653-138">Minimum supported server</span></span><br/> | <span data-ttu-id="91653-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="91653-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="91653-140">Header</span><span class="sxs-lookup"><span data-stu-id="91653-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="91653-141"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="91653-141"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="91653-142">IDL</span><span class="sxs-lookup"><span data-stu-id="91653-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="91653-143"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="91653-143"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91653-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91653-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91653-145">**Inapsystemhealthagentcallback**</span><span class="sxs-lookup"><span data-stu-id="91653-145">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> <dt>

[<span data-ttu-id="91653-146">**SoH**</span><span class="sxs-lookup"><span data-stu-id="91653-146">**SoH**</span></span>](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> </dl>

 

 





