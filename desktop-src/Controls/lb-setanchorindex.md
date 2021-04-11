---
title: LB_SETANCHORINDEX Meldung (Winuser. h)
description: Legt das Anker Element \ 8212 fest, d. h. das Element, aus dem eine Mehrfachauswahl beginnt. Eine Mehrfachauswahl umfasst alle Elemente vom Anker Element bis zum Caretzeichen.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setanchorindex.htm
keywords:
- Windows-Steuerelemente für LB_SETANCHORINDEX Meldung
topic_type:
- apiref
api_name:
- LB_SETANCHORINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3ac2aa8798d0e13d8191f630fef7f54f510ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105537"
---
# <a name="lb_setanchorindex-message"></a><span data-ttu-id="fa0c6-105">LB- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="fa0c6-105">LB\_SETANCHORINDEX message</span></span>

<span data-ttu-id="fa0c6-106">Legt das Anker Element fest, das das Element ist, aus dem eine Mehrfachauswahl beginnt.</span><span class="sxs-lookup"><span data-stu-id="fa0c6-106">Sets the anchor item that is, the item from which a multiple selection starts.</span></span> <span data-ttu-id="fa0c6-107">Eine Mehrfachauswahl umfasst alle Elemente vom Anker Element bis zum Caretzeichen.</span><span class="sxs-lookup"><span data-stu-id="fa0c6-107">A multiple selection spans all items from the anchor item to the caret item.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa0c6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa0c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa0c6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa0c6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa0c6-110">Gibt den Index des neuen Anker Elements an.</span><span class="sxs-lookup"><span data-stu-id="fa0c6-110">Specifies the index of the new anchor item.</span></span>

<span data-ttu-id="fa0c6-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="fa0c6-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="fa0c6-112">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="fa0c6-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="fa0c6-113">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="fa0c6-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="fa0c6-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa0c6-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa0c6-115">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fa0c6-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa0c6-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa0c6-116">Return value</span></span>

<span data-ttu-id="fa0c6-117">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fa0c6-117">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="fa0c6-118">Wenn die Meldung fehlschlägt, ist der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="fa0c6-118">If the message fails, the return value is LB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa0c6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa0c6-119">Requirements</span></span>



| <span data-ttu-id="fa0c6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa0c6-120">Requirement</span></span> | <span data-ttu-id="fa0c6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="fa0c6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa0c6-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa0c6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fa0c6-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa0c6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fa0c6-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa0c6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fa0c6-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fa0c6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fa0c6-126">Header</span><span class="sxs-lookup"><span data-stu-id="fa0c6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa0c6-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="fa0c6-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa0c6-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa0c6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa0c6-129">**LB- \_ getanchorindex**</span><span class="sxs-lookup"><span data-stu-id="fa0c6-129">**LB\_GETANCHORINDEX**</span></span>](lb-getanchorindex.md)
</dt> </dl>

 

 





