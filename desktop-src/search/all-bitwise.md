---
description: Alle bitweisen und einige bitweise Schlüsselwörter werden zum Testen der Bits in einem ganzzahligen Typ verwendet.
ms.assetid: 649f763f-45aa-4086-9e7f-b8934b5bd22c
title: Alle bitweisen und einige bitweise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709db4829f5b620bcb14e0b4261fac7e7d9a6f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525472"
---
# <a name="all-bitwise-and-some-bitwise"></a><span data-ttu-id="46d86-103">Alle bitweisen und einige bitweise</span><span class="sxs-lookup"><span data-stu-id="46d86-103">ALL BITWISE and SOME BITWISE</span></span>

<span data-ttu-id="46d86-104">**Alle bitweisen** und **einige bitweise** Schlüsselwörter werden zum Testen der Bits in einem ganzzahligen Typ verwendet.</span><span class="sxs-lookup"><span data-stu-id="46d86-104">The **ALL BITWISE** and **SOME BITWISE** keywords are used for testing the bits in an integral type.</span></span> <span data-ttu-id="46d86-105">Wenn alle Satz Bits in einer Eigenschaft mit der Maske identisch sind, ist **all bitweise** true.</span><span class="sxs-lookup"><span data-stu-id="46d86-105">If all of the set bits in a property match the mask, **ALL BITWISE** is true.</span></span> <span data-ttu-id="46d86-106">Wenn mindestens eines der Satz Bits in einer Eigenschaft mit der Maske übereinstimmt, ist **bitweise** true.</span><span class="sxs-lookup"><span data-stu-id="46d86-106">If at least one of the set bits in a property matches the mask, **SOME BITWISE** is true.</span></span>

<span data-ttu-id="46d86-107">Operatoren können sowohl auf skalare Eigenschaften (Einzelwert Eigenschaften) als auch auf Vektor Eigenschaften (mehrfach Wert) angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="46d86-107">Operators can be applied to both scalar (single-value) properties and vector (multiple-value) properties.</span></span> <span data-ttu-id="46d86-108">Im folgenden Codebeispiel wird gezeigt, wie Eigenschaftswerte mit **allen bitweisen** und **einigen bitweisen** getestet werden.</span><span class="sxs-lookup"><span data-stu-id="46d86-108">The following code example shows how to test property values with **ALL BITWISE** and **SOME BITWISE**.</span></span>


```sql
ALL array ALL BITWISE [values?]
ALL array SOME BITWISE [values?]
            
```



## <a name="comparison-operators"></a><span data-ttu-id="46d86-109">Vergleichsoperatoren</span><span class="sxs-lookup"><span data-stu-id="46d86-109">Comparison Operators</span></span>

<span data-ttu-id="46d86-110">Die unterstützten Vergleichs Operatoren für bitweise Tests sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="46d86-110">The supported comparison operators for BITWISE tests are listed in the following table.</span></span>



| <span data-ttu-id="46d86-111">Vergleichsoperator</span><span class="sxs-lookup"><span data-stu-id="46d86-111">Comparison operator</span></span> | <span data-ttu-id="46d86-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46d86-112">Description</span></span>  |
|---------------------|--------------|
| =                   | <span data-ttu-id="46d86-113">Gleich</span><span class="sxs-lookup"><span data-stu-id="46d86-113">Equal to</span></span>     |
| <span data-ttu-id="46d86-114">! = oder <></span><span class="sxs-lookup"><span data-stu-id="46d86-114">!= or <></span></span>      | <span data-ttu-id="46d86-115">Ungleich</span><span class="sxs-lookup"><span data-stu-id="46d86-115">Not equal to</span></span> |



 

<span data-ttu-id="46d86-116">Die Logik von bitweisen Tests ist in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="46d86-116">The logic of BITWISE tests is listed in the following table.</span></span>



| <span data-ttu-id="46d86-117">Bitweiser Test-und Vergleichs Operator</span><span class="sxs-lookup"><span data-stu-id="46d86-117">BITWISE test and comparison operator</span></span> | <span data-ttu-id="46d86-118">Logik</span><span class="sxs-lookup"><span data-stu-id="46d86-118">Logic</span></span>                   |
|--------------------------------------|-------------------------|
| <span data-ttu-id="46d86-119">= alle bitweisen</span><span class="sxs-lookup"><span data-stu-id="46d86-119">= ALL BITWISE</span></span>                        | <span data-ttu-id="46d86-120">Property & mask = mask</span><span class="sxs-lookup"><span data-stu-id="46d86-120">Property & Mask = Mask</span></span>  |
| <span data-ttu-id="46d86-121">= Einige bitweise</span><span class="sxs-lookup"><span data-stu-id="46d86-121">= SOME BITWISE</span></span>                       | <span data-ttu-id="46d86-122">Eigenschaft & Maske! = 0</span><span class="sxs-lookup"><span data-stu-id="46d86-122">Property & Mask != 0</span></span>    |
| <span data-ttu-id="46d86-123"><> alle bitweisen</span><span class="sxs-lookup"><span data-stu-id="46d86-123"><> ALL BITWISE</span></span>                 | <span data-ttu-id="46d86-124">Property & mask! = mask</span><span class="sxs-lookup"><span data-stu-id="46d86-124">Property & Mask != Mask</span></span> |
| <span data-ttu-id="46d86-125"><> einige bitweise</span><span class="sxs-lookup"><span data-stu-id="46d86-125"><> SOME BITWISE</span></span>                | <span data-ttu-id="46d86-126">Property & mask = 0</span><span class="sxs-lookup"><span data-stu-id="46d86-126">Property & Mask = 0</span></span>     |



 

<span data-ttu-id="46d86-127">In der folgenden Wahrheitstabelle werden binäre und hexadezimale Werte verwendet, um die Logik von bitweisen Tests zu verteueren.</span><span class="sxs-lookup"><span data-stu-id="46d86-127">The following truth table uses example binary and hex values to demonstate the logic of BITWISE tests.</span></span>



| <span data-ttu-id="46d86-128">Eigenschaft in binary (Hex)</span><span class="sxs-lookup"><span data-stu-id="46d86-128">Property in binary (hex)</span></span> | <span data-ttu-id="46d86-129">Mask in binary (Hex)</span><span class="sxs-lookup"><span data-stu-id="46d86-129">Mask in binary (hex)</span></span> | <span data-ttu-id="46d86-130">Property & Mask = Binary (Hex)</span><span class="sxs-lookup"><span data-stu-id="46d86-130">Property & Mask = binary (hex)</span></span> | <span data-ttu-id="46d86-131">= Einige bitweise</span><span class="sxs-lookup"><span data-stu-id="46d86-131">= SOME BITWISE</span></span> | <span data-ttu-id="46d86-132">= alle bitweisen</span><span class="sxs-lookup"><span data-stu-id="46d86-132">= ALL BITWISE</span></span> |
|--------------------------|----------------------|--------------------------------|----------------|---------------|
| <span data-ttu-id="46d86-133">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="46d86-133">0001 (0x1)</span></span>               | <span data-ttu-id="46d86-134">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="46d86-134">0001 (0x1)</span></span>           | <span data-ttu-id="46d86-135">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="46d86-135">0001 (0x1)</span></span>                     | <span data-ttu-id="46d86-136">True</span><span class="sxs-lookup"><span data-stu-id="46d86-136">True</span></span>           | <span data-ttu-id="46d86-137">True</span><span class="sxs-lookup"><span data-stu-id="46d86-137">True</span></span>          |
| <span data-ttu-id="46d86-138">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="46d86-138">0001 (0x1)</span></span>               | <span data-ttu-id="46d86-139">0011 (0x3)</span><span class="sxs-lookup"><span data-stu-id="46d86-139">0011 (0x3)</span></span>           | <span data-ttu-id="46d86-140">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="46d86-140">0001 (0x1)</span></span>                     | <span data-ttu-id="46d86-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="46d86-141">True</span></span>           | <span data-ttu-id="46d86-142">False</span><span class="sxs-lookup"><span data-stu-id="46d86-142">False</span></span>         |
| <span data-ttu-id="46d86-143">0011 (0x3)</span><span class="sxs-lookup"><span data-stu-id="46d86-143">0011 (0x3)</span></span>               | <span data-ttu-id="46d86-144">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="46d86-144">0001 (0x1)</span></span>           | <span data-ttu-id="46d86-145">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="46d86-145">0001 (0x1)</span></span>                     | <span data-ttu-id="46d86-146">True</span><span class="sxs-lookup"><span data-stu-id="46d86-146">True</span></span>           | <span data-ttu-id="46d86-147">True</span><span class="sxs-lookup"><span data-stu-id="46d86-147">True</span></span>          |
| <span data-ttu-id="46d86-148">0010 (0x2)</span><span class="sxs-lookup"><span data-stu-id="46d86-148">0010 (0x2)</span></span>               | <span data-ttu-id="46d86-149">0001 (0x1)</span><span class="sxs-lookup"><span data-stu-id="46d86-149">0001 (0x1)</span></span>           | <span data-ttu-id="46d86-150">0000 (0x0)</span><span class="sxs-lookup"><span data-stu-id="46d86-150">0000 (0x0)</span></span>                     | <span data-ttu-id="46d86-151">False</span><span class="sxs-lookup"><span data-stu-id="46d86-151">False</span></span>          | <span data-ttu-id="46d86-152">False</span><span class="sxs-lookup"><span data-stu-id="46d86-152">False</span></span>         |
| <span data-ttu-id="46d86-153">11110000 (0xF)</span><span class="sxs-lookup"><span data-stu-id="46d86-153">11110000 (0xF0)</span></span>          | <span data-ttu-id="46d86-154">00000011 (0x03)</span><span class="sxs-lookup"><span data-stu-id="46d86-154">00000011 (0x03)</span></span>      | <span data-ttu-id="46d86-155">00000000 (0x00)</span><span class="sxs-lookup"><span data-stu-id="46d86-155">00000000 (0x00)</span></span>                | <span data-ttu-id="46d86-156">False</span><span class="sxs-lookup"><span data-stu-id="46d86-156">False</span></span>          | <span data-ttu-id="46d86-157">False</span><span class="sxs-lookup"><span data-stu-id="46d86-157">False</span></span>         |
| <span data-ttu-id="46d86-158">11110010 (0xF 2)</span><span class="sxs-lookup"><span data-stu-id="46d86-158">11110010 (0xF2)</span></span>          | <span data-ttu-id="46d86-159">11110010 (0xF 2)</span><span class="sxs-lookup"><span data-stu-id="46d86-159">11110010 (0xF2)</span></span>      | <span data-ttu-id="46d86-160">11110010 (0xF 2)</span><span class="sxs-lookup"><span data-stu-id="46d86-160">11110010 (0xF2)</span></span>                | <span data-ttu-id="46d86-161">True</span><span class="sxs-lookup"><span data-stu-id="46d86-161">True</span></span>           | <span data-ttu-id="46d86-162">True</span><span class="sxs-lookup"><span data-stu-id="46d86-162">True</span></span>          |
| <span data-ttu-id="46d86-163">11110010 (0xF 2)</span><span class="sxs-lookup"><span data-stu-id="46d86-163">11110010 (0xF2)</span></span>          | <span data-ttu-id="46d86-164">00000011 (0x03)</span><span class="sxs-lookup"><span data-stu-id="46d86-164">00000011 (0x03)</span></span>      | <span data-ttu-id="46d86-165">00000010 (0x02)</span><span class="sxs-lookup"><span data-stu-id="46d86-165">00000010 (0x02)</span></span>                | <span data-ttu-id="46d86-166">Richtig</span><span class="sxs-lookup"><span data-stu-id="46d86-166">True</span></span>           | <span data-ttu-id="46d86-167">False</span><span class="sxs-lookup"><span data-stu-id="46d86-167">False</span></span>         |



 

## <a name="example"></a><span data-ttu-id="46d86-168">Beispiel</span><span class="sxs-lookup"><span data-stu-id="46d86-168">Example</span></span>

<span data-ttu-id="46d86-169">Im folgenden finden Sie ein Beispiel für das **bitweise all** -Prädikat.</span><span class="sxs-lookup"><span data-stu-id="46d86-169">The following is an example of the **ALL BITWISE** predicate.</span></span>


```sql
Select system.itemnamedisplay, system.FileAttributes from SystemIndex Where System.FileAttributes <> ALL BITWISE 0x4 AND Scope = 'file:c:\bitwise'
                
```



## <a name="related-topics"></a><span data-ttu-id="46d86-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="46d86-170">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="46d86-171">**Licher**</span><span class="sxs-lookup"><span data-stu-id="46d86-171">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="46d86-172">Voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="46d86-172">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="46d86-173">Nicht-voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="46d86-173">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



