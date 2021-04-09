---
title: UDM_GETUNICODEFORMAT Meldung (kommstrg. h)
description: Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab.
ms.assetid: 8c09d37b-95a2-49cd-b578-919f9c39fa8b
keywords:
- Windows-Steuerelemente für UDM_GETUNICODEFORMAT Meldung
topic_type:
- apiref
api_name:
- UDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2f9eef604af6cf5dfcefbf1e3e03dec561ac21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957212"
---
# <a name="udm_getunicodeformat-message"></a><span data-ttu-id="a0498-104">UDM \_ getunicodeformat-Meldung</span><span class="sxs-lookup"><span data-stu-id="a0498-104">UDM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="a0498-105">Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="a0498-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0498-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0498-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0498-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0498-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a0498-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a0498-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a0498-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0498-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a0498-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a0498-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0498-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0498-111">Return value</span></span>

<span data-ttu-id="a0498-112">Gibt das Unicode-formatflag für das-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="a0498-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="a0498-113">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a0498-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="a0498-114">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a0498-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0498-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0498-115">Remarks</span></span>

<span data-ttu-id="a0498-116">Eine Erörterung dieser Nachricht finden Sie in den Hinweisen für [**ccm \_ getunicodeformat**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="a0498-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0498-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0498-117">Requirements</span></span>



| <span data-ttu-id="a0498-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0498-118">Requirement</span></span> | <span data-ttu-id="a0498-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a0498-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0498-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0498-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a0498-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0498-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0498-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a0498-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a0498-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a0498-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0498-124">Header</span><span class="sxs-lookup"><span data-stu-id="a0498-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0498-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0498-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0498-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0498-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0498-127">**UDM- \_ Format-Code Format**</span><span class="sxs-lookup"><span data-stu-id="a0498-127">**UDM\_SETUNICODEFORMAT**</span></span>](udm-setunicodeformat.md)
</dt> </dl>

 

 





