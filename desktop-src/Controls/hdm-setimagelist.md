---
title: HDM_SETIMAGELIST Meldung (kommstrg. h)
description: Weist einem vorhandenen Header Steuerelement eine Bildliste zu. Sie können diese Nachricht explizit senden oder den Header \_ SetImageList oder das \_ setstateimagelist-Makro des Headers verwenden.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- Windows-Steuerelemente für HDM_SETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- HDM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17fe21d64b141cf27d32e00fac0ce78228421518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949819"
---
# <a name="hdm_setimagelist-message"></a><span data-ttu-id="75d38-105">HDM \_ SetImageList-Meldung</span><span class="sxs-lookup"><span data-stu-id="75d38-105">HDM\_SETIMAGELIST message</span></span>

<span data-ttu-id="75d38-106">Weist einem vorhandenen Header Steuerelement eine Bildliste zu.</span><span class="sxs-lookup"><span data-stu-id="75d38-106">Assigns an image list to an existing header control.</span></span> <span data-ttu-id="75d38-107">Sie können diese Nachricht explizit senden oder den [**Header \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) oder das [**\_ setstateimagelist**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) -Makro des Headers verwenden.</span><span class="sxs-lookup"><span data-stu-id="75d38-107">You can send this message explicitly or use the [**Header\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) or [**Header\_SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="75d38-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="75d38-108">Parameters</span></span>

<dl> <span data-ttu-id="75d38-109"><dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="75d38-109"><dt>*wParam* </dt> </span></span><dd><span data-ttu-id="75d38-110">Einer der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="75d38-110">One of the following values:</span></span>

| <span data-ttu-id="75d38-111">Wert</span><span class="sxs-lookup"><span data-stu-id="75d38-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="75d38-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="75d38-112">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <span data-ttu-id="75d38-113"><dt>**hdsil \_ Normal**</dt></span><span class="sxs-lookup"><span data-stu-id="75d38-113"><dt>**HDSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="75d38-114">Gibt an, dass es sich hierbei um eine normale Bildliste handelt.</span><span class="sxs-lookup"><span data-stu-id="75d38-114">Indicates that this is a normal image list.</span></span><br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <span data-ttu-id="75d38-115"><dt>**hdsil- \_ Status**</dt></span><span class="sxs-lookup"><span data-stu-id="75d38-115"><dt>**HDSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="75d38-116">Gibt an, dass es sich um eine Status Bild Liste handelt.</span><span class="sxs-lookup"><span data-stu-id="75d38-116">Indicates that this is a state image list.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="75d38-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75d38-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75d38-118">Ein Handle für eine Bildliste.</span><span class="sxs-lookup"><span data-stu-id="75d38-118">A handle to an image list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75d38-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75d38-119">Return value</span></span>

<span data-ttu-id="75d38-120">Gibt das Handle für die Bildliste zurück, die dem Steuerelement zuvor zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="75d38-120">Returns the handle to the image list previously associated with the control.</span></span> <span data-ttu-id="75d38-121">Gibt bei einem Fehler **null** zurück oder, wenn zuvor keine Bildliste festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="75d38-121">Returns **NULL** upon failure or if no image list was set previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="75d38-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75d38-122">Requirements</span></span>



| <span data-ttu-id="75d38-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75d38-123">Requirement</span></span> | <span data-ttu-id="75d38-124">Wert</span><span class="sxs-lookup"><span data-stu-id="75d38-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75d38-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75d38-125">Minimum supported client</span></span><br/> | <span data-ttu-id="75d38-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75d38-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="75d38-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75d38-127">Minimum supported server</span></span><br/> | <span data-ttu-id="75d38-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75d38-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="75d38-129">Header</span><span class="sxs-lookup"><span data-stu-id="75d38-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="75d38-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="75d38-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





