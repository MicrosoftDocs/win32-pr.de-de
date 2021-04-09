---
title: LVM_ARRANGE Meldung (kommstrg. h)
description: Ordnet Elemente in der Symbol Ansicht an. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ Makros anordnen senden.
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- Windows-Steuerelemente für LVM_ARRANGE Meldung
topic_type:
- apiref
api_name:
- LVM_ARRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b6a081cf963a649329951358ea4c972f200f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102910"
---
# <a name="lvm_arrange-message"></a><span data-ttu-id="b07a2-105">LVM- \_ Anordnungs Nachricht</span><span class="sxs-lookup"><span data-stu-id="b07a2-105">LVM\_ARRANGE message</span></span>

<span data-ttu-id="b07a2-106">Ordnet Elemente in der Symbol Ansicht an.</span><span class="sxs-lookup"><span data-stu-id="b07a2-106">Arranges items in icon view.</span></span> <span data-ttu-id="b07a2-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView-Makros \_ anordnen**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) senden.</span><span class="sxs-lookup"><span data-stu-id="b07a2-107">You can send this message explicitly or by using the [**ListView\_Arrange**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b07a2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b07a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b07a2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b07a2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b07a2-110">Einer der folgenden Werte, der die Ausrichtung angibt:</span><span class="sxs-lookup"><span data-stu-id="b07a2-110">One of the following values that specifies alignment:</span></span>



| <span data-ttu-id="b07a2-111">Wert</span><span class="sxs-lookup"><span data-stu-id="b07a2-111">Value</span></span>                                                                                                                                                            | <span data-ttu-id="b07a2-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b07a2-112">Meaning</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <span data-ttu-id="b07a2-113"><dt>**LVA \_ alignleft**</dt></span><span class="sxs-lookup"><span data-stu-id="b07a2-113"><dt>**LVA\_ALIGNLEFT**</dt></span></span> </dl>    | <span data-ttu-id="b07a2-114">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b07a2-114">Not implemented.</span></span> <span data-ttu-id="b07a2-115">Wenden Sie stattdessen den [**LVS \_ alignleft**](list-view-window-styles.md) -Stil an.</span><span class="sxs-lookup"><span data-stu-id="b07a2-115">Apply the [**LVS\_ALIGNLEFT**](list-view-window-styles.md) style instead.</span></span><br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <span data-ttu-id="b07a2-116"><dt>**LVA \_ AlignTop**</dt></span><span class="sxs-lookup"><span data-stu-id="b07a2-116"><dt>**LVA\_ALIGNTOP**</dt></span></span> </dl>       | <span data-ttu-id="b07a2-117">Nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b07a2-117">Not implemented.</span></span> <span data-ttu-id="b07a2-118">Verwenden Sie stattdessen den [**LVS \_ AlignTop**](list-view-window-styles.md) -Stil.</span><span class="sxs-lookup"><span data-stu-id="b07a2-118">Apply the [**LVS\_ALIGNTOP**](list-view-window-styles.md) style instead.</span></span><br/>   |
| <span id="LVA_DEFAULT"></span><span id="lva_default"></span><dl> <span data-ttu-id="b07a2-119"><dt>**LVA- \_ Standard**</dt></span><span class="sxs-lookup"><span data-stu-id="b07a2-119"><dt>**LVA\_DEFAULT**</dt></span></span> </dl>          | <span data-ttu-id="b07a2-120">Richtet Elemente gemäß den aktuellen Ausrichtungs Stilen des Listenansicht-Steuer Elements (Standardwert) aus.</span><span class="sxs-lookup"><span data-stu-id="b07a2-120">Aligns items according to the list-view control's current alignment styles (the default value).</span></span><br/>           |
| <span id="LVA_SNAPTOGRID"></span><span id="lva_snaptogrid"></span><dl> <span data-ttu-id="b07a2-121"><dt>**LVA- \_ snapragrid**</dt></span><span class="sxs-lookup"><span data-stu-id="b07a2-121"><dt>**LVA\_SNAPTOGRID**</dt></span></span> </dl> | <span data-ttu-id="b07a2-122">Andoppt alle Symbole an die nächste Raster Position.</span><span class="sxs-lookup"><span data-stu-id="b07a2-122">Snaps all icons to the nearest grid position.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="b07a2-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b07a2-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b07a2-124">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="b07a2-124">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b07a2-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b07a2-125">Return value</span></span>

<span data-ttu-id="b07a2-126">Gibt **true** zurück, wenn erfolgreich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="b07a2-126">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b07a2-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b07a2-127">Requirements</span></span>



| <span data-ttu-id="b07a2-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b07a2-128">Requirement</span></span> | <span data-ttu-id="b07a2-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b07a2-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b07a2-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b07a2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b07a2-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b07a2-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b07a2-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b07a2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b07a2-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b07a2-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b07a2-134">Header</span><span class="sxs-lookup"><span data-stu-id="b07a2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b07a2-135"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b07a2-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





