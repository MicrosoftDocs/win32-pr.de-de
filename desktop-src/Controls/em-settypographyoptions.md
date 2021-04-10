---
title: EM_SETTYPOGRAPHYOPTIONS Meldung (RichEdit. h)
description: Legt den aktuellen Zustand der Typografieoptionen eines Rich-Edit-Steuer Elements fest.
ms.assetid: 000e72a6-3f8c-4735-8190-3ac06a2206ac
keywords:
- Windows-Steuerelemente für EM_SETTYPOGRAPHYOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_SETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0528e19aacec394c5af6250536fdc4f693e60ece
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956633"
---
# <a name="em_settypographyoptions-message"></a><span data-ttu-id="e33c7-104">EM \_ settypographyoptions-Meldung</span><span class="sxs-lookup"><span data-stu-id="e33c7-104">EM\_SETTYPOGRAPHYOPTIONS message</span></span>

<span data-ttu-id="e33c7-105">Legt den aktuellen Zustand der Typografieoptionen eines Rich-Edit-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="e33c7-105">Sets the current state of the typography options of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e33c7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e33c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e33c7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e33c7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e33c7-108">Gibt einen oder beide der folgenden Werte an.</span><span class="sxs-lookup"><span data-stu-id="e33c7-108">Specifies one or both of the following values.</span></span>



| <span data-ttu-id="e33c7-109">Wert</span><span class="sxs-lookup"><span data-stu-id="e33c7-109">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="e33c7-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e33c7-110">Meaning</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="TO_ADVANCEDTYPOGRAPHY_"></span><span id="to_advancedtypography_"></span><dl> <span data-ttu-id="e33c7-111"><dt>**An \_ Advancedtypografie**</dt></span><span class="sxs-lookup"><span data-stu-id="e33c7-111"><dt>**TO\_ADVANCEDTYPOGRAPHY** </dt></span></span> </dl> | <span data-ttu-id="e33c7-112">Erweiterte Zeilenumbruch und Zeilen Formatierung sind aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e33c7-112">Advanced line breaking and line formatting is turned on.</span></span> <br/>                    |
| <span id="TO_SIMPLELINEBREAK"></span><span id="to_simplelinebreak"></span><dl> <span data-ttu-id="e33c7-113"><dt>**an \_ simplelinebreak**</dt></span><span class="sxs-lookup"><span data-stu-id="e33c7-113"><dt>**TO\_SIMPLELINEBREAK**</dt></span></span> </dl>             | <span data-ttu-id="e33c7-114">Schnelleres Zeilenumbruch bei einfachem Text ( **erfordert \_ advancedtypografie**).</span><span class="sxs-lookup"><span data-stu-id="e33c7-114">Faster line breaking for simple text (requires **TO\_ADVANCEDTYPOGRAPHY**).</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="e33c7-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e33c7-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e33c7-116">Eine Maske, die aus einem oder mehreren der Flags in *wParam* besteht.</span><span class="sxs-lookup"><span data-stu-id="e33c7-116">A mask consisting of one or more of the flags in *wParam*.</span></span> <span data-ttu-id="e33c7-117">Nur die Flags, die in dieser Maske festgelegt sind, werden festgelegt oder gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e33c7-117">Only the flags that are set in this mask will be set or cleared.</span></span> <span data-ttu-id="e33c7-118">Dadurch kann ein einzelnes Flag festgelegt oder gelöscht werden, ohne die aktuellen flagzustände zu lesen.</span><span class="sxs-lookup"><span data-stu-id="e33c7-118">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e33c7-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e33c7-119">Return value</span></span>

<span data-ttu-id="e33c7-120">Gibt **true** zurück, wenn *wParam* gültig ist, andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="e33c7-120">Returns **TRUE** if *wParam* is valid, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e33c7-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e33c7-121">Remarks</span></span>

<span data-ttu-id="e33c7-122">Der erweiterte Zeilenumbruch wird automatisch durch das Rich Edit-Steuerelement aktiviert, z. b. für die Behandlung komplexer Skripts wie Arabisch und Hebräisch und für Mathematik.</span><span class="sxs-lookup"><span data-stu-id="e33c7-122">Advanced line breaking is turned on automatically by the rich edit control when needed, such as for handling complex scripts like Arabic and Hebrew, and for mathematics.</span></span> <span data-ttu-id="e33c7-123">Es ist auch für begründete Absätze, Bindestriche und andere typografische Features erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e33c7-123">It s also needed for justified paragraphs, hyphenation, and other typographic features.</span></span>

## <a name="requirements"></a><span data-ttu-id="e33c7-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e33c7-124">Requirements</span></span>



| <span data-ttu-id="e33c7-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e33c7-125">Requirement</span></span> | <span data-ttu-id="e33c7-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e33c7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e33c7-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e33c7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e33c7-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e33c7-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e33c7-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e33c7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e33c7-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e33c7-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e33c7-131">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e33c7-131">Redistributable</span></span><br/>          | <span data-ttu-id="e33c7-132">Rich Edit 3,0</span><span class="sxs-lookup"><span data-stu-id="e33c7-132">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="e33c7-133">Header</span><span class="sxs-lookup"><span data-stu-id="e33c7-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e33c7-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e33c7-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e33c7-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e33c7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e33c7-136">**EM \_ gettypographyoptions**</span><span class="sxs-lookup"><span data-stu-id="e33c7-136">**EM\_GETTYPOGRAPHYOPTIONS**</span></span>](em-gettypographyoptions.md)
</dt> </dl>

 

 





