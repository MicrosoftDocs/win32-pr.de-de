---
title: BCM_GETIMAGELIST Meldung (kommstrg. h)
description: Ruft die ImageList-Struktur der Schaltfläche ab \_ , die die einem Schaltflächen-Steuerelement zugewiesene Bildliste beschreibt. Sie können diese Nachricht explizit senden oder das \_ GetImageList-Makro der Schaltfläche verwenden.
ms.assetid: 79383758-53d4-4955-b472-befd338cbec6
keywords:
- Windows-Steuerelemente für BCM_GETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- BCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c28e997e23d6df63150fe2283d04be1a8c0d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476995"
---
# <a name="bcm_getimagelist-message"></a><span data-ttu-id="d2935-105">BCM \_ GetImageList-Meldung</span><span class="sxs-lookup"><span data-stu-id="d2935-105">BCM\_GETIMAGELIST message</span></span>

<span data-ttu-id="d2935-106">Ruft die [**\_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) -Struktur der Schaltfläche ab, die die einem Schaltflächen-Steuerelement zugewiesene Bildliste beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d2935-106">Gets the [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that describes the image list assigned to a button control.</span></span> <span data-ttu-id="d2935-107">Sie können diese Nachricht explizit senden oder das [**\_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) -Makro der Schaltfläche verwenden.</span><span class="sxs-lookup"><span data-stu-id="d2935-107">You can send this message explicitly or use the [**Button\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2935-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2935-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2935-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2935-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2935-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="d2935-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d2935-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2935-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2935-112">Ein Zeiger auf eine [**Schaltflächen- \_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) -Struktur, die Bildlisten Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="d2935-112">A pointer to a [**BUTTON\_IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) structure that contains image list information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2935-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2935-113">Return value</span></span>

<span data-ttu-id="d2935-114">Wenn die Nachricht erfolgreich ist, wird **true** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d2935-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="d2935-115">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d2935-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2935-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2935-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d2935-117">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="d2935-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d2935-118">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d2935-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d2935-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2935-119">Requirements</span></span>



| <span data-ttu-id="d2935-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2935-120">Requirement</span></span> | <span data-ttu-id="d2935-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d2935-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2935-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2935-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d2935-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2935-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2935-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2935-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d2935-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2935-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2935-126">Header</span><span class="sxs-lookup"><span data-stu-id="d2935-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2935-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2935-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





