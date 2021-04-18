---
description: Ein Effekt (der häufig in einer Datei mit der Dateierweiterung ". FX" gespeichert ist) deklariert den Pipeline Status, der durch einen Effekt festgelegt wird.
ms.assetid: 75b76d65-be97-41c2-8c45-4369fcfd69ce
title: Effekt Format (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5671750d7b4146ae5da8b0ba61ceae390b60a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393221"
---
# <a name="effect-format-direct3d-10"></a><span data-ttu-id="18dcd-103">Effekt Format (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="18dcd-103">Effect Format (Direct3D 10)</span></span>

<span data-ttu-id="18dcd-104">Ein Effekt (der häufig in einer Datei mit der Dateierweiterung ". FX" gespeichert ist) deklariert den Pipeline Status, der durch einen Effekt festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="18dcd-104">An effect (which is often stored in a file with a .fx file extension) declares the pipeline state set by an effect.</span></span> <span data-ttu-id="18dcd-105">Der Effekt Zustand kann ungefähr in drei Kategorien unterteilt werden:</span><span class="sxs-lookup"><span data-stu-id="18dcd-105">Effect state can be roughly broken down into three categories:</span></span>

-   <span data-ttu-id="18dcd-106">[Variablen](d3d10-effect-variable-syntax.md), die in der Regel am Anfang eines Effekts deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="18dcd-106">[Variables](d3d10-effect-variable-syntax.md), which are usually declared at the top of an effect.</span></span>
-   <span data-ttu-id="18dcd-107">[Funktionen](d3d10-effect-function-syntax.md), die Shader-Code implementieren oder von anderen Funktionen als Hilfsfunktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18dcd-107">[Functions](d3d10-effect-function-syntax.md), which implement shader code, or are used as helper functions by other functions.</span></span>
-   <span data-ttu-id="18dcd-108">[Eine Technik](d3d10-effect-technique-syntax.md), die renderingsequenzen mit einem oder mehreren Effekt Sequenzen implementiert.</span><span class="sxs-lookup"><span data-stu-id="18dcd-108">[A technique](d3d10-effect-technique-syntax.md), which implements rendering sequences using one or more effect passes.</span></span> <span data-ttu-id="18dcd-109">Jeder Durchlauf legt eine oder mehrere [Zustands Gruppen fest](d3d10-effect-states.md) und ruft Shaderfunktionen auf.</span><span class="sxs-lookup"><span data-stu-id="18dcd-109">Each pass sets one or more [state groups](d3d10-effect-states.md) and calls shader functions.</span></span>

![Diagramm der Kategorien des Wirkungs Zustands](images/d3d10-effect-intro.png)

<span data-ttu-id="18dcd-111">Das obige Diagramm zeigt die Kategorien des Wirkungs Zustands.</span><span class="sxs-lookup"><span data-stu-id="18dcd-111">The preceding diagram shows the categories of effect state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18dcd-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="18dcd-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18dcd-113">Effekt Referenz</span><span class="sxs-lookup"><span data-stu-id="18dcd-113">Effect Reference</span></span>](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



