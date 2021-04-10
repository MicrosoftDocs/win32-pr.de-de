---
title: LB_GETCURSEL Meldung (Winuser. h)
description: Ruft den Index des derzeit ausgewählten Elements (sofern vorhanden) in einem Listenfeld mit einer einzelnen Auswahl ab.
ms.assetid: 39ab7f77-6c8e-45a4-aad4-47eba0a11a11
keywords:
- Windows-Steuerelemente für LB_GETCURSEL Meldung
topic_type:
- apiref
api_name:
- LB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6209f1f5b67e059f9a2b8a224e6f96ec671e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040953"
---
# <a name="lb_getcursel-message"></a><span data-ttu-id="22c67-104">LB- \_ getcurrsel-Nachricht</span><span class="sxs-lookup"><span data-stu-id="22c67-104">LB\_GETCURSEL message</span></span>

<span data-ttu-id="22c67-105">Ruft den Index des derzeit ausgewählten Elements (sofern vorhanden) in einem Listenfeld mit einer einzelnen Auswahl ab.</span><span class="sxs-lookup"><span data-stu-id="22c67-105">Gets the index of the currently selected item, if any, in a single-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="22c67-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22c67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22c67-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22c67-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22c67-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="22c67-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="22c67-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22c67-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22c67-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="22c67-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22c67-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22c67-111">Return value</span></span>

<span data-ttu-id="22c67-112">Der Rückgabewert in einem Listenfeld mit einer einzelnen Auswahl ist der null basierte Index des aktuell ausgewählten Elements.</span><span class="sxs-lookup"><span data-stu-id="22c67-112">In a single-selection list box, the return value is the zero-based index of the currently selected item.</span></span> <span data-ttu-id="22c67-113">Wenn keine Auswahl vorhanden ist, lautet der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="22c67-113">If there is no selection, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="22c67-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22c67-114">Remarks</span></span>

<span data-ttu-id="22c67-115">Um die Indizes der ausgewählten Elemente in einem Listenfeld mit Mehrfachauswahl abzurufen, verwenden Sie die [**\_ getselitems**](lb-getselitems.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="22c67-115">To retrieve the indexes of the selected items in a multiple-selection list box, use the [**LB\_GETSELITEMS**](lb-getselitems.md) message.</span></span> <span data-ttu-id="22c67-116">Um zu ermitteln, ob das Element, das das Fokus Rechteck enthält, in einem Mehrfachauswahl-Listenfeld ausgewählt ist, verwenden Sie die [**\_ GetSEL**](lb-getsel.md) -Nachricht "lb".</span><span class="sxs-lookup"><span data-stu-id="22c67-116">To determine whether the item that has the focus rectangle in a multiple selection list box is selected, use the [**LB\_GETSEL**](lb-getsel.md) message.</span></span>

<span data-ttu-id="22c67-117">Beim Senden an ein Listenfeld mit Mehrfachauswahl gibt **lb \_ getcurrsel** den Index des Elements zurück, das über das Fokus Rechteck verfügt.</span><span class="sxs-lookup"><span data-stu-id="22c67-117">If sent to a multiple-selection list box, **LB\_GETCURSEL** returns the index of the item that has the focus rectangle.</span></span> <span data-ttu-id="22c67-118">Wenn keine Elemente ausgewählt sind, wird NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="22c67-118">If no items are selected, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="22c67-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22c67-119">Requirements</span></span>



| <span data-ttu-id="22c67-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22c67-120">Requirement</span></span> | <span data-ttu-id="22c67-121">Wert</span><span class="sxs-lookup"><span data-stu-id="22c67-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22c67-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22c67-122">Minimum supported client</span></span><br/> | <span data-ttu-id="22c67-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22c67-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="22c67-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22c67-124">Minimum supported server</span></span><br/> | <span data-ttu-id="22c67-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22c67-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="22c67-126">Header</span><span class="sxs-lookup"><span data-stu-id="22c67-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="22c67-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="22c67-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22c67-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22c67-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="22c67-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="22c67-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="22c67-130">**LB \_ getcaretindex**</span><span class="sxs-lookup"><span data-stu-id="22c67-130">**LB\_GETCARETINDEX**</span></span>](lb-getcaretindex.md)
</dt> <dt>

[<span data-ttu-id="22c67-131">**LB- \_ GetSEL**</span><span class="sxs-lookup"><span data-stu-id="22c67-131">**LB\_GETSEL**</span></span>](lb-getsel.md)
</dt> <dt>

[<span data-ttu-id="22c67-132">**LB- \_ getselitems**</span><span class="sxs-lookup"><span data-stu-id="22c67-132">**LB\_GETSELITEMS**</span></span>](lb-getselitems.md)
</dt> <dt>

[<span data-ttu-id="22c67-133">**LB- \_ setcurrsel**</span><span class="sxs-lookup"><span data-stu-id="22c67-133">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> </dl>

 

 





