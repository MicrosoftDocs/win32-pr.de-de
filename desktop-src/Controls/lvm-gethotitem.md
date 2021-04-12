---
title: LVM_GETHOTITEM Meldung (kommstrg. h)
description: Ruft den Index des aktiven Elements ab. Sie können diese Nachricht explizit senden oder das ListView \_ gethotitem-Makro verwenden.
ms.assetid: f80189da-6c8b-4faf-925a-0c33fedf8c4e
keywords:
- Windows-Steuerelemente für LVM_GETHOTITEM Meldung
topic_type:
- apiref
api_name:
- LVM_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c7bbfb845518eb40b55556df5294d59cff3d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105513"
---
# <a name="lvm_gethotitem-message"></a><span data-ttu-id="a4f8f-105">LVM- \_ gethotitem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a4f8f-105">LVM\_GETHOTITEM message</span></span>

<span data-ttu-id="a4f8f-106">Ruft den Index des aktiven Elements ab.</span><span class="sxs-lookup"><span data-stu-id="a4f8f-106">Retrieves the index of the hot item.</span></span> <span data-ttu-id="a4f8f-107">Sie können diese Nachricht explizit senden oder das [**ListView \_ gethotitem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4f8f-107">You can send this message explicitly or use the [**ListView\_GetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a4f8f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4f8f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4f8f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a4f8f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a4f8f-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a4f8f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a4f8f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4f8f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a4f8f-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a4f8f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4f8f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4f8f-113">Return value</span></span>

<span data-ttu-id="a4f8f-114">Gibt den Index des aktiven Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="a4f8f-114">Returns the index of the item that is hot.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f8f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4f8f-115">Requirements</span></span>



| <span data-ttu-id="a4f8f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4f8f-116">Requirement</span></span> | <span data-ttu-id="a4f8f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a4f8f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f8f-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4f8f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a4f8f-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4f8f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a4f8f-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4f8f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a4f8f-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4f8f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a4f8f-122">Header</span><span class="sxs-lookup"><span data-stu-id="a4f8f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4f8f-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4f8f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





