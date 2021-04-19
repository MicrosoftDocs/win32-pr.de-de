---
title: TCM_ADJUSTRECT Meldung (kommstrg. h)
description: Berechnet den Anzeigebereich eines Registerkarten-Steuer Elements bei Angabe eines Fenster Rechtecks oder berechnet das Fenster Rechteck, das einem angegebenen Anzeigebereich entsprechen würde. Sie können diese Nachricht explizit oder mithilfe des tabstrg-Elements "tabctrl" senden \_ .
ms.assetid: 2f14201a-e4a3-4ae5-b9cf-4a674c52f24a
keywords:
- Windows-Steuerelemente für TCM_ADJUSTRECT Meldung
topic_type:
- apiref
api_name:
- TCM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c1612a4f6c2fc436f858807fca59112c376a35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342871"
---
# <a name="tcm_adjustrect-message"></a><span data-ttu-id="94068-105">TCM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="94068-105">TCM\_ADJUSTRECT message</span></span>

<span data-ttu-id="94068-106">Berechnet den Anzeigebereich eines Registerkarten-Steuer Elements bei Angabe eines Fenster Rechtecks oder berechnet das Fenster Rechteck, das einem angegebenen Anzeigebereich entsprechen würde.</span><span class="sxs-lookup"><span data-stu-id="94068-106">Calculates a tab control's display area given a window rectangle, or calculates the window rectangle that would correspond to a specified display area.</span></span> <span data-ttu-id="94068-107">Sie können diese Nachricht explizit oder mithilfe des [**tabstrg-Elements \_ "tabctrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) " senden.</span><span class="sxs-lookup"><span data-stu-id="94068-107">You can send this message explicitly or by using the [**TabCtrl\_AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="94068-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="94068-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94068-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="94068-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94068-110">Der auszuführende Vorgang.</span><span class="sxs-lookup"><span data-stu-id="94068-110">Operation to perform.</span></span> <span data-ttu-id="94068-111">Wenn dieser Parameter auf **true** festgelegt ist, gibt *LPARAM* ein Anzeige Rechteck an und empfängt das entsprechende Fenster Rechteck.</span><span class="sxs-lookup"><span data-stu-id="94068-111">If this parameter is **TRUE**, *lParam* specifies a display rectangle and receives the corresponding window rectangle.</span></span> <span data-ttu-id="94068-112">Wenn dieser Parameter auf **false** festgelegt ist, gibt *LPARAM* ein Fenster Rechteck an und empfängt den entsprechenden Anzeigebereich.</span><span class="sxs-lookup"><span data-stu-id="94068-112">If this parameter is **FALSE**, *lParam* specifies a window rectangle and receives the corresponding display area.</span></span>

</dd> <dt>

<span data-ttu-id="94068-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="94068-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="94068-114">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das angegebene Rechteck angibt und das berechnete Rechteck empfängt.</span><span class="sxs-lookup"><span data-stu-id="94068-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the given rectangle and receives the calculated rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94068-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94068-115">Return value</span></span>

<span data-ttu-id="94068-116">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="94068-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="94068-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94068-117">Remarks</span></span>

<span data-ttu-id="94068-118">Diese Meldung gilt nur für Registerkarten-Steuerelemente, die sich im oberen Bereich befinden.</span><span class="sxs-lookup"><span data-stu-id="94068-118">This message applies only to tab controls that are at the top.</span></span> <span data-ttu-id="94068-119">Es gilt nicht für Registerkarten-Steuerelemente, die sich auf der Seite oder im unteren Bereich befinden.</span><span class="sxs-lookup"><span data-stu-id="94068-119">It does not apply to tab controls that are on the sides or bottom.</span></span>

## <a name="requirements"></a><span data-ttu-id="94068-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94068-120">Requirements</span></span>



| <span data-ttu-id="94068-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94068-121">Requirement</span></span> | <span data-ttu-id="94068-122">Wert</span><span class="sxs-lookup"><span data-stu-id="94068-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94068-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94068-123">Minimum supported client</span></span><br/> | <span data-ttu-id="94068-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94068-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="94068-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94068-125">Minimum supported server</span></span><br/> | <span data-ttu-id="94068-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94068-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="94068-127">Header</span><span class="sxs-lookup"><span data-stu-id="94068-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="94068-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="94068-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

