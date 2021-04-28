---
title: TBM_SETUNICODEFORMAT (Commctrl.h)
description: 'TBM_SETUNICODEFORMAT Meldung: Legt das Unicode-Zeichenformatflag für das Steuerelement fest. Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen.'
ms.assetid: c50a49e8-6042-490d-bb7b-baf917d5c30a
keywords:
- TBM_SETUNICODEFORMAT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TBM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f076efe2a575eff131c9bc2a1fe3df9ecab0fe68
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104038"
---
# <a name="tbm_setunicodeformat-message"></a><span data-ttu-id="31d81-105">TBM \_ SETUNICODEFORMAT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="31d81-105">TBM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="31d81-106">Legt das Unicode-Zeichenformatflag für das Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="31d81-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="31d81-107">Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="31d81-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="31d81-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="31d81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31d81-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31d81-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="31d81-110">Bestimmt den Zeichensatz, der vom -Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="31d81-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="31d81-111">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="31d81-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="31d81-112">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="31d81-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="31d81-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31d81-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="31d81-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="31d81-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31d81-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31d81-115">Return value</span></span>

<span data-ttu-id="31d81-116">Gibt das vorherige Unicode-Formatflag für das Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="31d81-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="31d81-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31d81-117">Remarks</span></span>

<span data-ttu-id="31d81-118">Eine Erläuterung dieser Meldung finden Sie in den Anmerkungen zu [**CCM \_ SETUNICODEFORMAT.**](ccm-setunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="31d81-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="31d81-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31d81-119">Requirements</span></span>



| <span data-ttu-id="31d81-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31d81-120">Requirement</span></span> | <span data-ttu-id="31d81-121">Wert</span><span class="sxs-lookup"><span data-stu-id="31d81-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31d81-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31d81-122">Minimum supported client</span></span><br/> | <span data-ttu-id="31d81-123">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31d81-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="31d81-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31d81-124">Minimum supported server</span></span><br/> | <span data-ttu-id="31d81-125">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31d81-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="31d81-126">Header</span><span class="sxs-lookup"><span data-stu-id="31d81-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="31d81-127"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="31d81-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31d81-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="31d81-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31d81-129">**TBM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="31d81-129">**TBM\_GETUNICODEFORMAT**</span></span>](tbm-getunicodeformat.md)
</dt> </dl>

 

 





