---
title: ButtonGroup. Radio
description: Das Radio-Attribut gibt einen Wert an bzw. Ruft einen Wert ab, der angibt, ob die ButtonGroup aus Options Feldern besteht.
ms.assetid: f84479f8-af4f-4ca8-991e-1c2ab39d7110
keywords:
- ButtonGroup. Radio Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.radio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1765a7756aedcebc2b7b030634d8598a5cd89e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368642"
---
# <a name="buttongroupradio"></a><span data-ttu-id="bda08-104">ButtonGroup. Radio</span><span class="sxs-lookup"><span data-stu-id="bda08-104">BUTTONGROUP.radio</span></span>

<span data-ttu-id="bda08-105">Das **Radio** -Attribut gibt einen Wert an bzw. Ruft einen Wert ab, der angibt, ob die **ButtonGroup** aus Options Feldern besteht.</span><span class="sxs-lookup"><span data-stu-id="bda08-105">The **radio** attribute specifies or retrieves a value indicating whether the **BUTTONGROUP** is composed of radio buttons.</span></span>

``` syntax
        elementID.radio
```

## <a name="possible-values"></a><span data-ttu-id="bda08-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="bda08-106">Possible Values</span></span>

<span data-ttu-id="bda08-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="bda08-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="bda08-108">Wert</span><span class="sxs-lookup"><span data-stu-id="bda08-108">Value</span></span> | <span data-ttu-id="bda08-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bda08-109">Description</span></span>                                      |
|-------|--------------------------------------------------|
| <span data-ttu-id="bda08-110">true</span><span class="sxs-lookup"><span data-stu-id="bda08-110">true</span></span>  | <span data-ttu-id="bda08-111">Die **ButtonGroup** ist ein Optionsfeld.</span><span class="sxs-lookup"><span data-stu-id="bda08-111">The **BUTTONGROUP** is radio style.</span></span>              |
| <span data-ttu-id="bda08-112">false</span><span class="sxs-lookup"><span data-stu-id="bda08-112">false</span></span> | <span data-ttu-id="bda08-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="bda08-113">Default.</span></span> <span data-ttu-id="bda08-114">Die **ButtonGroup** ist kein Optionsfeld.</span><span class="sxs-lookup"><span data-stu-id="bda08-114">The **BUTTONGROUP** is not radio style.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bda08-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bda08-115">Remarks</span></span>

<span data-ttu-id="bda08-116">Wenn **Radio** auf true festgelegt ist, werden alle Button **Element** -Elemente in der **ButtonGroup** als Kurznotiz angezeigt, aber immer nur eine Schaltfläche im Zustand "gedrückt".</span><span class="sxs-lookup"><span data-stu-id="bda08-116">If **radio** is set to true, all the **BUTTONELEMENT** elements in the **BUTTONGROUP** will be sticky, but only one button at a time will be in the down state.</span></span>

## <a name="requirements"></a><span data-ttu-id="bda08-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bda08-117">Requirements</span></span>



| <span data-ttu-id="bda08-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bda08-118">Requirement</span></span> | <span data-ttu-id="bda08-119">Wert</span><span class="sxs-lookup"><span data-stu-id="bda08-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="bda08-120">Version</span><span class="sxs-lookup"><span data-stu-id="bda08-120">Version</span></span><br/> | <span data-ttu-id="bda08-121">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="bda08-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bda08-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bda08-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bda08-123">**ButtonElement. Kurznotiz**</span><span class="sxs-lookup"><span data-stu-id="bda08-123">**BUTTONELEMENT.sticky**</span></span>](buttonelement-sticky.md)
</dt> <dt>

[<span data-ttu-id="bda08-124">**ButtonGroup-Element**</span><span class="sxs-lookup"><span data-stu-id="bda08-124">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> </dl>

 

 





