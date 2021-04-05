---
title: TB_SETCOLORSCHEME Meldung (kommstrg. h)
description: Legt die Farbschema Informationen für das Symbolleisten-Steuerelement fest.
ms.assetid: 96cf6464-b760-46af-910f-984e41dbfca5
keywords:
- Windows-Steuerelemente für TB_SETCOLORSCHEME Meldung
topic_type:
- apiref
api_name:
- TB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ed278ea31dfa156dcc8a64afdb98a2ae3b938
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859240"
---
# <a name="tb_setcolorscheme-message"></a><span data-ttu-id="3cf4f-104">TB \_ SetColorScheme-Meldung</span><span class="sxs-lookup"><span data-stu-id="3cf4f-104">TB\_SETCOLORSCHEME message</span></span>

<span data-ttu-id="3cf4f-105">Legt die Farbschema Informationen für das Symbolleisten-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="3cf4f-105">Sets the color scheme information for the toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3cf4f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cf4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cf4f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3cf4f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3cf4f-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="3cf4f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3cf4f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3cf4f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3cf4f-110">Zeiger auf eine [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) -Struktur, die die Farbschema Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="3cf4f-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that contains the color scheme information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cf4f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3cf4f-111">Return value</span></span>

<span data-ttu-id="3cf4f-112">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3cf4f-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cf4f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3cf4f-113">Remarks</span></span>

<span data-ttu-id="3cf4f-114">Das Symbolleisten-Steuerelement verwendet beim Zeichnen der 3D-Elemente im-Steuerelement die Farbschema Informationen.</span><span class="sxs-lookup"><span data-stu-id="3cf4f-114">The toolbar control uses the color scheme information when drawing the 3-D elements in the control.</span></span>

<span data-ttu-id="3cf4f-115">Wenn visuelle Stile aktiviert sind, hat diese Nachricht keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="3cf4f-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cf4f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cf4f-116">Requirements</span></span>



| <span data-ttu-id="3cf4f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3cf4f-117">Requirement</span></span> | <span data-ttu-id="3cf4f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3cf4f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf4f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3cf4f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3cf4f-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3cf4f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3cf4f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3cf4f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3cf4f-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3cf4f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3cf4f-123">Header</span><span class="sxs-lookup"><span data-stu-id="3cf4f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cf4f-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cf4f-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cf4f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cf4f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cf4f-126">**TB \_ getcolorscheme**</span><span class="sxs-lookup"><span data-stu-id="3cf4f-126">**TB\_GETCOLORSCHEME**</span></span>](tb-getcolorscheme.md)
</dt> </dl>

 

 





