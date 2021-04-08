---
title: TB_GETEXTENDEDSTYLE Meldung (kommstrg. h)
description: Ruft die erweiterten Stile für ein Symbolleisten-Steuerelement ab.
ms.assetid: d9e31a8e-5e5a-4d2d-bc3b-65ac40e8592f
keywords:
- Windows-Steuerelemente für TB_GETEXTENDEDSTYLE Meldung
topic_type:
- apiref
api_name:
- TB_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80bc4f4ad45e5c1c75366e0890f3fd76ec1fa74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741209"
---
# <a name="tb_getextendedstyle-message"></a><span data-ttu-id="73503-104">TB \_ GetExtendedStyle-Nachricht</span><span class="sxs-lookup"><span data-stu-id="73503-104">TB\_GETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="73503-105">Ruft die erweiterten Stile für ein Symbolleisten-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="73503-105">Retrieves the extended styles for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="73503-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="73503-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73503-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="73503-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="73503-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="73503-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="73503-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73503-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="73503-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="73503-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73503-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="73503-111">Return value</span></span>

<span data-ttu-id="73503-112">Gibt ein **DWORD** zurück, das die derzeit für das Symbolleisten-Steuerelement verwendeten Stile darstellt.</span><span class="sxs-lookup"><span data-stu-id="73503-112">Returns a **DWORD** that represents the styles currently in use for the toolbar control.</span></span> <span data-ttu-id="73503-113">Bei diesem Wert kann es sich um eine Kombination [erweiterter Stile](toolbar-extended-styles.md)handeln.</span><span class="sxs-lookup"><span data-stu-id="73503-113">This value can be a combination of [extended styles](toolbar-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="73503-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73503-114">Requirements</span></span>



| <span data-ttu-id="73503-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73503-115">Requirement</span></span> | <span data-ttu-id="73503-116">Wert</span><span class="sxs-lookup"><span data-stu-id="73503-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73503-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73503-117">Minimum supported client</span></span><br/> | <span data-ttu-id="73503-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73503-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73503-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73503-119">Minimum supported server</span></span><br/> | <span data-ttu-id="73503-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73503-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73503-121">Header</span><span class="sxs-lookup"><span data-stu-id="73503-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="73503-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="73503-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73503-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73503-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73503-124">**TB/ \_ textendecodstyle**</span><span class="sxs-lookup"><span data-stu-id="73503-124">**TB\_SETEXTENDEDSTYLE**</span></span>](tb-setextendedstyle.md)
</dt> </dl>

 

 





