---
title: LVM_SETIMAGELIST Meldung (kommstrg. h)
description: Weist einem Listenansicht-Steuerelement eine Bildliste zu. Sie können diese Nachricht explizit oder mithilfe des ListView \_ SetImageList-Makros senden.
ms.assetid: 5241065b-85e4-412e-9868-fd5b15ff7c17
keywords:
- Windows-Steuerelemente für LVM_SETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- LVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 779d31fd781a72dbdfbc4738e091482ca4a08528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949420"
---
# <a name="lvm_setimagelist-message"></a><span data-ttu-id="d7f7b-105">LVM \_ SetImageList-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d7f7b-105">LVM\_SETIMAGELIST message</span></span>

<span data-ttu-id="d7f7b-106">Weist einem Listenansicht-Steuerelement eine Bildliste zu.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-106">Assigns an image list to a list-view control.</span></span> <span data-ttu-id="d7f7b-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-107">You can send this message explicitly or by using the [**ListView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7f7b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7f7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7f7b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7f7b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7f7b-110">Typ der Bildliste.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-110">Type of image list.</span></span> <span data-ttu-id="d7f7b-111">Dieser Parameter kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="d7f7b-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="d7f7b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="d7f7b-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="d7f7b-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d7f7b-113">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <span data-ttu-id="d7f7b-114"><dt>**lvsil \_ Normal**</dt></span><span class="sxs-lookup"><span data-stu-id="d7f7b-114"><dt>**LVSIL\_NORMAL**</dt></span></span> </dl>                | <span data-ttu-id="d7f7b-115">Bildliste mit großen Symbolen.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-115">Image list with large icons.</span></span><br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <span data-ttu-id="d7f7b-116"><dt>**lvsil \_ Small**</dt></span><span class="sxs-lookup"><span data-stu-id="d7f7b-116"><dt>**LVSIL\_SMALL**</dt></span></span> </dl>                   | <span data-ttu-id="d7f7b-117">Bildliste mit kleinen Symbolen.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-117">Image list with small icons.</span></span><br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <span data-ttu-id="d7f7b-118"><dt>**Zustand "lvsil" \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7f7b-118"><dt>**LVSIL\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="d7f7b-119">Bildliste mit Zustands Bildern.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-119">Image list with state images.</span></span><br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <span data-ttu-id="d7f7b-120"><dt>**lvsil- \_ GroupHeader**</dt></span><span class="sxs-lookup"><span data-stu-id="d7f7b-120"><dt>**LVSIL\_GROUPHEADER**</dt></span></span> </dl> | <span data-ttu-id="d7f7b-121">Bildliste für Gruppen Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-121">Image list for group header.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="d7f7b-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7f7b-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7f7b-123">Handle der zuzuweisenden Bildliste.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-123">Handle to the image list to assign.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7f7b-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7f7b-124">Return value</span></span>

<span data-ttu-id="d7f7b-125">Gibt das Handle für die Bildliste zurück, die zuvor dem Steuerelement zugeordnet war, wenn erfolgreich, andernfalls **null** .</span><span class="sxs-lookup"><span data-stu-id="d7f7b-125">Returns the handle to the image list previously associated with the control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7f7b-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7f7b-126">Remarks</span></span>

<span data-ttu-id="d7f7b-127">Die aktuelle Bildliste wird zerstört, wenn das Listenansicht-Steuerelement zerstört wird, es sei denn, der LVS-Stil " [**\_ shareimagelists**](list-view-window-styles.md) " ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-127">The current image list will be destroyed when the list-view control is destroyed unless the [**LVS\_SHAREIMAGELISTS**](list-view-window-styles.md) style is set.</span></span> <span data-ttu-id="d7f7b-128">Wenn Sie diese Meldung verwenden, um eine Bildliste durch einen anderen zu ersetzen, muss Ihre Anwendung alle anderen Bildlisten explizit zerstören als die aktuelle.</span><span class="sxs-lookup"><span data-stu-id="d7f7b-128">If you use this message to replace one image list with another, your application must explicitly destroy all image lists other than the current one.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7f7b-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7f7b-129">Requirements</span></span>



| <span data-ttu-id="d7f7b-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7f7b-130">Requirement</span></span> | <span data-ttu-id="d7f7b-131">Wert</span><span class="sxs-lookup"><span data-stu-id="d7f7b-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f7b-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7f7b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d7f7b-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7f7b-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7f7b-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7f7b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d7f7b-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7f7b-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7f7b-136">Header</span><span class="sxs-lookup"><span data-stu-id="d7f7b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7f7b-137"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7f7b-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





