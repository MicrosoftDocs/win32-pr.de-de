---
title: Informationen zu den CDROM-und cdromcollection-Objekten
description: Informationen zu den CDROM-und cdromcollection-Objekten
ms.assetid: b764806b-d9e1-4c36-b86b-24613501c926
keywords:
- Windows Media Player, cdrom-Objekt
- Windows Media Player-Objektmodell, cdrom-Objekt
- Objektmodell, cdrom-Objekt
- Windows Media Player ActiveX-Steuerelement, cdrom-Objekt
- ActiveX-Steuerelement, cdrom-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, cdrom-Objekt
- Windows Media Player Mobile, cdrom-Objekt
- Cdrom-Objekt
- Windows Media Player, cdromcollection-Objekt
- Windows Media Player-Objektmodell, cdromcollection-Objekt
- Objektmodell, cdromcollection-Objekt
- Windows Media Player ActiveX-Steuerelement, cdromcollection-Objekt
- ActiveX-Steuerelement, cdromcollection-Objekt
- Windows Media Player Mobile ActiveX-Steuerelement, cdromcollection-Objekt
- Windows Media Player Mobile, cdromcollection-Objekt
- Cdromcollection-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8fca9f7097f67226e31173670ca2935969704a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711400"
---
# <a name="about-the-cdrom-and-cdromcollection-objects"></a><span data-ttu-id="f0b4d-119">Informationen zu den CDROM-und cdromcollection-Objekten</span><span class="sxs-lookup"><span data-stu-id="f0b4d-119">About the Cdrom and CdromCollection Objects</span></span>

<span data-ttu-id="f0b4d-120">Die **Crom** -und **cdromcollection** -Objekte steuern die Schnittstelle zu den CD-Laufwerken Ihres Computers zum Lesen und Abspielen von CDs.</span><span class="sxs-lookup"><span data-stu-id="f0b4d-120">The **Cdrom** and **CdromCollection** objects govern the interface to the CD drives in your computer for purposes of reading and playing CDs.</span></span>

<span data-ttu-id="f0b4d-121">Der Zugriff auf das **cdromcollection** -Objekt erfolgt nur über die **cdromcollection** -Eigenschaft des **Player** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f0b4d-121">The **CdromCollection** object is accessed only through the **cdromCollection** property of the **Player** object.</span></span> <span data-ttu-id="f0b4d-122">Die **cdromcollection** -Eigenschaft gibt das **cdromcollection** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="f0b4d-122">The **cdromCollection** property returns the **CdromCollection** object.</span></span> <span data-ttu-id="f0b4d-123">Sie können nur auf die Eigenschaften des **cdromcollection** -Objekts zugreifen, nachdem Sie es erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="f0b4d-123">You can only access the properties of the **CdromCollection** object after you have created it.</span></span> <span data-ttu-id="f0b4d-124">Wenn Sie z. b. die **count** -Eigenschaft verwenden möchten, müssen Sie den folgenden Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="f0b4d-124">For example, to use the **count** property, you must use the following code:</span></span>


```C++
mycount = player.cdromcollection.count;
```



<span data-ttu-id="f0b4d-125">Sie können nur über das **cdromcollection** -Objekt auf das **CDROM** -Objekt zugreifen.</span><span class="sxs-lookup"><span data-stu-id="f0b4d-125">You can only access the **Cdrom** object through the **CdromCollection** object.</span></span> <span data-ttu-id="f0b4d-126">Wenn Sie z. b. die CD mithilfe der **auswerfen** -Methode auswerfen möchten, müssen Sie zuerst das Sammlungsobjekt und dann ein Element im-Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="f0b4d-126">For example, to eject the CD by using the **Eject** method, you must first create the collection object and then an item in the object.</span></span> <span data-ttu-id="f0b4d-127">Verwenden Sie zum Auswerfen der CD den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="f0b4d-127">To eject the CD, use the following code:</span></span>


```C++
player.cdromcollection.item(0).eject();
```



<span data-ttu-id="f0b4d-128">In beiden Fällen erstellen Sie zuerst das Auflistungs Objekt (**cdromcollection**) und dann ein bestimmtes Objekt dieser Sammlung.</span><span class="sxs-lookup"><span data-stu-id="f0b4d-128">In both cases, you are first creating the collection object (**CdromCollection**) and then getting a specific object of that collection.</span></span> <span data-ttu-id="f0b4d-129">Das-Objekt ist das erste Element in der Auflistung, **Element**(0), das dem ersten CD-Laufwerk entspricht.</span><span class="sxs-lookup"><span data-stu-id="f0b4d-129">The object is the first item in the collection, **Item**(0), which corresponds to the first CD drive.</span></span> <span data-ttu-id="f0b4d-130">Anschließend wird die Methode **eject** für dieses Element aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f0b4d-130">You then call a method, **Eject**, on that item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0b4d-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0b4d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0b4d-132">**Cdrom-Objekt**</span><span class="sxs-lookup"><span data-stu-id="f0b4d-132">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="f0b4d-133">**Cdromcollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="f0b4d-133">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="f0b4d-134">**Player-Objektmodell für Skriptsprachen**</span><span class="sxs-lookup"><span data-stu-id="f0b4d-134">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




