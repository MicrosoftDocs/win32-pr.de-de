---
title: LVM_INSERTGROUP Meldung (kommstrg. h)
description: Fügt eine Gruppe in ein Listenansicht-Steuerelement ein.
ms.assetid: d43e21bc-e212-42dd-af88-48813d40cd50
keywords:
- Windows-Steuerelemente für LVM_INSERTGROUP Meldung
topic_type:
- apiref
api_name:
- LVM_INSERTGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dbae780f7de26a5c791477e1a7321794054056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339580"
---
# <a name="lvm_insertgroup-message"></a><span data-ttu-id="07a4d-104">LVM \_ insertgroup-Meldung</span><span class="sxs-lookup"><span data-stu-id="07a4d-104">LVM\_INSERTGROUP message</span></span>

<span data-ttu-id="07a4d-105">Fügt eine Gruppe in ein Listenansicht-Steuerelement ein.</span><span class="sxs-lookup"><span data-stu-id="07a4d-105">Inserts a group into a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="07a4d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="07a4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07a4d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="07a4d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="07a4d-108">Der Index, an dem die Gruppe hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="07a4d-108">Index where the group is to be added.</span></span> <span data-ttu-id="07a4d-109">Wenn der Wert-1 ist, wird die Gruppe am Ende der Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="07a4d-109">If this is -1, the group is added at the end of the list.</span></span></dd> <dt>

<span data-ttu-id="07a4d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07a4d-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="07a4d-111">Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**orgroup**</a> -Struktur, die die hinzu zufügende Gruppe enthält.</span><span class="sxs-lookup"><span data-stu-id="07a4d-111">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> structure that contains the group to add.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07a4d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07a4d-112">Return value</span></span>

<span data-ttu-id="07a4d-113">Gibt den Index des Elements zurück, dem die Gruppe hinzugefügt wurde, oder-1, wenn der Vorgang fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="07a4d-113">Returns the index of the item that the group was added to, or -1 if the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="07a4d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07a4d-114">Remarks</span></span>

<span data-ttu-id="07a4d-115">Um den Gruppenmodus zu aktivieren, müssen Sie [**LVM \_ enablegroupview**](lvm-enablegroupview.md) oder [**ListView \_ enablegroupview**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="07a4d-115">To turn on group mode, call [**LVM\_ENABLEGROUPVIEW**](lvm-enablegroupview.md) or [**ListView\_EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).</span></span>

<span data-ttu-id="07a4d-116">Eine Gruppe kann nicht in ein leeres Listenansicht-Steuerelement eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="07a4d-116">A group cannot be inserted into an empty list-view control.</span></span>

<span data-ttu-id="07a4d-117">Stellen Sie sicher, dass die **igroupid** in den Elementen festgelegt ist, der die Gruppe hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="07a4d-117">Be sure to set the **iGroupId** in the item(s) the group was added to.</span></span> <span data-ttu-id="07a4d-118">Andernfalls zeigt das ListView-Steuerelement nach der [**LVM- \_ enablegroupview**](lvm-enablegroupview.md) -Nachrichtenverarbeitung mit **true** keine Elemente an.</span><span class="sxs-lookup"><span data-stu-id="07a4d-118">Otherwise after [**LVM\_ENABLEGROUPVIEW**](lvm-enablegroupview.md) message processing with **TRUE** the listview control will not show any items.</span></span>

> [!Note]  
> <span data-ttu-id="07a4d-119">Um diese Meldung zu verwenden, müssen Sie ein Manifest angeben, in dem die Comclt32-Version 6,0 angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="07a4d-119">To use this message, you must provide a manifest specifying Comclt32 version 6.0.</span></span> <span data-ttu-id="07a4d-120">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="07a4d-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="07a4d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07a4d-121">Requirements</span></span>



| <span data-ttu-id="07a4d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07a4d-122">Requirement</span></span> | <span data-ttu-id="07a4d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="07a4d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07a4d-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07a4d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="07a4d-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07a4d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="07a4d-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07a4d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="07a4d-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07a4d-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="07a4d-128">Header</span><span class="sxs-lookup"><span data-stu-id="07a4d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="07a4d-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="07a4d-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





