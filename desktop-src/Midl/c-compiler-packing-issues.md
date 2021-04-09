---
title: C-Compilerprobleme beim Packen
description: Komprimierungs Ebenen wirken sich auf das Speicher Layout von Typen für die Mittel-und den Microsoft C/C++-Compiler auf die gleiche Weise aus.
ms.assetid: 029e2f68-e68f-4627-bdf0-889939d7d3c6
keywords:
- Mittel l compilermittell, C-Compilerprobleme beim Packen
- Verpacken der Mittel l
- Mittell für das arbeitsspeicherlayout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c441439499d1a9b22e36c697ab6615f3292744
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858220"
---
# <a name="c-compiler-packing-issues"></a><span data-ttu-id="6de28-106">C-Compilerprobleme beim Packen</span><span class="sxs-lookup"><span data-stu-id="6de28-106">C-Compiler Packing Issues</span></span>

<span data-ttu-id="6de28-107">Komprimierungs Ebenen wirken sich auf das Speicher Layout von Typen für die Mittel-und den Microsoft C/C++-Compiler auf die gleiche Weise aus.</span><span class="sxs-lookup"><span data-stu-id="6de28-107">Packing levels affect the memory layout of types for both MIDL and the Microsoft C/C++ compiler in the same way.</span></span> <span data-ttu-id="6de28-108">In Microsoft Build-Umgebungen, wie z. b. in der durch VC + + oder dem Platform Software Development Kit (SDK) definierten Buildumgebung, ist die Standard Packungs Stufe für die Kompilier-und C/C++-Compiler identisch. die Standard Packungs Ebene für die Windows-Buildumgebung 32-Bit und 64-Bit ist 8.</span><span class="sxs-lookup"><span data-stu-id="6de28-108">In Microsoft build environments, such as the build environment defined by VC++ or the Platform Software Development Kit (SDK), the default packing level for MIDL and C/C++ compilers is the same; the default packing level for the 32-bit and 64-bit Windows build environments is 8.</span></span>

## <a name="natural-alignment"></a><span data-ttu-id="6de28-109">Natürliche Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="6de28-109">Natural Alignment</span></span>

<span data-ttu-id="6de28-110">Bei Typen im Arbeitsspeicher ist die Standardausrichtung identisch mit ihrer natürlichen Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="6de28-110">For types in memory, the default alignment is the same as its natural alignment.</span></span>

-   <span data-ttu-id="6de28-111">Ein Basistyp, z. b. Short, float und \_ \_ Int64, und ein Zeiger werden natürlich ausgerichtet, wenn seine Darstellung bei einer Adresse beginnt, deren Größe Modulo ist.</span><span class="sxs-lookup"><span data-stu-id="6de28-111">A base type, such as short, float and \_\_int64, and a pointer is aligned naturally if its representation starts at an address that is modulo its size.</span></span> <span data-ttu-id="6de28-112">Alle derzeit unterstützten Basis Typen haben die Größen 1, 2, 4 oder 8.</span><span class="sxs-lookup"><span data-stu-id="6de28-112">All the currently supported base types have sizes of 1, 2, 4 or 8.</span></span> <span data-ttu-id="6de28-113">Zeiger haben eine Größe von 4 in 32-Bit-Umgebungen und 8 in 64-Bit-Umgebungen.</span><span class="sxs-lookup"><span data-stu-id="6de28-113">Pointers have a size of 4 in 32-bit environments and 8 in 64-bit environments.</span></span>
-   <span data-ttu-id="6de28-114">Ein Verbund-Typ wird auf natürliche Weise ausgerichtet, wenn die einzelnen Komponenten natürlich relativ zum Anfang des Typs ausgerichtet sind und keine unnötigen Lücken (Auffüll Zeichen) zwischen Komponenten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6de28-114">A compound type is aligned naturally if each of its components is aligned naturally relative to the beginning of the type, and if there are no unnecessary gaps (padding) between components.</span></span> <span data-ttu-id="6de28-115">Verbundkomponenten, z. b. Felder oder Elemente, werden zu Zeiger-oder Basistyp Komponenten rekurert.</span><span class="sxs-lookup"><span data-stu-id="6de28-115">Compound components, such as fields or elements, are recursed to pointer or base type components.</span></span>

<span data-ttu-id="6de28-116">Eine einfache Regel, um dieses Verhalten zu merken, besteht darin, dass die natürliche Ausrichtung eines Typs gleich den größten Ausrichtungen der Komponenten ist.</span><span class="sxs-lookup"><span data-stu-id="6de28-116">A simple rule to help remember this behavior is that the natural alignment of a type is equal to the biggest alignments of its components.</span></span>

<span data-ttu-id="6de28-117">Es gibt eine Verbindung zwischen der Ausrichtung und der Arbeitsspeicher Größe eines Typs in Sprachen wie C oder C++ und IDL, wie vom Operator **sizeof ()** ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="6de28-117">There is a connection between alignment and memory size of a type in languages like C or C++ and IDL as expressed by the operator **sizeof()**.</span></span> <span data-ttu-id="6de28-118">Die Größe ist ein Vielfaches der Ausrichtung (das minimale Vielfache, das den Typ umfasst).</span><span class="sxs-lookup"><span data-stu-id="6de28-118">The size is a multiple of the alignment (the minimal multiple spanning the type).</span></span> <span data-ttu-id="6de28-119">Dies folgt aus einer Array Darstellung im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="6de28-119">This follows from an array representation in memory.</span></span>

<span data-ttu-id="6de28-120">Die natürliche Ausrichtung ist wichtig, da der Zugriff auf falsch ausgerichtete Daten auf einigen Systemen zu einer Ausnahme führen kann.</span><span class="sxs-lookup"><span data-stu-id="6de28-120">Natural alignment is important because accessing misaligned data may cause an exception on some systems.</span></span> <span data-ttu-id="6de28-121">Daten können für eine sichere Bearbeitung gekennzeichnet werden, wenn Sie falsch ausgerichtet sind, aber in der Regel eine Geschwindigkeits Einbuße, die auf manchen Plattformen beträchtlich sein kann.</span><span class="sxs-lookup"><span data-stu-id="6de28-121">Data can be marked for a safe manipulation when misaligned, but typically that involves a speed penalty that may be substantial on some platforms.</span></span>

> [!Note]  
> <span data-ttu-id="6de28-122">Im Arbeitsspeicher werden Objekte von Typen mit einer natürlichen Ausrichtung von *n* garantiert ordnungsgemäß ausgerichtet, wenn Sie an Adressen platziert werden, die ein Vielfaches von *n* sind.</span><span class="sxs-lookup"><span data-stu-id="6de28-122">In memory, objects of types with a natural alignment of *n* are guaranteed to be aligned properly when placed at addresses that are a multiple of *n*.</span></span>

 

## <a name="packing-versus-alignment"></a><span data-ttu-id="6de28-123">Verpacken im Vergleich zu Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="6de28-123">Packing versus Alignment</span></span>

<span data-ttu-id="6de28-124">Wenn Sie eine Packungs Ebene angeben, die größer als die natürliche Ausrichtung eines Typs ist, wird die typausrichtung nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="6de28-124">Specifying a packing level larger than the natural alignment of a type does not change the type alignment.</span></span> <span data-ttu-id="6de28-125">Wenn Sie einen Verpackungs Grad angeben, der kleiner als die natürliche Ausrichtung ist, wird die typausrichtung auf die Verpackungs Ebene reduziert.</span><span class="sxs-lookup"><span data-stu-id="6de28-125">Specifying a packing level smaller than the natural alignment reduces the type alignment to the packing level.</span></span> <span data-ttu-id="6de28-126">Daher können die gepackten Typen bei Adressen, bei denen es sich um ein Vielfaches der Packungs Ebene (der reduzierten Ausrichtung) handelt, in den Arbeitsspeicher eingefügt werden, ohne dass eine Fehlausrichtung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="6de28-126">As a result, the packed types may be placed in memory at addresses that are a multiple of the packing level (the reduced alignment) without causing a misalignment.</span></span> <span data-ttu-id="6de28-127">Dies wirkt sich sowohl auf einfache Typen als auch auf Komponenten Typen aus.</span><span class="sxs-lookup"><span data-stu-id="6de28-127">This affects both simple types and component types.</span></span> <span data-ttu-id="6de28-128">Bei Verbund Typen kann das interne Layout des Typs beeinträchtigt werden, da die reduzierte Ausrichtung der Komponenten möglicherweise die Größe des Auffüllung ändert, das für die ordnungsgemäße Ausrichtung der Komponenten erforderlich ist, wodurch die Größe des Typs reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="6de28-128">For compound types, the internal layout of the type may be affected, because the reduced alignment of the components may change the size of padding necessary for the proper alignment of the components, thus reducing the size of the type.</span></span>

<span data-ttu-id="6de28-129">Eine einfache Regel, um dieses Verhalten zu merken, besteht darin, dass die neue Ausrichtung eines gepackten Typs der kleinere der Packungs Ebene und ihrer natürlichen Ausrichtung entspricht.</span><span class="sxs-lookup"><span data-stu-id="6de28-129">A simple rule to help remember this behavior is that the new alignment of a packed type is the smaller of the packing level and its natural alignment.</span></span> <span data-ttu-id="6de28-130">Die Größe des Typs ist ein Vielfaches der neuen Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="6de28-130">The size of the type is a multiple of the new alignment.</span></span> <span data-ttu-id="6de28-131">Der **sizeof ()** -Operator gibt die reduzierte Größe für gepackte Typen zurück.</span><span class="sxs-lookup"><span data-stu-id="6de28-131">The **sizeof()** operator returns the reduced size for packed types.</span></span>

<span data-ttu-id="6de28-132">Beispielsweise wird mit dem paketegrad 2 eine lange an 2 ausgerichtet und kann daher auch an einer beliebigen geraden Adresse platziert werden, nicht nur an den Adressen, bei denen es sich um ein Vielfaches von 4 handelt, was bei natürlicher Ausrichtung der Fall wäre.</span><span class="sxs-lookup"><span data-stu-id="6de28-132">For example, with packing level 2 a long becomes aligned at 2, and therefore may be placed at any even address, not only at the addresses that are a multiple of 4 as would be the case with natural alignment.</span></span> <span data-ttu-id="6de28-133">Eine-Struktur mit einem kurzen und einem langen, gepackt bei 2, benötigt nicht die interne Lücke zwischen der kurzen und der folgenden Länge, die für die natürliche Ausrichtung notwendig war. Daher ist nicht nur die-Struktur nun bei 2 ausgerichtet, sondern auch die Größe von 8 auf 6 reduziert.</span><span class="sxs-lookup"><span data-stu-id="6de28-133">A structure with a short and a long, packed at 2, does not need the internal gap between the short and the following long that was necessary for the natural alignment; hence, not only is the structure now aligned at 2, it also has its size reduced from 8 to 6.</span></span>

<span data-ttu-id="6de28-134">Angenommen, ein zusammengesetzter Typ besteht aus einem 1-Byte-Zeichen, einem Integer-Wert von 4 Bytes und einem 1-Byte-Zeichen:</span><span class="sxs-lookup"><span data-stu-id="6de28-134">As an example, consider a compound type consisting of a 1-byte character, an integer 4 bytes long, and a 1-byte character:</span></span>

``` syntax
struct mystructtype 
{    
    char c1;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
    long l2;  /* requires 4 bytes */
    char c3;  /* requires 1 byte  */
              /* 3 bytes of padding with natural alignment only */
 } mystruct;
```

<span data-ttu-id="6de28-135">Diese Struktur wird natürlich an 4 ausgerichtet und hat die natürliche Größe von 12.</span><span class="sxs-lookup"><span data-stu-id="6de28-135">This structure is naturally aligned at 4 and has the natural size of 12.</span></span>

<span data-ttu-id="6de28-136">Bei einem Verpackungs Grad von 4 oder höher wird die Struktur **MyStruct** um 4 ausgerichtet und `sizeof(struct mystructtype)` ist gleich 12.</span><span class="sxs-lookup"><span data-stu-id="6de28-136">For packing level 4 or greater, the structure **mystruct** is aligned at 4 and `sizeof(struct mystructtype)` is equal to 12.</span></span> <span data-ttu-id="6de28-137">Die Struktur wird falsch ausgerichtet, wenn Sie sich im Arbeitsspeicher an einer Adresse befindet, die kein Vielfaches von 4 ist.</span><span class="sxs-lookup"><span data-stu-id="6de28-137">The structure will be misaligned if located in memory at an address that is not a multiple of 4.</span></span>

<span data-ttu-id="6de28-138">Für das Verpackungs Niveau 2 wird die Struktur bei 2 ausgerichtet, und die Größe ist 8.</span><span class="sxs-lookup"><span data-stu-id="6de28-138">For packing level 2, the structure is aligned at 2 and its size is 8.</span></span> <span data-ttu-id="6de28-139">Die mit Ebene 2 gepackte Struktur wird falsch ausgerichtet, wenn Sie sich im Speicher an einer Adresse befindet, die kein Vielfaches von 2 ist.</span><span class="sxs-lookup"><span data-stu-id="6de28-139">The structure packed with level 2 will be misaligned if located in memory at an address that is not a multiple of 2.</span></span>

<span data-ttu-id="6de28-140">Für das Verpackungs Niveau 1 wird die Struktur an 1 ausgerichtet, und die Größe ist 6.</span><span class="sxs-lookup"><span data-stu-id="6de28-140">For packing level 1, the structure is aligned at 1 and its size is 6.</span></span> <span data-ttu-id="6de28-141">Die Struktur, die mit Ebene 1 gepackt ist, kann überall platziert werden, ohne dass ein Fehler aufgrund einer Fehlausrichtung verursacht</span><span class="sxs-lookup"><span data-stu-id="6de28-141">The structure packed with level 1 can be placed anywhere without causing a misalignment fault.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6de28-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6de28-142">Related topics</span></span>

<dl> <span data-ttu-id="6de28-143"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="6de28-143"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="6de28-144">/ZP</span><span class="sxs-lookup"><span data-stu-id="6de28-144">/Zp</span></span>](./-zp.md)
</dt> <dt>

[<span data-ttu-id="6de28-145">/Pack</span><span class="sxs-lookup"><span data-stu-id="6de28-145">/pack</span></span>](./-pack.md)
</dt> </dl>

 

 