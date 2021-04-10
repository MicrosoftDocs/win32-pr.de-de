---
title: Hinzufügen einer ButtonGroup
description: Hinzufügen einer ButtonGroup
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- Erstellen von Skins, ButtonGroup-Element
- Windows Media Player Skins, ButtonGroup-Element
- Skins, ButtonGroup-Element
- Skin-Definitions Dateien, ButtonGroup-Element
- ButtonGroup-Element
- Elemente, ButtonGroup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90659a2e867a65d2751532701b71810a532c8ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309580"
---
# <a name="adding-buttongroup"></a><span data-ttu-id="fd16e-109">Hinzufügen einer ButtonGroup</span><span class="sxs-lookup"><span data-stu-id="fd16e-109">Adding BUTTONGROUP</span></span>

<span data-ttu-id="fd16e-110">In diesem Beispiel wird das **ButtonGroup** -Element für die Codierung in der Skin-Definitionsdatei verwendet.</span><span class="sxs-lookup"><span data-stu-id="fd16e-110">This example uses the **BUTTONGROUP** element for the coding in the skin definition file.</span></span> <span data-ttu-id="fd16e-111">**ButtonGroup** stellt eine einfache Möglichkeit zum Verarbeiten von Mausereignissen dar, ohne dass exakte Positionen auf dem Bildschirm berechnet werden müssen und anstelle von x-und y-Koordinaten Farben verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd16e-111">**BUTTONGROUP** creates an easy way to process mouse events without having to calculate exact locations on the screen and uses color instead of x and y-coordinates.</span></span>

<span data-ttu-id="fd16e-112">Zuerst müssen Sie der von Ihnen erstellten Skin-Definitionsdatei die **ButtonGroup** -Tags hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fd16e-112">First you must add the **BUTTONGROUP** tags to the skin definition file you created.</span></span> <span data-ttu-id="fd16e-113">Fügen Sie Sie nach **den Design** -Tagattributen ein.</span><span class="sxs-lookup"><span data-stu-id="fd16e-113">Put them after the **THEME** tag attributes.</span></span>


```C++
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">


        </BUTTONGROUP>

```



<span data-ttu-id="fd16e-114">Lassen Sie für die Schaltflächen, die Sie als nächstes hinzufügen, ein paar leere Zeilen oberhalb des schließenden **ButtonGroup** -Tags.</span><span class="sxs-lookup"><span data-stu-id="fd16e-114">Leave a few blank lines above the closing **BUTTONGROUP** tag for the buttons you will add next.</span></span>

<span data-ttu-id="fd16e-115">Die folgenden Attribute werden verwendet, um **ButtonGroup** zu definieren:</span><span class="sxs-lookup"><span data-stu-id="fd16e-115">The following attributes are used to define **BUTTONGROUP**:</span></span>

<span data-ttu-id="fd16e-116">**mappingImage**</span><span class="sxs-lookup"><span data-stu-id="fd16e-116">**mappingImage**</span></span>

<span data-ttu-id="fd16e-117">Dies ist der Dateiname der Datei, die Sie zuvor erstellt haben, die mit den roten und grünen Kreisen.</span><span class="sxs-lookup"><span data-stu-id="fd16e-117">This is the file name of the mapping art file you created before, the one with the red and green circles.</span></span> <span data-ttu-id="fd16e-118">Dieses Attribut ist für jede **ButtonGroup** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fd16e-118">This attribute is required for any **BUTTONGROUP**.</span></span>

<span data-ttu-id="fd16e-119">**hoverimage**</span><span class="sxs-lookup"><span data-stu-id="fd16e-119">**hoverImage**</span></span>

<span data-ttu-id="fd16e-120">Dies ist der Dateiname der Hover-Art-Datei, die Sie zuvor erstellt haben, die mit den beiden gelben Schaltflächen "Play" und "Close".</span><span class="sxs-lookup"><span data-stu-id="fd16e-120">This is the file name of the hover art file you created before, the one with the two yellow buttons that read "Play" and "Close".</span></span> <span data-ttu-id="fd16e-121">Dies ist nicht erforderlich, aber ein Hover-Bild hilft beim Bereitstellen von Feedback für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="fd16e-121">This is not required, but a hover image helps to provide feedback to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd16e-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd16e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd16e-123">**Erstellen der Skin-Definitionsdatei**</span><span class="sxs-lookup"><span data-stu-id="fd16e-123">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




