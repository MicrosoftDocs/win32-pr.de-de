---
title: TTM_SETWINDOWTHEME Meldung (kommstrg. h)
description: Legt den visuellen Stil eines QuickInfo-Steuer Elements fest.
ms.assetid: eeddb91e-8eb8-4480-9ab2-5efa9e3ef48a
keywords:
- Windows-Steuerelemente für TTM_SETWINDOWTHEME Meldung
topic_type:
- apiref
api_name:
- TTM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9c3f25b62bf0fe38a679234183cd5046f60784f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518863"
---
# <a name="ttm_setwindowtheme-message"></a><span data-ttu-id="e06b6-104">TTM- \_ SetWindowTheme-Meldung</span><span class="sxs-lookup"><span data-stu-id="e06b6-104">TTM\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="e06b6-105">Legt den visuellen Stil eines QuickInfo-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="e06b6-105">Sets the visual style of a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e06b6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e06b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e06b6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e06b6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e06b6-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e06b6-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e06b6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e06b6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e06b6-110">Zeiger auf eine Unicode-Zeichenfolge, die den festzulegenden visuellen QuickInfo-Stil enthält.</span><span class="sxs-lookup"><span data-stu-id="e06b6-110">Pointer to a Unicode string that contains the tooltip visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e06b6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e06b6-111">Return value</span></span>

<span data-ttu-id="e06b6-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e06b6-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e06b6-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e06b6-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e06b6-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="e06b6-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="e06b6-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e06b6-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e06b6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e06b6-116">Requirements</span></span>



| <span data-ttu-id="e06b6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e06b6-117">Requirement</span></span> | <span data-ttu-id="e06b6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e06b6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e06b6-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e06b6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e06b6-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e06b6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e06b6-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e06b6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e06b6-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e06b6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e06b6-123">Header</span><span class="sxs-lookup"><span data-stu-id="e06b6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e06b6-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e06b6-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





