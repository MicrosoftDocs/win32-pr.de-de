---
title: HDM_SETORDERARRAY Meldung (kommstrg. h)
description: Legt die Reihenfolge von Header Elementen von links nach rechts fest. Sie können diese Nachricht explizit senden oder das Header- \_ /s--Makro-Makro verwenden.
ms.assetid: 094c424f-10bd-484d-8236-937811b703a6
keywords:
- Windows-Steuerelemente für HDM_SETORDERARRAY Meldung
topic_type:
- apiref
api_name:
- HDM_SETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f07874bfc102babec18b142a087b14e330044ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476974"
---
# <a name="hdm_setorderarray-message"></a><span data-ttu-id="96dab-105">HDM- \_ Nachricht "abderarray"</span><span class="sxs-lookup"><span data-stu-id="96dab-105">HDM\_SETORDERARRAY message</span></span>

<span data-ttu-id="96dab-106">Legt die Reihenfolge von Header Elementen von links nach rechts fest.</span><span class="sxs-lookup"><span data-stu-id="96dab-106">Sets the left-to-right order of header items.</span></span> <span data-ttu-id="96dab-107">Sie können diese Nachricht explizit senden oder das [**Header- \_**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) /s--Makro-Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="96dab-107">You can send this message explicitly or use the [**Header\_SetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="96dab-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="96dab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96dab-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96dab-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96dab-110">Die Größe des Puffers bei *LPARAM* in-Elementen.</span><span class="sxs-lookup"><span data-stu-id="96dab-110">The size of the buffer at *lParam*, in elements.</span></span> <span data-ttu-id="96dab-111">Dieser Wert muss mit dem von [**HDM \_ GetItemCount**](hdm-getitemcount.md)zurückgegebenen Wert identisch sein.</span><span class="sxs-lookup"><span data-stu-id="96dab-111">This value must equal the value returned by [**HDM\_GETITEMCOUNT**](hdm-getitemcount.md).</span></span>

</dd> <dt>

<span data-ttu-id="96dab-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96dab-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96dab-113">Ein Zeiger auf ein Array, das die Reihenfolge angibt, in der Elemente angezeigt werden sollen, von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="96dab-113">A pointer to an array that specifies the order in which items should be displayed, from left to right.</span></span> <span data-ttu-id="96dab-114">Wenn der Inhalt des-Arrays beispielsweise {2,0,1} ist, zeigt das-Steuerelement Element 2, Element 0 und Element 1 von links nach rechts an.</span><span class="sxs-lookup"><span data-stu-id="96dab-114">For example, if the contents of the array are {2,0,1}, the control displays item 2, item 0, and item 1, from left to right.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96dab-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96dab-115">Return value</span></span>

<span data-ttu-id="96dab-116">Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.</span><span class="sxs-lookup"><span data-stu-id="96dab-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="96dab-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96dab-117">Requirements</span></span>



| <span data-ttu-id="96dab-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96dab-118">Requirement</span></span> | <span data-ttu-id="96dab-119">Wert</span><span class="sxs-lookup"><span data-stu-id="96dab-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96dab-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96dab-120">Minimum supported client</span></span><br/> | <span data-ttu-id="96dab-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96dab-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="96dab-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96dab-122">Minimum supported server</span></span><br/> | <span data-ttu-id="96dab-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96dab-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96dab-124">Header</span><span class="sxs-lookup"><span data-stu-id="96dab-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="96dab-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="96dab-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





