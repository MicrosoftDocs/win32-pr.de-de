---
title: TB_HITTEST Meldung (kommstrg. h)
description: Bestimmt, wo sich ein Punkt in einem ToolBar-Steuerelement befindet.
ms.assetid: d08f3805-2042-470e-8f5a-8a6a681d1189
keywords:
- Windows-Steuerelemente für TB_HITTEST Meldung
topic_type:
- apiref
api_name:
- TB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6264bc0191f091d3819081ddd67e428b64c84570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949697"
---
# <a name="tb_hittest-message"></a><span data-ttu-id="940aa-104">TB- \_ HitTest-Meldung</span><span class="sxs-lookup"><span data-stu-id="940aa-104">TB\_HITTEST message</span></span>

<span data-ttu-id="940aa-105">Bestimmt, wo sich ein Punkt in einem ToolBar-Steuerelement befindet.</span><span class="sxs-lookup"><span data-stu-id="940aa-105">Determines where a point lies in a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="940aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="940aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="940aa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="940aa-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="940aa-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="940aa-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="940aa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="940aa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="940aa-110">Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur, die die x-Koordinate des Treffer Tests im **x** -Element und die y-Koordinate des Treffer Tests im **y** -Member enthält.</span><span class="sxs-lookup"><span data-stu-id="940aa-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that contains the x-coordinate of the hit test in the **x** member and the y-coordinate of the hit test in the **y** member.</span></span> <span data-ttu-id="940aa-111">Die Koordinaten sind relativ zum Client Bereich der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="940aa-111">The coordinates are relative to the toolbar's client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="940aa-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="940aa-112">Return value</span></span>

<span data-ttu-id="940aa-113">Gibt einen Ganzzahlwert zurück.</span><span class="sxs-lookup"><span data-stu-id="940aa-113">Returns an integer value.</span></span> <span data-ttu-id="940aa-114">Wenn der Rückgabewert 0 (null) oder ein positiver Wert ist, handelt es sich um den NULL basierten Index des nicht Trennzeichens, in dem sich der Punkt befindet.</span><span class="sxs-lookup"><span data-stu-id="940aa-114">If the return value is zero or a positive value, it is the zero-based index of the nonseparator item in which the point lies.</span></span> <span data-ttu-id="940aa-115">Wenn der Rückgabewert negativ ist, liegt der Punkt nicht innerhalb einer Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="940aa-115">If the return value is negative, the point does not lie within a button.</span></span> <span data-ttu-id="940aa-116">Der absolute Wert des Rückgabewerts ist der Index eines Trenn Zeichens oder das nächste nicht Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="940aa-116">The absolute value of the return value is the index of a separator item or the nearest nonseparator item.</span></span>

## <a name="requirements"></a><span data-ttu-id="940aa-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="940aa-117">Requirements</span></span>



| <span data-ttu-id="940aa-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="940aa-118">Requirement</span></span> | <span data-ttu-id="940aa-119">Wert</span><span class="sxs-lookup"><span data-stu-id="940aa-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="940aa-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="940aa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="940aa-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="940aa-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="940aa-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="940aa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="940aa-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="940aa-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="940aa-124">Header</span><span class="sxs-lookup"><span data-stu-id="940aa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="940aa-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="940aa-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

