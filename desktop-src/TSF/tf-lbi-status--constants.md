---
title: TF_LBI_STATUS_ Konstanten (ctfutb. h)
description: Die TF \_ LBI- \_ Status \_ \-Konstanten geben den Status eines sprach leisten Elements an. Diese Werte werden mit der itflangbaritem GetStatus-Methode verwendet.
ms.assetid: 5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc
topic_type:
- apiref
api_name:
- TF_LBI_STATUS_HIDDEN
- TF_LBI_STATUS_DISABLED
- TF_LBI_STATUS_BTN_TOGGLED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de9dcf0272eaf79fd001461aa555d78c9d6ae30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742921"
---
# <a name="tf_lbi_status_-constants"></a><span data-ttu-id="633b1-104">TF \_ LBI- \_ Status \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="633b1-104">TF\_LBI\_STATUS\_\* Constants</span></span>

<span data-ttu-id="633b1-105">Die "\**tf \_ LBI \_ Status \_ \** _-Konstanten" geben den Status eines sprach leisten Elements an.</span><span class="sxs-lookup"><span data-stu-id="633b1-105">The \**TF\_LBI\_STATUS\_\** _ constants indicate the status of a language bar item.</span></span> <span data-ttu-id="633b1-106">Diese Werte werden mit der [itflangbaritem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="633b1-106">These values are used with the [ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) method.</span></span>



| <span data-ttu-id="633b1-107">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="633b1-107">Constant/value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="633b1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="633b1-108">Description</span></span>                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STATUS_HIDDEN"></span><span id="tf_lbi_status_hidden"></span><dl> <span data-ttu-id="633b1-109"><dt>_ \* TF \_ LBI- \_ Status \_ ausgeblendet \* \*</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="633b1-109"><dt>_\*TF\_LBI\_STATUS\_HIDDEN\*\*</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="633b1-110">Das Element ist ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="633b1-110">The item is hidden.</span></span> <span data-ttu-id="633b1-111">Dieser Stil wird ignoriert, wenn das Element den Stil des TF- \_ LBI- \_ Stils " \_ hiddenstatus Control" nicht enthält.</span><span class="sxs-lookup"><span data-stu-id="633b1-111">This style is ignored if the item does not include the TF\_LBI\_STYLE\_HIDDENSTATUSCONTROL style.</span></span><br/>                  |
| <span id="TF_LBI_STATUS_DISABLED"></span><span id="tf_lbi_status_disabled"></span><dl> <span data-ttu-id="633b1-112"><dt>**Tf \_ LBI- \_ Status \_ deaktiviert**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="633b1-112"><dt>**TF\_LBI\_STATUS\_DISABLED**</dt> <dt>0x00000002</dt></span></span> </dl>           | <span data-ttu-id="633b1-113">Das Element ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="633b1-113">The item is disabled.</span></span><br/>                                                                                                                  |
| <span id="TF_LBI_STATUS_BTN_TOGGLED"></span><span id="tf_lbi_status_btn_toggled"></span><dl> <span data-ttu-id="633b1-114"><dt>**Tf \_ LBI- \_ Status \_ \_ BTN**</dt> -ein-/ausgeschaltet <dt>0x00010000 bis</dt></span><span class="sxs-lookup"><span data-stu-id="633b1-114"><dt>**TF\_LBI\_STATUS\_BTN\_TOGGLED**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="633b1-115">Das Element befindet sich im UMSCHALT-oder gedrückten Zustand.</span><span class="sxs-lookup"><span data-stu-id="633b1-115">The item is in the toggled or pressed state.</span></span> <span data-ttu-id="633b1-116">Dieser Stil wird ignoriert, wenn das Element den TF \_ LBI- \_ Stil \_ BTN- \_ UMSCHALT Stil nicht enthält.</span><span class="sxs-lookup"><span data-stu-id="633b1-116">This style is ignored if the item does not include the TF\_LBI\_STYLE\_BTN\_TOGGLE style.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="633b1-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="633b1-117">Requirements</span></span>



| <span data-ttu-id="633b1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="633b1-118">Requirement</span></span> | <span data-ttu-id="633b1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="633b1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="633b1-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="633b1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="633b1-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="633b1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="633b1-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="633b1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="633b1-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="633b1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="633b1-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="633b1-124">Redistributable</span></span><br/>          | <span data-ttu-id="633b1-125">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="633b1-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="633b1-126">Header</span><span class="sxs-lookup"><span data-stu-id="633b1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="633b1-127"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="633b1-127"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="633b1-128">IDL</span><span class="sxs-lookup"><span data-stu-id="633b1-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="633b1-129"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="633b1-129"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="633b1-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="633b1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="633b1-131">Itflangbaritem:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="633b1-131">ITfLangBarItem::GetStatus</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





