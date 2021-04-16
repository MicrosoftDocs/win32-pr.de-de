---
title: LVM_MAPINDEXTOID Meldung (kommstrg. h)
description: Ordnet den Index eines Elements einer eindeutigen ID zu.
ms.assetid: d0486e21-2703-4289-abb0-f5f9c7b60b40
keywords:
- Windows-Steuerelemente für LVM_MAPINDEXTOID Meldung
topic_type:
- apiref
api_name:
- LVM_MAPINDEXTOID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a2a5de558b025e61bef26fd20278f125372769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476089"
---
# <a name="lvm_mapindextoid-message"></a><span data-ttu-id="98e92-104">LVM \_ mapindextoid-Meldung</span><span class="sxs-lookup"><span data-stu-id="98e92-104">LVM\_MAPINDEXTOID message</span></span>

<span data-ttu-id="98e92-105">Ordnet den Index eines Elements einer eindeutigen ID zu.</span><span class="sxs-lookup"><span data-stu-id="98e92-105">Maps the index of an item to a unique ID.</span></span>

## <a name="parameters"></a><span data-ttu-id="98e92-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="98e92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98e92-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="98e92-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98e92-108">Der Index eines Elements.</span><span class="sxs-lookup"><span data-stu-id="98e92-108">The index of an item.</span></span>

</dd> <dt>

<span data-ttu-id="98e92-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98e92-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98e92-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="98e92-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98e92-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98e92-111">Return value</span></span>

<span data-ttu-id="98e92-112">Gibt eine eindeutige ID zurück.</span><span class="sxs-lookup"><span data-stu-id="98e92-112">Returns a unique ID.</span></span>

## <a name="remarks"></a><span data-ttu-id="98e92-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98e92-113">Remarks</span></span>

<span data-ttu-id="98e92-114">Listenansicht-Steuerelemente nachverfolgen Elemente intern nach Index.</span><span class="sxs-lookup"><span data-stu-id="98e92-114">List-view controls internally track items by index.</span></span> <span data-ttu-id="98e92-115">Dies kann Probleme darstellen, da Indizes sich während der Lebensdauer des Steuer Elements ändern können.</span><span class="sxs-lookup"><span data-stu-id="98e92-115">This can present problems because indexes can change during the control's lifetime.</span></span>

<span data-ttu-id="98e92-116">Das Listenansicht-Steuerelement kann ein Element mit einer ID markieren, wenn das Element erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="98e92-116">The list-view control can tag an item with an ID when the item is created.</span></span> <span data-ttu-id="98e92-117">Sie können diese ID verwenden, um die Eindeutigkeit während der Lebensdauer des Listenansicht-Steuer Elements sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="98e92-117">You can use this ID to guarantee uniqueness during the lifetime of the list-view control.</span></span>

<span data-ttu-id="98e92-118">Wenn Sie ein Element eindeutig identifizieren möchten, nehmen Sie den Index an, der von einem-Befehl wie [**IComponent:: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) zurückgegeben wird, und nennen Sie **LVM \_ mapindextoid**.</span><span class="sxs-lookup"><span data-stu-id="98e92-118">To uniquely identify an item, take the index that is returned from a call such as [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) and call **LVM\_MAPINDEXTOID**.</span></span> <span data-ttu-id="98e92-119">Der Rückgabewert ist eine eindeutige ID.</span><span class="sxs-lookup"><span data-stu-id="98e92-119">The return value is a unique ID.</span></span>

> [!Note]  
> <span data-ttu-id="98e92-120">In einer Multithreadumgebung wird der Index nur für den Thread garantiert, der das Listenansicht-Steuerelement hostet, nicht für Hintergrundthreads.</span><span class="sxs-lookup"><span data-stu-id="98e92-120">In a multithreaded environment, the index is only guaranteed on the thread that hosts the list-view control, not on background threads.</span></span>

 

> [!Note]  
> <span data-ttu-id="98e92-121">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="98e92-121">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="98e92-122">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="98e92-122">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="98e92-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98e92-123">Requirements</span></span>



| <span data-ttu-id="98e92-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98e92-124">Requirement</span></span> | <span data-ttu-id="98e92-125">Wert</span><span class="sxs-lookup"><span data-stu-id="98e92-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98e92-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98e92-126">Minimum supported client</span></span><br/> | <span data-ttu-id="98e92-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98e92-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="98e92-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98e92-128">Minimum supported server</span></span><br/> | <span data-ttu-id="98e92-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98e92-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="98e92-130">Header</span><span class="sxs-lookup"><span data-stu-id="98e92-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="98e92-131"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="98e92-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

