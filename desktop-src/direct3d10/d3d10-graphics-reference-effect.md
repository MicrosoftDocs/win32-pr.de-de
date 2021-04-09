---
description: Die Direct3D-API definiert mehrere API-Elemente, die Sie beim Erstellen und Verwalten des Effekt Systems unterstützen.
ms.assetid: d3b0b7a2-0820-4bb1-8b9e-c6b55a039963
title: Effekt Referenz (Direct3D 10-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c903959096e1192555fd813a256d03fb1969fa9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958350"
---
# <a name="effect-reference-direct3d-10-graphics"></a><span data-ttu-id="a4c79-103">Effekt Referenz (Direct3D 10-Grafiken)</span><span class="sxs-lookup"><span data-stu-id="a4c79-103">Effect Reference (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="a4c79-104">Die Direct3D-API definiert mehrere API-Elemente, die Sie beim Erstellen und Verwalten des Effekt Systems unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a4c79-104">The Direct3D API defines several API elements to help you create and manage the effect system.</span></span>

-   [<span data-ttu-id="a4c79-105">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a4c79-105">Interfaces</span></span>](d3d10-graphics-reference-effect-interfaces.md)
-   [<span data-ttu-id="a4c79-106">Funktionen</span><span class="sxs-lookup"><span data-stu-id="a4c79-106">Functions</span></span>](d3d10-graphics-reference-effect-functions.md)
-   [<span data-ttu-id="a4c79-107">Strukturen</span><span class="sxs-lookup"><span data-stu-id="a4c79-107">Structures</span></span>](d3d10-graphics-reference-effect-structures.md)
-   [<span data-ttu-id="a4c79-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="a4c79-108">Constants</span></span>](d3d10-graphics-reference-effect-constants.md)

<span data-ttu-id="a4c79-109">Das Effektsystem kapselt Zustands Zuweisungen in einem Effekt.</span><span class="sxs-lookup"><span data-stu-id="a4c79-109">The effect system encapsulates state assignments in an effect.</span></span> <span data-ttu-id="a4c79-110">Jeder Effekt ist eine Auflistung von Pipeline Zuständen, die unter Verwendung von Zustands Blöcken, Ressourcen und Shadern in Zustands Zuweisungen aufgeteilt werden können.</span><span class="sxs-lookup"><span data-stu-id="a4c79-110">Each effect is a collection of pipeline state which can be broken down into state assignments using state blocks, resources, and shaders.</span></span> <span data-ttu-id="a4c79-111">Abhängig von der Größe eines Effekts können Sie auswählen, ob Sie einen in einer ASCII-Text Zeichenfolge oder einer Effekt Datei (. fx) implementieren möchten.</span><span class="sxs-lookup"><span data-stu-id="a4c79-111">Depending on the size of an effect, you can choose to implement one in an ASCII text string or an effect file (.fx).</span></span> <span data-ttu-id="a4c79-112">Informationen zum Organisieren von Informationen finden Sie im [Effekt Format](d3d10-effect-format.md).</span><span class="sxs-lookup"><span data-stu-id="a4c79-112">To organize information in an effect, see the [effect format](d3d10-effect-format.md).</span></span>

<span data-ttu-id="a4c79-113">Wenn Sie einen Effekt entwickelt haben, verwenden Sie die Effekt-API, um den Status im Gerät beim Rendern festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a4c79-113">Having designed an effect, use the effect API to set state in the device during rendering.</span></span> <span data-ttu-id="a4c79-114">Das Effect-System unterstützt auch eine Reihe von reflektionsapis, um Effekt Daten zu erhalten und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a4c79-114">As well, the effect system supports a series of reflection API's for getting and setting effect data.</span></span> <span data-ttu-id="a4c79-115">Weitere Informationen finden Sie unter [Effect System Interfaces (Direct3D 10)](d3d10-graphics-programming-guide-effects-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="a4c79-115">For more information, see [Effect System Interfaces (Direct3D 10)](d3d10-graphics-programming-guide-effects-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4c79-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a4c79-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4c79-117">Direct3D-Referenz</span><span class="sxs-lookup"><span data-stu-id="a4c79-117">Direct3D Reference</span></span>](d3d10-graphics-reference-d3d10.md)
</dt> </dl>

 

 



