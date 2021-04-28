---
title: TCM_SETUNICODEFORMAT Meldung (Commctrl.h)
description: 'TCM_SETUNICODEFORMAT Meldung: Legt das Unicode-Zeichenformatflag für das Steuerelement fest.'
ms.assetid: 4a9bacfc-d1b7-432a-9b61-b0fe18576679
keywords:
- TCM_SETUNICODEFORMAT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b84f944be9bd20897d25e4b111f55ced558a43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085848"
---
# <a name="tcm_setunicodeformat-message"></a><span data-ttu-id="34f2a-104">TCM \_ SETUNICODEFORMAT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="34f2a-104">TCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="34f2a-105">Legt das Unicode-Zeichenformatflag für das Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="34f2a-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="34f2a-106">Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="34f2a-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="34f2a-107">Sie können diese Nachricht explizit senden oder das [**TabCtrl \_ SetUnicodeFormat-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat) verwenden.</span><span class="sxs-lookup"><span data-stu-id="34f2a-107">You can send this message explicitly or use the [**TabCtrl\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="34f2a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="34f2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34f2a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="34f2a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34f2a-110">Bestimmt den Zeichensatz, der vom -Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34f2a-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="34f2a-111">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="34f2a-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="34f2a-112">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="34f2a-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="34f2a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="34f2a-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="34f2a-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="34f2a-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34f2a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34f2a-115">Return value</span></span>

<span data-ttu-id="34f2a-116">Gibt das vorherige Unicode-Formatflag für das Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="34f2a-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="34f2a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34f2a-117">Remarks</span></span>

<span data-ttu-id="34f2a-118">Eine Erläuterung dieser Meldung finden Sie in den Hinweisen zu [**CCM \_ SETUNICODEFORMAT.**](ccm-setunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="34f2a-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="34f2a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34f2a-119">Requirements</span></span>



| <span data-ttu-id="34f2a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34f2a-120">Requirement</span></span> | <span data-ttu-id="34f2a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="34f2a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34f2a-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="34f2a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="34f2a-123">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34f2a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="34f2a-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="34f2a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="34f2a-125">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34f2a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="34f2a-126">Header</span><span class="sxs-lookup"><span data-stu-id="34f2a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="34f2a-127"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="34f2a-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34f2a-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="34f2a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34f2a-129">**TCM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="34f2a-129">**TCM\_GETUNICODEFORMAT**</span></span>](tcm-getunicodeformat.md)
</dt> </dl>

 

 





