---
title: TCM_SETUNICODEFORMAT Meldung (kommstrg. h)
description: Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest.
ms.assetid: 4a9bacfc-d1b7-432a-9b61-b0fe18576679
keywords:
- Windows-Steuerelemente für TCM_SETUNICODEFORMAT Meldung
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
ms.openlocfilehash: 033851411f95811f202ea6d87e23717d39141c04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391512"
---
# <a name="tcm_setunicodeformat-message"></a><span data-ttu-id="fc717-104">TCM- \_ /codeformatmeldung</span><span class="sxs-lookup"><span data-stu-id="fc717-104">TCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="fc717-105">Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="fc717-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="fc717-106">Mit dieser Meldung können Sie den Zeichensatz ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="fc717-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="fc717-107">Sie können diese Nachricht explizit senden oder das [**tabctrl-Format tabctrl- \_ Code Format**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat) verwenden.</span><span class="sxs-lookup"><span data-stu-id="fc717-107">You can send this message explicitly or use the [**TabCtrl\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc717-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc717-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc717-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc717-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc717-110">Bestimmt den Zeichensatz, der vom-Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc717-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="fc717-111">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fc717-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="fc717-112">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fc717-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="fc717-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc717-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fc717-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fc717-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc717-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc717-115">Return value</span></span>

<span data-ttu-id="fc717-116">Gibt das vorherige Unicode-formatflag für das-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="fc717-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc717-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc717-117">Remarks</span></span>

<span data-ttu-id="fc717-118">Eine Erörterung dieser Nachricht finden Sie in den Hinweisen zu [**ccm- \_ Code Format**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="fc717-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc717-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc717-119">Requirements</span></span>



| <span data-ttu-id="fc717-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc717-120">Requirement</span></span> | <span data-ttu-id="fc717-121">Wert</span><span class="sxs-lookup"><span data-stu-id="fc717-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc717-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc717-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fc717-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc717-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fc717-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc717-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fc717-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc717-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc717-126">Header</span><span class="sxs-lookup"><span data-stu-id="fc717-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc717-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc717-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc717-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc717-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc717-129">**TCM \_ getunicodeformat**</span><span class="sxs-lookup"><span data-stu-id="fc717-129">**TCM\_GETUNICODEFORMAT**</span></span>](tcm-getunicodeformat.md)
</dt> </dl>

 

 





