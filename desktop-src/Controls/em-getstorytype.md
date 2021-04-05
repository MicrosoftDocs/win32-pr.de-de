---
title: EM_GETSTORYTYPE Meldung (RichEdit. h)
description: Ruft den Story-Typ ab.
ms.assetid: 06D87AA1-5AA3-4235-AC1D-045CE9975384
keywords:
- Windows-Steuerelemente für EM_GETSTORYTYPE Meldung
topic_type:
- apiref
api_name:
- EM_GETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fed85183f292bd1c69e3bbebdadb4b38f9f3bdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858850"
---
# <a name="em_getstorytype-message"></a><span data-ttu-id="905e2-104">EM \_ getstorytype-Meldung</span><span class="sxs-lookup"><span data-stu-id="905e2-104">EM\_GETSTORYTYPE message</span></span>

<span data-ttu-id="905e2-105">Ruft den Story-Typ ab.</span><span class="sxs-lookup"><span data-stu-id="905e2-105">Gets the story type.</span></span>


```C++
#define EM_GETSTORYTYPE       (WM_USER + 290)
```



## <a name="parameters"></a><span data-ttu-id="905e2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="905e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="905e2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="905e2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="905e2-108">Der Story-Index.</span><span class="sxs-lookup"><span data-stu-id="905e2-108">The story index.</span></span>

</dd> <dt>

<span data-ttu-id="905e2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="905e2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="905e2-110">Bleiben muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="905e2-110">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="905e2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="905e2-111">Return value</span></span>

<span data-ttu-id="905e2-112">Gibt den Story-Typ zurück, bei dem es sich um einen vom Client definierten benutzerdefinierten Wert oder einen der folgenden Werte handeln kann:</span><span class="sxs-lookup"><span data-stu-id="905e2-112">Returns the story type, which can be a client-defined custom value, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="905e2-113">**[**tomcommentsstory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="905e2-113">**[**tomCommentsStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="905e2-114">**[**tomendnotesstory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="905e2-114">**[**tomEndnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="905e2-115">**[**tomevenpgesfooterstory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="905e2-115">**[**tomEvenPagesFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="905e2-116">**[**tomevenpagesheaderstory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="905e2-116">**[**tomEvenPagesHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="905e2-117">**[**tomfindstory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="905e2-117">**[**tomFindStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="905e2-118">**[**tomfirstpagefooterstory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="905e2-118">**[**tomFirstPageFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="905e2-119">**[**tomfirstpageheaderstory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="905e2-119">**[**tomFirstPageHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="905e2-120">**[**tomfootnotesstory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="905e2-120">**[**tomFootnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="905e2-121">**[**tommaintextstory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="905e2-121">**[**tomMainTextStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="905e2-122">**[**tomprimaryfooterstory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="905e2-122">**[**tomPrimaryFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="905e2-123">**[**tomprimaryheaderstory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="905e2-123">**[**tomPrimaryHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="905e2-124">**[**tomreplacestory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="905e2-124">**[**tomReplaceStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="905e2-125">**[**tomscratchstory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="905e2-125">**[**tomScratchStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="905e2-126">**[**tomtextframestory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="905e2-126">**[**tomTextFrameStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="905e2-127">**[**tomunknownstory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="905e2-127">**[**tomUnknownStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="905e2-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="905e2-128">Requirements</span></span>



| <span data-ttu-id="905e2-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="905e2-129">Requirement</span></span> | <span data-ttu-id="905e2-130">Wert</span><span class="sxs-lookup"><span data-stu-id="905e2-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="905e2-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="905e2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="905e2-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="905e2-132">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="905e2-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="905e2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="905e2-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="905e2-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="905e2-135">Header</span><span class="sxs-lookup"><span data-stu-id="905e2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="905e2-136"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="905e2-136"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="905e2-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="905e2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="905e2-138">**EM \_ setstorytype**</span><span class="sxs-lookup"><span data-stu-id="905e2-138">**EM\_SETSTORYTYPE**</span></span>](em-setstorytype.md)
</dt> <dt>

[<span data-ttu-id="905e2-139">**Itextstoryranges:: Item**</span><span class="sxs-lookup"><span data-stu-id="905e2-139">**ITextStoryRanges::Item**</span></span>](/windows/desktop/api/Tom/nf-tom-itextstoryranges-item)
</dt> </dl>

 

 





