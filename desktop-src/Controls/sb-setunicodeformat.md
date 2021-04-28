---
title: SB_SETUNICODEFORMAT (Commctrl.h)
description: 'SB_SETUNICODEFORMAT Meldung: Legt das Unicode-Zeichenformatflag für das Steuerelement fest. Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen.'
ms.assetid: 022e7138-c12f-4c59-82da-2ac6d276fa77
keywords:
- SB_SETUNICODEFORMAT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- SB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 278a5645928a51732b87c12447bb2524bfadfbcd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085888"
---
# <a name="sb_setunicodeformat-message"></a><span data-ttu-id="3e8f3-105">SB \_ SETUNICODEFORMAT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="3e8f3-105">SB\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="3e8f3-106">Legt das Unicode-Zeichenformatflag für das Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="3e8f3-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="3e8f3-107">Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="3e8f3-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3e8f3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e8f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e8f3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e8f3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e8f3-110">Bestimmt den Zeichensatz, der vom -Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e8f3-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="3e8f3-111">Wenn dieser Wert **TRUE ist,** verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3e8f3-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="3e8f3-112">Wenn dieser Wert **FALSE ist,** verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3e8f3-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="3e8f3-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e8f3-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3e8f3-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="3e8f3-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e8f3-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e8f3-115">Return value</span></span>

<span data-ttu-id="3e8f3-116">Gibt das vorherige Unicode-Formatflag für das Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="3e8f3-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e8f3-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e8f3-117">Remarks</span></span>

<span data-ttu-id="3e8f3-118">Eine Erläuterung dieser Meldung finden Sie in den Anmerkungen zu [**CCM \_ SETUNICODEFORMAT.**](ccm-setunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="3e8f3-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e8f3-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e8f3-119">Requirements</span></span>



| <span data-ttu-id="3e8f3-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e8f3-120">Requirement</span></span> | <span data-ttu-id="3e8f3-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3e8f3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e8f3-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e8f3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3e8f3-123">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e8f3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3e8f3-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e8f3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3e8f3-125">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e8f3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3e8f3-126">Header</span><span class="sxs-lookup"><span data-stu-id="3e8f3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e8f3-127"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="3e8f3-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e8f3-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3e8f3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e8f3-129">**SB \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="3e8f3-129">**SB\_GETUNICODEFORMAT**</span></span>](sb-getunicodeformat.md)
</dt> </dl>

 

 





