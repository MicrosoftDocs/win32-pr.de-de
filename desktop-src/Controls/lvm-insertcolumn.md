---
title: LVM_INSERTCOLUMN Meldung (kommstrg. h)
description: Fügt eine neue Spalte in ein Listenansicht-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des ListView \_ InsertColumn-Makros senden.
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- Windows-Steuerelemente für LVM_INSERTCOLUMN Meldung
topic_type:
- apiref
api_name:
- LVM_INSERTCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be89ff0b4ef417a715085582544112cb90cb6b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518647"
---
# <a name="lvm_insertcolumn-message"></a><span data-ttu-id="193d7-105">LVM- \_ InsertColumn-Meldung</span><span class="sxs-lookup"><span data-stu-id="193d7-105">LVM\_INSERTCOLUMN message</span></span>

<span data-ttu-id="193d7-106">Fügt eine neue Spalte in ein Listenansicht-Steuerelement ein.</span><span class="sxs-lookup"><span data-stu-id="193d7-106">Inserts a new column in a list-view control.</span></span> <span data-ttu-id="193d7-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="193d7-107">You can send this message explicitly or by using the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="193d7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="193d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="193d7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="193d7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="193d7-110">Index der neuen Spalte.</span><span class="sxs-lookup"><span data-stu-id="193d7-110">Index of the new column.</span></span>

</dd> <dt>

<span data-ttu-id="193d7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="193d7-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="193d7-112">Zeiger auf eine [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) -Struktur, die die Attribute der neuen Spalte enthält.</span><span class="sxs-lookup"><span data-stu-id="193d7-112">Pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that contains the attributes of the new column.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="193d7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="193d7-113">Return value</span></span>

<span data-ttu-id="193d7-114">Gibt den Index der neuen Spalte zurück, wenn erfolgreich, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="193d7-114">Returns the index of the new column if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="193d7-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="193d7-115">Remarks</span></span>

<span data-ttu-id="193d7-116">Spalten sind nur in der Berichtsansicht (Details) sichtbar.</span><span class="sxs-lookup"><span data-stu-id="193d7-116">Columns are visible only in report (details) view.</span></span>

## <a name="requirements"></a><span data-ttu-id="193d7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="193d7-117">Requirements</span></span>



| <span data-ttu-id="193d7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="193d7-118">Requirement</span></span> | <span data-ttu-id="193d7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="193d7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="193d7-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="193d7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="193d7-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="193d7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="193d7-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="193d7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="193d7-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="193d7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="193d7-124">Header</span><span class="sxs-lookup"><span data-stu-id="193d7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="193d7-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="193d7-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





