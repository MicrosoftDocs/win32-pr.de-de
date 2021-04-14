---
title: TBM_SETTOOLTIPS Meldung (kommstrg. h)
description: Weist einem TrackBar-Steuerelement ein QuickInfo-Steuerelement zu.
ms.assetid: 9bba1084-d04e-4631-a5cc-408849a14eb1
keywords:
- Windows-Steuerelemente für TBM_SETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- TBM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d60c7e108db926b85e7d9e1167f33c1ed807a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475909"
---
# <a name="tbm_settooltips-message"></a><span data-ttu-id="1b182-104">TBM- \_ SetToolTips-Meldung</span><span class="sxs-lookup"><span data-stu-id="1b182-104">TBM\_SETTOOLTIPS message</span></span>

<span data-ttu-id="1b182-105">Weist einem TrackBar-Steuerelement ein QuickInfo-Steuerelement zu.</span><span class="sxs-lookup"><span data-stu-id="1b182-105">Assigns a tooltip control to a trackbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b182-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b182-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b182-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b182-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b182-108">Handle für ein vorhandenes QuickInfo-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="1b182-108">Handle to an existing tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="1b182-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b182-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1b182-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="1b182-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b182-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b182-111">Return value</span></span>

<span data-ttu-id="1b182-112">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1b182-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b182-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b182-113">Remarks</span></span>

<span data-ttu-id="1b182-114">Beim Erstellen eines TrackBar-Steuer Elements mit dem [**TPS- \_ Tooltips**](trackbar-control-styles.md) -Stil wird ein Standardmäßiges QuickInfo-Steuerelement erstellt, das neben dem Schieberegler angezeigt wird und die aktuelle Position des Schiebereglers anzeigt.</span><span class="sxs-lookup"><span data-stu-id="1b182-114">When a trackbar control is created with the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style, it creates a default tooltip control that appears next to the slider, displaying the slider's current position.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b182-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b182-115">Requirements</span></span>



| <span data-ttu-id="1b182-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b182-116">Requirement</span></span> | <span data-ttu-id="1b182-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1b182-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b182-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b182-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1b182-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b182-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b182-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b182-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1b182-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b182-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b182-122">Header</span><span class="sxs-lookup"><span data-stu-id="1b182-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b182-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b182-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





