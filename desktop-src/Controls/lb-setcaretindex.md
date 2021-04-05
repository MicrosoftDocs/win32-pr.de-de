---
title: LB_SETCARETINDEX Meldung (Winuser. h)
description: Legt das Fokus Rechteck auf das Element am angegebenen Index in einem Mehrfachauswahl-Listenfeld fest. Wenn das Element nicht sichtbar ist, wird es in die Ansicht gescrollt.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setcaretindex.htm
keywords:
- Windows-Steuerelemente für LB_SETCARETINDEX Meldung
topic_type:
- apiref
api_name:
- LB_SETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857e5c2637e5bcc90b2c60bfd8295a91ff297fb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859164"
---
# <a name="lb_setcaretindex-message"></a><span data-ttu-id="3f344-105">LB- \_ setcaretindex-Meldung</span><span class="sxs-lookup"><span data-stu-id="3f344-105">LB\_SETCARETINDEX message</span></span>

<span data-ttu-id="3f344-106">Legt das Fokus Rechteck auf das Element am angegebenen Index in einem Mehrfachauswahl-Listenfeld fest.</span><span class="sxs-lookup"><span data-stu-id="3f344-106">Sets the focus rectangle to the item at the specified index in a multiple-selection list box.</span></span> <span data-ttu-id="3f344-107">Wenn das Element nicht sichtbar ist, wird es in die Ansicht gescrollt.</span><span class="sxs-lookup"><span data-stu-id="3f344-107">If the item is not visible, it is scrolled into view.</span></span>

## <a name="parameters"></a><span data-ttu-id="3f344-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f344-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f344-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3f344-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f344-110">Gibt den NULL basierten Index des Listenfeld Elements an, das das Fokus Rechteck erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="3f344-110">Specifies the zero-based index of the list box item that is to receive the focus rectangle.</span></span>

<span data-ttu-id="3f344-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="3f344-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="3f344-112">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="3f344-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="3f344-113">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="3f344-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="3f344-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3f344-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f344-115">Wenn dieser Wert **false** ist, wird das Element gescrollt, bis es vollständig sichtbar ist. Wenn der Wert **true** ist, wird das Element so lange gescrollt, bis es mindestens teilweise sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="3f344-115">If this value is **FALSE**, the item is scrolled until it is fully visible; if it is **TRUE**, the item is scrolled until it is at least partially visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f344-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f344-116">Return value</span></span>

<span data-ttu-id="3f344-117">Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err (-1).</span><span class="sxs-lookup"><span data-stu-id="3f344-117">If an error occurs, the return value is LB\_ERR (-1).</span></span> <span data-ttu-id="3f344-118">Andernfalls wird der Lastenausgleich OK \_ (0) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3f344-118">Otherwise, LB\_OKAY (0) is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f344-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f344-119">Remarks</span></span>

<span data-ttu-id="3f344-120">Wenn diese Meldung an ein Listenfeld mit einer Auswahl gesendet wird, das kein ausgewähltes Element enthält, wird der Einfügeindex auf das vom *wParam* -Parameter angegebene Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3f344-120">If this message is sent to a single-selection list box that does not contain a selected item, the caret index is set to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="3f344-121">Wenn das Listenfeld für die Einzel Auswahl ein ausgewähltes Element enthält, gibt das Listenfeld lb \_ Err zurück.</span><span class="sxs-lookup"><span data-stu-id="3f344-121">If the single-selection list box does contain a selected item, the list box returns LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f344-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f344-122">Requirements</span></span>



| <span data-ttu-id="3f344-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f344-123">Requirement</span></span> | <span data-ttu-id="3f344-124">Wert</span><span class="sxs-lookup"><span data-stu-id="3f344-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f344-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f344-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3f344-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f344-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3f344-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f344-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3f344-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f344-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3f344-129">Header</span><span class="sxs-lookup"><span data-stu-id="3f344-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f344-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="3f344-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f344-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f344-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f344-132">**LB \_ getcaretindex**</span><span class="sxs-lookup"><span data-stu-id="3f344-132">**LB\_GETCARETINDEX**</span></span>](lb-getcaretindex.md)
</dt> </dl>

 

 





