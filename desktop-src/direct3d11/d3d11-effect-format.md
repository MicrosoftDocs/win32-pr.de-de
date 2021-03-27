---
title: Effekt Format (Direct3D 11)
ms.assetid: c425f57b-fc14-46a5-bb65-a0a2305bd406
description: 'Weitere Informationen zum: Effekt Format (Direct3D 11)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c08589fcb041591591d033b88e4fafe597e98520
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214134"
---
# <a name="effect-format-direct3d-11"></a><span data-ttu-id="e8e21-103">Effekt Format (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="e8e21-103">Effect Format (Direct3D 11)</span></span>

<span data-ttu-id="e8e21-104">Ein Effekt (der häufig in einer Datei mit der Dateierweiterung ". FX" gespeichert ist) deklariert den Pipeline Status, der durch einen Effekt festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e8e21-104">An effect (which is often stored in a file with a .fx file extension) declares the pipeline state set by an effect.</span></span> <span data-ttu-id="e8e21-105">Der Effekt Zustand kann ungefähr in drei Kategorien unterteilt werden:</span><span class="sxs-lookup"><span data-stu-id="e8e21-105">Effect state can be roughly broken down into three categories:</span></span>

-   <span data-ttu-id="e8e21-106">[Variablen](d3d11-effect-variable-syntax.md), die in der Regel am Anfang eines Effekts deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="e8e21-106">[Variables](d3d11-effect-variable-syntax.md), which are usually declared at the top of an effect.</span></span>
-   <span data-ttu-id="e8e21-107">[Funktionen](d3d11-effect-function-syntax.md), die Shader-Code implementieren oder von anderen Funktionen als Hilfsfunktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8e21-107">[Functions](d3d11-effect-function-syntax.md), which implement shader code, or are used as helper functions by other functions.</span></span>
-   <span data-ttu-id="e8e21-108">[Techniken](d3d11-effect-technique-syntax.md), die in Wirkungs Gruppen angeordnet werden können, und Implementieren von renderingsequenzen mithilfe mindestens eines Effekts.</span><span class="sxs-lookup"><span data-stu-id="e8e21-108">[Techniques](d3d11-effect-technique-syntax.md), which can be arranged in effect groups, and implement rendering sequences using one or more effect passes.</span></span> <span data-ttu-id="e8e21-109">Jeder Durchlauf legt eine oder mehrere [Zustands Gruppen fest](d3d11-effect-states.md) und ruft Shaderfunktionen auf.</span><span class="sxs-lookup"><span data-stu-id="e8e21-109">Each pass sets one or more [state groups](d3d11-effect-states.md) and calls shader functions.</span></span>

![Diagramm der Kategorien von Deklarationen für Effekte, einschließlich Variablen oben, Funktionen in der Mitte und Techniken im unteren Bereich](images/d3d10-effect-intro.png)

<span data-ttu-id="e8e21-111">Das obige Diagramm zeigt die Kategorien des Wirkungs Zustands.</span><span class="sxs-lookup"><span data-stu-id="e8e21-111">The preceding diagram shows the categories of effect state.</span></span>

<span data-ttu-id="e8e21-112">Die Definition des Effekt Binär Formats finden Sie in \\ der "effectbinaryformat. h"-Datei im Effekt Quell Code.</span><span class="sxs-lookup"><span data-stu-id="e8e21-112">The definition of the effect binary format can be found in Binary\\EffectBinaryFormat.h in the effects source code.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="e8e21-113">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="e8e21-113">In this section</span></span>



| <span data-ttu-id="e8e21-114">Thema</span><span class="sxs-lookup"><span data-stu-id="e8e21-114">Topic</span></span>                                                                   | <span data-ttu-id="e8e21-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8e21-115">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8e21-116">Syntax der Effekt Variablen</span><span class="sxs-lookup"><span data-stu-id="e8e21-116">Effect Variable Syntax</span></span>](d3d11-effect-variable-syntax.md)<br/>   | <span data-ttu-id="e8e21-117">Eine Effekt Variable wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="e8e21-117">An effect variable is declared with the syntax described in this section.</span></span><br/>                                 |
| [<span data-ttu-id="e8e21-118">Syntax der Anmerkung</span><span class="sxs-lookup"><span data-stu-id="e8e21-118">Annotation Syntax</span></span>](d3d11-effect-annotation-syntax.md)<br/>      | <span data-ttu-id="e8e21-119">Eine Anmerkung ist ein benutzerdefiniertes Informationselement, das mit der in diesem Abschnitt beschriebenen Syntax deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="e8e21-119">An annotation is a user-defined piece of information, declared with the syntax described in this section.</span></span><br/> |
| [<span data-ttu-id="e8e21-120">Syntax der Effekt Funktion</span><span class="sxs-lookup"><span data-stu-id="e8e21-120">Effect Function Syntax</span></span>](d3d11-effect-function-syntax.md)<br/>   | <span data-ttu-id="e8e21-121">Eine Effekt Funktion ist in HLSL geschrieben und wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="e8e21-121">An effect function is written in HLSL and is declared with the syntax described in this section.</span></span><br/>          |
| [<span data-ttu-id="e8e21-122">Syntax der Effekt Technik</span><span class="sxs-lookup"><span data-stu-id="e8e21-122">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)<br/> | <span data-ttu-id="e8e21-123">Eine Effekt Technik wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="e8e21-123">An effect technique is declared with the syntax described in this section.</span></span><br/>                                |
| [<span data-ttu-id="e8e21-124">Effekt Zustands Gruppen</span><span class="sxs-lookup"><span data-stu-id="e8e21-124">Effect State Groups</span></span>](d3d11-effect-states.md)<br/>               | <span data-ttu-id="e8e21-125">Effekt Zustände sind Name-Wert-Paare in Form eines Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="e8e21-125">Effect states are name value pairs in the form of an expression.</span></span><br/>                                          |
| [<span data-ttu-id="e8e21-126">Effekt Gruppen Syntax</span><span class="sxs-lookup"><span data-stu-id="e8e21-126">Effect Group Syntax</span></span>](d3d11-effect-group-syntax.md)<br/>         | <span data-ttu-id="e8e21-127">Eine Effekt Gruppe wird mit der in diesem Abschnitt beschriebenen Syntax deklariert.</span><span class="sxs-lookup"><span data-stu-id="e8e21-127">An effect group is declared with the syntax described in this section.</span></span><br/>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="e8e21-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e8e21-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8e21-129">Auswirkung 11-Referenz</span><span class="sxs-lookup"><span data-stu-id="e8e21-129">Effects 11 Reference</span></span>](d3d11-graphics-reference-effects11.md)
</dt> </dl>

 

 





