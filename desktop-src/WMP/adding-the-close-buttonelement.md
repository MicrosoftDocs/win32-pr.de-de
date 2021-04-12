---
title: Hinzufügen des schließenden ButtonElement
description: Hinzufügen des schließenden ButtonElement
ms.assetid: 18f0ee9d-b0d4-4134-8dd6-6ece480b2818
keywords:
- Erstellen von Skins, ButtonElement-Element
- Windows Media Player Skins, ButtonElement-Element
- Skins, ButtonElement-Element
- Skin-Definitions Dateien, ButtonElement-Element
- ButtonElement-Element
- Elemente, ButtonElement
- Erstellen von Skins, schließen von Schaltflächen
- Windows Media Player Skins, schließen von Schaltflächen
- Skins, Schaltflächen Schließen
- Skin-Definitions Dateien, schließen-Schaltflächen
- Schließen von Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40716d4094d23eaf6ab86414f37c0778cc8d89cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206854"
---
# <a name="adding-the-close-buttonelement"></a><span data-ttu-id="69e43-114">Hinzufügen des schließenden ButtonElement</span><span class="sxs-lookup"><span data-stu-id="69e43-114">Adding the Close BUTTONELEMENT</span></span>

<span data-ttu-id="69e43-115">Die Schaltfläche Schließen ähnelt dem Konzept der Wiedergabe Schaltfläche, verfügt aber über unterschiedliche Codes und Farben.</span><span class="sxs-lookup"><span data-stu-id="69e43-115">The Close button is similar in concept to the Play button, but has different codes and colors.</span></span>

<span data-ttu-id="69e43-116">Fügen Sie den schließenden **ButtonElement** -Code nach der schließenden Spitze Klammer des Wiedergabe- **buttonelements** ein.</span><span class="sxs-lookup"><span data-stu-id="69e43-116">Put the Close **BUTTONELEMENT** code after the closing angle bracket of the Play **BUTTONELEMENT**.</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick="JScript: view.close();" />

```



<span data-ttu-id="69e43-117">Die folgenden Attribute werden verwendet, um das **ButtonElement** für die Schaltfläche "Schließen" zu definieren:</span><span class="sxs-lookup"><span data-stu-id="69e43-117">The following attributes are used to define the **BUTTONELEMENT** for the Close button:</span></span>

<span data-ttu-id="69e43-118">**mappingColor**</span><span class="sxs-lookup"><span data-stu-id="69e43-118">**mappingColor**</span></span>

<span data-ttu-id="69e43-119">Dies ist der Farbwert des Bereichs in der Mappings-Grafikdatei, den Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="69e43-119">This is the color value of the region in the mapping art file you created before.</span></span> <span data-ttu-id="69e43-120">In diesem Fall ist es die rote Farbe.</span><span class="sxs-lookup"><span data-stu-id="69e43-120">In this case it is the solid red color.</span></span> <span data-ttu-id="69e43-121">Dieses Attribut ist für ein beliebiges **ButtonElement** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="69e43-121">This attribute is required for any **BUTTONELEMENT**.</span></span> <span data-ttu-id="69e43-122">Wenn Sie diese Farbe definieren, sagen Sie Windows Media Player, diesen Farbbereich dem XML-Code dieser Schaltfläche zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="69e43-122">By defining this color, you are telling Windows Media Player to associate this color area with the XML code of this button.</span></span>

<span data-ttu-id="69e43-123">**uptooltip**</span><span class="sxs-lookup"><span data-stu-id="69e43-123">**upToolTip**</span></span>

<span data-ttu-id="69e43-124">Dadurch wird der Text definiert, der angezeigt wird, wenn der Benutzer mit dem Mauszeiger auf die Schaltfläche bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="69e43-124">This defines the text that will be displayed when the user hovers the mouse over the button.</span></span> <span data-ttu-id="69e43-125">Dies ist identisch mit der Wiedergabe Schaltfläche, mit der Ausnahme, dass Sie mit "Close" gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="69e43-125">This is the same as the Play button except that it is labeled "Close".</span></span>

<span data-ttu-id="69e43-126">**OnClick**</span><span class="sxs-lookup"><span data-stu-id="69e43-126">**onClick**</span></span>

<span data-ttu-id="69e43-127">Definiert das Ereignis, das auftritt, wenn mit der Maus auf die Schaltfläche geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="69e43-127">This defines the event that occurs when the mouse clicks on the button.</span></span> <span data-ttu-id="69e43-128">Der Wert dieses Ereignis Attributs wird als Ereignishandler bezeichnet und ist entweder eine Zeile von Microsoft JScript-Code oder eine JScript-Funktion in einer externen Textdatei, die vom **loadscript** -Attribut einer **Ansicht** geladen wird.</span><span class="sxs-lookup"><span data-stu-id="69e43-128">The value of this event attribute is called an event handler and will be either a line of Microsoft JScript code, or a JScript function in an external text file that is loaded by the **loadScript** attribute of a **VIEW**.</span></span> <span data-ttu-id="69e43-129">In diesem Fall ruft der JScript-Code die **Close** -Methode des **Ansichts** Elements mithilfe der globalen Attribut **Ansicht** auf, die die Ansicht schließt und Windows-Media Player herunterfährt.</span><span class="sxs-lookup"><span data-stu-id="69e43-129">In this case, the JScript code calls the **close** method of the **VIEW** element using the global attribute **view**, which closes the view and shuts down Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69e43-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="69e43-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69e43-131">**Erstellen der Skin-Definitionsdatei**</span><span class="sxs-lookup"><span data-stu-id="69e43-131">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




