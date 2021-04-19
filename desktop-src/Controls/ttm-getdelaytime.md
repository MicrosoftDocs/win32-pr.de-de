---
title: TTM_GETDELAYTIME Meldung (kommstrg. h)
description: Ruft die anfänglichen, Popup-und neuanschau Dauer ab, die aktuell für ein QuickInfo-Steuerelement festgelegt sind.
ms.assetid: f89a75ed-ba80-4741-927f-c571f3b2efe7
keywords:
- Windows-Steuerelemente für TTM_GETDELAYTIME Meldung
topic_type:
- apiref
api_name:
- TTM_GETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff8c75f078465646333cae1f519049733a0c9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342435"
---
# <a name="ttm_getdelaytime-message"></a><span data-ttu-id="5983d-104">TTM \_ getdelta-Zeit Nachricht</span><span class="sxs-lookup"><span data-stu-id="5983d-104">TTM\_GETDELAYTIME message</span></span>

<span data-ttu-id="5983d-105">Ruft die anfänglichen, Popup-und neuanschau Dauer ab, die aktuell für ein QuickInfo-Steuerelement festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="5983d-105">Retrieves the initial, pop-up, and reshow durations currently set for a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5983d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5983d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5983d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5983d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5983d-108">Flag, das angibt, welcher Duration-Wert abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5983d-108">Flag that specifies which duration value will be retrieved.</span></span> <span data-ttu-id="5983d-109">Dieser Parameter kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="5983d-109">This parameter can have one of the following values:</span></span>



| <span data-ttu-id="5983d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="5983d-110">Value</span></span>                                                                                                                                                      | <span data-ttu-id="5983d-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5983d-111">Meaning</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <span data-ttu-id="5983d-112"><dt>**ttdt- \_ autopop**</dt></span><span class="sxs-lookup"><span data-stu-id="5983d-112"><dt>**TTDT\_AUTOPOP**</dt></span></span> </dl> | <span data-ttu-id="5983d-113">Ruft die Zeitspanne ab, die das QuickInfo-Fenster sichtbar bleibt, wenn der Zeiger innerhalb des umgebenden Rechtecks eines Tools stationär ist.</span><span class="sxs-lookup"><span data-stu-id="5983d-113">Retrieve the amount of time the tooltip window remains visible if the pointer is stationary within a tool's bounding rectangle.</span></span><br/>      |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <span data-ttu-id="5983d-114"><dt>**ttdt- \_ Initial**</dt></span><span class="sxs-lookup"><span data-stu-id="5983d-114"><dt>**TTDT\_INITIAL**</dt></span></span> </dl> | <span data-ttu-id="5983d-115">Ruft die Zeitspanne ab, die der Zeiger innerhalb des umgebenden Rechtecks eines Tools stationär bleiben muss, bevor das QuickInfo-Fenster angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5983d-115">Retrieve the amount of time the pointer must remain stationary within a tool's bounding rectangle before the tooltip window appears.</span></span><br/> |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <span data-ttu-id="5983d-116"><dt>**ttdt \_ erneut anzeigen**</dt></span><span class="sxs-lookup"><span data-stu-id="5983d-116"><dt>**TTDT\_RESHOW**</dt></span></span> </dl>    | <span data-ttu-id="5983d-117">Ruft die Zeitspanne ab, die benötigt wird, bis nachfolgende QuickInfo-Fenster angezeigt werden, wenn der Zeiger von einem Tool zu einem anderen verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="5983d-117">Retrieve the amount of time it takes for subsequent tooltip windows to appear as the pointer moves from one tool to another.</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="5983d-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5983d-118">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5983d-119">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="5983d-119">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5983d-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5983d-120">Return value</span></span>

<span data-ttu-id="5983d-121">Gibt einen int-Wert mit der angegebenen Dauer in Millisekunden zurück.</span><span class="sxs-lookup"><span data-stu-id="5983d-121">Returns and INT value with the specified duration in milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="5983d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5983d-122">Requirements</span></span>



| <span data-ttu-id="5983d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5983d-123">Requirement</span></span> | <span data-ttu-id="5983d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5983d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5983d-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5983d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5983d-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5983d-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5983d-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5983d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5983d-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5983d-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5983d-129">Header</span><span class="sxs-lookup"><span data-stu-id="5983d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5983d-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5983d-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5983d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5983d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5983d-132">**TTM \_ setdelta Time**</span><span class="sxs-lookup"><span data-stu-id="5983d-132">**TTM\_SETDELAYTIME**</span></span>](ttm-setdelaytime.md)
</dt> </dl>

 

 





