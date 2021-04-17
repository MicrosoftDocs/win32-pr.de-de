---
title: EM_SETCUEBANNER Meldung (kommstrg. h)
description: Legt den Text Hinweis oder Tip fest, der vom Bearbeitungs Steuerelement angezeigt wird, um den Benutzer zur Eingabe von Informationen aufzufordern.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- Windows-Steuerelemente für EM_SETCUEBANNER Meldung
topic_type:
- apiref
api_name:
- EM_SETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d740bf0a3a055f45c6d104d44349f078d3bf9ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478576"
---
# <a name="em_setcuebanner-message"></a><span data-ttu-id="9a855-104">EM \_ setcuebanner-Meldung</span><span class="sxs-lookup"><span data-stu-id="9a855-104">EM\_SETCUEBANNER message</span></span>

<span data-ttu-id="9a855-105">Legt den Text Hinweis oder Tip fest, der vom Bearbeitungs Steuerelement angezeigt wird, um den Benutzer zur Eingabe von Informationen aufzufordern.</span><span class="sxs-lookup"><span data-stu-id="9a855-105">Sets the textual cue, or tip, that is displayed by the edit control to prompt the user for information.</span></span>

## <a name="parameters"></a><span data-ttu-id="9a855-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a855-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a855-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a855-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a855-108">**True** , wenn das Hinweis Banner auch dann angezeigt werden soll, wenn das Bearbeitungs Steuerelement den Fokus besitzt. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="9a855-108">**TRUE** if the cue banner should show even when the edit control has focus; otherwise, **FALSE**.</span></span> <span data-ttu-id="9a855-109">**False** ist das Standardverhalten, das das Hinweis Banner verschwindet, wenn der Benutzer auf das-Steuerelement klickt.</span><span class="sxs-lookup"><span data-stu-id="9a855-109">**FALSE** is the default behavior the cue banner disappears when the user clicks in the control.</span></span>

</dd> <dt>

<span data-ttu-id="9a855-110">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a855-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a855-111">Ein Zeiger auf eine Unicode-Zeichenfolge, die den Text enthält, der als Text Hinweis angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a855-111">A pointer to a Unicode string that contains the text to display as the textual cue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a855-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a855-112">Return value</span></span>

<span data-ttu-id="9a855-113">Wenn die Nachricht erfolgreich ist, wird **true** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9a855-113">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="9a855-114">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9a855-114">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a855-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a855-115">Remarks</span></span>

<span data-ttu-id="9a855-116">Ein Bearbeitungs Steuerelement, das verwendet wird, um eine Suche zu starten, kann in grauem Text als Text Hinweis den Text "hier suchen hier eingeben" anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9a855-116">An edit control that is used to begin a search may display "Enter search here" in gray text as a textual cue.</span></span> <span data-ttu-id="9a855-117">Wenn der Benutzer auf den Text klickt, geht der Text Weg, und der Benutzer kann eingeben.</span><span class="sxs-lookup"><span data-stu-id="9a855-117">When the user clicks the text, the text goes away and the user can type.</span></span>

<span data-ttu-id="9a855-118">Sie können kein Hinweis Banner in einem mehrzeiligen Bearbeitungs Steuerelement oder in einem Rich-Edit-Steuerelement festlegen.</span><span class="sxs-lookup"><span data-stu-id="9a855-118">You cannot set a cue banner on a multiline edit control or on a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="9a855-119">Um diese API zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="9a855-119">To use this API, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="9a855-120">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9a855-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9a855-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a855-121">Requirements</span></span>



| <span data-ttu-id="9a855-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a855-122">Requirement</span></span> | <span data-ttu-id="9a855-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9a855-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a855-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a855-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9a855-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a855-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9a855-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a855-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9a855-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a855-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9a855-128">Header</span><span class="sxs-lookup"><span data-stu-id="9a855-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a855-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a855-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a855-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a855-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a855-131">**Bearbeiten von \_ setcuebannertext**</span><span class="sxs-lookup"><span data-stu-id="9a855-131">**Edit\_SetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
</dt> </dl>

 

 





