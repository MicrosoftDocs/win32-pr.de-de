---
title: CBEM_SETUNICODEFORMAT Meldung (kommstrg. h)
description: Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest. Diese Meldung ermöglicht es Ihnen, den Zeichensatz zu ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen.
ms.assetid: 4811709b-1639-4468-8598-97d9dc8d9057
keywords:
- Windows-Steuerelemente für CBEM_SETUNICODEFORMAT Meldung
topic_type:
- apiref
api_name:
- CBEM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89540d4e942b8b705685c13addeeb17adf0b4f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105764"
---
# <a name="cbem_setunicodeformat-message"></a><span data-ttu-id="260dc-105">CBEM- \_ Code Format Meldung</span><span class="sxs-lookup"><span data-stu-id="260dc-105">CBEM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="260dc-106">Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="260dc-106">Sets the UNICODE character format flag for the control.</span></span> <span data-ttu-id="260dc-107">Diese Meldung ermöglicht es Ihnen, den Zeichensatz zu ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="260dc-107">This message enables you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="260dc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="260dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="260dc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="260dc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="260dc-110">Bestimmt den Zeichensatz, der vom-Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="260dc-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="260dc-111">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="260dc-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="260dc-112">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="260dc-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="260dc-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="260dc-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="260dc-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="260dc-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="260dc-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="260dc-115">Return value</span></span>

<span data-ttu-id="260dc-116">Gibt das vorherige Unicode-formatflag für das-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="260dc-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="260dc-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="260dc-117">Remarks</span></span>

<span data-ttu-id="260dc-118">Eine Erörterung dieser Nachricht finden Sie in den Hinweisen zu [**ccm- \_ Code Format**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="260dc-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="260dc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="260dc-119">Requirements</span></span>



| <span data-ttu-id="260dc-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="260dc-120">Requirement</span></span> | <span data-ttu-id="260dc-121">Wert</span><span class="sxs-lookup"><span data-stu-id="260dc-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="260dc-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="260dc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="260dc-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="260dc-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="260dc-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="260dc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="260dc-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="260dc-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="260dc-126">Header</span><span class="sxs-lookup"><span data-stu-id="260dc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="260dc-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="260dc-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="260dc-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="260dc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="260dc-129">**CBEM \_ getunicodeformat**</span><span class="sxs-lookup"><span data-stu-id="260dc-129">**CBEM\_GETUNICODEFORMAT**</span></span>](cbem-getunicodeformat.md)
</dt> </dl>

 

 





