---
title: UDM_SETUNICODEFORMAT Meldung (kommstrg. h)
description: Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest. Mit dieser Meldung können Sie den Zeichensatz ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen.
ms.assetid: abe882db-bf32-40b0-a1c0-3e89cdc93fe7
keywords:
- Windows-Steuerelemente für UDM_SETUNICODEFORMAT Meldung
topic_type:
- apiref
api_name:
- UDM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db3f9dbc1e19fdb43aa0b7d5e6de6fdddd308eb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040662"
---
# <a name="udm_setunicodeformat-message"></a><span data-ttu-id="99325-105">UDM-Nachricht "- \_ Code Format"</span><span class="sxs-lookup"><span data-stu-id="99325-105">UDM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="99325-106">Legt das Unicode-Zeichenformat Flag für das-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="99325-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="99325-107">Mit dieser Meldung können Sie den Zeichensatz ändern, der vom Steuerelement zur Laufzeit verwendet wird, anstatt das Steuerelement neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="99325-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="99325-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="99325-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99325-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99325-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99325-110">Bestimmt den Zeichensatz, der vom-Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="99325-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="99325-111">Wenn dieser Wert **true** ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="99325-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="99325-112">Wenn dieser Wert **false** ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="99325-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="99325-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99325-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="99325-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="99325-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99325-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99325-115">Return value</span></span>

<span data-ttu-id="99325-116">Gibt das vorherige Unicode-formatflag für das-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="99325-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="99325-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99325-117">Remarks</span></span>

<span data-ttu-id="99325-118">Eine Erörterung dieser Nachricht finden Sie in den Hinweisen zu [**ccm- \_ Code Format**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="99325-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="99325-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99325-119">Requirements</span></span>



| <span data-ttu-id="99325-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99325-120">Requirement</span></span> | <span data-ttu-id="99325-121">Wert</span><span class="sxs-lookup"><span data-stu-id="99325-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99325-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99325-122">Minimum supported client</span></span><br/> | <span data-ttu-id="99325-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99325-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="99325-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99325-124">Minimum supported server</span></span><br/> | <span data-ttu-id="99325-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99325-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="99325-126">Header</span><span class="sxs-lookup"><span data-stu-id="99325-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="99325-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="99325-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99325-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99325-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99325-129">**UDM \_ getunicodeformat**</span><span class="sxs-lookup"><span data-stu-id="99325-129">**UDM\_GETUNICODEFORMAT**</span></span>](udm-getunicodeformat.md)
</dt> </dl>

 

 





