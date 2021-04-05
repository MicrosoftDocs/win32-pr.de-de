---
title: PBM_GETBKCOLOR Meldung (kommstrg. h)
description: Ruft die Hintergrundfarbe der Statusanzeige ab.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- Windows-Steuerelemente für PBM_GETBKCOLOR Meldung
topic_type:
- apiref
api_name:
- PBM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2240025629bbcc242ea7ed47be2e3db42ae73b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859074"
---
# <a name="pbm_getbkcolor-message"></a><span data-ttu-id="e32de-104">PBM \_ GetBkColor-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e32de-104">PBM\_GETBKCOLOR message</span></span>

<span data-ttu-id="e32de-105">Ruft die Hintergrundfarbe der Statusanzeige ab.</span><span class="sxs-lookup"><span data-stu-id="e32de-105">Gets the background color of the progress bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="e32de-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e32de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e32de-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e32de-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e32de-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e32de-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e32de-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e32de-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e32de-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e32de-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e32de-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e32de-111">Return value</span></span>

<span data-ttu-id="e32de-112">Gibt die Hintergrundfarbe der Statusanzeige zurück.</span><span class="sxs-lookup"><span data-stu-id="e32de-112">Returns the background color of the progress bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="e32de-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e32de-113">Remarks</span></span>

<span data-ttu-id="e32de-114">Dies ist die Farbe, die von der [**PBM- \_ SetBkColor**](pbm-setbkcolor.md) -Nachricht festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e32de-114">This is the color set by the [**PBM\_SETBKCOLOR**](pbm-setbkcolor.md) message.</span></span> <span data-ttu-id="e32de-115">Der Standardwert ist CLR \_ Default, der in "kommctrl. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e32de-115">The default value is CLR\_DEFAULT, which is defined in commctrl.h.</span></span>

<span data-ttu-id="e32de-116">Diese Funktion wirkt sich nur auf den klassischen Modus aus, nicht auf einen visuellen Stil.</span><span class="sxs-lookup"><span data-stu-id="e32de-116">This function only affects the classic mode, not any visual style.</span></span>

## <a name="requirements"></a><span data-ttu-id="e32de-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e32de-117">Requirements</span></span>



| <span data-ttu-id="e32de-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e32de-118">Requirement</span></span> | <span data-ttu-id="e32de-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e32de-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e32de-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e32de-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e32de-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e32de-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e32de-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e32de-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e32de-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e32de-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e32de-124">Header</span><span class="sxs-lookup"><span data-stu-id="e32de-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e32de-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e32de-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





