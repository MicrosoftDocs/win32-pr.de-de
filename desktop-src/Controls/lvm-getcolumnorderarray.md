---
title: LVM_GETCOLUMNORDERARRAY Meldung (kommstrg. h)
description: Ruft die aktuelle Reihenfolge von links nach rechts von Spalten in einem Listenansicht-Steuerelement ab. Sie können diese Nachricht explizit senden oder das ListView \_ getcolumnorderarray-Makro verwenden.
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- Windows-Steuerelemente für LVM_GETCOLUMNORDERARRAY Meldung
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee387f65abd3f30826e361778d5acac02dfab7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040107"
---
# <a name="lvm_getcolumnorderarray-message"></a><span data-ttu-id="d44ea-105">LVM \_ getcolumnorderarray-Meldung</span><span class="sxs-lookup"><span data-stu-id="d44ea-105">LVM\_GETCOLUMNORDERARRAY message</span></span>

<span data-ttu-id="d44ea-106">Ruft die aktuelle Reihenfolge von links nach rechts von Spalten in einem Listenansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="d44ea-106">Gets the current left-to-right order of columns in a list-view control.</span></span> <span data-ttu-id="d44ea-107">Sie können diese Nachricht explizit senden oder das [**ListView \_ getcolumnorderarray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="d44ea-107">You can send this message explicitly or use the [**ListView\_GetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d44ea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d44ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d44ea-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d44ea-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d44ea-110">Die Anzahl der Spalten im Listenansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="d44ea-110">The number of columns in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="d44ea-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d44ea-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d44ea-112">Ein Zeiger auf ein Array von ganzen Zahlen, das die Indexwerte der Spalten im Listenansicht-Steuerelement empfängt.</span><span class="sxs-lookup"><span data-stu-id="d44ea-112">A pointer to an array of integers that receives the index values of the columns in the list-view control.</span></span> <span data-ttu-id="d44ea-113">Das Array muss groß genug sein, um *wParam* -Elemente zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d44ea-113">The array must be large enough to hold *wParam* elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d44ea-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d44ea-114">Return value</span></span>

<span data-ttu-id="d44ea-115">Wenn erfolgreich, wird ein Wert ungleich 0 (null) zurückgegeben, und der Puffer bei *LPARAM* empfängt den Spalten Index jeder Spalte im Steuerelement in der Reihenfolge, in der Sie von links nach rechts angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d44ea-115">If successful, returns nonzero, and the buffer at *lParam* receives the column index of each column in the control in the order they appear from left to right.</span></span> <span data-ttu-id="d44ea-116">Andernfalls ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="d44ea-116">Otherwise, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d44ea-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d44ea-117">Requirements</span></span>



| <span data-ttu-id="d44ea-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d44ea-118">Requirement</span></span> | <span data-ttu-id="d44ea-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d44ea-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d44ea-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d44ea-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d44ea-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d44ea-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d44ea-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d44ea-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d44ea-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d44ea-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d44ea-124">Header</span><span class="sxs-lookup"><span data-stu-id="d44ea-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d44ea-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d44ea-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





