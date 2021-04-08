---
title: CBEM_SETIMAGELIST Meldung (kommstrg. h)
description: Legt eine Bildliste für ein ComboBoxEx-Steuerelement fest.
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- Windows-Steuerelemente für CBEM_SETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- CBEM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33816abe36e2d1e1593e6365061a500d072c155b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957109"
---
# <a name="cbem_setimagelist-message"></a><span data-ttu-id="56da9-104">CBEM \_ SetImageList-Meldung</span><span class="sxs-lookup"><span data-stu-id="56da9-104">CBEM\_SETIMAGELIST message</span></span>

<span data-ttu-id="56da9-105">Legt eine Bildliste für ein ComboBoxEx-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="56da9-105">Sets an image list for a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="56da9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56da9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56da9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56da9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="56da9-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="56da9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="56da9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56da9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56da9-110">Ein Handle für die Bildliste, die für das-Steuerelement festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="56da9-110">A handle to the image list to be set for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56da9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56da9-111">Return value</span></span>

<span data-ttu-id="56da9-112">Gibt das Handle für die Bildliste zurück, die dem Steuerelement zuvor zugeordnet ist, oder gibt **null** zurück, wenn zuvor keine Bildliste festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="56da9-112">Returns the handle to the image list previously associated with the control, or returns **NULL** if no image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="56da9-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56da9-113">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="56da9-114">Die Höhe der Bilder in der Bildliste kann die Größenanforderungen des ComboBoxEx-Steuer Elements ändern.</span><span class="sxs-lookup"><span data-stu-id="56da9-114">The height of images in your image list might change the size requirements of the ComboBoxEx control.</span></span> <span data-ttu-id="56da9-115">Es wird empfohlen, die Größe des Steuer Elements nach dem Senden dieser Nachricht zu ändern, um sicherzustellen, dass Sie ordnungsgemäß angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="56da9-115">It is recommended that you resize the control after sending this message to ensure that it is displayed properly.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="56da9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56da9-116">Requirements</span></span>



| <span data-ttu-id="56da9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56da9-117">Requirement</span></span> | <span data-ttu-id="56da9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="56da9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56da9-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56da9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="56da9-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56da9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56da9-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56da9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="56da9-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56da9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56da9-123">Header</span><span class="sxs-lookup"><span data-stu-id="56da9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="56da9-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="56da9-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





