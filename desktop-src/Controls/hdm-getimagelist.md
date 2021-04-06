---
title: HDM_GETIMAGELIST Meldung (kommstrg. h)
description: Ruft das Handle für die Bildliste ab, die für ein vorhandenes Header Steuerelement festgelegt wurde. Sie können diese Nachricht explizit senden oder den Header \_ GetImageList oder das \_ getstateimagelist-Makro des Headers verwenden.
ms.assetid: 3e1a979c-60c5-4538-bd4d-16238829062e
keywords:
- Windows-Steuerelemente für HDM_GETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- HDM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e199d603af873f1957d33855ccf5c59a90a4002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742280"
---
# <a name="hdm_getimagelist-message"></a><span data-ttu-id="e9617-105">HDM \_ GetImageList-Meldung</span><span class="sxs-lookup"><span data-stu-id="e9617-105">HDM\_GETIMAGELIST message</span></span>

<span data-ttu-id="e9617-106">Ruft das Handle für die Bildliste ab, die für ein vorhandenes Header Steuerelement festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="e9617-106">Gets the handle to the image list that has been set for an existing header control.</span></span> <span data-ttu-id="e9617-107">Sie können diese Nachricht explizit senden oder den [**Header \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) oder das [**\_ getstateimagelist**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) -Makro des Headers verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9617-107">You can send this message explicitly or use the [**Header\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) or [**Header\_GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e9617-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9617-108">Parameters</span></span>

<dl> <span data-ttu-id="e9617-109"><dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="e9617-109"><dt>*wParam* </dt> </span></span><dd><span data-ttu-id="e9617-110">Einer der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="e9617-110">One of the following values:</span></span>

| <span data-ttu-id="e9617-111">Wert</span><span class="sxs-lookup"><span data-stu-id="e9617-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="e9617-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e9617-112">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <span data-ttu-id="e9617-113"><dt>**hdsil \_ Normal**</dt></span><span class="sxs-lookup"><span data-stu-id="e9617-113"><dt>**HDSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="e9617-114">Gibt an, dass es sich hierbei um eine normale Bildliste handelt.</span><span class="sxs-lookup"><span data-stu-id="e9617-114">Indicates that this is a normal image list.</span></span><br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <span data-ttu-id="e9617-115"><dt>**hdsil- \_ Status**</dt></span><span class="sxs-lookup"><span data-stu-id="e9617-115"><dt>**HDSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="e9617-116">Gibt an, dass es sich um eine Status Bild Liste handelt.</span><span class="sxs-lookup"><span data-stu-id="e9617-116">Indicates that this is a state image list.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="e9617-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e9617-117">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e9617-118">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e9617-118">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9617-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9617-119">Return value</span></span>

<span data-ttu-id="e9617-120">Gibt ein Handle für die Bildliste zurück, die für das Header Steuerelement festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e9617-120">Returns a handle to the image list set for the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9617-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9617-121">Requirements</span></span>



| <span data-ttu-id="e9617-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9617-122">Requirement</span></span> | <span data-ttu-id="e9617-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e9617-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9617-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9617-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e9617-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9617-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e9617-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9617-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e9617-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9617-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e9617-128">Header</span><span class="sxs-lookup"><span data-stu-id="e9617-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9617-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9617-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





