---
title: MCM_GETUNICODEFORMAT Meldung (kommstrg. h)
description: Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab. Sie können diese Nachricht explizit senden oder das monthcal \_ getunicodeformat-Makro verwenden.
ms.assetid: 28261e11-0fd0-407e-9f62-446536d62460
keywords:
- Windows-Steuerelemente für MCM_GETUNICODEFORMAT Meldung
topic_type:
- apiref
api_name:
- MCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4be573923f154958e1defd0be2adb02068076950
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743576"
---
# <a name="mcm_getunicodeformat-message"></a><span data-ttu-id="f2629-105">MCM \_ getunicodeformat-Meldung</span><span class="sxs-lookup"><span data-stu-id="f2629-105">MCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="f2629-106">Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="f2629-106">Retrieves the Unicode character format flag for the control.</span></span> <span data-ttu-id="f2629-107">Sie können diese Nachricht explizit senden oder das [**monthcal \_ getunicodeformat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getunicodeformat) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2629-107">You can send this message explicitly or use the [**MonthCal\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2629-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2629-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2629-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2629-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f2629-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f2629-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f2629-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2629-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f2629-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f2629-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2629-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2629-113">Return value</span></span>

<span data-ttu-id="f2629-114">Gibt das Unicode-formatflag für das-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="f2629-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="f2629-115">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f2629-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="f2629-116">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f2629-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2629-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2629-117">Remarks</span></span>

<span data-ttu-id="f2629-118">Eine Erörterung dieser Nachricht finden Sie in den Hinweisen für [**ccm \_ getunicodeformat**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="f2629-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2629-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2629-119">Requirements</span></span>



| <span data-ttu-id="f2629-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2629-120">Requirement</span></span> | <span data-ttu-id="f2629-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f2629-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2629-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2629-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f2629-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2629-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2629-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2629-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f2629-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2629-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2629-126">Header</span><span class="sxs-lookup"><span data-stu-id="f2629-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2629-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2629-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2629-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2629-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2629-129">**MCM- \_ Format-Code Format**</span><span class="sxs-lookup"><span data-stu-id="f2629-129">**MCM\_SETUNICODEFORMAT**</span></span>](mcm-setunicodeformat.md)
</dt> </dl>

 

 





