---
title: TTM_TRACKACTIVATE Meldung (kommstrg. h)
description: Aktiviert oder deaktiviert eine nach Verfolgungs-QuickInfo.
ms.assetid: 6cf43377-a772-4749-81c4-a685998092e5
keywords:
- Windows-Steuerelemente für TTM_TRACKACTIVATE Meldung
topic_type:
- apiref
api_name:
- TTM_TRACKACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3d0a6caf110045d694208c63aa81d63c265c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956714"
---
# <a name="ttm_trackactivate-message"></a><span data-ttu-id="d81d6-104">TTM \_ trackaktivierungs Meldung</span><span class="sxs-lookup"><span data-stu-id="d81d6-104">TTM\_TRACKACTIVATE message</span></span>

<span data-ttu-id="d81d6-105">Aktiviert oder deaktiviert eine nach Verfolgungs-QuickInfo.</span><span class="sxs-lookup"><span data-stu-id="d81d6-105">Activates or deactivates a tracking tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="d81d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d81d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d81d6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d81d6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d81d6-108">Ein Wert, der angibt, ob die Überwachung aktiviert oder deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="d81d6-108">Value specifying whether tracking is being activated or deactivated.</span></span> <span data-ttu-id="d81d6-109">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="d81d6-109">This value can be one of the following:</span></span>



| <span data-ttu-id="d81d6-110">Wert</span><span class="sxs-lookup"><span data-stu-id="d81d6-110">Value</span></span>                                                                                                                                | <span data-ttu-id="d81d6-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d81d6-111">Meaning</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="d81d6-112"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="d81d6-112"><dt>**TRUE**</dt></span></span> </dl>    | <span data-ttu-id="d81d6-113">Aktivieren Sie die Überwachung.</span><span class="sxs-lookup"><span data-stu-id="d81d6-113">Activate tracking.</span></span><br/>   |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="d81d6-114"><dt>**Alarm**</dt></span><span class="sxs-lookup"><span data-stu-id="d81d6-114"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="d81d6-115">Deaktivieren Sie die Überwachung.</span><span class="sxs-lookup"><span data-stu-id="d81d6-115">Deactivate tracking.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d81d6-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d81d6-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d81d6-117">Ein Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur, die das Tool identifiziert, für das diese Meldung gilt.</span><span class="sxs-lookup"><span data-stu-id="d81d6-117">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that identifies the tool to which this message applies.</span></span> <span data-ttu-id="d81d6-118">Die **HWND** -und **UID** -Member identifizieren das Tool, und das **CBSIZE** -Element gibt die Größe der Struktur an.</span><span class="sxs-lookup"><span data-stu-id="d81d6-118">The **hwnd** and **uId** members identify the tool, and the **cbSize** member specifies the size of the structure.</span></span> <span data-ttu-id="d81d6-119">Alle anderen Member werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d81d6-119">All other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d81d6-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d81d6-120">Return value</span></span>

<span data-ttu-id="d81d6-121">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d81d6-121">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d81d6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d81d6-122">Requirements</span></span>



| <span data-ttu-id="d81d6-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d81d6-123">Requirement</span></span> | <span data-ttu-id="d81d6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d81d6-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d81d6-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d81d6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d81d6-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d81d6-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d81d6-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d81d6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d81d6-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d81d6-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d81d6-129">Header</span><span class="sxs-lookup"><span data-stu-id="d81d6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d81d6-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d81d6-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d81d6-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d81d6-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="d81d6-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d81d6-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d81d6-133">**TTM \_ trackposition**</span><span class="sxs-lookup"><span data-stu-id="d81d6-133">**TTM\_TRACKPOSITION**</span></span>](ttm-trackposition.md)
</dt> <dt>

<span data-ttu-id="d81d6-134">**Licher**</span><span class="sxs-lookup"><span data-stu-id="d81d6-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d81d6-135">Verwenden von Quick Infos</span><span class="sxs-lookup"><span data-stu-id="d81d6-135">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 





