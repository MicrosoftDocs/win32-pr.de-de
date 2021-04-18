---
title: LVM_MAPIDTOINDEX Meldung (kommstrg. h)
description: Ordnet die ID eines Elements einem Index zu.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_mapidtoindex.htm
keywords:
- Windows-Steuerelemente für LVM_MAPIDTOINDEX Meldung
topic_type:
- apiref
api_name:
- LVM_MAPIDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb4cb8aa49b37186ef689ed8cb319bbb92b62d75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343461"
---
# <a name="lvm_mapidtoindex-message"></a><span data-ttu-id="48a76-104">LVM- \_ mapiddeindex-Meldung</span><span class="sxs-lookup"><span data-stu-id="48a76-104">LVM\_MAPIDTOINDEX message</span></span>

<span data-ttu-id="48a76-105">Ordnet die ID eines Elements einem Index zu.</span><span class="sxs-lookup"><span data-stu-id="48a76-105">Maps the ID of an item to an index.</span></span>

## <a name="parameters"></a><span data-ttu-id="48a76-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48a76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48a76-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="48a76-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48a76-108">Die eindeutige ID eines Elements.</span><span class="sxs-lookup"><span data-stu-id="48a76-108">The unique ID of an item.</span></span>

</dd> <dt>

<span data-ttu-id="48a76-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="48a76-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="48a76-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="48a76-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48a76-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48a76-111">Return value</span></span>

<span data-ttu-id="48a76-112">Gibt den aktuellen Index zurück.</span><span class="sxs-lookup"><span data-stu-id="48a76-112">Returns the most current index.</span></span>

## <a name="remarks"></a><span data-ttu-id="48a76-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48a76-113">Remarks</span></span>

<span data-ttu-id="48a76-114">Listenansicht-Steuerelemente nachverfolgen Elemente intern nach Index.</span><span class="sxs-lookup"><span data-stu-id="48a76-114">List-view controls internally track items by index.</span></span> <span data-ttu-id="48a76-115">Dies kann Probleme darstellen, da Indizes sich während der Lebensdauer des Steuer Elements ändern können.</span><span class="sxs-lookup"><span data-stu-id="48a76-115">This can present problems because indexes can change during the control's lifetime.</span></span>

<span data-ttu-id="48a76-116">Das Listenansicht-Steuerelement kann ein Element mit einer ID markieren, wenn das Element erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="48a76-116">The list-view control can tag an item with an ID when the item is created.</span></span> <span data-ttu-id="48a76-117">Sie können diese ID verwenden, um die Eindeutigkeit während der Lebensdauer des Listenansicht-Steuer Elements sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="48a76-117">You can use this ID to guarantee uniqueness during the lifetime of the list-view control.</span></span>

<span data-ttu-id="48a76-118">Wenn Sie ein Element eindeutig identifizieren möchten, nehmen Sie den Index an, der von einem-Befehl wie [**IComponent:: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) zurückgegeben wird, und nennen Sie [**LVM \_ mapindextoid**](lvm-mapindextoid.md).</span><span class="sxs-lookup"><span data-stu-id="48a76-118">To uniquely identify an item, take the index that is returned from a call such as [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) and call [**LVM\_MAPINDEXTOID**](lvm-mapindextoid.md).</span></span> <span data-ttu-id="48a76-119">Der Rückgabewert ist eine eindeutige ID.</span><span class="sxs-lookup"><span data-stu-id="48a76-119">The return value is a unique ID.</span></span>

<span data-ttu-id="48a76-120">Wenn Sie den Index eines Elements benötigen, nachdem eine ID erstellt wurde, können Sie **LVM \_ mapidtoindex** mit der eindeutigen ID aufrufen und den aktuellen Index zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="48a76-120">If you need the index of an item after an ID is created you can call **LVM\_MAPIDTOINDEX** with the unique ID and it returns the most current index.</span></span>

<span data-ttu-id="48a76-121">**LVM \_ Mapidumindex** wird unter dem [**LVS-Besitzer \_ Daten**](list-view-window-styles.md) Stil nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="48a76-121">**LVM\_MAPIDTOINDEX** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="48a76-122">In einer Multithreadumgebung wird der Index nur für den Thread garantiert, der das Listenansicht-Steuerelement hostet, nicht für Hintergrundthreads.</span><span class="sxs-lookup"><span data-stu-id="48a76-122">In a multithreaded environment, the index is only guaranteed on the thread that hosts the list-view control, not on background threads.</span></span>

 

> [!Note]  
> <span data-ttu-id="48a76-123">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="48a76-123">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="48a76-124">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="48a76-124">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="48a76-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48a76-125">Requirements</span></span>



| <span data-ttu-id="48a76-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48a76-126">Requirement</span></span> | <span data-ttu-id="48a76-127">Wert</span><span class="sxs-lookup"><span data-stu-id="48a76-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="48a76-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48a76-128">Minimum supported client</span></span><br/> | <span data-ttu-id="48a76-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48a76-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48a76-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48a76-130">Minimum supported server</span></span><br/> | <span data-ttu-id="48a76-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48a76-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="48a76-132">Header</span><span class="sxs-lookup"><span data-stu-id="48a76-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="48a76-133"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="48a76-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

