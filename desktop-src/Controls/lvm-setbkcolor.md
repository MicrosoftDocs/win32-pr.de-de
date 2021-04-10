---
title: LVM_SETBKCOLOR Meldung (kommstrg. h)
description: Legt die Hintergrundfarbe eines Listenansicht-Steuer Elements fest. Sie können diese Nachricht explizit oder mithilfe des ListView \_ SetBkColor-Makros senden.
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- Windows-Steuerelemente für LVM_SETBKCOLOR Meldung
topic_type:
- apiref
api_name:
- LVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80977ed6c95a1353889265e52cfc05c26aaa2a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956720"
---
# <a name="lvm_setbkcolor-message"></a><span data-ttu-id="61297-105">LVM- \_ SetBkColor-Nachricht</span><span class="sxs-lookup"><span data-stu-id="61297-105">LVM\_SETBKCOLOR message</span></span>

<span data-ttu-id="61297-106">Legt die Hintergrundfarbe eines Listenansicht-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="61297-106">Sets the background color of a list-view control.</span></span> <span data-ttu-id="61297-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="61297-107">You can send this message explicitly or by using the [**ListView\_SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="61297-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="61297-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61297-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="61297-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="61297-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="61297-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="61297-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61297-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61297-112">Die festzulegende Hintergrundfarbe oder der CLR \_ None-Wert für keine Hintergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="61297-112">Background color to set or the CLR\_NONE value for no background color.</span></span> <span data-ttu-id="61297-113">Listenansicht-Steuerelemente mit Hintergrundfarben zeichnen sich deutlich schneller aus als solche ohne Hintergrundfarben.</span><span class="sxs-lookup"><span data-stu-id="61297-113">List-view controls with background colors redraw themselves significantly faster than those without background colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61297-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61297-114">Return value</span></span>

<span data-ttu-id="61297-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="61297-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="61297-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61297-116">Requirements</span></span>



| <span data-ttu-id="61297-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61297-117">Requirement</span></span> | <span data-ttu-id="61297-118">Wert</span><span class="sxs-lookup"><span data-stu-id="61297-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61297-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61297-119">Minimum supported client</span></span><br/> | <span data-ttu-id="61297-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61297-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61297-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61297-121">Minimum supported server</span></span><br/> | <span data-ttu-id="61297-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61297-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61297-123">Header</span><span class="sxs-lookup"><span data-stu-id="61297-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="61297-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="61297-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





