---
title: Text (Windows Media Player SDK)
description: Text
ms.assetid: 8c10cefb-d0d0-4214-8712-d171a76de95d
keywords:
- Windows Media Player Mobile Skins, Text
- Skins, Text
- Verweis für Skins, Text
- Text in Skins, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801d93698bc7a17eea34df71514dd88b485f0d9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103858614"
---
# <a name="text-windows-media-player-sdk"></a><span data-ttu-id="9b08a-107">Text (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="9b08a-107">Text (Windows Media Player SDK)</span></span>

<span data-ttu-id="9b08a-108">Möglicherweise möchten Sie ein oder mehrere Textanzeige Felder in der Skin verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b08a-108">You may want to use one or more text display boxes in your skin.</span></span> <span data-ttu-id="9b08a-109">Jedes verwendete Textanzeige Feld muss in der Skin-Definitionsdatei definiert werden.</span><span class="sxs-lookup"><span data-stu-id="9b08a-109">Each text display box you use must be defined in the skin definition file.</span></span> <span data-ttu-id="9b08a-110">Wenn Sie in diesem Abschnitt kein Textfeld für die Anzeige definieren, kann es von der Skin nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b08a-110">If you do not define a text display box in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="9b08a-111">Der Text Abschnitt der Skin-Definitionsdatei beginnt mit der folgenden Zeile:</span><span class="sxs-lookup"><span data-stu-id="9b08a-111">The Text section of the skin definition file begins with this line:</span></span>


```C++
[ Text ]

```



<span data-ttu-id="9b08a-112">Sie müssen dann mindestens eine Zeile hinzufügen, die Informationen zu jedem der Textanzeige Felder in der Skin enthält.</span><span class="sxs-lookup"><span data-stu-id="9b08a-112">You then must add one or more lines that contain information about each of the text display boxes in your skin</span></span>


```C++
    Time         180,46,50,30   Right    Tahoma,16,N     255,255,255

```



<span data-ttu-id="9b08a-113">Sie können die folgende Vorlage für den Text Abschnitt der Skin-Definitionsdatei verwenden:</span><span class="sxs-lookup"><span data-stu-id="9b08a-113">You can use the following template for the Text section of your skin definition file:</span></span>


```C++
//  <Type>       <Location>     <Align> <Font>          <Color>
//  ------       ----------     ------- ------          -------

```



<span data-ttu-id="9b08a-114">Sie müssen die in der vorangehenden Vorlage gezeigte Reihenfolge für Textanzeige Feldinformationen für jede Zeile im Textabschnitt verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b08a-114">You must use the order shown in the preceding template for text display box information for each line in the Text section.</span></span> <span data-ttu-id="9b08a-115">Jeder Teil der Zeile ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9b08a-115">Each part of the line is required.</span></span> <span data-ttu-id="9b08a-116">In den folgenden Abschnitten werden die einzelnen Elemente ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9b08a-116">The following sections describe each item in detail.</span></span>

1.  [<span data-ttu-id="9b08a-117">Texttyp</span><span class="sxs-lookup"><span data-stu-id="9b08a-117">Text Type</span></span>](text-type.md)
2.  [<span data-ttu-id="9b08a-118">Text Speicherort</span><span class="sxs-lookup"><span data-stu-id="9b08a-118">Text Location</span></span>](text-location.md)
3.  [<span data-ttu-id="9b08a-119">Text Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="9b08a-119">Text Alignment</span></span>](text-alignment.md)
4.  [<span data-ttu-id="9b08a-120">Text Schriftart</span><span class="sxs-lookup"><span data-stu-id="9b08a-120">Text Font</span></span>](text-font.md)
5.  [<span data-ttu-id="9b08a-121">Textfarbe</span><span class="sxs-lookup"><span data-stu-id="9b08a-121">Text Color</span></span>](text-color.md)

<span data-ttu-id="9b08a-122">Ein Beispiel für Textcode finden Sie unter [Sample Text section](sample-text-section.md).</span><span class="sxs-lookup"><span data-stu-id="9b08a-122">For an example of Text code, see [Sample Text Section](sample-text-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b08a-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9b08a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b08a-124">**Skin-Referenz**</span><span class="sxs-lookup"><span data-stu-id="9b08a-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




