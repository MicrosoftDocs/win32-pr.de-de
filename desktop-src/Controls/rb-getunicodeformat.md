---
title: RB_GETUNICODEFORMAT Nachricht (Commctrl.h)
description: 'RB_GETUNICODEFORMAT Meldung: Ruft das Unicode-Zeichenformatflag für das Steuerelement ab.'
ms.assetid: 48a4472b-dda4-41a2-b5bc-6f74b1cdc70b
keywords:
- RB_GETUNICODEFORMAT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- RB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e1a4546c9c33e87943d305c85939ab280fa122
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085978"
---
# <a name="rb_getunicodeformat-message"></a><span data-ttu-id="31dcf-104">RB \_ GETUNICODEFORMAT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="31dcf-104">RB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="31dcf-105">Ruft das Unicode-Zeichenformatflag für das Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="31dcf-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="31dcf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="31dcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31dcf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="31dcf-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="31dcf-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="31dcf-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="31dcf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="31dcf-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="31dcf-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="31dcf-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31dcf-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31dcf-111">Return value</span></span>

<span data-ttu-id="31dcf-112">Gibt das Unicode-Formatflag für das Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="31dcf-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="31dcf-113">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="31dcf-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="31dcf-114">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="31dcf-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="31dcf-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31dcf-115">Remarks</span></span>

<span data-ttu-id="31dcf-116">Eine Erläuterung dieser Meldung finden Sie in den Hinweisen zu [**CCM \_ GETUNICODEFORMAT.**](ccm-getunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="31dcf-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="31dcf-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31dcf-117">Requirements</span></span>



| <span data-ttu-id="31dcf-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31dcf-118">Requirement</span></span> | <span data-ttu-id="31dcf-119">Wert</span><span class="sxs-lookup"><span data-stu-id="31dcf-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31dcf-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31dcf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="31dcf-121">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31dcf-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="31dcf-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31dcf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="31dcf-123">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31dcf-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="31dcf-124">Header</span><span class="sxs-lookup"><span data-stu-id="31dcf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="31dcf-125"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="31dcf-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31dcf-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="31dcf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31dcf-127">**RB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="31dcf-127">**RB\_SETUNICODEFORMAT**</span></span>](rb-setunicodeformat.md)
</dt> </dl>

 

 





