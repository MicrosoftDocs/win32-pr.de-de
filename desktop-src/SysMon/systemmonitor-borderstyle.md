---
title: Systemmonitor. BorderStyle (Eigenschaft)
description: Ruft die Rahmenart des Steuer Elements ab oder legt diese fest.
ms.assetid: 9151a3f6-71fb-43ea-b7f6-cc35048145cb
keywords:
- BorderStyle-Eigenschaften-sysmon
- BorderStyle-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse sysmon, BorderStyle (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.BorderStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5dd0cec7e4d0d6d3223da4486d4569f8bc611e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858844"
---
# <a name="systemmonitorborderstyle-property"></a><span data-ttu-id="f15b6-106">Systemmonitor. BorderStyle (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f15b6-106">SystemMonitor.BorderStyle property</span></span>

<span data-ttu-id="f15b6-107">Ruft die Rahmenart des Steuer Elements ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="f15b6-107">Retrieves or sets the border style of the control.</span></span>

<span data-ttu-id="f15b6-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f15b6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f15b6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f15b6-109">Syntax</span></span>


```VB
Property BorderStyle As Long
```



## <a name="property-value"></a><span data-ttu-id="f15b6-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f15b6-110">Property value</span></span>

<span data-ttu-id="f15b6-111">Rahmenart des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="f15b6-111">Border style of the control.</span></span>

<span data-ttu-id="f15b6-112">Sie können diese Eigenschaft auf einen der folgenden Werte festlegen.</span><span class="sxs-lookup"><span data-stu-id="f15b6-112">You can set this property to one of the following values.</span></span>



| <span data-ttu-id="f15b6-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f15b6-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="f15b6-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f15b6-114">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="System.Windows.Forms.FormBorderStyle.VbBSNone"></span><span id="system.windows.forms.formborderstyle.vbbsnone"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBBSNONE"></span><dl> <span data-ttu-id="f15b6-115"><dt>**System. Windows. Forms. FormBorderStyle. vbbsnone**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f15b6-115"><dt>**System.Windows.Forms.FormBorderStyle.VbBSNone**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="f15b6-116">Kein Rahmen.</span><span class="sxs-lookup"><span data-stu-id="f15b6-116">No border.</span></span> <span data-ttu-id="f15b6-117">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="f15b6-117">This is the default value.</span></span><br/> |
| <span id="System.Windows.Forms.FormBorderStyle.VbFixedSingle"></span><span id="system.windows.forms.formborderstyle.vbfixedsingle"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBFIXEDSINGLE"></span><dl> <span data-ttu-id="f15b6-118"><dt>**System. Windows. Forms. FormBorderStyle. vbfixedsingle**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f15b6-118"><dt>**System.Windows.Forms.FormBorderStyle.VbFixedSingle**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="f15b6-119">Fixed, Single Border.</span><span class="sxs-lookup"><span data-stu-id="f15b6-119">Fixed, single border.</span></span><br/>                 |



 

## <a name="exceptions"></a><span data-ttu-id="f15b6-120">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="f15b6-120">Exceptions</span></span>



| <span data-ttu-id="f15b6-121">Ausnahmetyp</span><span class="sxs-lookup"><span data-stu-id="f15b6-121">Exception type</span></span>               | <span data-ttu-id="f15b6-122">Bedingung</span><span class="sxs-lookup"><span data-stu-id="f15b6-122">Condition</span></span>                                |
|------------------------------|------------------------------------------|
| <span data-ttu-id="f15b6-123">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="f15b6-123">**System.ArgumentException**</span></span> | <span data-ttu-id="f15b6-124">Die angegebene Rahmenart ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f15b6-124">The specified border style is not valid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="f15b6-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f15b6-125">Requirements</span></span>



| <span data-ttu-id="f15b6-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f15b6-126">Requirement</span></span> | <span data-ttu-id="f15b6-127">Wert</span><span class="sxs-lookup"><span data-stu-id="f15b6-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f15b6-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f15b6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f15b6-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f15b6-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f15b6-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f15b6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f15b6-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f15b6-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f15b6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f15b6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f15b6-133"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f15b6-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f15b6-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f15b6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f15b6-135">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="f15b6-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





