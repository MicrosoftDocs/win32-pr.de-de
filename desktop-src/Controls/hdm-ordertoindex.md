---
title: HDM_ORDERTOINDEX Meldung (kommstrg. h)
description: Ruft einen Indexwert für ein Element auf Grundlage seiner Reihenfolge im Header Steuerelement ab. Sie können diese Nachricht explizit senden oder den Header \_ orderdeindex-Makro verwenden.
ms.assetid: vs|controls|~\controls\header\messages\hdm_ordertoindex.htm
keywords:
- Windows-Steuerelemente für HDM_ORDERTOINDEX Meldung
topic_type:
- apiref
api_name:
- HDM_ORDERTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b65d10fb27c9a07639ebbd5770a53d72cbf0aba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040544"
---
# <a name="hdm_ordertoindex-message"></a><span data-ttu-id="27777-105">HDM \_ Order$ Index-Meldung</span><span class="sxs-lookup"><span data-stu-id="27777-105">HDM\_ORDERTOINDEX message</span></span>

<span data-ttu-id="27777-106">Ruft einen Indexwert für ein Element auf Grundlage seiner Reihenfolge im Header Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="27777-106">Retrieves an index value for an item based on its order in the header control.</span></span> <span data-ttu-id="27777-107">Sie können diese Nachricht explizit senden oder den [**Header \_ orderdeindex**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="27777-107">You can send this message explicitly or use the [**Header\_OrderToIndex**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="27777-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="27777-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27777-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27777-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27777-110">Die Reihenfolge, in der das Element im Header Steuerelement angezeigt wird, von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="27777-110">The order in which the item appears within the header control, from left to right.</span></span> <span data-ttu-id="27777-111">Der Indexwert des Elements in der Spalte ganz links wäre z. b. 0.</span><span class="sxs-lookup"><span data-stu-id="27777-111">For example, the index value of the item in the far left column would be 0.</span></span> <span data-ttu-id="27777-112">Der Wert für das nächste Element rechts ist 1 usw.</span><span class="sxs-lookup"><span data-stu-id="27777-112">The value for the next item to the right would be 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="27777-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27777-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="27777-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="27777-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27777-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27777-115">Return value</span></span>

<span data-ttu-id="27777-116">Gibt int zurück, das den Element Index angibt.</span><span class="sxs-lookup"><span data-stu-id="27777-116">Returns INT that indicates the item index.</span></span> <span data-ttu-id="27777-117">Wenn *wParam* ungültig ist (negativ oder zu groß), ist die Rückgabe gleich *wParam*.</span><span class="sxs-lookup"><span data-stu-id="27777-117">If *wParam* is invalid (negative or too large), the return equals *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="27777-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27777-118">Requirements</span></span>



| <span data-ttu-id="27777-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27777-119">Requirement</span></span> | <span data-ttu-id="27777-120">Wert</span><span class="sxs-lookup"><span data-stu-id="27777-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27777-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27777-121">Minimum supported client</span></span><br/> | <span data-ttu-id="27777-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27777-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="27777-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27777-123">Minimum supported server</span></span><br/> | <span data-ttu-id="27777-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="27777-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="27777-125">Header</span><span class="sxs-lookup"><span data-stu-id="27777-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="27777-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="27777-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





