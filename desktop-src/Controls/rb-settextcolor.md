---
title: RB_SETTEXTCOLOR Meldung (kommstrg. h)
description: Legt die Standard Textfarbe eines Grund leisten-Steuer Elements fest.
ms.assetid: 85f120bd-39aa-43f8-a794-3bb4f3fe1cd4
keywords:
- Windows-Steuerelemente für RB_SETTEXTCOLOR Meldung
topic_type:
- apiref
api_name:
- RB_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68311572927f2e8dac623c697ac366d37d7ab5fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477859"
---
# <a name="rb_settextcolor-message"></a><span data-ttu-id="e2857-104">RB \_ SetTextColor-Meldung</span><span class="sxs-lookup"><span data-stu-id="e2857-104">RB\_SETTEXTCOLOR message</span></span>

<span data-ttu-id="e2857-105">Legt die Standard Textfarbe eines Grund leisten-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="e2857-105">Sets a rebar control's default text color.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2857-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2857-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2857-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2857-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e2857-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="e2857-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e2857-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2857-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2857-110">[**COLORREF**](/windows/desktop/gdi/colorref) -Wert, der die neue Standard Textfarbe darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2857-110">[**COLORREF**](/windows/desktop/gdi/colorref) value that represents the new default text color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2857-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2857-111">Return value</span></span>

<span data-ttu-id="e2857-112">Gibt einen [**COLORREF**](/windows/desktop/gdi/colorref) -Wert zurück, der die vorherige Standard Textfarbe darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2857-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that represents the previous default text color.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2857-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2857-113">Remarks</span></span>

<span data-ttu-id="e2857-114">Die Standard Textfarbe des Grund leisten-Steuer Elements wird verwendet, um den Text in einem Grund leisten-Steuerelement und alle Bänder zu zeichnen, die nach dem Senden dieser Nachricht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e2857-114">The rebar control's default text color is used to draw the text in a rebar control and all bands that are added after this message has been sent.</span></span> <span data-ttu-id="e2857-115">Die Standard Textfarbe für ein bestimmtes Band kann überschrieben werden, wenn ein Band hinzugefügt oder geändert wird, indem das Flag rbbim \_ Colors in der Datei **Maske** festgelegt und **clrback** in der [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e2857-115">The default text color for a particular band can be overridden when a band is added or modified by setting the RBBIM\_COLORS flag in **fMask** and setting **clrBack** in the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2857-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2857-116">Requirements</span></span>



| <span data-ttu-id="e2857-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2857-117">Requirement</span></span> | <span data-ttu-id="e2857-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e2857-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2857-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2857-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e2857-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2857-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2857-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2857-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e2857-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2857-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2857-123">Header</span><span class="sxs-lookup"><span data-stu-id="e2857-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2857-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2857-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2857-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2857-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2857-126">**RB \_ gettextcolor**</span><span class="sxs-lookup"><span data-stu-id="e2857-126">**RB\_GETTEXTCOLOR**</span></span>](rb-gettextcolor.md)
</dt> </dl>

 

