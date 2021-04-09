---
title: MCM_GETMAXTODAYWIDTH Meldung (kommstrg. h)
description: Ruft die maximale Breite von \ 0034; heute \ 0034; ab. Zeichenfolge in einem Monatskalender-Steuerelement. Dies schließt den Beschriftungs Text und den Datums Text ein. Sie können diese Nachricht explizit oder mit dem monthcal \_ getmaxredaywidth-Makro senden.
ms.assetid: bb55c24e-ba04-4a57-97b0-ff04d77e1d43
keywords:
- Windows-Steuerelemente für MCM_GETMAXTODAYWIDTH Meldung
topic_type:
- apiref
api_name:
- MCM_GETMAXTODAYWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2b4c188e994a1dcc5a8fbd80ae3f1b06894bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741817"
---
# <a name="mcm_getmaxtodaywidth-message"></a><span data-ttu-id="f701f-106">MCM \_ getMax| Day Width-Meldung</span><span class="sxs-lookup"><span data-stu-id="f701f-106">MCM\_GETMAXTODAYWIDTH message</span></span>

<span data-ttu-id="f701f-107">Ruft die maximale Breite der "heute"-Zeichenfolge in einem Monatskalender-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="f701f-107">Retrieves the maximum width of the "today" string in a month calendar control.</span></span> <span data-ttu-id="f701f-108">Dies schließt den Beschriftungs Text und den Datums Text ein.</span><span class="sxs-lookup"><span data-stu-id="f701f-108">This includes the label text and the date text.</span></span> <span data-ttu-id="f701f-109">Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getmaxredaywidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="f701f-109">You can send this message explicitly or by using the [**MonthCal\_GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f701f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f701f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f701f-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f701f-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f701f-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f701f-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f701f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f701f-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f701f-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f701f-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f701f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f701f-115">Return value</span></span>

<span data-ttu-id="f701f-116">Gibt die Breite der "Today"-Zeichenfolge in Pixel zurück.</span><span class="sxs-lookup"><span data-stu-id="f701f-116">Returns the width of the "today" string, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="f701f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f701f-117">Requirements</span></span>



| <span data-ttu-id="f701f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f701f-118">Requirement</span></span> | <span data-ttu-id="f701f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f701f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f701f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f701f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f701f-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f701f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f701f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f701f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f701f-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f701f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f701f-124">Header</span><span class="sxs-lookup"><span data-stu-id="f701f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f701f-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f701f-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





