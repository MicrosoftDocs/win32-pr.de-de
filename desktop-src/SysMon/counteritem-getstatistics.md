---
title: Countryteritem. getstatistics-Methode
description: Ruft die durchschnittlichen, maximalen und minimalen Werte für den Zählers ab.
ms.assetid: fb55d68b-1dbe-48b1-88c8-51f33048ec24
keywords:
- Getstatistics-Methode (Sysmon)
- Getstatistics-Methode "sysmon", "count"-Klasse
- Namteritem Class sysmon, getstatistics-Methode
topic_type:
- apiref
api_name:
- CounterItem.GetStatistics
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c993ed8b9bb39a4d8bb3ff18663f2d884ece156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956596"
---
# <a name="counteritemgetstatistics-method"></a><span data-ttu-id="5f0fd-106">Countryteritem. getstatistics-Methode</span><span class="sxs-lookup"><span data-stu-id="5f0fd-106">CounterItem.GetStatistics method</span></span>

<span data-ttu-id="5f0fd-107">Ruft die durchschnittlichen, maximalen und minimalen Werte für den Zählers ab.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-107">Retrieves the average, maximum, and minimum values for the counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f0fd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f0fd-108">Syntax</span></span>


```VB
CounterItem.GetStatistics( _
  ByRef max As Double, _
  ByRef min As Double, _
  ByRef average As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="5f0fd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f0fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f0fd-110">*Max* \[ . vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5f0fd-110">*max* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f0fd-111">Maximaler Wert des Zählers.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-111">Maximum value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="5f0fd-112">*Min* \[ . vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5f0fd-112">*min* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f0fd-113">Der Minimalwert des Zählers.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-113">Minimum value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="5f0fd-114">*Durchschnitt* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5f0fd-114">*average* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f0fd-115">Der Durchschnittswert des Zählers.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-115">Average value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="5f0fd-116">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5f0fd-116">*status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f0fd-117">Gibt an, ob die Werte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-117">Indicates if the values are valid.</span></span>



| <span data-ttu-id="5f0fd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5f0fd-118">Value</span></span>                                                                                              | <span data-ttu-id="5f0fd-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5f0fd-119">Meaning</span></span>                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="5f0fd-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5f0fd-120"><dt>0</dt></span></span> </dl>                       | <span data-ttu-id="5f0fd-121">Die Werte sind gültig.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-121">The values are valid.</span></span><br/>     |
| <dl> <span data-ttu-id="5f0fd-122"><dt>0xc0000bba (3221228474)</dt></span><span class="sxs-lookup"><span data-stu-id="5f0fd-122"><dt>0xC0000BBA (3221228474)</dt></span></span> </dl> | <span data-ttu-id="5f0fd-123">Die Werte sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-123">The values are not valid.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f0fd-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f0fd-124">Return value</span></span>

<span data-ttu-id="5f0fd-125">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-125">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f0fd-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f0fd-126">Remarks</span></span>

<span data-ttu-id="5f0fd-127">Es werden nur die im Diagramm fenstersicht baren Werte verwendet, um die statistischen Werte zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="5f0fd-127">Only those counter values that are visible in the graph window are used to calculate the statistical values.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f0fd-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f0fd-128">Requirements</span></span>



| <span data-ttu-id="5f0fd-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f0fd-129">Requirement</span></span> | <span data-ttu-id="5f0fd-130">Wert</span><span class="sxs-lookup"><span data-stu-id="5f0fd-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5f0fd-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f0fd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5f0fd-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f0fd-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5f0fd-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f0fd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5f0fd-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f0fd-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5f0fd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5f0fd-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f0fd-136"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="5f0fd-136"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f0fd-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f0fd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f0fd-138">**Ratteritem**</span><span class="sxs-lookup"><span data-stu-id="5f0fd-138">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="5f0fd-139">**"Count. getdataat"**</span><span class="sxs-lookup"><span data-stu-id="5f0fd-139">**CounterItem.GetDataAt**</span></span>](counteritem-getdataat.md)
</dt> <dt>

[<span data-ttu-id="5f0fd-140">**"Count. GetValue"**</span><span class="sxs-lookup"><span data-stu-id="5f0fd-140">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





