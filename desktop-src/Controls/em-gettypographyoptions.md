---
title: EM_GETTYPOGRAPHYOPTIONS Meldung (RichEdit. h)
description: Gibt den aktuellen Zustand der Typografieoptionen eines Rich-Edit-Steuer Elements zurück.
ms.assetid: 6ff5980e-3201-4b0f-9a03-3de78730ce33
keywords:
- Windows-Steuerelemente für EM_GETTYPOGRAPHYOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_GETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d692639ba6c8cea758abe694faed3a46e3f65be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105105"
---
# <a name="em_gettypographyoptions-message"></a><span data-ttu-id="85e5c-104">EM \_ gettypographyoptions-Meldung</span><span class="sxs-lookup"><span data-stu-id="85e5c-104">EM\_GETTYPOGRAPHYOPTIONS message</span></span>

<span data-ttu-id="85e5c-105">Gibt den aktuellen Zustand der Typografieoptionen eines Rich-Edit-Steuer Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="85e5c-105">Returns the current state of the typography options of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="85e5c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="85e5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85e5c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="85e5c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85e5c-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="85e5c-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="85e5c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="85e5c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85e5c-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="85e5c-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85e5c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85e5c-111">Return value</span></span>

<span data-ttu-id="85e5c-112">Gibt die aktuellen Typografieoptionen zurück.</span><span class="sxs-lookup"><span data-stu-id="85e5c-112">Returns the current typography options.</span></span> <span data-ttu-id="85e5c-113">Eine Liste der Optionen finden Sie unter [**EM \_ settypographyoptions**](em-settypographyoptions.md).</span><span class="sxs-lookup"><span data-stu-id="85e5c-113">For a list of options, see [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="85e5c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85e5c-114">Remarks</span></span>

<span data-ttu-id="85e5c-115">Sie können den erweiterten Zeilenumbruch aktivieren, indem Sie die Nachricht " [**EM \_ settypographyoptions**](em-settypographyoptions.md) " senden.</span><span class="sxs-lookup"><span data-stu-id="85e5c-115">You can turn on advanced line breaking by sending the [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md) message.</span></span> <span data-ttu-id="85e5c-116">Erweiterte und normale Zeilenumbruch können auch automatisch durch das Rich Edit-Steuerelement aktiviert werden, wenn es für bestimmte Sprachen benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="85e5c-116">Advanced and normal line breaking may also be turned on automatically by the rich edit control if it is needed for certain languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="85e5c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85e5c-117">Requirements</span></span>



| <span data-ttu-id="85e5c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85e5c-118">Requirement</span></span> | <span data-ttu-id="85e5c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="85e5c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85e5c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85e5c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="85e5c-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85e5c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="85e5c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85e5c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="85e5c-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85e5c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="85e5c-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="85e5c-124">Redistributable</span></span><br/>          | <span data-ttu-id="85e5c-125">Rich Edit 3,0</span><span class="sxs-lookup"><span data-stu-id="85e5c-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="85e5c-126">Header</span><span class="sxs-lookup"><span data-stu-id="85e5c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="85e5c-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="85e5c-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85e5c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85e5c-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="85e5c-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="85e5c-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="85e5c-130">**EM \_ settypographyoptions**</span><span class="sxs-lookup"><span data-stu-id="85e5c-130">**EM\_SETTYPOGRAPHYOPTIONS**</span></span>](em-settypographyoptions.md)
</dt> <dt>

<span data-ttu-id="85e5c-131">**Licher**</span><span class="sxs-lookup"><span data-stu-id="85e5c-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="85e5c-132">Informationen zu Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="85e5c-132">About Rich Edit Controls</span></span>](about-rich-edit-controls.md)
</dt> </dl>

 

 





