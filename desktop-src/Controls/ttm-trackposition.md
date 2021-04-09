---
title: TTM_TRACKPOSITION Meldung (kommstrg. h)
description: Legt die Position einer nach Verfolgungs-QuickInfo fest.
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- Windows-Steuerelemente für TTM_TRACKPOSITION Meldung
topic_type:
- apiref
api_name:
- TTM_TRACKPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6eab8184049d8bf876a7e782b9adc2091d5fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040759"
---
# <a name="ttm_trackposition-message"></a><span data-ttu-id="a4059-104">TTM \_ trackposition-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a4059-104">TTM\_TRACKPOSITION message</span></span>

<span data-ttu-id="a4059-105">Legt die Position einer nach Verfolgungs-QuickInfo fest.</span><span class="sxs-lookup"><span data-stu-id="a4059-105">Sets the position of a tracking tooltip.</span></span>

## <a name="parameters"></a><span data-ttu-id="a4059-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4059-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4059-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a4059-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4059-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a4059-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a4059-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4059-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4059-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die x-Koordinate des Punkts an, an dem die nach Verfolgungs-QuickInfo in Bildschirm Koordinaten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a4059-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the x-coordinate of the point at which the tracking tooltip will be displayed, in screen coordinates.</span></span> <span data-ttu-id="a4059-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die y-Koordinate des Punkts an, an dem die nach Verfolgungs-QuickInfo in Bildschirm Koordinaten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a4059-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the y-coordinate of the point at which the tracking tooltip will be displayed, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4059-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4059-112">Return value</span></span>

<span data-ttu-id="a4059-113">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a4059-113">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4059-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4059-114">Remarks</span></span>

<span data-ttu-id="a4059-115">Das QuickInfo-Steuerelement wählt basierend auf den Koordinaten, die Sie mit dieser Meldung bereitstellen, das QuickInfo-Fenster aus.</span><span class="sxs-lookup"><span data-stu-id="a4059-115">The tooltip control chooses where to display the tooltip window based on the coordinates you provide with this message.</span></span> <span data-ttu-id="a4059-116">Dies bewirkt, dass das QuickInfo-Fenster neben dem Tool angezeigt wird, dem es entspricht.</span><span class="sxs-lookup"><span data-stu-id="a4059-116">This causes the tooltip window to appear beside the tool to which it corresponds.</span></span> <span data-ttu-id="a4059-117">Wenn QuickInfo-Fenster an bestimmten Koordinaten angezeigt werden sollen, schließen Sie beim Hinzufügen des Tools das "ttf absolute"- \_ Flag in den **uFlags** -Member der [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur ein.</span><span class="sxs-lookup"><span data-stu-id="a4059-117">To have tooltip windows displayed at specific coordinates, include the TTF\_ABSOLUTE flag in the **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure when adding the tool.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4059-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4059-118">Requirements</span></span>



| <span data-ttu-id="a4059-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4059-119">Requirement</span></span> | <span data-ttu-id="a4059-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a4059-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4059-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4059-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a4059-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4059-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a4059-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4059-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a4059-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4059-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a4059-125">Header</span><span class="sxs-lookup"><span data-stu-id="a4059-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4059-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4059-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4059-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4059-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="a4059-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="a4059-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a4059-129">**TTM \_ trackaktivierungs**</span><span class="sxs-lookup"><span data-stu-id="a4059-129">**TTM\_TRACKACTIVATE**</span></span>](ttm-trackactivate.md)
</dt> <dt>

<span data-ttu-id="a4059-130">**Licher**</span><span class="sxs-lookup"><span data-stu-id="a4059-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a4059-131">Verwenden von Quick Infos</span><span class="sxs-lookup"><span data-stu-id="a4059-131">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

