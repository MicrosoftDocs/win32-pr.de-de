---
title: EM_REQUESTRESIZE Meldung (RichEdit. h)
description: Erzwingt, dass ein RichEdit-Steuerelement einen en \_ RequestResize-Benachrichtigungs Code an das übergeordnete Fenster sendet.
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- Windows-Steuerelemente für EM_REQUESTRESIZE Meldung
topic_type:
- apiref
api_name:
- EM_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41e7be8e0f30d5c1ec011247f3964292c2218e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213743"
---
# <a name="em_requestresize-message"></a><span data-ttu-id="100ae-104">EM \_ RequestResize-Meldung</span><span class="sxs-lookup"><span data-stu-id="100ae-104">EM\_REQUESTRESIZE message</span></span>

<span data-ttu-id="100ae-105">Erzwingt, dass ein RichEdit-Steuerelement einen [**en \_ RequestResize**](en-requestresize.md) -Benachrichtigungs Code an das übergeordnete Fenster sendet.</span><span class="sxs-lookup"><span data-stu-id="100ae-105">Forces a rich edit control to send an [**EN\_REQUESTRESIZE**](en-requestresize.md) notification code to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="100ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="100ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="100ae-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="100ae-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="100ae-108">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="100ae-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="100ae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="100ae-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="100ae-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="100ae-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="100ae-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="100ae-111">Return value</span></span>

<span data-ttu-id="100ae-112">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="100ae-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="100ae-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="100ae-113">Remarks</span></span>

<span data-ttu-id="100ae-114">Diese Meldung ist während der Verarbeitung der [**WM- \_ Größe**](/windows/desktop/winmsg/wm-size) für das übergeordnete Element eines untersten Rich-Edit-Steuer Elements nützlich.</span><span class="sxs-lookup"><span data-stu-id="100ae-114">This message is useful during [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) processing for the parent of a bottomless rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="100ae-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="100ae-115">Requirements</span></span>



| <span data-ttu-id="100ae-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="100ae-116">Requirement</span></span> | <span data-ttu-id="100ae-117">Wert</span><span class="sxs-lookup"><span data-stu-id="100ae-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="100ae-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="100ae-118">Minimum supported client</span></span><br/> | <span data-ttu-id="100ae-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="100ae-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="100ae-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="100ae-120">Minimum supported server</span></span><br/> | <span data-ttu-id="100ae-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="100ae-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="100ae-122">Header</span><span class="sxs-lookup"><span data-stu-id="100ae-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="100ae-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="100ae-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="100ae-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="100ae-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="100ae-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="100ae-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="100ae-126">**de \_ RequestResize**</span><span class="sxs-lookup"><span data-stu-id="100ae-126">**EN\_REQUESTRESIZE**</span></span>](en-requestresize.md)
</dt> <dt>

<span data-ttu-id="100ae-127">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="100ae-127">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="100ae-128">**WM- \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="100ae-128">**WM\_SIZE**</span></span>](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

