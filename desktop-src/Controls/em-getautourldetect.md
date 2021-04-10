---
title: EM_GETAUTOURLDETECT Meldung (RichEdit. h)
description: Gibt an, ob die automatische URL-Erkennung im Rich Edit-Steuerelement aktiviert ist.
ms.assetid: f723f15c-bf8f-41ab-aef0-bd8f2c0b9e5d
keywords:
- Windows-Steuerelemente für EM_GETAUTOURLDETECT Meldung
topic_type:
- apiref
api_name:
- EM_GETAUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e68e4f2991c5f8780cb587594289674e07ec992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040693"
---
# <a name="em_getautourldetect-message"></a><span data-ttu-id="3fa0a-104">EM \_ GETAUTOURLDETECT Meldung</span><span class="sxs-lookup"><span data-stu-id="3fa0a-104">EM\_GETAUTOURLDETECT message</span></span>

<span data-ttu-id="3fa0a-105">Gibt an, ob die automatische URL-Erkennung im Rich Edit-Steuerelement aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3fa0a-105">Indicates whether the auto URL detection is turned on in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3fa0a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fa0a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fa0a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3fa0a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fa0a-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="3fa0a-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3fa0a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fa0a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fa0a-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="3fa0a-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fa0a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3fa0a-111">Return value</span></span>

<span data-ttu-id="3fa0a-112">Wenn die automatische URL-Erkennung aktiv ist, ist der Rückgabewert 1.</span><span class="sxs-lookup"><span data-stu-id="3fa0a-112">If auto-URL detection is active, the return value is 1.</span></span>

<span data-ttu-id="3fa0a-113">Wenn die automatische URL-Erkennung inaktiv ist, ist der Rückgabewert 0.</span><span class="sxs-lookup"><span data-stu-id="3fa0a-113">If auto-URL detection is inactive, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fa0a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3fa0a-114">Remarks</span></span>

<span data-ttu-id="3fa0a-115">Wenn die automatische URL-Erkennung eingeschaltet ist, überprüft Microsoft Rich Edit den typisierten Text ständig auf eine gültige URL.</span><span class="sxs-lookup"><span data-stu-id="3fa0a-115">When auto URL detection is on, Microsoft Rich Edit is constantly checking typed text for a valid URL.</span></span> <span data-ttu-id="3fa0a-116">Bei der umfassenden Bearbeitung werden URLs erkannt, die mit den folgenden Präfixen beginnen:</span><span class="sxs-lookup"><span data-stu-id="3fa0a-116">Rich Edit recognizes URLs that start with these prefixes:</span></span>

-   <span data-ttu-id="3fa0a-117">http:</span><span class="sxs-lookup"><span data-stu-id="3fa0a-117">http:</span></span>
-   <span data-ttu-id="3fa0a-118">file:</span><span class="sxs-lookup"><span data-stu-id="3fa0a-118">file:</span></span>
-   <span data-ttu-id="3fa0a-119">mailto:</span><span class="sxs-lookup"><span data-stu-id="3fa0a-119">mailto:</span></span>
-   <span data-ttu-id="3fa0a-120">FTP</span><span class="sxs-lookup"><span data-stu-id="3fa0a-120">ftp:</span></span>
-   <span data-ttu-id="3fa0a-121">http</span><span class="sxs-lookup"><span data-stu-id="3fa0a-121">https:</span></span>
-   <span data-ttu-id="3fa0a-122">Gopher</span><span class="sxs-lookup"><span data-stu-id="3fa0a-122">gopher:</span></span>
-   <span data-ttu-id="3fa0a-123">NNTP-</span><span class="sxs-lookup"><span data-stu-id="3fa0a-123">nntp:</span></span>
-   <span data-ttu-id="3fa0a-124">Prospero:</span><span class="sxs-lookup"><span data-stu-id="3fa0a-124">prospero:</span></span>
-   <span data-ttu-id="3fa0a-125">Telnet</span><span class="sxs-lookup"><span data-stu-id="3fa0a-125">telnet:</span></span>
-   <span data-ttu-id="3fa0a-126">News</span><span class="sxs-lookup"><span data-stu-id="3fa0a-126">news:</span></span>
-   <span data-ttu-id="3fa0a-127">Wais:</span><span class="sxs-lookup"><span data-stu-id="3fa0a-127">wais:</span></span>
-   <span data-ttu-id="3fa0a-128">positiv</span><span class="sxs-lookup"><span data-stu-id="3fa0a-128">outlook:</span></span>

<span data-ttu-id="3fa0a-129">Rich Edit erkennt auch Standard Pfadnamen, die mit beginnen \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="3fa0a-129">Rich Edit also recognizes standard path names that start with \\\\.</span></span> <span data-ttu-id="3fa0a-130">Wenn Rich Edit eine URL verwendet, ändert Sie die Textfarbe der URL, unterstreicht den Text und benachrichtigt den Client über den [ \_ Link "en](en-link.md)".</span><span class="sxs-lookup"><span data-stu-id="3fa0a-130">When Rich Edit locates a URL, it changes the URL text color, underlines the text, and notifies the client using [EN\_LINK](en-link.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3fa0a-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3fa0a-131">Requirements</span></span>



| <span data-ttu-id="3fa0a-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3fa0a-132">Requirement</span></span> | <span data-ttu-id="3fa0a-133">Wert</span><span class="sxs-lookup"><span data-stu-id="3fa0a-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa0a-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3fa0a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3fa0a-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3fa0a-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3fa0a-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3fa0a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3fa0a-137">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3fa0a-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3fa0a-138">Header</span><span class="sxs-lookup"><span data-stu-id="3fa0a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fa0a-139"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fa0a-139"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fa0a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fa0a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fa0a-141">Link "en" \_</span><span class="sxs-lookup"><span data-stu-id="3fa0a-141">EN\_LINK</span></span>](en-link.md)
</dt> </dl>

 

 





