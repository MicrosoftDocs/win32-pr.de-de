---
title: Ziel Register Maskierung
description: Die Maskierung gibt an, welche Komponenten des Ziel Registers mit dem Ergebnis einer Anweisung aktualisiert werden. Textur Register verfügen über einen Regelsatz, und nicht Textur Register verfügen über einen anderen Satz von Regeln.
ms.assetid: 989ebe55-1f80-4063-b116-4284520f52cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ce15f75f424cb7796ef7db7a8b89bd5bcbfa9cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388520"
---
# <a name="destination-register-masking"></a><span data-ttu-id="ab16a-104">Ziel Register Maskierung</span><span class="sxs-lookup"><span data-stu-id="ab16a-104">Destination Register Masking</span></span>

<span data-ttu-id="ab16a-105">Die Maskierung gibt an, welche Komponenten des Ziel Registers mit dem Ergebnis einer Anweisung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ab16a-105">Masking specifies which components of the destination register will be updated with the result of an instruction.</span></span> <span data-ttu-id="ab16a-106">Textur Register verfügen über einen Regelsatz, und nicht Textur Register verfügen über einen anderen Satz von Regeln.</span><span class="sxs-lookup"><span data-stu-id="ab16a-106">Texture registers have one set of rules and nontexture registers have another set of rules.</span></span>

-   <span data-ttu-id="ab16a-107">DX9 \_ Graphics \_ Reference \_ ASM \_ vs \_ registriert \_ \_ modifizierermaskierung: Dieser Abschnitt enthält Regeln zum Anwenden von Masken auf Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="ab16a-107">dx9\_graphics\_reference\_asm\_vs\_registers\_modifiers\_masking - This section contains rules for applying masks to destination registers.</span></span>
-   <span data-ttu-id="ab16a-108">Textur \_ Register \_ Masken: Textur Register verfügen über einige eindeutige Regeln.</span><span class="sxs-lookup"><span data-stu-id="ab16a-108">Texture\_Register\_Masks - Texture registers have some unique rules.</span></span>

## <a name="destination-register-masking"></a><span data-ttu-id="ab16a-109">Ziel Register Maskierung</span><span class="sxs-lookup"><span data-stu-id="ab16a-109">Destination Register Masking</span></span>

<span data-ttu-id="ab16a-110">Wie in der folgenden Tabelle gezeigt, kann die Maskierung (wobei eine der gültigen Vertex-Shader- [Register für Vertex-Shader](dx9-graphics-reference-asm-vs-registers.md)ist) auf die einzelnen Komponenten der Vektordaten angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab16a-110">As shown in the following table, masking (where r is one of the valid vertex shader [Vertex Shader Registers](dx9-graphics-reference-asm-vs-registers.md)) can be applied to the individual components of the vector data.</span></span>



| <span data-ttu-id="ab16a-111">Komponentenmodifizierer</span><span class="sxs-lookup"><span data-stu-id="ab16a-111">Component modifier</span></span> | <span data-ttu-id="ab16a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab16a-112">Description</span></span>      |
|--------------------|------------------|
| <span data-ttu-id="ab16a-113">r. {x} {y} {z} {w}</span><span class="sxs-lookup"><span data-stu-id="ab16a-113">r.{x}{y}{z}{w}</span></span>     | <span data-ttu-id="ab16a-114">Ziel Maske</span><span class="sxs-lookup"><span data-stu-id="ab16a-114">Destination mask</span></span> |



 

-   <span data-ttu-id="ab16a-115">Im Allgemeinen ist die Angabe von Schreib Masken für die Ziel Registrierung ein guter Codierungsstil.</span><span class="sxs-lookup"><span data-stu-id="ab16a-115">In general, specifying destination register write masks is good coding style.</span></span> <span data-ttu-id="ab16a-116">Dadurch wird der Code einfacher zu lesen und zu warten.</span><span class="sxs-lookup"><span data-stu-id="ab16a-116">It makes code easier to read and maintain.</span></span>
-   <span data-ttu-id="ab16a-117">Eine beliebige Kombination von Komponenten kann angegeben werden (einschließlich "None"), solange "x" vor "y", "y" vor "z" und "z" vorangeht.</span><span class="sxs-lookup"><span data-stu-id="ab16a-117">Any combination of components may be specified (including none) as long as x precedes y, y precedes z, and z precedes w.</span></span>
-   <span data-ttu-id="ab16a-118">Die OPTS-und ofog-Ausgabe Register dürfen nur eine Maske verwenden.</span><span class="sxs-lookup"><span data-stu-id="ab16a-118">The oPts and oFog output registers must use only one mask.</span></span>
-   <span data-ttu-id="ab16a-119">Bestimmte Anweisungen erfordern, dass das Ziel Register eine einzelne Schreib Maske verwendet: Exp, EXPP, Log, LogP, Pow, rcp und RSQ.</span><span class="sxs-lookup"><span data-stu-id="ab16a-119">Certain instructions require the destination register to use a single write mask: exp, expp, log, logp, pow, rcp, and rsq.</span></span>
-   <span data-ttu-id="ab16a-120">In Version 1,0 erforderte die FRC-Anweisung eine der folgenden Masken Kombinationen:. x oder. y oder. XY.</span><span class="sxs-lookup"><span data-stu-id="ab16a-120">In version 1.0, the frc instruction required one of the following mask combinations: .x or .y or .xy.</span></span> <span data-ttu-id="ab16a-121">Version 2,0 hat keine Masken Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="ab16a-121">Version 2.0 has no mask restriction.</span></span>
-   <span data-ttu-id="ab16a-122">SinCos erfordert eine der folgenden Masken Kombinationen:. x,. y oder. xyz.</span><span class="sxs-lookup"><span data-stu-id="ab16a-122">sincos requires one of the following mask combinations: .x or .y or .xyz.</span></span>
-   <span data-ttu-id="ab16a-123">m3x2 erfordert die. XY-Schreib Maske.</span><span class="sxs-lookup"><span data-stu-id="ab16a-123">m3x2 requires the .xy write mask.</span></span>
-   <span data-ttu-id="ab16a-124">M3x3 und m4x3 erfordern die Schreib Maske ". xyz".</span><span class="sxs-lookup"><span data-stu-id="ab16a-124">m3x3 and m4x3 require the .xyz write mask.</span></span>
-   <span data-ttu-id="ab16a-125">M3x4 und M4x4 erfordern entweder die. XYZ-Schreib Maske oder die Standard Schreib Maske (xyzw).</span><span class="sxs-lookup"><span data-stu-id="ab16a-125">m3x4 and m4x4 require either the .xyz write mask or the default write mask (xyzw).</span></span>

## <a name="texture-register-masks"></a><span data-ttu-id="ab16a-126">Textur Register Masken</span><span class="sxs-lookup"><span data-stu-id="ab16a-126">Texture Register Masks</span></span>

<span data-ttu-id="ab16a-127">Die Validierungsregeln für die Verwendung von modifiziererregistern für Texturkoordinaten Register sind enger als die Validierungsregeln für andere Register.</span><span class="sxs-lookup"><span data-stu-id="ab16a-127">The validation rules for using modifiers on texture coordinate registers are tighter than the validation rules for other registers.</span></span>

-   <span data-ttu-id="ab16a-128">Wenn OTN geschrieben ist, müssen auch alle vorherigen Register (OTN-1 ~ oT0) geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ab16a-128">If oTn is written, all previous registers (oTn-1 ~ oT0) have to be written as well.</span></span>
-   <span data-ttu-id="ab16a-129">Die "kombinierte" Schreib Maske für alle oT- \# Register muss genau eines der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="ab16a-129">The "combined" write mask for any oT\# register must be exactly one of the following:</span></span>
    -   <span data-ttu-id="ab16a-130">.x</span><span class="sxs-lookup"><span data-stu-id="ab16a-130">.x</span></span>
    -   <span data-ttu-id="ab16a-131">. XY</span><span class="sxs-lookup"><span data-stu-id="ab16a-131">.xy</span></span>
    -   <span data-ttu-id="ab16a-132">. XYZ</span><span class="sxs-lookup"><span data-stu-id="ab16a-132">.xyz</span></span>
    -   <span data-ttu-id="ab16a-133">. xyzw (entspricht nicht der Verwendung von komponentenmodifizierersätzen)</span><span class="sxs-lookup"><span data-stu-id="ab16a-133">.xyzw (which is equivalent to not using any component modifiers)</span></span>

<span data-ttu-id="ab16a-134">Beispielsweise kann ein Vertex-Shader in separaten Anweisungen an Textur Register ausgeben.</span><span class="sxs-lookup"><span data-stu-id="ab16a-134">For example, a vertex shader can output to texture registers in separate instructions.</span></span>


```
    oT1.y  
    oT0.y  
    oT2  
    oT0.xz  
    oT1.x
```



<span data-ttu-id="ab16a-135">Oder die Anweisungen können kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="ab16a-135">Or, the instructions can be combined.</span></span>


```
    oT0.xyz  
    oT1.xy  
    oT2.xyzw    
```



<span data-ttu-id="ab16a-136">Diese Einschränkungen gelten nur für die Texturkoordinaten Register.</span><span class="sxs-lookup"><span data-stu-id="ab16a-136">These restrictions apply only to the texture coordinate registers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab16a-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ab16a-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab16a-138">Vertex-Shader-registermodifiziererer</span><span class="sxs-lookup"><span data-stu-id="ab16a-138">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




