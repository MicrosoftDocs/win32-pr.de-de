---
title: UDM_SETUNICODEFORMAT (Commctrl.h)
description: 'UDM_SETUNICODEFORMAT Meldung: Legt das Unicode-Zeichenformatflag für das Steuerelement fest. Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen.'
ms.assetid: abe882db-bf32-40b0-a1c0-3e89cdc93fe7
keywords:
- UDM_SETUNICODEFORMAT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- UDM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09eeb63d5c06a5e64c354c950cd84fc451568d36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116538"
---
# <a name="udm_setunicodeformat-message"></a><span data-ttu-id="d4d4f-105">UDM \_ SETUNICODEFORMAT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d4d4f-105">UDM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="d4d4f-106">Legt das Unicode-Zeichenformatflag für das Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="d4d4f-107">Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d4d4f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4d4f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4d4f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d4d4f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d4d4f-110">Bestimmt den Zeichensatz, der vom -Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="d4d4f-111">Wenn dieser Wert **TRUE ist,** verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="d4d4f-112">Wenn dieser Wert **FALSE ist,** verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="d4d4f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4d4f-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d4d4f-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4d4f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4d4f-115">Return value</span></span>

<span data-ttu-id="d4d4f-116">Gibt das vorherige Unicode-Formatflag für das Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4d4f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4d4f-117">Remarks</span></span>

<span data-ttu-id="d4d4f-118">Eine Erläuterung dieser Meldung finden Sie in den Anmerkungen zu [**CCM \_ SETUNICODEFORMAT.**](ccm-setunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="d4d4f-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4d4f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4d4f-119">Requirements</span></span>



| <span data-ttu-id="d4d4f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4d4f-120">Requirement</span></span> | <span data-ttu-id="d4d4f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d4d4f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d4f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4d4f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d4d4f-123">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4d4f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d4d4f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4d4f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d4d4f-125">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4d4f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4d4f-126">Header</span><span class="sxs-lookup"><span data-stu-id="d4d4f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4d4f-127"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="d4d4f-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4d4f-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d4d4f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d4f-129">**UDM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d4d4f-129">**UDM\_GETUNICODEFORMAT**</span></span>](udm-getunicodeformat.md)
</dt> </dl>

 

 





