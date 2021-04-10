---
title: HDM_GETITEMDROPDOWNRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck der Trenn Schaltfläche für ein Header Element mit dem Format "HDF \_ SplitButton" ab. Senden Sie diese Nachricht explizit oder mithilfe des Headers \_ getitemdropdownrect-Makros.
ms.assetid: d7188dfb-4ffa-4641-b210-2c2ec480ca13
keywords:
- Windows-Steuerelemente für HDM_GETITEMDROPDOWNRECT Meldung
topic_type:
- apiref
api_name:
- HDM_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86f3df8de5224e79ca4e15ea18409e13972ca5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040640"
---
# <a name="hdm_getitemdropdownrect-message"></a><span data-ttu-id="835d4-105">HDM \_ getitemdropdownrect-Meldung</span><span class="sxs-lookup"><span data-stu-id="835d4-105">HDM\_GETITEMDROPDOWNRECT message</span></span>

<span data-ttu-id="835d4-106">Ruft das umgebende Rechteck der Trenn Schaltfläche für ein Header Element mit dem Format " **HDF \_ SplitButton**" ab.</span><span class="sxs-lookup"><span data-stu-id="835d4-106">Gets the bounding rectangle of the split button for a header item with style **HDF\_SPLITBUTTON**.</span></span> <span data-ttu-id="835d4-107">Senden Sie diese Nachricht explizit oder mithilfe des [**Headers \_ getitemdropdownrect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) -Makros.</span><span class="sxs-lookup"><span data-stu-id="835d4-107">Send this message explicitly or by using the [**Header\_GetItemDropDownRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="835d4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="835d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="835d4-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="835d4-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="835d4-110">Der null basierte Index des Header Steuerelement Elements, für das das umgebende Rechteck abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="835d4-110">The zero-based index of the header control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="835d4-111">*LPARAM* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="835d4-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="835d4-112">Ein Zeiger auf eine [**Rect**](/windows/win32/api/windef/ns-windef-rect) -Struktur, die die umschließenden Rechteck Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="835d4-112">A pointer to a [**RECT**](/windows/win32/api/windef/ns-windef-rect) structure that receives the bounding rectangle information.</span></span> <span data-ttu-id="835d4-113">Der Absender der Nachricht ist für die Zuordnung dieser Struktur verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="835d4-113">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="835d4-114">Die in der Rect-Struktur zurückgegebenen Koordinaten werden relativ zum übergeordneten Header Steuerelement ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="835d4-114">The coordinates returned in the RECT structure are expressed relative to the header control parent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="835d4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="835d4-115">Return value</span></span>

<span data-ttu-id="835d4-116">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="835d4-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="835d4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="835d4-117">Remarks</span></span>

<span data-ttu-id="835d4-118">Das Header Element muss den Stil **HDF \_ SplitButton** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="835d4-118">The header item must have style **HDF\_SPLITBUTTON**.</span></span>

## <a name="requirements"></a><span data-ttu-id="835d4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="835d4-119">Requirements</span></span>



| <span data-ttu-id="835d4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="835d4-120">Requirement</span></span> | <span data-ttu-id="835d4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="835d4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="835d4-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="835d4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="835d4-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="835d4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="835d4-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="835d4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="835d4-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="835d4-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="835d4-126">Header</span><span class="sxs-lookup"><span data-stu-id="835d4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="835d4-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="835d4-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="835d4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="835d4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="835d4-129">Informationen über Header Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="835d4-129">About Header Controls</span></span>](header-controls.md)
</dt> </dl>

 

 





