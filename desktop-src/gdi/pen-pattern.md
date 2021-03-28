---
description: Das Pattern-Attribut gibt das Muster eines geometrischen Stifts an.
ms.assetid: 5a330416-3b83-4f0f-825c-80e47903966e
title: Stift Muster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577b5e2cb31e44a4631760c82e678af069322cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528298"
---
# <a name="pen-pattern"></a><span data-ttu-id="e32f8-103">Stift Muster</span><span class="sxs-lookup"><span data-stu-id="e32f8-103">Pen Pattern</span></span>

<span data-ttu-id="e32f8-104">Das Pattern-Attribut gibt das Muster eines geometrischen Stifts an.</span><span class="sxs-lookup"><span data-stu-id="e32f8-104">The pattern attribute specifies the pattern of a geometric pen.</span></span>

<span data-ttu-id="e32f8-105">Die folgende Abbildung zeigt Linien, die mit unterschiedlichen geometrischen stiften gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="e32f8-105">The following illustration shows lines drawn with different geometric pens.</span></span> <span data-ttu-id="e32f8-106">Jeder Stift wurde mit einem anderen Pattern-Attribut erstellt.</span><span class="sxs-lookup"><span data-stu-id="e32f8-106">Each pen was created using a different pattern attribute.</span></span>

![Abbildung, die vier Zeilen anzeigt, die jeweils mit einem anderen Stift gefüllt sind](images/cspen-02.png)

<span data-ttu-id="e32f8-108">Die erste Zeile in der vorherigen Abbildung wird mit einem der sechs verfügbaren Schraffurmuster gezeichnet. Weitere Informationen zu Schraffurmustern finden Sie unter [Stift Schraffur](pen-hatch.md).</span><span class="sxs-lookup"><span data-stu-id="e32f8-108">The first line in the previous illustration is drawn using one of the six available hatch patterns; for more information about hatch patterns, see [Pen Hatch](pen-hatch.md).</span></span> <span data-ttu-id="e32f8-109">Die nächste Zeile wird mithilfe des hohlen Musters gezeichnet, das mit dem NULL-Muster identisch ist.</span><span class="sxs-lookup"><span data-stu-id="e32f8-109">The next line is drawn using the hollow pattern, identical to the null pattern.</span></span> <span data-ttu-id="e32f8-110">Die dritte Zeile wird mithilfe eines benutzerdefinierten Musters gezeichnet, das aus einer 8-x-8-Pixel-Bitmap erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e32f8-110">The third line is drawn using a custom pattern created from an 8-by-8-pixel bitmap.</span></span> <span data-ttu-id="e32f8-111">(Weitere Informationen zu Bitmaps und deren Erstellung finden Sie unter [Bitmaps](bitmaps.md).) Die letzte Zeile wird mithilfe eines voll soliden Musters gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e32f8-111">(For more information about bitmaps and their creation, see [Bitmaps](bitmaps.md).) The last line is drawn using a solid pattern.</span></span> <span data-ttu-id="e32f8-112">Durch das Erstellen eines Pinsels und das Übergeben des Handles an die [**extkreatepen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) -Funktion wird ein Muster erstellt.</span><span class="sxs-lookup"><span data-stu-id="e32f8-112">Creating a brush and passing its handle to the [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function creates a pattern.</span></span>

 

 



