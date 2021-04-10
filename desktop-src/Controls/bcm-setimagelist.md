---
title: BCM_SETIMAGELIST Meldung (kommstrg. h)
description: Weist einem Schaltflächen-Steuerelement eine Bildliste zu. Sie können diese Nachricht explizit senden oder das \_ SetImageList-Makro der Schaltfläche verwenden.
ms.assetid: 805d2d9b-3e8f-4323-abaf-0dd5765cd740
keywords:
- Windows-Steuerelemente für BCM_SETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- BCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bdf29735958f3c40af544bca4b946458df8431
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040510"
---
# <a name="bcm_setimagelist-message"></a><span data-ttu-id="89d44-105">BCM \_ SetImageList-Meldung</span><span class="sxs-lookup"><span data-stu-id="89d44-105">BCM\_SETIMAGELIST message</span></span>

<span data-ttu-id="89d44-106">Weist einem Schaltflächen-Steuerelement eine Bildliste zu.</span><span class="sxs-lookup"><span data-stu-id="89d44-106">Assigns an image list to a button control.</span></span> <span data-ttu-id="89d44-107">Sie können diese Nachricht explizit senden oder das [**\_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) -Makro der Schaltfläche verwenden.</span><span class="sxs-lookup"><span data-stu-id="89d44-107">You can send this message explicitly or use the [**Button\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="89d44-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="89d44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89d44-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89d44-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89d44-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="89d44-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="89d44-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89d44-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89d44-112">Ein Zeiger auf eine [**Schaltflächen- \_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) -Struktur, die Bildlisten Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="89d44-112">A pointer to a [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that contains image list information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89d44-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89d44-113">Return value</span></span>

<span data-ttu-id="89d44-114">Wenn die Nachricht erfolgreich ist, wird **true** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="89d44-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="89d44-115">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="89d44-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="89d44-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89d44-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="89d44-117">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="89d44-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="89d44-118">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="89d44-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="89d44-119">Die Bildliste, auf die im **HIML** -Member der [**Schaltfläche \_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) -Struktur verwiesen wird, muss entweder ein einzelnes Bild enthalten, das für alle Zustände oder einzelne Bilder für jeden Zustand verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="89d44-119">The image list referred to in the **himl** member of the [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure should contain either a single image to be used for all states or individual images for each state.</span></span> <span data-ttu-id="89d44-120">Die folgenden Zustände sind in vssym32. h definiert.</span><span class="sxs-lookup"><span data-stu-id="89d44-120">The following states are defined in vssym32.h.</span></span>

``` syntax
enum PUSHBUTTONSTATES {
    PBS_NORMAL = 1,
    PBS_HOT = 2,
    PBS_PRESSED = 3,
    PBS_DISABLED = 4,
    PBS_DEFAULTED = 5,
    PBS_STYLUSHOT = 6,
};
```

<span data-ttu-id="89d44-121">Beachten Sie, dass PSB \_ stylushot nur auf Tablet-Computern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="89d44-121">Note that PBS\_STYLUSHOT is used only on tablet computers.</span></span>

<span data-ttu-id="89d44-122">Jeder Wert ist ein Index des entsprechenden Bilds in der Bildliste.</span><span class="sxs-lookup"><span data-stu-id="89d44-122">Each value is an index to the appropriate image in the image list.</span></span> <span data-ttu-id="89d44-123">Wenn nur ein Bild vorhanden ist, wird es für alle Zustände verwendet.</span><span class="sxs-lookup"><span data-stu-id="89d44-123">If only one image is present, it is used for all states.</span></span> <span data-ttu-id="89d44-124">Wenn die Bildliste mehr als ein Bild enthält, entspricht jeder Index einem Zustand der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="89d44-124">If the image list contains more than one image, each index corresponds to one state of the button.</span></span> <span data-ttu-id="89d44-125">Wenn für jeden Zustand kein Bild bereitgestellt wird, wird für diese Zustände ohne Bilder nichts gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="89d44-125">If an image is not provided for each state, nothing is drawn for those states without images.</span></span>

## <a name="requirements"></a><span data-ttu-id="89d44-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89d44-126">Requirements</span></span>



| <span data-ttu-id="89d44-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89d44-127">Requirement</span></span> | <span data-ttu-id="89d44-128">Wert</span><span class="sxs-lookup"><span data-stu-id="89d44-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89d44-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89d44-129">Minimum supported client</span></span><br/> | <span data-ttu-id="89d44-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89d44-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89d44-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89d44-131">Minimum supported server</span></span><br/> | <span data-ttu-id="89d44-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89d44-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89d44-133">Header</span><span class="sxs-lookup"><span data-stu-id="89d44-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="89d44-134"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="89d44-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





