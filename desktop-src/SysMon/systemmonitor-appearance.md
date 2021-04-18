---
title: Systemmonitor. Appearance (Eigenschaft)
description: Ruft die Darstellung des Steuer Elements ab oder legt diese fest, um dreidimensionale Anzeige Effekte einzuschließen oder auszulassen.
ms.assetid: cbc1f17f-991a-4b35-9c64-7750a17b42c8
keywords:
- Darstellungs Eigenschaft (Sysmon)
- Darstellungs Eigenschaft "sysmon", Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", Darstellungs Eigenschaft
topic_type:
- apiref
api_name:
- SystemMonitor.Appearance
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200c66f83a47f15421480967e8ea1ae9509b13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340308"
---
# <a name="systemmonitorappearance-property"></a><span data-ttu-id="5bba3-106">Systemmonitor. Appearance (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5bba3-106">SystemMonitor.Appearance property</span></span>

<span data-ttu-id="5bba3-107">Ruft die Darstellung des Steuer Elements ab oder legt diese fest, um dreidimensionale Anzeige Effekte einzuschließen oder auszulassen.</span><span class="sxs-lookup"><span data-stu-id="5bba3-107">Retrieves or sets the control's appearance to include or omit three-dimensional display effects.</span></span>

<span data-ttu-id="5bba3-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5bba3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bba3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bba3-109">Syntax</span></span>


```VB
Property Appearance As Long
```



## <a name="property-value"></a><span data-ttu-id="5bba3-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5bba3-110">Property value</span></span>

<span data-ttu-id="5bba3-111">Der Darstellungs Wert, der bestimmt, ob das Steuerelement mit dreidimensionalen Effekten gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="5bba3-111">Appearance value that determines if the control is painted with three-dimensional effects.</span></span>

<span data-ttu-id="5bba3-112">Sie können diese Eigenschaft auf einen der folgenden Werte festlegen.</span><span class="sxs-lookup"><span data-stu-id="5bba3-112">You can set this property to one of the following values.</span></span>



| <span data-ttu-id="5bba3-113">Wert</span><span class="sxs-lookup"><span data-stu-id="5bba3-113">Value</span></span>                                                                        | <span data-ttu-id="5bba3-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5bba3-114">Meaning</span></span>                                                                                  |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5bba3-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5bba3-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="5bba3-116">Zeichnet das Steuerelement ohne visuelle Effekte.</span><span class="sxs-lookup"><span data-stu-id="5bba3-116">Paints the control without visual effects.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5bba3-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5bba3-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="5bba3-118">Zeichnet das-Steuerelement mit dreidimensionalen Effekten.</span><span class="sxs-lookup"><span data-stu-id="5bba3-118">Paints the control with three-dimensional effects.</span></span> <span data-ttu-id="5bba3-119">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="5bba3-119">This is the default value.</span></span><br/> |



 

## <a name="exceptions"></a><span data-ttu-id="5bba3-120">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="5bba3-120">Exceptions</span></span>



| <span data-ttu-id="5bba3-121">Ausnahmetyp</span><span class="sxs-lookup"><span data-stu-id="5bba3-121">Exception type</span></span>               | <span data-ttu-id="5bba3-122">Bedingung</span><span class="sxs-lookup"><span data-stu-id="5bba3-122">Condition</span></span>                                    |
|------------------------------|----------------------------------------------|
| <span data-ttu-id="5bba3-123">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="5bba3-123">**System.ArgumentException**</span></span> | <span data-ttu-id="5bba3-124">Der angegebene Darstellungs Wert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5bba3-124">The specified appearance value is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5bba3-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bba3-125">Remarks</span></span>

<span data-ttu-id="5bba3-126">Dies ist eine Ambient-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5bba3-126">This is an ambient property.</span></span> <span data-ttu-id="5bba3-127">Der Wert dieser Eigenschaft wird vom Container bestimmt.</span><span class="sxs-lookup"><span data-stu-id="5bba3-127">The value of this property is determined by the container.</span></span> <span data-ttu-id="5bba3-128">Das Festlegen des Werts dieser Eigenschaft kann sich auf die Illusion des Steuer Elements und Containers auswirken, die eine einzelne Anwendung sind.</span><span class="sxs-lookup"><span data-stu-id="5bba3-128">Setting the value of this property could affect the illusion of the control and container being a single application.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bba3-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5bba3-129">Requirements</span></span>



| <span data-ttu-id="5bba3-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5bba3-130">Requirement</span></span> | <span data-ttu-id="5bba3-131">Wert</span><span class="sxs-lookup"><span data-stu-id="5bba3-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5bba3-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5bba3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5bba3-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bba3-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5bba3-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5bba3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5bba3-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bba3-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5bba3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5bba3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bba3-137"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="5bba3-137"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bba3-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bba3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bba3-139">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="5bba3-139">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





