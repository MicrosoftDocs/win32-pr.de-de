---
title: EM_FORMATRANGE Meldung (RichEdit. h)
description: Formatiert einen Textbereich in einem Rich-Edit-Steuerelement für ein bestimmtes Gerät.
ms.assetid: 6d1e562b-d741-4d4a-a395-554083cb0dbb
keywords:
- Windows-Steuerelemente für EM_FORMATRANGE Meldung
topic_type:
- apiref
api_name:
- EM_FORMATRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8f235fb054643623510ea23e73001aaeb070be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858964"
---
# <a name="em_formatrange-message"></a><span data-ttu-id="e0ef1-104">EM \_ FormatRange-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e0ef1-104">EM\_FORMATRANGE message</span></span>

<span data-ttu-id="e0ef1-105">Formatiert einen Textbereich in einem Rich-Edit-Steuerelement für ein bestimmtes Gerät.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-105">Formats a range of text in a rich edit control for a specific device.</span></span>

## <a name="parameters"></a><span data-ttu-id="e0ef1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0ef1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0ef1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0ef1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0ef1-108">Gibt an, ob der Text dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-108">Specifies whether to render the text.</span></span> <span data-ttu-id="e0ef1-109">Wenn dieser Parameter nicht 0 (null) ist, wird der Text gerendert.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-109">If this parameter is not zero, the text is rendered.</span></span> <span data-ttu-id="e0ef1-110">Andernfalls wird der Text direkt gemessen.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-110">Otherwise, the text is just measured.</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0ef1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0ef1-112">Eine [**Format Bereichs**](/windows/desktop/api/Richedit/ns-richedit-formatrange) Struktur, die Informationen über das Ausgabegerät enthält, oder **null** , um vom-Steuerelement zwischengespeicherte Informationen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-112">A [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) structure containing information about the output device, or **NULL** to free information cached by the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0ef1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0ef1-113">Return value</span></span>

<span data-ttu-id="e0ef1-114">Diese Meldung gibt den Index des letzten Zeichens zurück, das in den Bereich passt, plus 1.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-114">This message returns the index of the last character that fits in the region, plus 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0ef1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0ef1-115">Remarks</span></span>

<span data-ttu-id="e0ef1-116">Diese Meldung wird normalerweise verwendet, um den Inhalt eines Rich-Edit-Steuer Elements für ein Ausgabegerät wie einen Drucker zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-116">This message is typically used to format the content of rich edit control for an output device such as a printer.</span></span>

<span data-ttu-id="e0ef1-117">Nachdem Sie diese Meldung verwendet haben, um einen Textbereich zu formatieren, ist es wichtig, dass Sie die zwischengespeicherten Informationen freigeben, indem Sie **EM \_ FormatRange** erneut senden, wobei *LPARAM* jedoch auf **null** festgelegt ist. andernfalls tritt ein Speicherfehler auf.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-117">After using this message to format a range of text, it is important that you free cached information by sending **EM\_FORMATRANGE** again, but with *lParam* set to **NULL**; otherwise, a memory leak will occur.</span></span> <span data-ttu-id="e0ef1-118">Außerdem müssen Sie nach der Verwendung dieser Nachricht für ein Gerät zwischengespeicherte Informationen freigeben, bevor Sie es für ein anderes Gerät wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-118">Also, after using this message for one device, you must free cached information before using it again for a different device.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0ef1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0ef1-119">Requirements</span></span>



| <span data-ttu-id="e0ef1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0ef1-120">Requirement</span></span> | <span data-ttu-id="e0ef1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e0ef1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0ef1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e0ef1-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0ef1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e0ef1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e0ef1-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0ef1-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0ef1-126">Header</span><span class="sxs-lookup"><span data-stu-id="e0ef1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0ef1-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0ef1-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0ef1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0ef1-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="e0ef1-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e0ef1-130">**EM \_ DisplayBand**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-130">**EM\_DISPLAYBAND**</span></span>](em-displayband.md)
</dt> <dt>

<span data-ttu-id="e0ef1-131">**Licher**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e0ef1-132">Drucken von Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="e0ef1-132">Printing Rich Edit Controls</span></span>](printing-rich-edit-controls.md)
</dt> </dl>

 

 





