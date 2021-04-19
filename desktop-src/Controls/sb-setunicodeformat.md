---
title: SB_SETUNICODEFORMAT Meldung (kommstrg. h)
description: Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest. Mit dieser Meldung können Sie den Zeichensatz ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen.
ms.assetid: 022e7138-c12f-4c59-82da-2ac6d276fa77
keywords:
- Windows-Steuerelemente für SB_SETUNICODEFORMAT Meldung
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
ms.openlocfilehash: 95c5223f1e707747356c8869ad047a69f6e8d94a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346516"
---
# <a name="sb_setunicodeformat-message"></a><span data-ttu-id="95031-105">SB- \_ Nachricht "szcodeformat"</span><span class="sxs-lookup"><span data-stu-id="95031-105">SB\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="95031-106">Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="95031-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="95031-107">Mit dieser Meldung können Sie den Zeichensatz ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="95031-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="95031-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="95031-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95031-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95031-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95031-110">Bestimmt den Zeichensatz, der vom-Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="95031-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="95031-111">Wenn dieser Wert **true** ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="95031-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="95031-112">Wenn dieser Wert **false** ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="95031-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="95031-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95031-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="95031-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="95031-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95031-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95031-115">Return value</span></span>

<span data-ttu-id="95031-116">Gibt das vorherige Unicode-formatflag für das-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="95031-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="95031-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95031-117">Remarks</span></span>

<span data-ttu-id="95031-118">Eine Erörterung dieser Nachricht finden Sie in den Hinweisen zu [**ccm- \_ Code Format**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="95031-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="95031-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95031-119">Requirements</span></span>



| <span data-ttu-id="95031-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95031-120">Requirement</span></span> | <span data-ttu-id="95031-121">Wert</span><span class="sxs-lookup"><span data-stu-id="95031-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95031-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95031-122">Minimum supported client</span></span><br/> | <span data-ttu-id="95031-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95031-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95031-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95031-124">Minimum supported server</span></span><br/> | <span data-ttu-id="95031-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95031-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95031-126">Header</span><span class="sxs-lookup"><span data-stu-id="95031-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="95031-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="95031-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95031-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95031-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95031-129">**SB \_ getunicodeformat**</span><span class="sxs-lookup"><span data-stu-id="95031-129">**SB\_GETUNICODEFORMAT**</span></span>](sb-getunicodeformat.md)
</dt> </dl>

 

 





