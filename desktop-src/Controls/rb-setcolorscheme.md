---
title: RB_SETCOLORSCHEME Meldung (kommstrg. h)
description: Legt die Farbschema Informationen für das Grund leisten-Steuerelement fest.
ms.assetid: ddf8f3e4-66b7-4b53-a04e-b4dd372f71c4
keywords:
- Windows-Steuerelemente für RB_SETCOLORSCHEME Meldung
topic_type:
- apiref
api_name:
- RB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9c7725d3c0bc3f3a7a7a72db16e19626a3c4d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517963"
---
# <a name="rb_setcolorscheme-message"></a><span data-ttu-id="8ae0e-104">RB \_ SetColorScheme-Meldung</span><span class="sxs-lookup"><span data-stu-id="8ae0e-104">RB\_SETCOLORSCHEME message</span></span>

<span data-ttu-id="8ae0e-105">Legt die Farbschema Informationen für das Grund leisten-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="8ae0e-105">Sets the color scheme information for the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8ae0e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ae0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ae0e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ae0e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8ae0e-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="8ae0e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8ae0e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ae0e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae0e-110">Zeiger auf eine [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) -Struktur, die die Farbschema Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="8ae0e-110">Pointer to a [**COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) structure that contains the color scheme information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ae0e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ae0e-111">Return value</span></span>

<span data-ttu-id="8ae0e-112">Der Rückgabewert für diese Nachricht wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ae0e-112">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ae0e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ae0e-113">Remarks</span></span>

<span data-ttu-id="8ae0e-114">Das Grund leisten-Steuerelement verwendet die Farbschema Informationen beim Zeichnen der 3D-Elemente im Steuerelement und den Bändern.</span><span class="sxs-lookup"><span data-stu-id="8ae0e-114">The rebar control uses the color scheme information when drawing the 3-D elements in the control and bands.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ae0e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ae0e-115">Requirements</span></span>



| <span data-ttu-id="8ae0e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ae0e-116">Requirement</span></span> | <span data-ttu-id="8ae0e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8ae0e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae0e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ae0e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8ae0e-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ae0e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8ae0e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ae0e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8ae0e-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ae0e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8ae0e-122">Header</span><span class="sxs-lookup"><span data-stu-id="8ae0e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ae0e-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ae0e-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ae0e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ae0e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ae0e-125">**RB \_ getcolorscheme**</span><span class="sxs-lookup"><span data-stu-id="8ae0e-125">**RB\_GETCOLORSCHEME**</span></span>](rb-getcolorscheme.md)
</dt> </dl>

 

 





