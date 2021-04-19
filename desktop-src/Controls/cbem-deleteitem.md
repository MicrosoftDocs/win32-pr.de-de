---
title: CBEM_DELETEITEM Meldung (kommstrg. h)
description: Entfernt ein Element aus einem ComboBoxEx-Steuerelement.
ms.assetid: 688cf388-54ba-4b45-88d7-628da49d8615
keywords:
- Windows-Steuerelemente für CBEM_DELETEITEM Meldung
topic_type:
- apiref
api_name:
- CBEM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3034f79dffabcd7d7aa780582646e17d30b62f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342670"
---
# <a name="cbem_deleteitem-message"></a><span data-ttu-id="9e242-104">CBEM \_ DeleteItem-Meldung</span><span class="sxs-lookup"><span data-stu-id="9e242-104">CBEM\_DELETEITEM message</span></span>

<span data-ttu-id="9e242-105">Entfernt ein Element aus einem ComboBoxEx-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="9e242-105">Removes an item from a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e242-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e242-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e242-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e242-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e242-108">Der null basierte Index des zu entfernenden Elements.</span><span class="sxs-lookup"><span data-stu-id="9e242-108">The zero-based index of the item to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="9e242-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e242-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9e242-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9e242-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e242-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e242-111">Return value</span></span>

<span data-ttu-id="9e242-112">Gibt einen int-Wert zurück, der die Anzahl der im-Steuerelement verbleibenden Elemente darstellt.</span><span class="sxs-lookup"><span data-stu-id="9e242-112">Returns an INT value that represents the number of items remaining in the control.</span></span> <span data-ttu-id="9e242-113">Wenn *iIndex* ungültig ist, gibt die Nachricht CB \_ Err zurück.</span><span class="sxs-lookup"><span data-stu-id="9e242-113">If *iIndex* is invalid, the message returns CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e242-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e242-114">Remarks</span></span>

<span data-ttu-id="9e242-115">Diese Meldung wird der Kombinations Feld-Steuerelement Nachricht [**CB \_ deletestring**](cb-deletestring.md)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9e242-115">This message maps to the combo box control message [**CB\_DELETESTRING**](cb-deletestring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e242-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e242-116">Requirements</span></span>



| <span data-ttu-id="9e242-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e242-117">Requirement</span></span> | <span data-ttu-id="9e242-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9e242-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e242-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e242-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9e242-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e242-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e242-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e242-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9e242-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e242-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e242-123">Header</span><span class="sxs-lookup"><span data-stu-id="9e242-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e242-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e242-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





