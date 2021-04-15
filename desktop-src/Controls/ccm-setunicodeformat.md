---
title: CCM_SETUNICODEFORMAT Meldung (kommstrg. h)
description: Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest. Diese Meldung ermöglicht es Ihnen, den Zeichensatz zu ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen.
ms.assetid: 8028b7d7-30d2-4154-81c7-ba1ed095ef02
keywords:
- Windows-Steuerelemente für CCM_SETUNICODEFORMAT Meldung
topic_type:
- apiref
api_name:
- CCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffbe9f5032c193cb612f68ca8ed6ec6b04ce8094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477628"
---
# <a name="ccm_setunicodeformat-message"></a><span data-ttu-id="053f5-105">CCM-Nachricht "\*- \_ Code Format"</span><span class="sxs-lookup"><span data-stu-id="053f5-105">CCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="053f5-106">Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="053f5-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="053f5-107">Diese Meldung ermöglicht es Ihnen, den Zeichensatz zu ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="053f5-107">This message enables you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="053f5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="053f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="053f5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="053f5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="053f5-110">Ein-Wert, der den Zeichensatz bestimmt, der vom-Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="053f5-110">A value that determines the character set that is used by the control.</span></span> <span data-ttu-id="053f5-111">Wenn dieser Wert **true** ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="053f5-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="053f5-112">Wenn dieser Wert **false** ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="053f5-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="053f5-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="053f5-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="053f5-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="053f5-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="053f5-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="053f5-115">Return value</span></span>

<span data-ttu-id="053f5-116">Gibt das vorherige Unicode-formatflag für das-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="053f5-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="053f5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="053f5-117">Requirements</span></span>



| <span data-ttu-id="053f5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="053f5-118">Requirement</span></span> | <span data-ttu-id="053f5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="053f5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="053f5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="053f5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="053f5-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="053f5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="053f5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="053f5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="053f5-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="053f5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="053f5-124">Header</span><span class="sxs-lookup"><span data-stu-id="053f5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="053f5-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="053f5-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="053f5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="053f5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="053f5-127">**CCM \_ getunicodeformat**</span><span class="sxs-lookup"><span data-stu-id="053f5-127">**CCM\_GETUNICODEFORMAT**</span></span>](ccm-getunicodeformat.md)
</dt> </dl>

 

 





