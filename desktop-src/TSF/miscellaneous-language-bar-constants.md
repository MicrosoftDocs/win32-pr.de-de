---
title: Diverse sprach Balken Konstanten (ctfutb. h)
description: Die verschiedenen sprach leisten Konstanten legen bestimmte Eigenschaften von sprach leisten fest.
ms.assetid: c1740636-7ba3-4748-9005-ee94d04dbb15
topic_type:
- apiref
api_name:
- TF_DTLBI_USEPROFILEICON
- TF_INVALIDMENUITEM
- TF_LBI_BMPF_VERTICAL
- TF_LBI_DESC_MAXLEN
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91fd1a371581dea02226ba6539ca25a06ef98e75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392138"
---
# <a name="miscellaneous-language-bar-constants"></a><span data-ttu-id="63676-103">Diverse sprach Balken Konstanten</span><span class="sxs-lookup"><span data-stu-id="63676-103">Miscellaneous Language Bar Constants</span></span>

<span data-ttu-id="63676-104">Die verschiedenen sprach leisten Konstanten legen bestimmte Eigenschaften von sprach leisten fest.</span><span class="sxs-lookup"><span data-stu-id="63676-104">The miscellaneous language bar constants set certain properties of language bars.</span></span>



| <span data-ttu-id="63676-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="63676-105">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="63676-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63676-106">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DTLBI_USEPROFILEICON"></span><span id="tf_dtlbi_useprofileicon"></span><dl> <span data-ttu-id="63676-107"><dt>**Tf \_ Dtlbi \_ useprofileicon**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="63676-107"><dt>**TF\_DTLBI\_USEPROFILEICON**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="63676-108">Das Element System Language Bar sollte das Symbol anzeigen, das für das Sprachprofil angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="63676-108">The system language bar item should display the icon specified for the language profile.</span></span> <span data-ttu-id="63676-109">Wird in den Methoden [ITF systemdevicetypelangbaritem:: getianmode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) und [ITF systemdevicetypelangbaritem::](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="63676-109">Used in the [ITfSystemDeviceTypeLangBarItem::GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) and [ITfSystemDeviceTypeLangBarItem::SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) methods.</span></span><br/> |
| <span id="TF_INVALIDMENUITEM"></span><span id="tf_invalidmenuitem"></span><dl> <span data-ttu-id="63676-110"><dt>**Tf \_ Invalidmenuitem**</dt> <dt>(uint) (-1)</dt></span><span class="sxs-lookup"><span data-stu-id="63676-110"><dt>**TF\_INVALIDMENUITEM**</dt> <dt>(UINT)(-1)</dt></span></span> </dl>                 | <span data-ttu-id="63676-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="63676-111">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_BMPF_VERTICAL"></span><span id="tf_lbi_bmpf_vertical"></span><dl> <span data-ttu-id="63676-112"><dt>**Tf \_ LBI \_ BMPF \_ vertikal**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="63676-112"><dt>**TF\_LBI\_BMPF\_VERTICAL**</dt> <dt>0x00000001</dt></span></span> </dl>         | <span data-ttu-id="63676-113">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="63676-113">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_DESC_MAXLEN"></span><span id="tf_lbi_desc_maxlen"></span><dl> <span data-ttu-id="63676-114"><dt>**Tf \_ LBI-zu-Ende- \_ \_ maxlen**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="63676-114"><dt>**TF\_LBI\_DESC\_MAXLEN**</dt> <dt>32</dt></span></span> </dl>                       | <span data-ttu-id="63676-115">Länge in WCHAR-Zeichen des Strukturmembers [tf \_ langbariteminfo. szDescription](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo).</span><span class="sxs-lookup"><span data-stu-id="63676-115">Length, in WCHAR characters, of structure member [TF\_LANGBARITEMINFO.szDescription](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo).</span></span><br/>                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="63676-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63676-116">Requirements</span></span>



| <span data-ttu-id="63676-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63676-117">Requirement</span></span> | <span data-ttu-id="63676-118">Wert</span><span class="sxs-lookup"><span data-stu-id="63676-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63676-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63676-119">Minimum supported client</span></span><br/> | <span data-ttu-id="63676-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63676-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="63676-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63676-121">Minimum supported server</span></span><br/> | <span data-ttu-id="63676-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63676-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63676-123">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="63676-123">Redistributable</span></span><br/>          | <span data-ttu-id="63676-124">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="63676-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="63676-125">Header</span><span class="sxs-lookup"><span data-stu-id="63676-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="63676-126"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="63676-126"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="63676-127">IDL</span><span class="sxs-lookup"><span data-stu-id="63676-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63676-128"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="63676-128"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63676-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63676-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63676-130">ITF systemdevicetypelangbaritem:: getidesystemmode</span><span class="sxs-lookup"><span data-stu-id="63676-130">ITfSystemDeviceTypeLangBarItem::GetIconMode</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode)
</dt> <dt>

[<span data-ttu-id="63676-131">ITF systemdevicetypelangbaritem:: Settings-Modus</span><span class="sxs-lookup"><span data-stu-id="63676-131">ITfSystemDeviceTypeLangBarItem::SetIconMode</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode)
</dt> <dt>

[<span data-ttu-id="63676-132">TF \_ langbariteminfo</span><span class="sxs-lookup"><span data-stu-id="63676-132">TF\_LANGBARITEMINFO</span></span>](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> </dl>

 

 





