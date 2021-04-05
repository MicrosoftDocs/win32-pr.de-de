---
title: EM_SETBKGNDCOLOR Meldung (RichEdit. h)
description: Die "em \_ setbkgndcolor"-Meldung legt die Hintergrundfarbe für ein Rich-Edit-Steuerelement fest.
ms.assetid: 0ad191cd-6370-493e-bfe2-5aa8d81ed999
keywords:
- Windows-Steuerelemente für EM_SETBKGNDCOLOR Meldung
topic_type:
- apiref
api_name:
- EM_SETBKGNDCOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091f04909e2660498f1380628439c067b5438b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859174"
---
# <a name="em_setbkgndcolor-message"></a><span data-ttu-id="8bb4e-104">EM \_ setbkgndcolor-Meldung</span><span class="sxs-lookup"><span data-stu-id="8bb4e-104">EM\_SETBKGNDCOLOR message</span></span>

<span data-ttu-id="8bb4e-105">Die " **EM \_ setbkgndcolor** "-Meldung legt die Hintergrundfarbe für ein Rich-Edit-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="8bb4e-105">The **EM\_SETBKGNDCOLOR** message sets the background color for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8bb4e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bb4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bb4e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8bb4e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8bb4e-108">Gibt an, ob die System Farbe verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8bb4e-108">Specifies whether to use the system color.</span></span> <span data-ttu-id="8bb4e-109">Wenn dieser Parameter ein Wert ungleich 0 (null) ist, wird der Hintergrund auf die Hintergrundsystem Farbe des Fensters festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8bb4e-109">If this parameter is a nonzero value, the background is set to the window background system color.</span></span> <span data-ttu-id="8bb4e-110">Andernfalls wird der Hintergrund auf die angegebene Farbe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8bb4e-110">Otherwise, the background is set to the specified color.</span></span>

</dd> <dt>

<span data-ttu-id="8bb4e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8bb4e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8bb4e-112">Eine [**COLORREF**](/windows/desktop/gdi/colorref) -Struktur, die die Farbe angibt, wenn *wParam* NULL ist.</span><span class="sxs-lookup"><span data-stu-id="8bb4e-112">A [**COLORREF**](/windows/desktop/gdi/colorref) structure specifying the color if *wParam* is zero.</span></span> <span data-ttu-id="8bb4e-113">Verwenden Sie zum Generieren eines **COLORREF** das [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) -Makro.</span><span class="sxs-lookup"><span data-stu-id="8bb4e-113">To generate a **COLORREF**, use the [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bb4e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8bb4e-114">Return value</span></span>

<span data-ttu-id="8bb4e-115">Diese Meldung gibt die ursprüngliche Hintergrundfarbe zurück.</span><span class="sxs-lookup"><span data-stu-id="8bb4e-115">This message returns the original background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb4e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8bb4e-116">Requirements</span></span>



| <span data-ttu-id="8bb4e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8bb4e-117">Requirement</span></span> | <span data-ttu-id="8bb4e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8bb4e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb4e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8bb4e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8bb4e-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8bb4e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8bb4e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8bb4e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8bb4e-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8bb4e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8bb4e-123">Header</span><span class="sxs-lookup"><span data-stu-id="8bb4e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bb4e-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bb4e-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bb4e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8bb4e-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="8bb4e-126">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="8bb4e-126">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8bb4e-127">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="8bb4e-127">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> <dt>

[<span data-ttu-id="8bb4e-128">**RGB**</span><span class="sxs-lookup"><span data-stu-id="8bb4e-128">**RGB**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> </dl>

 

