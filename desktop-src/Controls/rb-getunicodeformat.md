---
title: RB_GETUNICODEFORMAT Meldung (kommstrg. h)
description: Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab.
ms.assetid: 48a4472b-dda4-41a2-b5bc-6f74b1cdc70b
keywords:
- Windows-Steuerelemente für RB_GETUNICODEFORMAT Meldung
topic_type:
- apiref
api_name:
- RB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a6ef31c409ddc0570b03a3bcd8bb0dd81e9c722
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475354"
---
# <a name="rb_getunicodeformat-message"></a><span data-ttu-id="fd131-104">RB \_ getunicodeformat-Meldung</span><span class="sxs-lookup"><span data-stu-id="fd131-104">RB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="fd131-105">Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="fd131-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fd131-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd131-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd131-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fd131-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fd131-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fd131-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fd131-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd131-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fd131-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fd131-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd131-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd131-111">Return value</span></span>

<span data-ttu-id="fd131-112">Gibt das Unicode-formatflag für das-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="fd131-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="fd131-113">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fd131-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="fd131-114">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fd131-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd131-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd131-115">Remarks</span></span>

<span data-ttu-id="fd131-116">Eine Erörterung dieser Nachricht finden Sie in den Hinweisen für [**ccm \_ getunicodeformat**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="fd131-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd131-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd131-117">Requirements</span></span>



| <span data-ttu-id="fd131-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd131-118">Requirement</span></span> | <span data-ttu-id="fd131-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fd131-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd131-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd131-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fd131-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd131-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd131-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd131-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fd131-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd131-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd131-124">Header</span><span class="sxs-lookup"><span data-stu-id="fd131-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd131-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd131-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd131-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd131-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd131-127">**RB- \_ Format**</span><span class="sxs-lookup"><span data-stu-id="fd131-127">**RB\_SETUNICODEFORMAT**</span></span>](rb-setunicodeformat.md)
</dt> </dl>

 

 





