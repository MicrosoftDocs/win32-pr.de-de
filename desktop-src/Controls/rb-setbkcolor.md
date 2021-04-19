---
title: RB_SETBKCOLOR Meldung (kommstrg. h)
description: Legt die Standard Hintergrundfarbe eines Grund leisten-Steuer Elements fest.
ms.assetid: 450a1e16-24f6-4f86-8e46-14009da05efc
keywords:
- Windows-Steuerelemente für RB_SETBKCOLOR Meldung
topic_type:
- apiref
api_name:
- RB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9365de2d790b1f28b1330c038b69d30b208143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345303"
---
# <a name="rb_setbkcolor-message"></a><span data-ttu-id="0485b-104">RB- \_ SetBkColor-Meldung</span><span class="sxs-lookup"><span data-stu-id="0485b-104">RB\_SETBKCOLOR message</span></span>

<span data-ttu-id="0485b-105">Legt die Standard Hintergrundfarbe eines Grund leisten-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="0485b-105">Sets a rebar control's default background color.</span></span>

## <a name="parameters"></a><span data-ttu-id="0485b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0485b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0485b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0485b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0485b-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="0485b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0485b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0485b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0485b-110">[**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der die neue Standard Hintergrundfarbe darstellt.</span><span class="sxs-lookup"><span data-stu-id="0485b-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the new default background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0485b-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0485b-111">Return value</span></span>

<span data-ttu-id="0485b-112">Gibt einen [**COLORREF**](/windows/desktop/gdi/colorref) -Wert zurück, der die vorherige Standard Hintergrundfarbe darstellt.</span><span class="sxs-lookup"><span data-stu-id="0485b-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous default background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="0485b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0485b-113">Remarks</span></span>

<span data-ttu-id="0485b-114">Die Standard Hintergrundfarbe des Grund leisten-Steuer Elements wird verwendet, um den Hintergrund in einem Grund leisten-Steuerelement und alle Bänder zu zeichnen, die nach dem Senden dieser Nachricht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0485b-114">The rebar control's default background color is used to draw the background in a rebar control and all bands that are added after this message has been sent.</span></span> <span data-ttu-id="0485b-115">Die Standard Hintergrundfarbe für ein bestimmtes Band kann überschrieben werden, wenn ein Band hinzugefügt oder geändert wird, indem das Flag rbbim \_ Colors in der Datei **Maske** **festgelegt** und in der [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="0485b-115">The default background color for a particular band can be overridden when a band is added or modified by setting the RBBIM\_COLORS flag in **fMask** and setting **clrBack** in the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure.</span></span>

<span data-ttu-id="0485b-116">Wenn visuelle Stile aktiviert sind, hat diese Nachricht keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="0485b-116">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="0485b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0485b-117">Requirements</span></span>



| <span data-ttu-id="0485b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0485b-118">Requirement</span></span> | <span data-ttu-id="0485b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0485b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0485b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0485b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0485b-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0485b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0485b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0485b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0485b-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0485b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0485b-124">Header</span><span class="sxs-lookup"><span data-stu-id="0485b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0485b-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0485b-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0485b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0485b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0485b-127">**RB \_ GetBkColor**</span><span class="sxs-lookup"><span data-stu-id="0485b-127">**RB\_GETBKCOLOR**</span></span>](rb-getbkcolor.md)
</dt> </dl>

 

