---
title: Ambientattribute. Visible
description: Das Visible-Attribut gibt die Sichtbarkeit für das Steuerelement an oder ruft Sie ab.
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- Ambientattribute. Visible Windows-Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72794b7bbba0237a687dc70bda761c505b839e59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369205"
---
# <a name="ambientattributesvisible"></a><span data-ttu-id="0c8fb-104">Ambientattribute. Visible</span><span class="sxs-lookup"><span data-stu-id="0c8fb-104">AmbientAttributes.visible</span></span>

<span data-ttu-id="0c8fb-105">Das **Visible** -Attribut gibt die Sichtbarkeit für das Steuerelement an oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="0c8fb-105">The **visible** attribute specifies or retrieves the visibility for the control.</span></span>

``` syntax
        elementID.visible
```

## <a name="possible-values"></a><span data-ttu-id="0c8fb-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="0c8fb-106">Possible Values</span></span>

<span data-ttu-id="0c8fb-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0c8fb-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="0c8fb-108">Wert</span><span class="sxs-lookup"><span data-stu-id="0c8fb-108">Value</span></span> | <span data-ttu-id="0c8fb-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c8fb-109">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="0c8fb-110">true</span><span class="sxs-lookup"><span data-stu-id="0c8fb-110">true</span></span>  | <span data-ttu-id="0c8fb-111">Standard.</span><span class="sxs-lookup"><span data-stu-id="0c8fb-111">Default.</span></span> <span data-ttu-id="0c8fb-112">Das Steuerelement ist sichtbar.</span><span class="sxs-lookup"><span data-stu-id="0c8fb-112">The control is visible.</span></span> |
| <span data-ttu-id="0c8fb-113">false</span><span class="sxs-lookup"><span data-stu-id="0c8fb-113">false</span></span> | <span data-ttu-id="0c8fb-114">Das Steuerelement ist nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="0c8fb-114">The control is not visible.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="0c8fb-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c8fb-115">Remarks</span></span>

<span data-ttu-id="0c8fb-116">Dieses Attribut ist nützlich zum Ausblenden von Steuerelementen, z. b. beim Austauschen einer Pause-Schaltfläche für eine Wiedergabe Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="0c8fb-116">This attribute is useful for hiding controls, for example when swapping a pause button for a play button.</span></span>

<span data-ttu-id="0c8fb-117">Wenn der Wert false ist, ist das Steuerelement nicht sichtbar, und die Click-Ereignisse werden an das dahinter liegende Steuerelement übermittelt.</span><span class="sxs-lookup"><span data-stu-id="0c8fb-117">If the value is false, the control is not visible and click events are passed to the control behind it.</span></span> <span data-ttu-id="0c8fb-118">Wenn der Wert true ist, ist das Steuerelement sichtbar und empfängt das Click-Ereignis selbst.</span><span class="sxs-lookup"><span data-stu-id="0c8fb-118">If the value is true, the control is visible and receives the click event itself.</span></span>

<span data-ttu-id="0c8fb-119">Der Standardwert für das **automenu** -Element ist false.</span><span class="sxs-lookup"><span data-stu-id="0c8fb-119">The default value for the **AUTOMENU** element is false.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c8fb-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c8fb-120">Requirements</span></span>



| <span data-ttu-id="0c8fb-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c8fb-121">Requirement</span></span> | <span data-ttu-id="0c8fb-122">Wert</span><span class="sxs-lookup"><span data-stu-id="0c8fb-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0c8fb-123">Version</span><span class="sxs-lookup"><span data-stu-id="0c8fb-123">Version</span></span><br/> | <span data-ttu-id="0c8fb-124">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="0c8fb-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c8fb-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c8fb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c8fb-126">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="0c8fb-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





