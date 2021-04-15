---
title: MCM_SETUNICODEFORMAT Meldung (kommstrg. h)
description: Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest.
ms.assetid: 250789b5-694b-4502-9cc0-3bc260ea06e7
keywords:
- Windows-Steuerelemente für MCM_SETUNICODEFORMAT Meldung
topic_type:
- apiref
api_name:
- MCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0aee3318479f4e94b4d85f15fe7c58e4417a1bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476965"
---
# <a name="mcm_setunicodeformat-message"></a><span data-ttu-id="74593-104">MCM-Meldung "\* \* \_ Format"</span><span class="sxs-lookup"><span data-stu-id="74593-104">MCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="74593-105">Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="74593-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="74593-106">Mit dieser Meldung können Sie den Zeichensatz ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="74593-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="74593-107">Sie können diese Nachricht explizit senden oder das [**monthcal- \_ Format**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat) "\*-Code Format" verwenden.</span><span class="sxs-lookup"><span data-stu-id="74593-107">You can send this message explicitly or use the [**MonthCal\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="74593-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="74593-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74593-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74593-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74593-110">Bestimmt den Zeichensatz, der vom-Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="74593-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="74593-111">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="74593-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="74593-112">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="74593-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="74593-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74593-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="74593-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="74593-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74593-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74593-115">Return value</span></span>

<span data-ttu-id="74593-116">Gibt das vorherige Unicode-formatflag für das-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="74593-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="74593-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74593-117">Remarks</span></span>

<span data-ttu-id="74593-118">Eine Erörterung dieser Nachricht finden Sie in den Hinweisen zu [**ccm- \_ Code Format**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="74593-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="74593-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74593-119">Requirements</span></span>



| <span data-ttu-id="74593-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74593-120">Requirement</span></span> | <span data-ttu-id="74593-121">Wert</span><span class="sxs-lookup"><span data-stu-id="74593-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74593-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74593-122">Minimum supported client</span></span><br/> | <span data-ttu-id="74593-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74593-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74593-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74593-124">Minimum supported server</span></span><br/> | <span data-ttu-id="74593-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74593-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74593-126">Header</span><span class="sxs-lookup"><span data-stu-id="74593-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="74593-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="74593-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74593-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74593-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74593-129">**MCM \_ getunicodeformat**</span><span class="sxs-lookup"><span data-stu-id="74593-129">**MCM\_GETUNICODEFORMAT**</span></span>](mcm-getunicodeformat.md)
</dt> </dl>

 

 





