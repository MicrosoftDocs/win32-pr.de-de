---
title: TF_LBMENUF_ Konstanten (ctfutb. h)
description: Die TF \_ lbmenuf \_ \-Konstanten werden in der itfmenu addmenuitem-Methode verwendet, um die Eigenschaften eines Menü Elements in der sprach Leiste anzugeben.
ms.assetid: f8f3f397-b84e-4635-b454-31369c679ce2
topic_type:
- apiref
api_name:
- TF_LBMENUF_CHECKED
- TF_LBMENUF_SUBMENU
- TF_LBMENUF_SEPARATOR
- TF_LBMENUF_RADIOCHECKED
- TF_LBMENUF_GRAYED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a056e9a758419965341b4d508db083fc8f31b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956422"
---
# <a name="tf_lbmenuf_-constants"></a><span data-ttu-id="cd057-103">TF- \_ lbmenuf- \_ \* Konstanten</span><span class="sxs-lookup"><span data-stu-id="cd057-103">TF\_LBMENUF\_\* Constants</span></span>

<span data-ttu-id="cd057-104">Die \**tf \_ lbmenuf \_ \** _-Konstanten werden in der [itfmenu:: addmenuitem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem) -Methode verwendet, um die Eigenschaften eines Menü Elements in der sprach Leiste anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cd057-104">The \**TF\_LBMENUF\_\** _ constants are used in the [ITfMenu::AddMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem) method to specify the characteristics of a menu item in the language bar.</span></span>



| <span data-ttu-id="cd057-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="cd057-105">Constant/value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="cd057-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd057-106">Description</span></span>                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="TF_LBMENUF_CHECKED"></span><span id="tf_lbmenuf_checked"></span><dl> <span data-ttu-id="cd057-107"><dt>_ \* TF \_ Lbmenuf \_ aktiviert \* \*</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="cd057-107"><dt>_\*TF\_LBMENUF\_CHECKED\*\*</dt> <dt>0x01</dt></span></span> </dl>                | <span data-ttu-id="cd057-108">Das Menü Element ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cd057-108">The menu item is checked.</span></span><br/>            |
| <span id="TF_LBMENUF_SUBMENU"></span><span id="tf_lbmenuf_submenu"></span><dl> <span data-ttu-id="cd057-109"><dt>**Tf \_ Lbmenuf- \_ Untermenü**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="cd057-109"><dt>**TF\_LBMENUF\_SUBMENU**</dt> <dt>0x02</dt></span></span> </dl>                | <span data-ttu-id="cd057-110">Das Menü Element ist ein Untermenü.</span><span class="sxs-lookup"><span data-stu-id="cd057-110">The menu item is a submenu.</span></span><br/>          |
| <span id="TF_LBMENUF_SEPARATOR"></span><span id="tf_lbmenuf_separator"></span><dl> <span data-ttu-id="cd057-111"><dt>**Tf \_ Lbmenuf- \_ Trenn**</dt> Zeichen <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="cd057-111"><dt>**TF\_LBMENUF\_SEPARATOR**</dt> <dt>0x04</dt></span></span> </dl>          | <span data-ttu-id="cd057-112">Das Menü Element ist ein Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="cd057-112">The menu item is a separator.</span></span><br/>        |
| <span id="TF_LBMENUF_RADIOCHECKED"></span><span id="tf_lbmenuf_radiochecked"></span><dl> <span data-ttu-id="cd057-113"><dt>**Tf \_ Lbmenuf \_ Radio Check**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="cd057-113"><dt>**TF\_LBMENUF\_RADIOCHECKED**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="cd057-114">Das Menü Element ist ein Optionsfeld.</span><span class="sxs-lookup"><span data-stu-id="cd057-114">The menu item is a radio check mark.</span></span><br/> |
| <span id="TF_LBMENUF_GRAYED"></span><span id="tf_lbmenuf_grayed"></span><dl> <span data-ttu-id="cd057-115"><dt>**Tf \_ Lbmenuf, \_ grau**</dt> , <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="cd057-115"><dt>**TF\_LBMENUF\_GRAYED**</dt> <dt>0x10</dt></span></span> </dl>                   | <span data-ttu-id="cd057-116">Das Menü Element ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="cd057-116">The menu item is disabled.</span></span><br/>           |



## <a name="requirements"></a><span data-ttu-id="cd057-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd057-117">Requirements</span></span>



| <span data-ttu-id="cd057-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd057-118">Requirement</span></span> | <span data-ttu-id="cd057-119">Wert</span><span class="sxs-lookup"><span data-stu-id="cd057-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd057-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd057-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cd057-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd057-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="cd057-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd057-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cd057-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd057-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd057-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="cd057-124">Redistributable</span></span><br/>          | <span data-ttu-id="cd057-125">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cd057-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="cd057-126">Header</span><span class="sxs-lookup"><span data-stu-id="cd057-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd057-127"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd057-127"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd057-128">IDL</span><span class="sxs-lookup"><span data-stu-id="cd057-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cd057-129"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cd057-129"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd057-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd057-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd057-131">ITF Menu:: addmenuitem</span><span class="sxs-lookup"><span data-stu-id="cd057-131">ITfMenu::AddMenuItem</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem)
</dt> </dl>

 

 





