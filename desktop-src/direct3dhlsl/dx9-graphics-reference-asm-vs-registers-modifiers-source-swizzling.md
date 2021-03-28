---
title: Quellen Register (swizzling) (HLSL vs-Referenz)
description: Bevor eine Anweisung ausgeführt wird, werden die Daten in einem Quell Register in ein temporäres Register kopiert. Swizzling bezieht sich auf die Möglichkeit, beliebige Quell Registrierungs Komponenten in beliebige temporäre Register Komponenten zu kopieren. Das Schwenken wirkt sich nicht auf die Quell Registrierungsdaten aus.
ms.assetid: 6271d846-c68d-467c-a110-be3279e0c11a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c075d8ff47b1f76adf378b6a583cd4d675651a87
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104389620"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a><span data-ttu-id="1b199-105">Quellen Register (swizzling) (HLSL vs-Referenz)</span><span class="sxs-lookup"><span data-stu-id="1b199-105">Source Register Swizzling (HLSL VS reference)</span></span>

<span data-ttu-id="1b199-106">Bevor eine Anweisung ausgeführt wird, werden die Daten in einem Quell Register in ein temporäres Register kopiert.</span><span class="sxs-lookup"><span data-stu-id="1b199-106">Before an instruction runs, the data in a source register is copied to a temporary register.</span></span> <span data-ttu-id="1b199-107">Swizzling bezieht sich auf die Möglichkeit, beliebige Quell Registrierungs Komponenten in beliebige temporäre Register Komponenten zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="1b199-107">Swizzling refers to the ability to copy any source register component to any temporary register component.</span></span> <span data-ttu-id="1b199-108">Das Schwenken wirkt sich nicht auf die Quell Registrierungsdaten aus.</span><span class="sxs-lookup"><span data-stu-id="1b199-108">Swizzling does not affect the source register data.</span></span>

## <a name="component-swizzling"></a><span data-ttu-id="1b199-109">Komponenten schwenken</span><span class="sxs-lookup"><span data-stu-id="1b199-109">Component Swizzling</span></span>

<span data-ttu-id="1b199-110">Wie in der folgenden Tabelle gezeigt, kann das Schwenken auf die einzelnen Komponenten der Quell Registrierungsdaten angewendet werden (wobei es sich bei um einen der gültigen Vertex-Shader [-Eingabe Register-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)handelt).</span><span class="sxs-lookup"><span data-stu-id="1b199-110">As shown in the following table, swizzling can be applied to the individual components of the source register data (where r is one of the valid vertex shader input [Registers - vs\_1\_1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).</span></span>



| <span data-ttu-id="1b199-111">Komponentenmodifizierer</span><span class="sxs-lookup"><span data-stu-id="1b199-111">Component modifier</span></span>                 | <span data-ttu-id="1b199-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b199-112">Description</span></span>    |
|------------------------------------|----------------|
| <span data-ttu-id="1b199-113">r. \[ xyzw xyzw xyzw xyzw \] \[ \] \[ \] \[\]</span><span class="sxs-lookup"><span data-stu-id="1b199-113">r.\[xyzw\]\[xyzw\]\[xyzw\]\[xyzw\]</span></span> | <span data-ttu-id="1b199-114">Quellen-wischen</span><span class="sxs-lookup"><span data-stu-id="1b199-114">Source swizzle</span></span> |



 

-   <span data-ttu-id="1b199-115">Alle vier Komponenten werden immer kopiert.</span><span class="sxs-lookup"><span data-stu-id="1b199-115">All four components are always copied.</span></span> <span data-ttu-id="1b199-116">Wenn weniger als vier Komponenten angegeben werden, wird die letzte Komponente wiederholt (XY means. XYYY).</span><span class="sxs-lookup"><span data-stu-id="1b199-116">If fewer than four components are specified, the last component is repeated (xy means .xyyy).</span></span> <span data-ttu-id="1b199-117">Wenn keine Komponenten angegeben werden, wird x wiederholt (. xxxx).</span><span class="sxs-lookup"><span data-stu-id="1b199-117">If no components are specified, x is repeated (.xxxx).</span></span>
-   <span data-ttu-id="1b199-118">Die Komponenten können in beliebiger Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1b199-118">The components can appear in any order.</span></span> <span data-ttu-id="1b199-119">"v0. ywx" ergibt "v0. ywxx".</span><span class="sxs-lookup"><span data-stu-id="1b199-119">v0.ywx results in v0.ywxx.</span></span>
-   <span data-ttu-id="1b199-120">Die RGBA-Komponenten können für xyzw verwendet werden (r für x, g für b usw.).</span><span class="sxs-lookup"><span data-stu-id="1b199-120">The rgba components can be used respectively for xyzw (r for x, g for b, etc.).</span></span>
-   <span data-ttu-id="1b199-121">Diese Anweisungen implementieren Quellen Register für einzelne Komponenten: Exp, EXPP, Log, LogP, Pow, rcp, RSQ.</span><span class="sxs-lookup"><span data-stu-id="1b199-121">These instructions implement source-register single component swizzles: exp, expp, log, logp, pow, rcp, rsq.</span></span> <span data-ttu-id="1b199-122">Das Ergebnis dieser Anweisungen wird in alle vier Ziel Register Komponenten kopiert.</span><span class="sxs-lookup"><span data-stu-id="1b199-122">The result of these instructions is copied to all four destination register components.</span></span>

<span data-ttu-id="1b199-123">"Swizzling" kann nicht in den Anweisungen [m3x2-vs](m3x2---vs.md), [M3x3-vs](m3x3---vs.md), [m4x3-vs](m4x3---vs.md)und [M4x4-vs](m4x4---vs.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b199-123">Swizzling cannot be used on the [m3x2 - vs](m3x2---vs.md), [m3x3 - vs](m3x3---vs.md), [m4x3 - vs](m4x3---vs.md), and [m4x4 - vs](m4x4---vs.md) instructions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b199-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1b199-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b199-125">Vertex-Shader-registermodifiziererer</span><span class="sxs-lookup"><span data-stu-id="1b199-125">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




