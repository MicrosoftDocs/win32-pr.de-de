---
title: LVM_ENABLEGROUPVIEW Meldung (kommstrg. h)
description: Aktiviert oder deaktiviert, ob die Elemente in einem Listenansicht-Steuerelement als Gruppe angezeigt werden.
ms.assetid: 783a5e23-d1cb-4523-a6d2-b2cf93fa7f62
keywords:
- Windows-Steuerelemente für LVM_ENABLEGROUPVIEW Meldung
topic_type:
- apiref
api_name:
- LVM_ENABLEGROUPVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d546e1236fa4f0800c0353810beb5b427ba4fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040112"
---
# <a name="lvm_enablegroupview-message"></a><span data-ttu-id="e001f-104">LVM \_ enablegroupview-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e001f-104">LVM\_ENABLEGROUPVIEW message</span></span>

<span data-ttu-id="e001f-105">Aktiviert oder deaktiviert, ob die Elemente in einem Listenansicht-Steuerelement als Gruppe angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e001f-105">Enables or disables whether the items in a list-view control display as a group.</span></span>

## <a name="parameters"></a><span data-ttu-id="e001f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e001f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e001f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e001f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e001f-108">Ein **boolescher** Wert, der angibt, ob ein Listenansicht-Steuerelement zum Gruppieren der angezeigten Elemente aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e001f-108">A **BOOL** that indicates whether to enable a list-view control to group displayed items.</span></span> <span data-ttu-id="e001f-109">Verwenden Sie **true** , um die Gruppierung zu aktivieren. **false** , um Sie zu deaktivieren</span><span class="sxs-lookup"><span data-stu-id="e001f-109">Use **TRUE** to enable grouping, **FALSE** to disable it.</span></span> </dd> <dt>

<span data-ttu-id="e001f-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e001f-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e001f-111">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e001f-111">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e001f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e001f-112">Return value</span></span>

<span data-ttu-id="e001f-113">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="e001f-113">Returns one of the following values.</span></span>



| <span data-ttu-id="e001f-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e001f-114">Return code</span></span>                                                                       | <span data-ttu-id="e001f-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e001f-115">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e001f-116"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="e001f-116"><dt>**0**</dt></span></span> </dl>  | <span data-ttu-id="e001f-117">Die Möglichkeit zum Anzeigen von Listen Ansichts Elementen als Gruppe ist bereits aktiviert oder deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e001f-117">The ability to display list-view items as a group is already enabled or disabled.</span></span><br/> |
| <dl> <span data-ttu-id="e001f-118"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="e001f-118"><dt>**1**</dt></span></span> </dl>  | <span data-ttu-id="e001f-119">Der Zustand des Steuer Elements wurde erfolgreich geändert.</span><span class="sxs-lookup"><span data-stu-id="e001f-119">The state of the control was successfully changed.</span></span><br/>                                |
| <dl> <span data-ttu-id="e001f-120"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="e001f-120"><dt>**-1**</dt></span></span> </dl> | <span data-ttu-id="e001f-121">Fehler beim Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e001f-121">The operation failed.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="e001f-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e001f-122">Remarks</span></span>

<span data-ttu-id="e001f-123">**LVM \_ Enablegroupview** wird unter dem [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e001f-123">**LVM\_ENABLEGROUPVIEW** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="e001f-124">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="e001f-124">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="e001f-125">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e001f-125">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e001f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e001f-126">Requirements</span></span>



| <span data-ttu-id="e001f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e001f-127">Requirement</span></span> | <span data-ttu-id="e001f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e001f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e001f-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e001f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e001f-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e001f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e001f-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e001f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e001f-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e001f-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e001f-133">Header</span><span class="sxs-lookup"><span data-stu-id="e001f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e001f-134"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="e001f-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





