---
title: LB_GETTOPINDEX Meldung (Winuser. h)
description: Ruft den Index des ersten sichtbaren Elements in einem Listenfeld ab.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_gettopindex.htm
keywords:
- Windows-Steuerelemente für LB_GETTOPINDEX Meldung
topic_type:
- apiref
api_name:
- LB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdeca8e3f40ab3105bb9703db9355d09a214f5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956505"
---
# <a name="lb_gettopindex-message"></a><span data-ttu-id="7afc4-104">LB- \_ gettopindex-Nachricht</span><span class="sxs-lookup"><span data-stu-id="7afc4-104">LB\_GETTOPINDEX message</span></span>

<span data-ttu-id="7afc4-105">Ruft den Index des ersten sichtbaren Elements in einem Listenfeld ab.</span><span class="sxs-lookup"><span data-stu-id="7afc4-105">Gets the index of the first visible item in a list box.</span></span> <span data-ttu-id="7afc4-106">Anfänglich befindet sich das Element mit dem Index 0 am oberen Rand des Listen Felds, aber wenn für den Listenfeld Inhalt ein Bildlauf ausgeführt wurde, befindet sich möglicherweise ein anderes Element im oberen Bereich.</span><span class="sxs-lookup"><span data-stu-id="7afc4-106">Initially the item with index 0 is at the top of the list box, but if the list box contents have been scrolled another item may be at the top.</span></span> <span data-ttu-id="7afc4-107">Das erste sichtbare Element in einem Listenfeld mit mehreren Spalten ist das linke obere Element.</span><span class="sxs-lookup"><span data-stu-id="7afc4-107">The first visible item in a multiple-column list box is the top-left item.</span></span>

## <a name="parameters"></a><span data-ttu-id="7afc4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7afc4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7afc4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7afc4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7afc4-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="7afc4-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7afc4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7afc4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7afc4-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="7afc4-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7afc4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7afc4-113">Return value</span></span>

<span data-ttu-id="7afc4-114">Der Rückgabewert ist der Index des ersten sichtbaren Elements im Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="7afc4-114">The return value is the index of the first visible item in the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="7afc4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7afc4-115">Requirements</span></span>



| <span data-ttu-id="7afc4-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7afc4-116">Requirement</span></span> | <span data-ttu-id="7afc4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7afc4-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7afc4-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7afc4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7afc4-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7afc4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7afc4-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7afc4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7afc4-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7afc4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7afc4-122">Header</span><span class="sxs-lookup"><span data-stu-id="7afc4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7afc4-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="7afc4-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7afc4-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7afc4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7afc4-125">**LB- \_ settopindex**</span><span class="sxs-lookup"><span data-stu-id="7afc4-125">**LB\_SETTOPINDEX**</span></span>](lb-settopindex.md)
</dt> </dl>

 

 





