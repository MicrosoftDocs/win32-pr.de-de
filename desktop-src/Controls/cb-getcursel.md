---
title: CB_GETCURSEL Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB \_ getcurrsel-Nachricht, um den Index des derzeit ausgewählten Elements (sofern vorhanden) im Listenfeld eines Kombinations Felds abzurufen.
ms.assetid: 47bf87f6-637f-48e9-849e-b2acbe5a6a7b
keywords:
- Windows-Steuerelemente für CB_GETCURSEL Meldung
topic_type:
- apiref
api_name:
- CB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fbc9aa1785738fb061696fbad64598747168269
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859357"
---
# <a name="cb_getcursel-message"></a><span data-ttu-id="5815d-104">CB \_ getcurrsel-Meldung</span><span class="sxs-lookup"><span data-stu-id="5815d-104">CB\_GETCURSEL message</span></span>

<span data-ttu-id="5815d-105">Eine Anwendung sendet eine **CB \_ getcurrsel** -Nachricht, um den Index des derzeit ausgewählten Elements (sofern vorhanden) im Listenfeld eines Kombinations Felds abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5815d-105">An application sends a **CB\_GETCURSEL** message to retrieve the index of the currently selected item, if any, in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="5815d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5815d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5815d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5815d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5815d-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="5815d-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5815d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5815d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5815d-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="5815d-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5815d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5815d-111">Return value</span></span>

<span data-ttu-id="5815d-112">Der Rückgabewert ist der null basierte Index des aktuell ausgewählten Elements.</span><span class="sxs-lookup"><span data-stu-id="5815d-112">The return value is the zero-based index of the currently selected item.</span></span> <span data-ttu-id="5815d-113">Wenn kein Element ausgewählt ist, ist es CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="5815d-113">If no item is selected, it is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="5815d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5815d-114">Requirements</span></span>



| <span data-ttu-id="5815d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5815d-115">Requirement</span></span> | <span data-ttu-id="5815d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5815d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5815d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5815d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5815d-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5815d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5815d-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5815d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5815d-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5815d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5815d-121">Header</span><span class="sxs-lookup"><span data-stu-id="5815d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5815d-122"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="5815d-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5815d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5815d-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="5815d-124">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="5815d-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5815d-125">**CB- \_ SelectString**</span><span class="sxs-lookup"><span data-stu-id="5815d-125">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="5815d-126">**CB \_ setcurrsel**</span><span class="sxs-lookup"><span data-stu-id="5815d-126">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> </dl>

 

 





