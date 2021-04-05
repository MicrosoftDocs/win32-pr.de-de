---
title: CBEM_GETUNICODEFORMAT Meldung (kommstrg. h)
description: Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab.
ms.assetid: 854ff8d5-6e2f-4918-a6c5-91356a4454af
keywords:
- Windows-Steuerelemente für CBEM_GETUNICODEFORMAT Meldung
topic_type:
- apiref
api_name:
- CBEM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b77bb0daabe6ef14d4be1b5e2de6bb1dd63248d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859283"
---
# <a name="cbem_getunicodeformat-message"></a><span data-ttu-id="4e2e5-104">CBEM \_ getunicodeformat-Meldung</span><span class="sxs-lookup"><span data-stu-id="4e2e5-104">CBEM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="4e2e5-105">Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="4e2e5-105">Gets the UNICODE character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e2e5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e2e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e2e5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e2e5-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4e2e5-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="4e2e5-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4e2e5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e2e5-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4e2e5-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="4e2e5-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e2e5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e2e5-111">Return value</span></span>

<span data-ttu-id="4e2e5-112">Gibt das Unicode-formatflag für das-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="4e2e5-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="4e2e5-113">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4e2e5-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="4e2e5-114">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4e2e5-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e2e5-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e2e5-115">Remarks</span></span>

<span data-ttu-id="4e2e5-116">Eine Erörterung dieser Nachricht finden Sie in den Hinweisen für [**ccm \_ getunicodeformat**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="4e2e5-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e2e5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e2e5-117">Requirements</span></span>



| <span data-ttu-id="4e2e5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e2e5-118">Requirement</span></span> | <span data-ttu-id="4e2e5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4e2e5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e2e5-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e2e5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4e2e5-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e2e5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e2e5-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e2e5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4e2e5-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4e2e5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e2e5-124">Header</span><span class="sxs-lookup"><span data-stu-id="4e2e5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e2e5-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e2e5-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e2e5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e2e5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e2e5-127">**CBEM- \_ Code Format**</span><span class="sxs-lookup"><span data-stu-id="4e2e5-127">**CBEM\_SETUNICODEFORMAT**</span></span>](cbem-setunicodeformat.md)
</dt> </dl>

 

 





