---
title: LVM_SETUNICODEFORMAT Meldung (Commctrl.h)
description: 'LVM_SETUNICODEFORMAT Meldung: Legt das Unicode-Zeichenformatflag für das Steuerelement fest.'
ms.assetid: e332ae88-821f-4341-a98d-59d8a01a126f
keywords:
- LVM_SETUNICODEFORMAT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- LVM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0f700cd057bc77eddc699404f37b19a6cc9c39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120148"
---
# <a name="lvm_setunicodeformat-message"></a><span data-ttu-id="96b33-104">LVM \_ SETUNICODEFORMAT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="96b33-104">LVM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="96b33-105">Legt das UNICODE-Zeichenformatflag für das Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="96b33-105">Sets the UNICODE character format flag for the control.</span></span> <span data-ttu-id="96b33-106">Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="96b33-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="96b33-107">Sie können diese Nachricht explizit senden oder das [**ListView \_ SetUnicodeFormat-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setunicodeformat) verwenden.</span><span class="sxs-lookup"><span data-stu-id="96b33-107">You can send this message explicitly or use the [**ListView\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="96b33-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="96b33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96b33-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96b33-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96b33-110">Bestimmt den Zeichensatz, der vom -Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="96b33-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="96b33-111">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="96b33-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="96b33-112">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="96b33-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="96b33-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96b33-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="96b33-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="96b33-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96b33-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96b33-115">Return value</span></span>

<span data-ttu-id="96b33-116">Gibt das vorherige Unicode-Formatflag für das Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="96b33-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="96b33-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96b33-117">Remarks</span></span>

<span data-ttu-id="96b33-118">Eine Erläuterung dieser Meldung finden Sie in den Hinweisen zu [**CCM \_ SETUNICODEFORMAT.**](ccm-setunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="96b33-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="96b33-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96b33-119">Requirements</span></span>



| <span data-ttu-id="96b33-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96b33-120">Requirement</span></span> | <span data-ttu-id="96b33-121">Wert</span><span class="sxs-lookup"><span data-stu-id="96b33-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96b33-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96b33-122">Minimum supported client</span></span><br/> | <span data-ttu-id="96b33-123">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96b33-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="96b33-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96b33-124">Minimum supported server</span></span><br/> | <span data-ttu-id="96b33-125">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96b33-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96b33-126">Header</span><span class="sxs-lookup"><span data-stu-id="96b33-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="96b33-127"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="96b33-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96b33-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="96b33-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96b33-129">**LVM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="96b33-129">**LVM\_GETUNICODEFORMAT**</span></span>](lvm-getunicodeformat.md)
</dt> </dl>

 

 





