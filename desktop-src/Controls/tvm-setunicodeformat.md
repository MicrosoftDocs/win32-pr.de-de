---
title: TVM_SETUNICODEFORMAT (Commctrl.h)
description: 'TVM_SETUNICODEFORMAT Meldung: Legt das Unicode-Zeichenformatflag für das Steuerelement fest.'
ms.assetid: e4b58ae5-6217-4a2e-80e5-3ba9e578859a
keywords:
- TVM_SETUNICODEFORMAT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TVM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b49fcdd22cff0ac91885ef8f54d49922f9c677e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116548"
---
# <a name="tvm_setunicodeformat-message"></a><span data-ttu-id="c3e65-104">TVM \_ SETUNICODEFORMAT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c3e65-104">TVM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="c3e65-105">Legt das Unicode-Zeichenformatflag für das Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="c3e65-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="c3e65-106">Mit dieser Meldung können Sie den vom Steuerelement zur Laufzeit verwendeten Zeichensatz ändern, anstatt das Steuerelement neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="c3e65-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="c3e65-107">Sie können diese Nachricht explizit senden oder das [**TreeView \_ SetUnicodeFormat-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setunicodeformat) verwenden.</span><span class="sxs-lookup"><span data-stu-id="c3e65-107">You can send this message explicitly or use the [**TreeView\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3e65-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3e65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3e65-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3e65-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3e65-110">Bestimmt den Zeichensatz, der vom -Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3e65-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="c3e65-111">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c3e65-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="c3e65-112">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c3e65-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="c3e65-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3e65-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c3e65-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c3e65-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3e65-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3e65-115">Return value</span></span>

<span data-ttu-id="c3e65-116">Gibt das vorherige Unicode-Formatflag für das Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="c3e65-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3e65-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3e65-117">Remarks</span></span>

<span data-ttu-id="c3e65-118">Eine Erläuterung dieser Meldung finden Sie in den Anmerkungen zu [**CCM \_ SETUNICODEFORMAT.**](ccm-setunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="c3e65-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3e65-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3e65-119">Requirements</span></span>



| <span data-ttu-id="c3e65-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3e65-120">Requirement</span></span> | <span data-ttu-id="c3e65-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c3e65-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3e65-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3e65-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c3e65-123">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3e65-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3e65-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3e65-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c3e65-125">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3e65-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3e65-126">Header</span><span class="sxs-lookup"><span data-stu-id="c3e65-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3e65-127"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="c3e65-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3e65-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c3e65-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3e65-129">**TVM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="c3e65-129">**TVM\_GETUNICODEFORMAT**</span></span>](tvm-getunicodeformat.md)
</dt> </dl>

 

 





