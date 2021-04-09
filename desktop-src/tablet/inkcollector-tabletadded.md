---
description: Tritt auf, wenn ein iinktablet zum System hinzugefügt wird.
ms.assetid: c5f90fce-faf7-411b-a4d6-deb5d0f22f4a
title: InkCollector. TabletAdded-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f18f66a45570b269d36efc012f543a8b25e23f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958758"
---
# <a name="inkcollectortabletadded-event"></a><span data-ttu-id="44758-103">InkCollector. TabletAdded-Ereignis</span><span class="sxs-lookup"><span data-stu-id="44758-103">InkCollector.TabletAdded event</span></span>

<span data-ttu-id="44758-104">Tritt auf, wenn ein [**iinktablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) zum System hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="44758-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="44758-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="44758-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="44758-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="44758-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44758-107">*Tablet* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44758-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44758-108">Das [**iinktablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) -Objekt, das dem System hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="44758-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44758-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44758-109">Return value</span></span>

<span data-ttu-id="44758-110">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="44758-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44758-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44758-111">Remarks</span></span>

<span data-ttu-id="44758-112">Diese Ereignismethode wird in den \_ Schnittstellen iinkcollectorevents, \_ iinkoverlayevents und \_ iinkpictureevents Dispatch-only (Dispinterfaces) mit der ID DISPID \_ icetabletadded definiert.</span><span class="sxs-lookup"><span data-stu-id="44758-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="44758-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44758-113">Requirements</span></span>



| <span data-ttu-id="44758-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44758-114">Requirement</span></span> | <span data-ttu-id="44758-115">Wert</span><span class="sxs-lookup"><span data-stu-id="44758-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44758-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44758-116">Minimum supported client</span></span><br/> | <span data-ttu-id="44758-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44758-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="44758-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44758-118">Minimum supported server</span></span><br/> | <span data-ttu-id="44758-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="44758-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="44758-120">Header</span><span class="sxs-lookup"><span data-stu-id="44758-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="44758-121"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="44758-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="44758-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="44758-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="44758-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44758-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="44758-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44758-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44758-125">**InkCollector-Klasse**</span><span class="sxs-lookup"><span data-stu-id="44758-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="44758-126">**Iinktablet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="44758-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




