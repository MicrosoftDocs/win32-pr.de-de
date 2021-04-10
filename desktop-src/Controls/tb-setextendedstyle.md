---
title: TB_SETEXTENDEDSTYLE Meldung (kommstrg. h)
description: Legt die erweiterten Stile für ein Symbolleisten-Steuerelement fest.
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- Windows-Steuerelemente für TB_SETEXTENDEDSTYLE Meldung
topic_type:
- apiref
api_name:
- TB_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a540aaeff61bd81b649f0509e064a29282f598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105039"
---
# <a name="tb_setextendedstyle-message"></a><span data-ttu-id="953e6-104">TB- \_ /textendedstyle-Nachricht</span><span class="sxs-lookup"><span data-stu-id="953e6-104">TB\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="953e6-105">Legt die erweiterten Stile für ein Symbolleisten-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="953e6-105">Sets the extended styles for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="953e6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="953e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="953e6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="953e6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="953e6-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="953e6-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="953e6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="953e6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="953e6-110">Ein-Wert, der die neuen erweiterten Stile angibt.</span><span class="sxs-lookup"><span data-stu-id="953e6-110">Value specifying the new extended styles.</span></span> <span data-ttu-id="953e6-111">Dieser Parameter kann eine Kombination aus [erweiterten Stilen](toolbar-extended-styles.md)sein.</span><span class="sxs-lookup"><span data-stu-id="953e6-111">This parameter can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="953e6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="953e6-112">Return value</span></span>

<span data-ttu-id="953e6-113">Gibt ein **DWORD** zurück, das die vorherigen erweiterten Stile darstellt.</span><span class="sxs-lookup"><span data-stu-id="953e6-113">Returns a **DWORD** that represents the previous extended styles.</span></span> <span data-ttu-id="953e6-114">Bei diesem Wert kann es sich um eine Kombination [erweiterter Stile](toolbar-extended-styles.md)handeln.</span><span class="sxs-lookup"><span data-stu-id="953e6-114">This value can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="953e6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="953e6-115">Requirements</span></span>



| <span data-ttu-id="953e6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="953e6-116">Requirement</span></span> | <span data-ttu-id="953e6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="953e6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="953e6-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="953e6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="953e6-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="953e6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="953e6-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="953e6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="953e6-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="953e6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="953e6-122">Header</span><span class="sxs-lookup"><span data-stu-id="953e6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="953e6-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="953e6-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="953e6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="953e6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="953e6-125">**TB \_ getextendecodstyle**</span><span class="sxs-lookup"><span data-stu-id="953e6-125">**TB\_GETEXTENDEDSTYLE**</span></span>](tb-getextendedstyle.md)
</dt> </dl>

 

 





