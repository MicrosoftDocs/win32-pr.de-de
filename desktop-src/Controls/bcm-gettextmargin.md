---
title: BCM_GETTEXTMARGIN Meldung (kommstrg. h)
description: Ruft die Ränder ab, mit denen Text in einem Schaltflächen-Steuerelement gezeichnet wird. Sie können diese Nachricht explizit senden oder das gettextmargin-Makro der Schaltfläche verwenden \_ .
ms.assetid: 6c141752-e636-41c4-9d05-df8b320ff59f
keywords:
- Windows-Steuerelemente für BCM_GETTEXTMARGIN Meldung
topic_type:
- apiref
api_name:
- BCM_GETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6a7d809207c21c74a36c796a9035ed0e3772481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949779"
---
# <a name="bcm_gettextmargin-message"></a><span data-ttu-id="f3b28-105">BCM \_ gettextmargin-Meldung</span><span class="sxs-lookup"><span data-stu-id="f3b28-105">BCM\_GETTEXTMARGIN message</span></span>

<span data-ttu-id="f3b28-106">Ruft die Ränder ab, mit denen Text in einem Schaltflächen-Steuerelement gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="f3b28-106">Gets the margins used to draw text in a button control.</span></span> <span data-ttu-id="f3b28-107">Sie können diese Nachricht explizit senden oder das [**\_ gettextmargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) -Makro der Schaltfläche verwenden.</span><span class="sxs-lookup"><span data-stu-id="f3b28-107">You can send this message explicitly or use the [**Button\_GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3b28-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3b28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3b28-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3b28-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3b28-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="f3b28-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f3b28-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3b28-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3b28-112">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Ränder enthält, die zum Zeichnen von Text verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f3b28-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the margins to use for drawing text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3b28-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3b28-113">Return value</span></span>

<span data-ttu-id="f3b28-114">Wenn die Nachricht erfolgreich ist, wird **true** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f3b28-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="f3b28-115">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f3b28-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3b28-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3b28-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f3b28-117">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="f3b28-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="f3b28-118">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f3b28-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f3b28-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3b28-119">Requirements</span></span>



| <span data-ttu-id="f3b28-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3b28-120">Requirement</span></span> | <span data-ttu-id="f3b28-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f3b28-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b28-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3b28-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f3b28-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3b28-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f3b28-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3b28-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f3b28-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f3b28-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3b28-126">Header</span><span class="sxs-lookup"><span data-stu-id="f3b28-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3b28-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3b28-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

