---
title: HDM_SETUNICODEFORMAT Meldung (Commctrl.h)
description: 'HDM_SETUNICODEFORMAT Meldung: Legt das Unicode-Zeichenformatflag für das Steuerelement fest.'
ms.assetid: 18161fe5-c779-4be0-9e7a-1b5948e42b80
keywords:
- HDM_SETUNICODEFORMAT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- HDM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32ffa5f7f90ab266c52c67899dbff3be0d51123
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085958"
---
# <a name="hdm_setunicodeformat-message"></a><span data-ttu-id="a89c4-104">HDM \_ SETUNICODEFORMAT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a89c4-104">HDM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="a89c4-105">Legt das UNICODE-Zeichenformatflag für das Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="a89c4-105">Sets the UNICODE character format flag for the control.</span></span> <span data-ttu-id="a89c4-106">Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="a89c4-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="a89c4-107">Sie können diese Nachricht explizit senden oder das [**\_ HeadersetUnicodeFormat-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-header_setunicodeformat) verwenden.</span><span class="sxs-lookup"><span data-stu-id="a89c4-107">You can send this message explicitly or use the [**Header\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-header_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a89c4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a89c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a89c4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a89c4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a89c4-110">Der Zeichensatz, der vom -Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a89c4-110">The character set that is used by the control.</span></span> <span data-ttu-id="a89c4-111">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a89c4-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="a89c4-112">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a89c4-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="a89c4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a89c4-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a89c4-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a89c4-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a89c4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a89c4-115">Return value</span></span>

<span data-ttu-id="a89c4-116">Gibt das vorherige Unicode-Formatflag für das Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="a89c4-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="a89c4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a89c4-117">Remarks</span></span>

<span data-ttu-id="a89c4-118">Eine Erläuterung dieser Meldung finden Sie in den Hinweisen zu [**CCM \_ SETUNICODEFORMAT.**](ccm-setunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="a89c4-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a89c4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a89c4-119">Requirements</span></span>



| <span data-ttu-id="a89c4-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a89c4-120">Requirement</span></span> | <span data-ttu-id="a89c4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a89c4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a89c4-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a89c4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a89c4-123">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a89c4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a89c4-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a89c4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a89c4-125">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a89c4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a89c4-126">Header</span><span class="sxs-lookup"><span data-stu-id="a89c4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a89c4-127"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="a89c4-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a89c4-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a89c4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a89c4-129">**HDM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="a89c4-129">**HDM\_GETUNICODEFORMAT**</span></span>](hdm-getunicodeformat.md)
</dt> </dl>

 

 





