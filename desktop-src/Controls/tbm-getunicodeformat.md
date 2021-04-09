---
title: TBM_GETUNICODEFORMAT Meldung (kommstrg. h)
description: Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab.
ms.assetid: cecd7e55-f482-4381-bde8-a60b8c5173eb
keywords:
- Windows-Steuerelemente für TBM_GETUNICODEFORMAT Meldung
topic_type:
- apiref
api_name:
- TBM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a9fafad2504e51a65b879e58298c5cd06f1f345
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858909"
---
# <a name="tbm_getunicodeformat-message"></a><span data-ttu-id="044ec-104">TBM \_ getunicodeformat-Meldung</span><span class="sxs-lookup"><span data-stu-id="044ec-104">TBM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="044ec-105">Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="044ec-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="044ec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="044ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="044ec-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="044ec-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="044ec-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="044ec-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="044ec-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="044ec-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="044ec-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="044ec-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="044ec-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="044ec-111">Return value</span></span>

<span data-ttu-id="044ec-112">Gibt das Unicode-formatflag für das-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="044ec-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="044ec-113">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="044ec-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="044ec-114">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="044ec-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="044ec-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="044ec-115">Remarks</span></span>

<span data-ttu-id="044ec-116">Eine Erörterung dieser Nachricht finden Sie in den Hinweisen für [**ccm \_ getunicodeformat**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="044ec-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="044ec-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="044ec-117">Requirements</span></span>



| <span data-ttu-id="044ec-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="044ec-118">Requirement</span></span> | <span data-ttu-id="044ec-119">Wert</span><span class="sxs-lookup"><span data-stu-id="044ec-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="044ec-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="044ec-120">Minimum supported client</span></span><br/> | <span data-ttu-id="044ec-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="044ec-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="044ec-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="044ec-122">Minimum supported server</span></span><br/> | <span data-ttu-id="044ec-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="044ec-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="044ec-124">Header</span><span class="sxs-lookup"><span data-stu-id="044ec-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="044ec-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="044ec-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="044ec-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="044ec-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="044ec-127">**TBM- \_ Code Format**</span><span class="sxs-lookup"><span data-stu-id="044ec-127">**TBM\_SETUNICODEFORMAT**</span></span>](tbm-setunicodeformat.md)
</dt> </dl>

 

 





