---
title: EM_GETMARGINS Meldung (Winuser. h)
description: Ruft die Breite des linken und rechten Rands für ein Bearbeitungs Steuerelement ab.
ms.assetid: 2482354b-aae0-4abd-8287-65c423f30abb
keywords:
- Windows-Steuerelemente für EM_GETMARGINS Meldung
topic_type:
- apiref
api_name:
- EM_GETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 239ad7e7888f5bceef60bf2719c3b67798b56220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740297"
---
# <a name="em_getmargins-message"></a><span data-ttu-id="cb746-104">EM \_ getMargin-Nachricht</span><span class="sxs-lookup"><span data-stu-id="cb746-104">EM\_GETMARGINS message</span></span>

<span data-ttu-id="cb746-105">Ruft die Breite des linken und rechten Rands für ein Bearbeitungs Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="cb746-105">Gets the widths of the left and right margins for an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb746-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb746-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb746-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb746-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb746-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="cb746-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cb746-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb746-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb746-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="cb746-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb746-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb746-111">Return value</span></span>

<span data-ttu-id="cb746-112">Gibt die Breite des linken Randes des loworts und die Breite des rechten Rands im HIWORD zurück.</span><span class="sxs-lookup"><span data-stu-id="cb746-112">Returns the width of the left margin in the LOWORD, and the width of the right margin in the HIWORD.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb746-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb746-113">Remarks</span></span>

<span data-ttu-id="cb746-114">Umfassende **Bearbeitung:** Die **EM \_ getMargin** -Meldung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb746-114">**Rich Edit:** The **EM\_GETMARGINS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb746-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb746-115">Requirements</span></span>



| <span data-ttu-id="cb746-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb746-116">Requirement</span></span> | <span data-ttu-id="cb746-117">Wert</span><span class="sxs-lookup"><span data-stu-id="cb746-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb746-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb746-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cb746-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb746-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cb746-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb746-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cb746-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb746-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cb746-122">Header</span><span class="sxs-lookup"><span data-stu-id="cb746-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb746-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="cb746-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb746-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb746-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb746-125">**EM- \_ setMargin**</span><span class="sxs-lookup"><span data-stu-id="cb746-125">**EM\_SETMARGINS**</span></span>](em-setmargins.md)
</dt> </dl>

 

 





