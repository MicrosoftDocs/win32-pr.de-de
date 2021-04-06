---
title: PGM_GETBKCOLOR Meldung (kommstrg. h)
description: Ruft die aktuelle Hintergrundfarbe für das Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das Pager- \_ GetBkColor-Makro verwenden.
ms.assetid: c39ad721-fe39-44e9-8305-67444acc5d65
keywords:
- Windows-Steuerelemente für PGM_GETBKCOLOR Meldung
topic_type:
- apiref
api_name:
- PGM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b58b139dd1caafcdefc6893e2b8a5e3312d3e28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742528"
---
# <a name="pgm_getbkcolor-message"></a><span data-ttu-id="31ca5-105">PGM \_ GetBkColor-Nachricht</span><span class="sxs-lookup"><span data-stu-id="31ca5-105">PGM\_GETBKCOLOR message</span></span>

<span data-ttu-id="31ca5-106">Ruft die aktuelle Hintergrundfarbe für das Pager-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="31ca5-106">Retrieves the current background color for the pager control.</span></span> <span data-ttu-id="31ca5-107">Sie können diese Nachricht explizit senden oder das [**Pager- \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="31ca5-107">You can send this message explicitly or use the [**Pager\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="31ca5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="31ca5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31ca5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31ca5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="31ca5-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="31ca5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="31ca5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31ca5-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="31ca5-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="31ca5-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31ca5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31ca5-113">Return value</span></span>

<span data-ttu-id="31ca5-114">Gibt einen **COLORREF** -Wert zurück, der die aktuelle Hintergrundfarbe enthält.</span><span class="sxs-lookup"><span data-stu-id="31ca5-114">Returns a **COLORREF** value that contains the current background color.</span></span>

## <a name="remarks"></a><span data-ttu-id="31ca5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31ca5-115">Remarks</span></span>

<span data-ttu-id="31ca5-116">Standardmäßig verwendet das Pager-Steuerelement die Vordergrundfarbe der System Schaltfläche als Hintergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="31ca5-116">By default, the pager control will use the system button face color as the background color.</span></span> <span data-ttu-id="31ca5-117">Dies ist die gleiche Farbe, die durch den Aufruf von [**getsyscolorbrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) mit Color \_ btnface abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="31ca5-117">This is the same color that can be retrieved by calling [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) with COLOR\_BTNFACE.</span></span>

## <a name="requirements"></a><span data-ttu-id="31ca5-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31ca5-118">Requirements</span></span>



| <span data-ttu-id="31ca5-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31ca5-119">Requirement</span></span> | <span data-ttu-id="31ca5-120">Wert</span><span class="sxs-lookup"><span data-stu-id="31ca5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31ca5-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31ca5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="31ca5-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31ca5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="31ca5-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31ca5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="31ca5-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31ca5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="31ca5-125">Header</span><span class="sxs-lookup"><span data-stu-id="31ca5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="31ca5-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="31ca5-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

