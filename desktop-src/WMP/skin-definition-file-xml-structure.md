---
title: XML-Struktur der Skin-Definitionsdatei
description: XML-Struktur der Skin-Definitionsdatei
ms.assetid: 93325b94-667a-42a6-92f8-78288d36da81
keywords:
- Erstellen von Skins, Skin-Definitions Dateien
- Windows Media Player Skins, Skin-Definitions Dateien
- Skins, Skin-Definitions Dateien
- Dateien für Skins, Skin-Definition
- Skin-Definitions Dateien, XML-Struktur
- XML-Struktur für Skin-Definitions Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8508f1a458930bc2b60d564a45ef08a9f9f5a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037228"
---
# <a name="skin-definition-file-xml-structure"></a><span data-ttu-id="9f1f5-109">XML-Struktur der Skin-Definitionsdatei</span><span class="sxs-lookup"><span data-stu-id="9f1f5-109">Skin Definition File XML Structure</span></span>

<span data-ttu-id="9f1f5-110">Die Skin-Definitionsdatei ist in XML geschrieben.</span><span class="sxs-lookup"><span data-stu-id="9f1f5-110">The skin definition file is written in XML.</span></span> <span data-ttu-id="9f1f5-111">Eines der wichtigen Features von XML ist, dass es vollständig strukturiert ist und einem Umriss ähnelt.</span><span class="sxs-lookup"><span data-stu-id="9f1f5-111">One of the important features of XML is that it is completely structured, and is similar to an outline.</span></span> <span data-ttu-id="9f1f5-112">Der XML-Code ist einfach eine Reihe von Elementen, wie z. b. **View** und **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="9f1f5-112">The XML code is simply a series of elements such as **VIEW** and **BUTTONGROUP**.</span></span> <span data-ttu-id="9f1f5-113">Sie beginnen mit den-Elementen und definieren Sie dann mit Attributen.</span><span class="sxs-lookup"><span data-stu-id="9f1f5-113">You will start with the elements and then define them with attributes.</span></span> <span data-ttu-id="9f1f5-114">Im weiteren Verlauf dieses Tutorials erhalten Sie Details zu den Attributen, aber hier finden Sie die Gliederung der Elemente, die verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="9f1f5-114">The rest of this tutorial will give you details on the attributes, but here is the outline of the elements that will be used:</span></span>


```C++
<THEME>
    <VIEW>
        <BUTTONGROUP>
            <BUTTONELEMENT/>
            <BUTTONELEMENT/>
        </BUTTONGROUP>
    </VIEW>
<THEME>

```



<span data-ttu-id="9f1f5-115">Wenn Sie die einfache Struktur der Elemente beachten, können Sie die Attribute, die die einzelnen Elemente eindeutig machen, sinnvoll gestalten.</span><span class="sxs-lookup"><span data-stu-id="9f1f5-115">By keeping in mind the simple structure of the elements, you can make sense of the attributes that make each element unique.</span></span> <span data-ttu-id="9f1f5-116">Details zu den einzelnen Elementen werden in den restlichen Themen dieses Abschnitts behandelt.</span><span class="sxs-lookup"><span data-stu-id="9f1f5-116">Details of each element will be covered in the remaining topics of this section.</span></span> <span data-ttu-id="9f1f5-117">Weitere Informationen zu Elementen und Attributen finden Sie in der [Skin-Programmier Referenz](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9f1f5-117">For more information about elements and attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f1f5-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9f1f5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f1f5-119">**Erstellen der Skin-Definitionsdatei**</span><span class="sxs-lookup"><span data-stu-id="9f1f5-119">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




