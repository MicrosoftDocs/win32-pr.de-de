---
title: WM_DWMCOLORIZATIONCOLORCHANGED Meldung (Winuser. h)
description: Informiert alle Fenster der obersten Ebene darüber, dass sich die Farbe der Farbgebung geändert hat.
ms.assetid: 6118d41b-f0b4-4034-aa98-d8757f18ca0d
keywords:
- WM_DWMCOLORIZATIONCOLORCHANGED Meldung Desktopfenster-Manager
topic_type:
- apiref
api_name:
- WM_DWMCOLORIZATIONCOLORCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc99d42fe2d4af77fa4534945a3396dda9c02b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103941"
---
# <a name="wm_dwmcolorizationcolorchanged-message"></a><span data-ttu-id="9d4cf-104">WM \_ dwmcolorizationcolorchanged-Meldung</span><span class="sxs-lookup"><span data-stu-id="9d4cf-104">WM\_DWMCOLORIZATIONCOLORCHANGED message</span></span>

<span data-ttu-id="9d4cf-105">Informiert alle Fenster der obersten Ebene darüber, dass sich die Farbe der Farbgebung geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9d4cf-105">Informs all top-level windows that the colorization color has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="9d4cf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d4cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d4cf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d4cf-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d4cf-108">Gibt die neue farbliche Farbe an.</span><span class="sxs-lookup"><span data-stu-id="9d4cf-108">Specifies the new colorization color.</span></span> <span data-ttu-id="9d4cf-109">Das Farb Format ist 0xaarrggbb.</span><span class="sxs-lookup"><span data-stu-id="9d4cf-109">The color format is 0xAARRGGBB.</span></span>

</dd> <dt>

<span data-ttu-id="9d4cf-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d4cf-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d4cf-111">Gibt an, ob die neue Farbe mit Deckkraft gemischt wird.</span><span class="sxs-lookup"><span data-stu-id="9d4cf-111">Specifies whether the new color is blended with opacity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d4cf-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d4cf-112">Return value</span></span>

<span data-ttu-id="9d4cf-113">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9d4cf-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d4cf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d4cf-114">Remarks</span></span>

<span data-ttu-id="9d4cf-115">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="9d4cf-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="9d4cf-116">" [**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) " wird verwendet, um den aktuellen Farbwert zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="9d4cf-116">[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) is used to determine the current color value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d4cf-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d4cf-117">Requirements</span></span>



| <span data-ttu-id="9d4cf-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d4cf-118">Requirement</span></span> | <span data-ttu-id="9d4cf-119">Wert</span><span class="sxs-lookup"><span data-stu-id="9d4cf-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4cf-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d4cf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9d4cf-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d4cf-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9d4cf-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d4cf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9d4cf-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d4cf-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9d4cf-124">Header</span><span class="sxs-lookup"><span data-stu-id="9d4cf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d4cf-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d4cf-125"><dt>Winuser.h</dt></span></span> </dl> |



 

