---
title: TF_LBI_ Konstanten (ctfutb. h)
description: Die TF \_ LBI \_ \-Konstanten werden mit der itflangbaritemsink OnUpdate-Methode verwendet, um anzugeben, welche sprach leisten Elemente geändert wurden.
ms.assetid: ed84012f-19ba-43b3-bbb5-7373ed174c33
topic_type:
- apiref
api_name:
- TF_LBI_ICON
- TF_LBI_TEXT
- TF_LBI_TOOLTIP
- TF_LBI_BITMAP
- TF_LBI_BALLOON
- TF_LBI_STATUS
- TF_LBI_BMPALL
- TF_LBI_BMPBTNALL
- TF_LBI_BTNALL
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72b69f1cb5a5b4a24e78a2bdc1ca0e7a9d79cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337726"
---
# <a name="tf_lbi_-constants"></a><span data-ttu-id="5d923-103">TF- \_ LBI- \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="5d923-103">TF\_LBI\_\* Constants</span></span>

<span data-ttu-id="5d923-104">Die \**tf \_ LBI \_ \** _-Konstanten werden mit der [itflangbaritemsink:: OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) -Methode verwendet, um anzugeben, welche sprach leisten Elemente geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="5d923-104">The \**TF\_LBI\_\** _ constants are used with the [ITfLangBarItemSink::OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) method to indicate which language bar items changed.</span></span>



| <span data-ttu-id="5d923-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="5d923-105">Constant/value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="5d923-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d923-106">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_ICON"></span><span id="tf_lbi_icon"></span><dl> <span data-ttu-id="5d923-107"><dt>_ \* TF \_ LBI- \_ Symbol \* \*</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="5d923-107"><dt>_\*TF\_LBI\_ICON\*\*</dt> <dt>0x00000001</dt></span></span> </dl>                                                        | <span data-ttu-id="5d923-108">Das Symbol des Elements wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="5d923-108">The icon of the item has changed.</span></span> <span data-ttu-id="5d923-109">Die sprach Leiste ruft [itflangbaritembutton:: GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) als Reaktion auf diese Benachrichtigung auf.</span><span class="sxs-lookup"><span data-stu-id="5d923-109">The language bar calls [ITfLangBarItemButton::GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) in response to this notification.</span></span><br/>                                                                                                                                             |
| <span id="TF_LBI_TEXT"></span><span id="tf_lbi_text"></span><dl> <span data-ttu-id="5d923-110"><dt>**Tf \_ LBI- \_ Text**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="5d923-110"><dt>**TF\_LBI\_TEXT**</dt> <dt>0x00000002</dt></span></span> </dl>                                                        | <span data-ttu-id="5d923-111">Der Text einer Schaltfläche oder eines Bitmap-Schaltflächen Elements wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="5d923-111">The text of a button or bitmap button item has changed.</span></span> <span data-ttu-id="5d923-112">Die sprach Leiste ruft [itflangbaritembutton:: gettext](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) oder [itflangbaritembitmapbutton:: gettext](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext)auf, je nachdem, was für diese Benachrichtigung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="5d923-112">The language bar calls [ITfLangBarItemButton::GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) or [ITfLangBarItemBitmapButton::GetText](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext), whichever is appropriate, in response to this notification.</span></span><br/>           |
| <span id="TF_LBI_TOOLTIP"></span><span id="tf_lbi_tooltip"></span><dl> <span data-ttu-id="5d923-113"><dt>**Tf \_ LBI \_**</dt> -QuickInfo <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="5d923-113"><dt>**TF\_LBI\_TOOLTIP**</dt> <dt>0x00000004</dt></span></span> </dl>                                               | <span data-ttu-id="5d923-114">Der QuickInfo-Text des Elements wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="5d923-114">The tooltip text of the item changed.</span></span> <span data-ttu-id="5d923-115">Die sprach Leiste ruft [itflangbaritem:: gettooltipstring](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) als Reaktion auf diese Benachrichtigung auf.</span><span class="sxs-lookup"><span data-stu-id="5d923-115">The language bar calls [ITfLangBarItem::GetTooltipString](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) in response to this notification.</span></span><br/>                                                                                                                                   |
| <span id="TF_LBI_BITMAP"></span><span id="tf_lbi_bitmap"></span><dl> <span data-ttu-id="5d923-116"><dt>**Tf \_ LBI- \_ Bitmap**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="5d923-116"><dt>**TF\_LBI\_BITMAP**</dt> <dt>0x00000008</dt></span></span> </dl>                                                  | <span data-ttu-id="5d923-117">Die Bitmap eines Bitmap-oder Bitmap-Schaltflächen Elements wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="5d923-117">The bitmap of a bitmap or bitmap button item changed.</span></span> <span data-ttu-id="5d923-118">Die sprach Leiste ruft [itflangbaritembitmap::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) oder [itflangbaritembitmapbutton::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap)auf, je nachdem, was für diese Benachrichtigung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="5d923-118">The language bar calls [ITfLangBarItemBitmap::DrawBitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) or [ITfLangBarItemBitmapButton::DrawBitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap), whichever is appropriate, in response to this notification.</span></span><br/> |
| <span id="TF_LBI_BALLOON"></span><span id="tf_lbi_balloon"></span><dl> <span data-ttu-id="5d923-119"><dt>**Tf \_ LBI \_**</dt> -Sprechblase <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="5d923-119"><dt>**TF\_LBI\_BALLOON**</dt> <dt>0x00000010</dt></span></span> </dl>                                               | <span data-ttu-id="5d923-120">Die Informationen für ein Sprechblasen Element wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="5d923-120">The information for a balloon item changed.</span></span> <span data-ttu-id="5d923-121">Die sprach Leiste ruft [itflangbaritemballoon:: getballooninfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) als Reaktion auf diese Benachrichtigung auf.</span><span class="sxs-lookup"><span data-stu-id="5d923-121">The language bar calls [ITfLangBarItemBalloon::GetBalloonInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) in response to this notification.</span></span><br/>                                                                                                                   |
| <span id="TF_LBI_STATUS"></span><span id="tf_lbi_status"></span><dl> <span data-ttu-id="5d923-122"><dt>**Tf \_ LBI- \_ Status**</dt> <dt>0x00010000 bis</dt></span><span class="sxs-lookup"><span data-stu-id="5d923-122"><dt>**TF\_LBI\_STATUS**</dt> <dt>0x00010000</dt></span></span> </dl>                                                  | <span data-ttu-id="5d923-123">Der Element Status wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="5d923-123">The item status changed.</span></span> <span data-ttu-id="5d923-124">Die sprach Leiste ruft [itflangbaritem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) als Reaktion auf diese Benachrichtigung auf.</span><span class="sxs-lookup"><span data-stu-id="5d923-124">The language bar calls [ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) in response to this notification.</span></span><br/>                                                                                                                                                              |
| <span id="TF_LBI_BMPALL"></span><span id="tf_lbi_bmpall"></span><dl> <span data-ttu-id="5d923-125"><dt>**Tf \_ LBI \_ bmpall**</dt> <dt>tf \_ LBI \_ Bitmap \| tf \_ LBI \_ TOOLTIP</dt></span><span class="sxs-lookup"><span data-stu-id="5d923-125"><dt>**TF\_LBI\_BMPALL**</dt> <dt>TF\_LBI\_BITMAP\| TF\_LBI\_TOOLTIP</dt></span></span> </dl>                          | <span data-ttu-id="5d923-126">Kombiniert TF \_ LBI \_ Bitmap und TF \_ LBI \_ TOOLTIP.</span><span class="sxs-lookup"><span data-stu-id="5d923-126">Combines TF\_LBI\_BITMAP and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="TF_LBI_BMPBTNALL"></span><span id="tf_lbi_bmpbtnall"></span><dl> <span data-ttu-id="5d923-127"><dt>**Tf \_ LBI \_ bmpbtnall**</dt> <dt>tf \_ LBI \_ Bitmap \| tf \_ LBI \_ Text \| tf \_ LBI \_ TOOLTIP</dt></span><span class="sxs-lookup"><span data-stu-id="5d923-127"><dt>**TF\_LBI\_BMPBTNALL**</dt> <dt>TF\_LBI\_BITMAP\| TF\_LBI\_TEXT\| TF\_LBI\_TOOLTIP</dt></span></span> </dl> | <span data-ttu-id="5d923-128">Kombiniert TF \_ LBI \_ Bitmap, TF \_ LBI \_ Text und TF \_ LBI \_ TOOLTIP.</span><span class="sxs-lookup"><span data-stu-id="5d923-128">Combines TF\_LBI\_BITMAP, TF\_LBI\_TEXT and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="TF_LBI_BTNALL"></span><span id="tf_lbi_btnall"></span><dl> <span data-ttu-id="5d923-129"><dt>**Tf \_ LBI \_ btnall**</dt> <dt>tf \_ LBI \_ Icon \| tf \_ LBI \_ Text \| tf \_ LBI \_ TOOLTIP</dt></span><span class="sxs-lookup"><span data-stu-id="5d923-129"><dt>**TF\_LBI\_BTNALL**</dt> <dt>TF\_LBI\_ICON\| TF\_LBI\_TEXT\| TF\_LBI\_TOOLTIP</dt></span></span> </dl>            | <span data-ttu-id="5d923-130">Kombiniert TF \_ LBI \_ Icon, TF \_ LBI \_ Text und TF \_ LBI \_ TOOLTIP.</span><span class="sxs-lookup"><span data-stu-id="5d923-130">Combines TF\_LBI\_ICON, TF\_LBI\_TEXT and TF\_LBI\_TOOLTIP.</span></span><br/>                                                                                                                                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="5d923-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d923-131">Requirements</span></span>



| <span data-ttu-id="5d923-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d923-132">Requirement</span></span> | <span data-ttu-id="5d923-133">Wert</span><span class="sxs-lookup"><span data-stu-id="5d923-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d923-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d923-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5d923-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d923-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5d923-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d923-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5d923-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d923-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d923-138">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="5d923-138">Redistributable</span></span><br/>          | <span data-ttu-id="5d923-139">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5d923-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="5d923-140">Header</span><span class="sxs-lookup"><span data-stu-id="5d923-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d923-141"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d923-141"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d923-142">IDL</span><span class="sxs-lookup"><span data-stu-id="5d923-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5d923-143"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5d923-143"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d923-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d923-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d923-145">ITF langbaritemsink:: OnUpdate</span><span class="sxs-lookup"><span data-stu-id="5d923-145">ITfLangBarItemSink::OnUpdate</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate)
</dt> </dl>

 

 





