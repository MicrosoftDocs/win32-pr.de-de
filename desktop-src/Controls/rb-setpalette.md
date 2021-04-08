---
title: RB_SETPALETTE Meldung (kommstrg. h)
description: Legt die aktuelle Palette des Grund leisten-Steuer Elements fest.
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- Windows-Steuerelemente für RB_SETPALETTE Meldung
topic_type:
- apiref
api_name:
- RB_SETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ee47985c05bcd8a857620e7fe501bddf53bdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956797"
---
# <a name="rb_setpalette-message"></a><span data-ttu-id="f81b4-104">RB- \_ SetPalette-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f81b4-104">RB\_SETPALETTE message</span></span>

<span data-ttu-id="f81b4-105">Legt die aktuelle Palette des Grund leisten-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="f81b4-105">Sets the rebar control's current palette.</span></span>

## <a name="parameters"></a><span data-ttu-id="f81b4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f81b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f81b4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f81b4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f81b4-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f81b4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f81b4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f81b4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f81b4-110">Eine **hpalette** , die die neue Palette angibt, die vom Grund leisten-Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f81b4-110">An **HPALETTE** that specifies the new palette that the rebar control will use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f81b4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f81b4-111">Return value</span></span>

<span data-ttu-id="f81b4-112">Gibt eine **hpalette** zurück, die die vorherige Palette des Grund leisten-Steuer Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="f81b4-112">Returns an **HPALETTE** that specifies the rebar control's previous palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="f81b4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f81b4-113">Remarks</span></span>

<span data-ttu-id="f81b4-114">Die Anwendung, die diese Nachricht sendet, ist dafür verantwortlich, die in dieser Nachricht übergebenen **hpalette** zu löschen (siehe [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)).</span><span class="sxs-lookup"><span data-stu-id="f81b4-114">It is the responsibility of the application sending this message to delete the **HPALETTE** passed in this message (see [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)).</span></span> <span data-ttu-id="f81b4-115">Das Grund leisten-Steuerelement löscht keinen **hpalette** -Satz mit dieser Meldung.</span><span class="sxs-lookup"><span data-stu-id="f81b4-115">The rebar control will not delete an **HPALETTE** set with this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f81b4-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f81b4-116">Requirements</span></span>



| <span data-ttu-id="f81b4-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f81b4-117">Requirement</span></span> | <span data-ttu-id="f81b4-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f81b4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f81b4-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f81b4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f81b4-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f81b4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f81b4-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f81b4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f81b4-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f81b4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f81b4-123">Header</span><span class="sxs-lookup"><span data-stu-id="f81b4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f81b4-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f81b4-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f81b4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f81b4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f81b4-126">**RB \_ getpalette**</span><span class="sxs-lookup"><span data-stu-id="f81b4-126">**RB\_GETPALETTE**</span></span>](rb-getpalette.md)
</dt> </dl>

 

