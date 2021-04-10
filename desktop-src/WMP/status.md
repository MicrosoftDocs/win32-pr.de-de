---
title: Status (Windows Media Player SDK)
description: Status
ms.assetid: b8d6d026-819c-4889-a894-c82fe81ec922
keywords:
- Windows Media Player Mobile Skins, Statusanzeige
- Skins, Statusanzeige
- Verweis für Skins, Statusanzeige
- Statusanzeige in Skins, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f1cd9e0df209d6a37ed880765fd607e939765
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039929"
---
# <a name="status-windows-media-player-sdk"></a><span data-ttu-id="a58ef-107">Status (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="a58ef-107">Status (Windows Media Player SDK)</span></span>

<span data-ttu-id="a58ef-108">Möglicherweise möchten Sie eine Statusanzeige in der Skin verwenden.</span><span class="sxs-lookup"><span data-stu-id="a58ef-108">You may want to use a status display in your skin.</span></span> <span data-ttu-id="a58ef-109">Wenn dies der Fall ist, muss das Status-Element in der Skin-Definitionsdatei definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a58ef-109">If so, the status element must be defined in the skin definition file.</span></span> <span data-ttu-id="a58ef-110">Als Alternative können Sie diese Informationen auch mithilfe des Status-Attributs im Text-Element anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a58ef-110">As an alternative, you may also display this information by using the Status attribute in the Text element.</span></span>

<span data-ttu-id="a58ef-111">Der Status Abschnitt der Skin-Definitionsdatei beginnt mit der folgenden Zeile:</span><span class="sxs-lookup"><span data-stu-id="a58ef-111">The Status section of the skin definition file begins with this line:</span></span>


```C++
[ Status ]

```



<span data-ttu-id="a58ef-112">Anschließend müssen Sie eine oder mehrere Zeilen hinzufügen, die Informationen über die Statusanzeige in der Skin enthalten.</span><span class="sxs-lookup"><span data-stu-id="a58ef-112">You then must add one or more lines that contain information about the status display in your skin.</span></span>


```C++
    On           45,193,120,13    Left    Tahoma,8,B        0,255,  0

```



<span data-ttu-id="a58ef-113">Sie können die folgende Vorlage für den Status Abschnitt Ihrer Skin-Definitionsdatei verwenden:</span><span class="sxs-lookup"><span data-stu-id="a58ef-113">You can use the following template for the Status section of your skin definition file:</span></span>


```C++
//  <Item>       <Location>     <Align>  <Font>          <Color>
//  ------       ----------     -------  ------          -------

```



<span data-ttu-id="a58ef-114">Sie müssen die in der vorangehenden Vorlage gezeigte Reihenfolge für Statusanzeige Informationen für jede Zeile im Abschnitt Status verwenden.</span><span class="sxs-lookup"><span data-stu-id="a58ef-114">You must use the order shown in the preceding template for status display information for each line in the Status section.</span></span> <span data-ttu-id="a58ef-115">Jeder Teil der Zeile ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a58ef-115">Each part of the line is required.</span></span> <span data-ttu-id="a58ef-116">In den folgenden Abschnitten werden die einzelnen Elemente beschrieben:</span><span class="sxs-lookup"><span data-stu-id="a58ef-116">The following sections describe each item:</span></span>

-   [<span data-ttu-id="a58ef-117">Angezeigter Status</span><span class="sxs-lookup"><span data-stu-id="a58ef-117">Status Item</span></span>](status-item.md)
-   [<span data-ttu-id="a58ef-118">Status Speicherort</span><span class="sxs-lookup"><span data-stu-id="a58ef-118">Status Location</span></span>](status-location.md)
-   [<span data-ttu-id="a58ef-119">Status Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="a58ef-119">Status Alignment</span></span>](status-alignment.md)
-   [<span data-ttu-id="a58ef-120">Status Schriftart</span><span class="sxs-lookup"><span data-stu-id="a58ef-120">Status Font</span></span>](status-font.md)
-   [<span data-ttu-id="a58ef-121">Status Farbe</span><span class="sxs-lookup"><span data-stu-id="a58ef-121">Status Color</span></span>](status-color.md)

<span data-ttu-id="a58ef-122">Ein Beispiel für einen Statuscode finden Sie im [Abschnitt Sample Status](sample-status-section.md).</span><span class="sxs-lookup"><span data-stu-id="a58ef-122">For an example of Status code, see [Sample Status Section](sample-status-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a58ef-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a58ef-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a58ef-124">**Skin-Referenz**</span><span class="sxs-lookup"><span data-stu-id="a58ef-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




