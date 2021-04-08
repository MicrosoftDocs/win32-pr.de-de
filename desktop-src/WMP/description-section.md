---
title: Abschnitt "Beschreibung"
description: Abschnitt "Beschreibung"
ms.assetid: 280a9a4d-935f-440d-a606-94aeba0007db
keywords:
- Windows Media Player Mobile Skins, Beschreibungs Abschnitt
- Skins, Beschreibungs Abschnitt
- Erstellen von Skins, Beschreibungs Abschnitt
- Schreiben von Code für Skins, Beschreibungs Abschnitt
- Beschreibungs Abschnitt in Skins
- Skin-Definitions Dateien, Beschreibungs Abschnitt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9518b6b1de128457dc3e6b3738ddab9be2a873
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856796"
---
# <a name="description-section"></a><span data-ttu-id="94cc1-109">Abschnitt "Beschreibung"</span><span class="sxs-lookup"><span data-stu-id="94cc1-109">Description Section</span></span>

<span data-ttu-id="94cc1-110">Als nächstes müssen Sie einen Abschnitt bereitstellen, der die Größe und Ausrichtung der Skin beim Erstellen eines Skin für Windows Media Player 9-Reihe für Windows Mobile 2003 und spätere Versionen beschreibt:</span><span class="sxs-lookup"><span data-stu-id="94cc1-110">Next, you must provide a section that describes the size and orientation of the skin when creating a skin for Windows Media Player 9 Series for Windows Mobile 2003 and later versions:</span></span>


```C++
[ Description ]
//              <X,Y>       <DPI>
//              ------      -----
    Dimensions  240, 320    96

//    <Orientation>
//    -------------
    Orientation Portrait

```



<span data-ttu-id="94cc1-111">Der Beschreibungs Abschnitt muss mit der Wort Beschreibung in Klammern beginnen und dann eine Zeile einschließen, in der die Abmessungen und die Bildschirmauflösung für die Skin angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="94cc1-111">The Description section must begin with the word Description in brackets, and then include a line that specifies the dimensions and display resolution for the skin.</span></span>

<span data-ttu-id="94cc1-112">Zeilen, die mit zwei Schrägstrichen beginnen, werden nicht verarbeitet und können für Kommentare verwendet werden, oder, wie im vorherigen Code gezeigt, eine Vorlage, die Ihnen hilft, sich zu merken, was in einem Abschnitt passiert.</span><span class="sxs-lookup"><span data-stu-id="94cc1-112">Lines beginning with two forward slashes are not processed, and can be used for comments or, as shown in the previous code, a template to help you remember what goes in a section.</span></span> <span data-ttu-id="94cc1-113">Sie können auch Vorlagen verwenden, um alles in Spalten auszurichten.</span><span class="sxs-lookup"><span data-stu-id="94cc1-113">You can also use templates to help align everything into columns.</span></span>

<span data-ttu-id="94cc1-114">Weitere Informationen zum Abschnitt Beschreibung finden Sie unter [Beschreibung](description.md) in der Skin-Referenz.</span><span class="sxs-lookup"><span data-stu-id="94cc1-114">For more information about the Description section, see [Description](description.md) in the Skin Reference.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94cc1-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94cc1-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94cc1-116">**Schreiben des Codes**</span><span class="sxs-lookup"><span data-stu-id="94cc1-116">**Writing the Code**</span></span>](writing-the-code.md)
</dt> </dl>

 

 




