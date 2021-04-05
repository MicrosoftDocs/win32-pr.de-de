---
title: TCM_GETUNICODEFORMAT Meldung (kommstrg. h)
description: Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab. Sie können diese Nachricht explizit senden oder das tabstrg \_ getunicodeformat-Makro verwenden.
ms.assetid: 720e0325-500b-436c-8713-38ed780735bf
keywords:
- Windows-Steuerelemente für TCM_GETUNICODEFORMAT Meldung
topic_type:
- apiref
api_name:
- TCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b497f1b2c2b5ac55ee949b498602b50b267fef3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859195"
---
# <a name="tcm_getunicodeformat-message"></a><span data-ttu-id="1ef4a-105">TCM \_ getunicodeformat-Meldung</span><span class="sxs-lookup"><span data-stu-id="1ef4a-105">TCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="1ef4a-106">Ruft das Unicode-Zeichenformat Flag für das-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="1ef4a-106">Retrieves the Unicode character format flag for the control.</span></span> <span data-ttu-id="1ef4a-107">Sie können diese Nachricht explizit senden oder das [**tabstrg \_ getunicodeformat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getunicodeformat) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="1ef4a-107">You can send this message explicitly or use the [**TabCtrl\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ef4a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ef4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ef4a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ef4a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1ef4a-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="1ef4a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1ef4a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ef4a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1ef4a-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="1ef4a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ef4a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ef4a-113">Return value</span></span>

<span data-ttu-id="1ef4a-114">Gibt das Unicode-formatflag für das-Steuerelement zurück.</span><span class="sxs-lookup"><span data-stu-id="1ef4a-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="1ef4a-115">Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1ef4a-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="1ef4a-116">Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="1ef4a-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ef4a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ef4a-117">Remarks</span></span>

<span data-ttu-id="1ef4a-118">Eine Erörterung dieser Nachricht finden Sie in den Hinweisen für [**ccm \_ getunicodeformat**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="1ef4a-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ef4a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ef4a-119">Requirements</span></span>



| <span data-ttu-id="1ef4a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ef4a-120">Requirement</span></span> | <span data-ttu-id="1ef4a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1ef4a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ef4a-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ef4a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1ef4a-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ef4a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1ef4a-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ef4a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1ef4a-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ef4a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ef4a-126">Header</span><span class="sxs-lookup"><span data-stu-id="1ef4a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ef4a-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ef4a-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ef4a-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ef4a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ef4a-129">**TCM- \_ Code Format**</span><span class="sxs-lookup"><span data-stu-id="1ef4a-129">**TCM\_SETUNICODEFORMAT**</span></span>](tcm-setunicodeformat.md)
</dt> </dl>

 

 





