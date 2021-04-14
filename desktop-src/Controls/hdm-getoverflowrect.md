---
title: HDM_GETOVERFLOWRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck der Überlauf Schaltfläche ab, wenn der HDS \_ -Überlauf Stil für das Header Steuerelement festgelegt ist und die Überlauf Schaltfläche sichtbar ist. Senden Sie diese Nachricht explizit oder mithilfe des GetOverflowRect-Makros des Headers \_ .
ms.assetid: 52fb3dc3-ce22-40da-8222-20fd75c005ae
keywords:
- Windows-Steuerelemente für HDM_GETOVERFLOWRECT Meldung
topic_type:
- apiref
api_name:
- HDM_GETOVERFLOWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f521bb6b188a10bb7af52ead46423e7ae0cf58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518119"
---
# <a name="hdm_getoverflowrect-message"></a><span data-ttu-id="e4fcd-105">HDM \_ GETOVERFLOWRECT Meldung</span><span class="sxs-lookup"><span data-stu-id="e4fcd-105">HDM\_GETOVERFLOWRECT message</span></span>

<span data-ttu-id="e4fcd-106">Ruft das umgebende Rechteck der Überlauf Schaltfläche ab, wenn der [**HDS- \_ Überlauf**](header-control-styles.md) Stil für das Header Steuerelement festgelegt ist und die Überlauf Schaltfläche sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="e4fcd-106">Gets the bounding rectangle of the overflow button when the [**HDS\_OVERFLOW**](header-control-styles.md) style is set on the header control and the overflow button is visible.</span></span> <span data-ttu-id="e4fcd-107">Senden Sie diese Nachricht explizit oder mithilfe des [**\_ GetOverflowRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) -Makros des Headers.</span><span class="sxs-lookup"><span data-stu-id="e4fcd-107">Send this message explicitly or by using the [**Header\_GetOverflowRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4fcd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4fcd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4fcd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4fcd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4fcd-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4fcd-110">Not used.</span></span> <span data-ttu-id="e4fcd-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e4fcd-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e4fcd-112">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4fcd-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4fcd-113">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, um die umschließenden Rechteck Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e4fcd-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the bounding rectangle information.</span></span> <span data-ttu-id="e4fcd-114">Der Absender der Nachricht ist für die Zuordnung dieser Struktur verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="e4fcd-114">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="e4fcd-115">Die in der **Rect** -Struktur zurückgegebenen Koordinaten werden als Bildschirm Koordinaten ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="e4fcd-115">The coordinates returned in the **RECT** structure are expressed as screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4fcd-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4fcd-116">Return value</span></span>

<span data-ttu-id="e4fcd-117">Gibt **true** zurück, wenn erfolgreich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="e4fcd-117">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4fcd-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4fcd-118">Remarks</span></span>

<span data-ttu-id="e4fcd-119">Das Header Steuerelement muss den Stil **HDF \_ SplitButton** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e4fcd-119">The header control must have style **HDF\_SPLITBUTTON**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4fcd-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4fcd-120">Requirements</span></span>



| <span data-ttu-id="e4fcd-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4fcd-121">Requirement</span></span> | <span data-ttu-id="e4fcd-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e4fcd-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4fcd-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4fcd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e4fcd-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4fcd-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4fcd-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4fcd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e4fcd-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e4fcd-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4fcd-127">Header</span><span class="sxs-lookup"><span data-stu-id="e4fcd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4fcd-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4fcd-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4fcd-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4fcd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4fcd-130">Informationen über Header Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="e4fcd-130">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

