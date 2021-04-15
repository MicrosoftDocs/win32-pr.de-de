---
title: CB_GETEXTENDEDUI Meldung (Winuser. h)
description: Bestimmt, ob ein Kombinations Feld über die Standardbenutzer Oberfläche oder die erweiterte Benutzeroberfläche verfügt.
ms.assetid: 4f5580e0-68b1-4584-bf79-561fb8222fe0
keywords:
- Windows-Steuerelemente für CB_GETEXTENDEDUI Meldung
topic_type:
- apiref
api_name:
- CB_GETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d90550bf341fc8586174c7ec57eb77fad08c59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476656"
---
# <a name="cb_getextendedui-message"></a><span data-ttu-id="f4472-104">CB \_ getextendedui-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f4472-104">CB\_GETEXTENDEDUI message</span></span>

<span data-ttu-id="f4472-105">Bestimmt, ob ein Kombinations Feld über die Standardbenutzer Oberfläche oder die erweiterte Benutzeroberfläche verfügt.</span><span class="sxs-lookup"><span data-stu-id="f4472-105">Determines whether a combo box has the default user interface or the extended user interface.</span></span>

## <a name="parameters"></a><span data-ttu-id="f4472-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4472-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4472-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4472-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4472-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="f4472-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f4472-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4472-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4472-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="f4472-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4472-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4472-111">Return value</span></span>

<span data-ttu-id="f4472-112">Wenn das Kombinations Feld über die erweiterte Benutzeroberfläche verfügt, ist der Rückgabewert " **true**". Andernfalls ist Sie **false**.</span><span class="sxs-lookup"><span data-stu-id="f4472-112">If the combo box has the extended user interface, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4472-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4472-113">Remarks</span></span>

<span data-ttu-id="f4472-114">Standardmäßig wird die Liste mit dem F4-Schlüssel geöffnet oder geschlossen, und der nach-unten-Pfeil ändert die aktuelle Auswahl.</span><span class="sxs-lookup"><span data-stu-id="f4472-114">By default, the F4 key opens or closes the list and the DOWN ARROW changes the current selection.</span></span> <span data-ttu-id="f4472-115">In einem Kombinations Feld mit der erweiterten Benutzeroberfläche ist die F4-Taste deaktiviert. durch Drücken der nach-unten-Taste wird die Dropdown Liste geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f4472-115">In a combo box with the extended user interface, the F4 key is disabled and pressing the DOWN ARROW key opens the drop-down list.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4472-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4472-116">Requirements</span></span>



| <span data-ttu-id="f4472-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4472-117">Requirement</span></span> | <span data-ttu-id="f4472-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f4472-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4472-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4472-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f4472-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4472-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f4472-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4472-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f4472-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4472-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f4472-123">Header</span><span class="sxs-lookup"><span data-stu-id="f4472-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4472-124"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="f4472-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4472-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4472-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="f4472-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f4472-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f4472-127">**CB- \_ textendedui**</span><span class="sxs-lookup"><span data-stu-id="f4472-127">**CB\_SETEXTENDEDUI**</span></span>](cb-setextendedui.md)
</dt> <dt>

<span data-ttu-id="f4472-128">**Licher**</span><span class="sxs-lookup"><span data-stu-id="f4472-128">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f4472-129">Kombinations Feld-Features</span><span class="sxs-lookup"><span data-stu-id="f4472-129">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





