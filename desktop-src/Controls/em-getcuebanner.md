---
title: EM_GETCUEBANNER Meldung (kommstrg. h)
description: Ruft den Text ab, der als Text Hinweis oder Tipp in einem Bearbeitungs Steuerelement angezeigt wird.
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- Windows-Steuerelemente für EM_GETCUEBANNER Meldung
topic_type:
- apiref
api_name:
- EM_GETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d28d4aeea5a206c74f2e6b41cee27b5073448ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957147"
---
# <a name="em_getcuebanner-message"></a><span data-ttu-id="5bef3-104">EM \_ getcuebanner-Meldung</span><span class="sxs-lookup"><span data-stu-id="5bef3-104">EM\_GETCUEBANNER message</span></span>

<span data-ttu-id="5bef3-105">Ruft den Text ab, der als Text Hinweis oder Tipp in einem Bearbeitungs Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5bef3-105">Gets the text that is displayed as the textual cue, or tip, in an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5bef3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bef3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bef3-107">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bef3-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bef3-108">Ein Zeiger auf einen Unicode-Puffer, der den Text erhält, der als Text Hinweis festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5bef3-108">A pointer to a Unicode buffer that receives the text set as the textual cue.</span></span> <span data-ttu-id="5bef3-109">Der Aufrufer ist für die Zuordnung des Puffers verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="5bef3-109">The caller is responsible for allocating the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5bef3-110">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bef3-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bef3-111">Die Größe des Puffers, auf den von *wParam* in **WCHARs** verwiesen wird, einschließlich des abschließenden **null**-Werte.</span><span class="sxs-lookup"><span data-stu-id="5bef3-111">The size of the buffer pointed to by *wParam* in **WCHARs**, including the terminating **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bef3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5bef3-112">Return value</span></span>

<span data-ttu-id="5bef3-113">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="5bef3-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bef3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bef3-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5bef3-115">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="5bef3-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="5bef3-116">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5bef3-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5bef3-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5bef3-117">Requirements</span></span>



| <span data-ttu-id="5bef3-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5bef3-118">Requirement</span></span> | <span data-ttu-id="5bef3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5bef3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5bef3-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5bef3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5bef3-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bef3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5bef3-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5bef3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5bef3-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bef3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5bef3-124">Header</span><span class="sxs-lookup"><span data-stu-id="5bef3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bef3-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bef3-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bef3-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bef3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bef3-127">**\_Getcuebannertext bearbeiten**</span><span class="sxs-lookup"><span data-stu-id="5bef3-127">**Edit\_GetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 





