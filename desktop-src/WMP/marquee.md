---
title: Marquee
description: Marquee
ms.assetid: 2715732a-25cc-4ba9-9aa6-181ebb9e1d1c
keywords:
- Windows Media Player Mobile Skins, marquees
- Skins, marquees
- Referenz für Skins, marquees
- marquees in Skins, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7efa2db2c6079d47d207240b18a57ebbf7e41ae1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388541"
---
# <a name="marquee"></a><span data-ttu-id="2a40b-107">Marquee</span><span class="sxs-lookup"><span data-stu-id="2a40b-107">Marquee</span></span>

<span data-ttu-id="2a40b-108">Ein Marquee ist ein Bild Lauf Text-Anzeige Feld, in dem Informationen von einem oder mehreren Textanzeige Feldern angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2a40b-108">A marquee is a scrolling text display box that displays information from one or more text display boxes.</span></span> <span data-ttu-id="2a40b-109">Sie müssen kein Marquee hinzufügen, aber es kann sehr nützlich sein, wenn Sie ausführliche Informationen haben, die Sie dem Benutzer in begrenztem Raum anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="2a40b-109">You do not need to add a marquee, but it can be very useful when you have detailed information you want to display to the user in a limited space.</span></span>

<span data-ttu-id="2a40b-110">Der Text im Marquee führt nur dann einen Bildlauf durch, wenn die beiden folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="2a40b-110">The text in the marquee will scroll only if both of the following conditions are met:</span></span>

-   <span data-ttu-id="2a40b-111">Sie haben mehr Text, der im Marquee angezeigt werden soll als die Breite des Marquee-Anzeige Felds.</span><span class="sxs-lookup"><span data-stu-id="2a40b-111">You have more text to display in the marquee than the width of the marquee display box.</span></span>
-   <span data-ttu-id="2a40b-112">Das Medien Element wird entweder beendet oder angehalten.</span><span class="sxs-lookup"><span data-stu-id="2a40b-112">The media item is either stopped or paused.</span></span>

<span data-ttu-id="2a40b-113">Der Marquee-Abschnitt der Skin-Definitionsdatei muss mit der folgenden Zeile beginnen:</span><span class="sxs-lookup"><span data-stu-id="2a40b-113">The Marquee section of the skin definition file must begin with this line:</span></span>


```C++
[ Marquee ]

```



> [!Note]  
> <span data-ttu-id="2a40b-114">Um die Kompatibilität mit Versionen von Windows Media Player Mobile zu gewährleisten, die älter als Windows Media Player 10 Mobile sind, wird die Verwendung von "Marquis" in einer Skin-Definitionsdatei weiterhin als gültig betrachtet.</span><span class="sxs-lookup"><span data-stu-id="2a40b-114">To maintain compatibility with versions of Windows Media Player Mobile older than Windows Media Player 10 Mobile, using "Marquis" in a skin definition file is still considered valid.</span></span>

 

<span data-ttu-id="2a40b-115">Anschließend müssen Sie eine oder mehrere Zeilen hinzufügen, die Informationen zu jedem der Marquee-Anzeigefelder in der Skin enthalten.</span><span class="sxs-lookup"><span data-stu-id="2a40b-115">You then must add one or more lines that contain information about each of the marquee display boxes in your skin.</span></span>


```C++
    3,2,234,20   Tahoma,12,N  255,0,0    Playlist, Time, Filename

```



<span data-ttu-id="2a40b-116">Sie können die folgende Vorlage für den Marquee-Abschnitt Ihrer Skin-Definitionsdatei verwenden:</span><span class="sxs-lookup"><span data-stu-id="2a40b-116">You can use the following template for the Marquee section of your skin definition file:</span></span>


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------

```



<span data-ttu-id="2a40b-117">Sie müssen die folgende Reihenfolge für Informationen in den einzelnen Zeilen des Marquee-Abschnitts verwenden (jeder Teil der Zeile ist erforderlich):</span><span class="sxs-lookup"><span data-stu-id="2a40b-117">You must use the following order for information in each line of the Marquee section (each part of the line is required):</span></span>

1.  [<span data-ttu-id="2a40b-118">Marquee-Speicherort</span><span class="sxs-lookup"><span data-stu-id="2a40b-118">Marquee Location</span></span>](marquee-location.md)
2.  [<span data-ttu-id="2a40b-119">Marquee-Schriftart</span><span class="sxs-lookup"><span data-stu-id="2a40b-119">Marquee Font</span></span>](marquee-font.md)
3.  [<span data-ttu-id="2a40b-120">Marquee-Farbe</span><span class="sxs-lookup"><span data-stu-id="2a40b-120">Marquee Color</span></span>](marquee-color.md)
4.  [<span data-ttu-id="2a40b-121">Text Kombinationen</span><span class="sxs-lookup"><span data-stu-id="2a40b-121">Text Combinations</span></span>](text-combinations.md)

<span data-ttu-id="2a40b-122">Ein Beispiel für einen Marquee-Code finden Sie unter [Sample Marquee section](sample-marquee-section.md).</span><span class="sxs-lookup"><span data-stu-id="2a40b-122">For an example of Marquee code, see [Sample Marquee Section](sample-marquee-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a40b-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2a40b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a40b-124">**Skin-Referenz**</span><span class="sxs-lookup"><span data-stu-id="2a40b-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




