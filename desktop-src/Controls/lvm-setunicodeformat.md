---
title: LVM_SETUNICODEFORMAT Meldung (kommstrg. h)
description: Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest.
ms.assetid: e332ae88-821f-4341-a98d-59d8a01a126f
keywords:
- Windows-Steuerelemente für LVM_SETUNICODEFORMAT Meldung
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
ms.openlocfilehash: 18b1e29d933892a24d7bc2ab472c7d591375362a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345503"
---
# <a name="lvm_setunicodeformat-message"></a><span data-ttu-id="1e269-104">LVM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="1e269-104">LVM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="1e269-105">Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="1e269-105">Sets the UNICODE character format flag for the control.</span></span> <span data-ttu-id="1e269-106">Mit dieser Meldung können Sie den Zeichensatz ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="1e269-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="1e269-107">Sie können diese Nachricht explizit senden oder das ListView-Makro "\*- [**\_ Code Format**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setunicodeformat) " verwenden.</span><span class="sxs-lookup"><span data-stu-id="1e269-107">You can send this message explicitly or use the [**ListView\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e269-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e269-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e269-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e269-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e269-110">Bestimmt den Zeichensatz, der vom-Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1e269-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="1e269-111">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1e269-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="1e269-112">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1e269-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="1e269-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e269-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1e269-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="1e269-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e269-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e269-115">Return value</span></span>

<span data-ttu-id="1e269-116">Gibt das vorherige Unicode-formatflag für das-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="1e269-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e269-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e269-117">Remarks</span></span>

<span data-ttu-id="1e269-118">Eine Erörterung dieser Nachricht finden Sie in den Hinweisen zu [**ccm- \_ Code Format**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="1e269-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e269-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e269-119">Requirements</span></span>



| <span data-ttu-id="1e269-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e269-120">Requirement</span></span> | <span data-ttu-id="1e269-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1e269-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e269-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e269-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1e269-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e269-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e269-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e269-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1e269-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e269-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e269-126">Header</span><span class="sxs-lookup"><span data-stu-id="1e269-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e269-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e269-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e269-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e269-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e269-129">**LVM \_ getunicodeformat**</span><span class="sxs-lookup"><span data-stu-id="1e269-129">**LVM\_GETUNICODEFORMAT**</span></span>](lvm-getunicodeformat.md)
</dt> </dl>

 

 





