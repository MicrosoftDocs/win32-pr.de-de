---
title: Counters. Remove-Methode
description: Entfernt eine-Instanz aus der Auflistung.
ms.assetid: 88e5907a-8c8f-4a24-9c5d-0c592f61dac0
keywords:
- Remove-Methode (Sysmon)
- Remove-Methode (Sysmon), counters-Klasse
- Zähler Klasse sysmon, Methode entfernen
topic_type:
- apiref
api_name:
- Counters.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa82a1a988be3554c265c097ba2a582035547391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949747"
---
# <a name="countersremove-method"></a><span data-ttu-id="f060a-106">Counters. Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="f060a-106">Counters.Remove method</span></span>

<span data-ttu-id="f060a-107">Entfernt eine [**-**](counteritem.md) Instanz aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="f060a-107">Removes a [**CounterItem**](counteritem.md) instance from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f060a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f060a-108">Syntax</span></span>


```VB
Counters.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="f060a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f060a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f060a-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f060a-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f060a-111">Der Index des aus der Auflistung zu entfernenden [**ratteritem**](counteritem.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f060a-111">Index of the [**CounterItem**](counteritem.md) object to remove from the collection.</span></span> <span data-ttu-id="f060a-112">Der Index ist 1-basiert.</span><span class="sxs-lookup"><span data-stu-id="f060a-112">The index is one-based.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f060a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f060a-113">Return value</span></span>

<span data-ttu-id="f060a-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f060a-114">This method does not return a value.</span></span>

## <a name="exceptions"></a><span data-ttu-id="f060a-115">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="f060a-115">Exceptions</span></span>



| <span data-ttu-id="f060a-116">Ausnahmetyp</span><span class="sxs-lookup"><span data-stu-id="f060a-116">Exception type</span></span>                                  | <span data-ttu-id="f060a-117">Bedingung</span><span class="sxs-lookup"><span data-stu-id="f060a-117">Condition</span></span>                                                      |
|-------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f060a-118">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="f060a-118">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="f060a-119">Der angegebene Index ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f060a-119">The specified index is not valid.</span></span> <span data-ttu-id="f060a-120">Der Err. Number-Wert ist???.</span><span class="sxs-lookup"><span data-stu-id="f060a-120">The Err.Number value is ???.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f060a-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f060a-121">Remarks</span></span>

<span data-ttu-id="f060a-122">Wenn Sie alle Leistungsindikatoren aus der Sammlung entfernen möchten, können Sie [**Systemmonitor. Reset**](systemmonitor-reset.md)abrufen.</span><span class="sxs-lookup"><span data-stu-id="f060a-122">To remove all counters from the collection, you can call [**SystemMonitor.Reset**](systemmonitor-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f060a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f060a-123">Requirements</span></span>



| <span data-ttu-id="f060a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f060a-124">Requirement</span></span> | <span data-ttu-id="f060a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f060a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f060a-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f060a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f060a-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f060a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f060a-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f060a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f060a-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f060a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f060a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f060a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f060a-131"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f060a-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f060a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f060a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f060a-133">**Counters**</span><span class="sxs-lookup"><span data-stu-id="f060a-133">**Counters**</span></span>](counters.md)
</dt> <dt>

[<span data-ttu-id="f060a-134">**Systemmonitor. Reset**</span><span class="sxs-lookup"><span data-stu-id="f060a-134">**SystemMonitor.Reset**</span></span>](systemmonitor-reset.md)
</dt> </dl>

 

 





