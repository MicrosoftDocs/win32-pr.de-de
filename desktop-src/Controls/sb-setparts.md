---
title: SB_SETPARTS Meldung (kommstrg. h)
description: Legt die Anzahl der Teile in einem Statusfenster und die Koordinate des rechten Rands der einzelnen Teile fest.
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- Windows-Steuerelemente für SB_SETPARTS Meldung
topic_type:
- apiref
api_name:
- SB_SETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 062058fa3778cd0394cadd9d76b363a0353ffb2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518437"
---
# <a name="sb_setparts-message"></a><span data-ttu-id="565e4-104">SB- \_ SetParts-Nachricht</span><span class="sxs-lookup"><span data-stu-id="565e4-104">SB\_SETPARTS message</span></span>

<span data-ttu-id="565e4-105">Legt die Anzahl der Teile in einem Statusfenster und die Koordinate des rechten Rands der einzelnen Teile fest.</span><span class="sxs-lookup"><span data-stu-id="565e4-105">Sets the number of parts in a status window and the coordinate of the right edge of each part.</span></span>

## <a name="parameters"></a><span data-ttu-id="565e4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="565e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="565e4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="565e4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="565e4-108">Anzahl der festzulegenden Teile (darf nicht größer als 256 sein).</span><span class="sxs-lookup"><span data-stu-id="565e4-108">Number of parts to set (cannot be greater than 256).</span></span>

</dd> <dt>

<span data-ttu-id="565e4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="565e4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="565e4-110">Zeiger auf ein ganzzahliges Array.</span><span class="sxs-lookup"><span data-stu-id="565e4-110">Pointer to an integer array.</span></span> <span data-ttu-id="565e4-111">Die Anzahl der Elemente wird in *wParam* angegeben.</span><span class="sxs-lookup"><span data-stu-id="565e4-111">The number of elements is specified in *wParam*.</span></span> <span data-ttu-id="565e4-112">Jedes Element gibt die Position (in Client Koordinaten) des rechten Rands des entsprechenden Teils an.</span><span class="sxs-lookup"><span data-stu-id="565e4-112">Each element specifies the position, in client coordinates, of the right edge of the corresponding part.</span></span> <span data-ttu-id="565e4-113">Wenn ein Element-1 ist, wird der Rechte Rand des entsprechenden Teils auf den Rahmen des Fensters erweitert.</span><span class="sxs-lookup"><span data-stu-id="565e4-113">If an element is -1, the right edge of the corresponding part extends to the border of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="565e4-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="565e4-114">Return value</span></span>

<span data-ttu-id="565e4-115">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="565e4-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="565e4-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="565e4-116">Requirements</span></span>



| <span data-ttu-id="565e4-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="565e4-117">Requirement</span></span> | <span data-ttu-id="565e4-118">Wert</span><span class="sxs-lookup"><span data-stu-id="565e4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="565e4-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="565e4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="565e4-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="565e4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="565e4-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="565e4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="565e4-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="565e4-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="565e4-123">Header</span><span class="sxs-lookup"><span data-stu-id="565e4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="565e4-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="565e4-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





