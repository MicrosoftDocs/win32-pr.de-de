---
title: EM_GETEVENTMASK Meldung (RichEdit. h)
description: Ruft die Ereignis Maske für ein Rich-Edit-Steuerelement ab. Die Ereignis Maske gibt an, welche Benachrichtigungs Codes das Steuerelement an das übergeordnete Fenster sendet.
ms.assetid: cdf99f2a-e747-4b0e-9235-2719477c3ce2
keywords:
- Windows-Steuerelemente für EM_GETEVENTMASK Meldung
topic_type:
- apiref
api_name:
- EM_GETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f4d231bbb9d5592ff2f90da6a5096783b38c292
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956829"
---
# <a name="em_geteventmask-message"></a><span data-ttu-id="c57e2-105">EM \_ GetEventMask-Meldung</span><span class="sxs-lookup"><span data-stu-id="c57e2-105">EM\_GETEVENTMASK message</span></span>

<span data-ttu-id="c57e2-106">Ruft die Ereignis Maske für ein Rich-Edit-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="c57e2-106">Retrieves the event mask for a rich edit control.</span></span> <span data-ttu-id="c57e2-107">Die Ereignis Maske gibt an, welche Benachrichtigungs Codes das Steuerelement an das übergeordnete Fenster sendet.</span><span class="sxs-lookup"><span data-stu-id="c57e2-107">The event mask specifies which notification codes the control sends to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="c57e2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c57e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c57e2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c57e2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c57e2-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="c57e2-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c57e2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c57e2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c57e2-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="c57e2-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c57e2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c57e2-113">Return value</span></span>

<span data-ttu-id="c57e2-114">Diese Meldung gibt die Ereignis Maske für das Rich Edit-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="c57e2-114">This message returns the event mask for the rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="c57e2-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c57e2-115">Requirements</span></span>



| <span data-ttu-id="c57e2-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c57e2-116">Requirement</span></span> | <span data-ttu-id="c57e2-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c57e2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c57e2-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c57e2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c57e2-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c57e2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c57e2-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c57e2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c57e2-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c57e2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c57e2-122">Header</span><span class="sxs-lookup"><span data-stu-id="c57e2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c57e2-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c57e2-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c57e2-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c57e2-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="c57e2-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c57e2-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c57e2-126">**EM-- \_ einventmask**</span><span class="sxs-lookup"><span data-stu-id="c57e2-126">**EM\_SETEVENTMASK**</span></span>](em-seteventmask.md)
</dt> <dt>

[<span data-ttu-id="c57e2-127">**Rich-Flags für Bearbeitungs Steuerelemente-Ereignis Maske**</span><span class="sxs-lookup"><span data-stu-id="c57e2-127">**Rich Edit Control Event Mask Flags**</span></span>](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





