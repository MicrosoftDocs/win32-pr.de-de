---
title: LVM_DELETECOLUMN Meldung (kommstrg. h)
description: Entfernt eine Spalte aus einem Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des ListView \_ deleteColumn-Makros senden.
ms.assetid: 1748a70b-9a13-4753-ac23-55b5652164c2
keywords:
- Windows-Steuerelemente für LVM_DELETECOLUMN Meldung
topic_type:
- apiref
api_name:
- LVM_DELETECOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa9005009ceaf42a01ede4f0f26334ae686c2df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739969"
---
# <a name="lvm_deletecolumn-message"></a><span data-ttu-id="32ca8-105">LVM \_ deleteColumn-Nachricht</span><span class="sxs-lookup"><span data-stu-id="32ca8-105">LVM\_DELETECOLUMN message</span></span>

<span data-ttu-id="32ca8-106">Entfernt eine Spalte aus einem Listenansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="32ca8-106">Removes a column from a list-view control.</span></span> <span data-ttu-id="32ca8-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ deleteColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="32ca8-107">You can send this message explicitly or by using the [**ListView\_DeleteColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="32ca8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="32ca8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32ca8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32ca8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32ca8-110">Der Index der zu löschenden Spalte.</span><span class="sxs-lookup"><span data-stu-id="32ca8-110">The index of the column to delete.</span></span>

</dd> <dt>

<span data-ttu-id="32ca8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32ca8-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="32ca8-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="32ca8-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32ca8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32ca8-113">Return value</span></span>

<span data-ttu-id="32ca8-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="32ca8-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="32ca8-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32ca8-115">Remarks</span></span>

<span data-ttu-id="32ca8-116">Das Löschen der Spalte NULL eines Listenansicht-Steuer Elements wird nur in ComCtl32.dll Version 6 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="32ca8-116">Deleting column zero of a list-view control is supported only in ComCtl32.dll version 6 and later.</span></span> <span data-ttu-id="32ca8-117">Version 5 unterstützt auch das Löschen von Spalten NULL, aber erst nach der Verwendung von [**ccm \_ setVersion**](ccm-setversion.md) , um die Version auf 5 oder höher festzulegen.</span><span class="sxs-lookup"><span data-stu-id="32ca8-117">Version 5 also supports deleting column zero, but only after you use [**CCM\_SETVERSION**](ccm-setversion.md) to set the version to 5 or later.</span></span> <span data-ttu-id="32ca8-118">Wenn Sie in Versionen vor Version 5 die Spalte NULL löschen müssen, fügen Sie eine dummyspalte der Länge 0 (null) ein, und löschen Sie die Spalte 1 und höher.</span><span class="sxs-lookup"><span data-stu-id="32ca8-118">In versions prior to version 5, if you must delete column zero, insert a zero length dummy column zero and delete column one and above.</span></span>

## <a name="requirements"></a><span data-ttu-id="32ca8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32ca8-119">Requirements</span></span>



| <span data-ttu-id="32ca8-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32ca8-120">Requirement</span></span> | <span data-ttu-id="32ca8-121">Wert</span><span class="sxs-lookup"><span data-stu-id="32ca8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32ca8-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32ca8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="32ca8-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32ca8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32ca8-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32ca8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="32ca8-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32ca8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32ca8-126">Header</span><span class="sxs-lookup"><span data-stu-id="32ca8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="32ca8-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="32ca8-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





