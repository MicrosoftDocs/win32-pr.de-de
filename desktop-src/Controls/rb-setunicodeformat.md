---
title: RB_SETUNICODEFORMAT Meldung (kommstrg. h)
description: Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest. Mit dieser Meldung können Sie den Zeichensatz ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen.
ms.assetid: 769b74e0-c1f0-4068-80c4-075f1db2058a
keywords:
- Windows-Steuerelemente für RB_SETUNICODEFORMAT Meldung
topic_type:
- apiref
api_name:
- RB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfc9d0ce256af0de740c487fd6514848db79c2e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742520"
---
# <a name="rb_setunicodeformat-message"></a><span data-ttu-id="4fa5f-105">RB- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="4fa5f-105">RB\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="4fa5f-106">Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="4fa5f-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="4fa5f-107">Mit dieser Meldung können Sie den Zeichensatz ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="4fa5f-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4fa5f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fa5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fa5f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4fa5f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4fa5f-110">Bestimmt den Zeichensatz, der vom-Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4fa5f-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="4fa5f-111">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4fa5f-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="4fa5f-112">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4fa5f-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="4fa5f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4fa5f-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4fa5f-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="4fa5f-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fa5f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4fa5f-115">Return value</span></span>

<span data-ttu-id="4fa5f-116">Gibt das vorherige Unicode-formatflag für das-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="4fa5f-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fa5f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fa5f-117">Remarks</span></span>

<span data-ttu-id="4fa5f-118">Eine Erörterung dieser Nachricht finden Sie in den Hinweisen zu [**ccm- \_ Code Format**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="4fa5f-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fa5f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fa5f-119">Requirements</span></span>



| <span data-ttu-id="4fa5f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fa5f-120">Requirement</span></span> | <span data-ttu-id="4fa5f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4fa5f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa5f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fa5f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4fa5f-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fa5f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4fa5f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fa5f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4fa5f-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fa5f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4fa5f-126">Header</span><span class="sxs-lookup"><span data-stu-id="4fa5f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fa5f-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fa5f-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fa5f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fa5f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fa5f-129">**RB \_ getunicodeformat**</span><span class="sxs-lookup"><span data-stu-id="4fa5f-129">**RB\_GETUNICODEFORMAT**</span></span>](rb-getunicodeformat.md)
</dt> </dl>

 

 





