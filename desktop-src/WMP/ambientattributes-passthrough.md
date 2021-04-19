---
title: Ambientattribute. Passthrough
description: Durch das Passthrough-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Steuerelement alle Mausereignisse an das Steuerelement darunter übergibt.
ms.assetid: 907ae233-3421-4e80-84be-64db4a3ab654
keywords:
- Ambientattribute. Passthrough-Windows-Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.passThrough
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b786aeefc182caab904c644dfd00ab4e76fec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367600"
---
# <a name="ambientattributespassthrough"></a><span data-ttu-id="06bfd-104">Ambientattribute. Passthrough</span><span class="sxs-lookup"><span data-stu-id="06bfd-104">AmbientAttributes.passThrough</span></span>

<span data-ttu-id="06bfd-105">Durch das **Passthrough** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Steuerelement alle Mausereignisse an das Steuerelement darunter übergibt.</span><span class="sxs-lookup"><span data-stu-id="06bfd-105">The **passThrough** attribute specifies or retrieves a value indicating whether the control will pass all mouse events through to the control under it.</span></span>

``` syntax
        elementID.passThrough
```

## <a name="possible-values"></a><span data-ttu-id="06bfd-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="06bfd-106">Possible Values</span></span>

<span data-ttu-id="06bfd-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="06bfd-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="06bfd-108">Wert</span><span class="sxs-lookup"><span data-stu-id="06bfd-108">Value</span></span> | <span data-ttu-id="06bfd-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06bfd-109">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="06bfd-110">true</span><span class="sxs-lookup"><span data-stu-id="06bfd-110">true</span></span>  | <span data-ttu-id="06bfd-111">Das Steuerelement übergibt Ereignisse an das Steuerelement darunter.</span><span class="sxs-lookup"><span data-stu-id="06bfd-111">Control passes events through to the control under it.</span></span> |
| <span data-ttu-id="06bfd-112">false</span><span class="sxs-lookup"><span data-stu-id="06bfd-112">false</span></span> | <span data-ttu-id="06bfd-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="06bfd-113">Default.</span></span> <span data-ttu-id="06bfd-114">Das Steuerelement übergibt Ereignisse nicht durch.</span><span class="sxs-lookup"><span data-stu-id="06bfd-114">Control does not pass events through.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="06bfd-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06bfd-115">Remarks</span></span>

<span data-ttu-id="06bfd-116">Dieses Attribut ist nützlich, wenn ein Text Steuerelement z. b. auf einem Schaltflächen-Steuerelement nur zur Angabe der Bezeichnung liegt.</span><span class="sxs-lookup"><span data-stu-id="06bfd-116">This attribute is useful if, for example, a text control sits on top of a button control only to provide labeling.</span></span> <span data-ttu-id="06bfd-117">In diesem Fall müssen Klicks auf das Text Steuerelement an das Schaltflächen-Steuerelement weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="06bfd-117">In this case, clicks on the text control must be passed through to the button control.</span></span>

<span data-ttu-id="06bfd-118">Das **Passthrough** -Attribut wird von den Elementen " **View**", " **subview**" und " **Playlist** " nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="06bfd-118">The **passThrough** attribute is not supported by the **VIEW**, **SUBVIEW**, and **PLAYLIST** elements.</span></span> <span data-ttu-id="06bfd-119">Es funktioniert nicht mit dem **Video** -Element, wenn es sich um *Video* handelt. **Windows less** ist auf false festgelegt, ebenso wie das **Effects** -Element bei *Effekten*. " **Fenster** " ist auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="06bfd-119">It will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if *EFFECTS*.**windowed** is set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="06bfd-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06bfd-120">Requirements</span></span>



| <span data-ttu-id="06bfd-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06bfd-121">Requirement</span></span> | <span data-ttu-id="06bfd-122">Wert</span><span class="sxs-lookup"><span data-stu-id="06bfd-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="06bfd-123">Version</span><span class="sxs-lookup"><span data-stu-id="06bfd-123">Version</span></span><br/> | <span data-ttu-id="06bfd-124">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="06bfd-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06bfd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06bfd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06bfd-126">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="06bfd-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





