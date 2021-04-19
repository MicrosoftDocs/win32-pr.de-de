---
title: Arrays (RPC) (TFS)
description: Remote Prozedur Aufruf (RPC)-Array Kategorien umfassen eine Übereinstimmung mit fester Größe, Konformität, konform, unterschiedlich und komplex.
ms.assetid: 7144ec87-90f2-463a-80e4-28cb4771325f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d564a2dfd838006be1667343b14a57bdaf4b07
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388812"
---
# <a name="arrays-rpc"></a><span data-ttu-id="fc380-103">Arrays (RPC)</span><span class="sxs-lookup"><span data-stu-id="fc380-103">Arrays (RPC)</span></span>

<span data-ttu-id="fc380-104">Mehrere Array Kategorien wurden basierend auf ihren Leistungsmerkmalen definiert, primär, ob das Array Block kopiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fc380-104">Several array categories have been defined based on their performance characteristics, primarily whether the array can be block-copied.</span></span>

<span data-ttu-id="fc380-105">Für einige Kategorien, z. b. ein Array mit fester Größe, sind zwei Typen von Array Deskriptoren vorhanden. Sie werden durch eine Korrektur im Namen des vorangehende FC-Tokens angegeben.</span><span class="sxs-lookup"><span data-stu-id="fc380-105">For some categories, such as a fixed-size array, two types of array descriptors exist; they are indicated by an in-fix in the name of the leading FC token.</span></span>



| <span data-ttu-id="fc380-106">Zeichen formatieren</span><span class="sxs-lookup"><span data-stu-id="fc380-106">Format character</span></span> | <span data-ttu-id="fc380-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc380-107">Description</span></span>                                                           |
|------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="fc380-108">SM</span><span class="sxs-lookup"><span data-stu-id="fc380-108">SM</span></span>               | <span data-ttu-id="fc380-109">Die Gesamtgröße des Typs kann in einem 16-Bit-Ganzzahl ohne Vorzeichen dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="fc380-109">The type's total size can be represented in a 16-bit unsigned int.</span></span>    |
| <span data-ttu-id="fc380-110">LG</span><span class="sxs-lookup"><span data-stu-id="fc380-110">LG</span></span>               | <span data-ttu-id="fc380-111">Die Gesamtgröße des Typs muss eine 32-Bit-Länge ohne Vorzeichen aufweisen, um dargestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="fc380-111">The type's total size needs a 32-bit unsigned long to be represented.</span></span> |



 

<span data-ttu-id="fc380-112">Felder, die Arrays gemeinsam haben:</span><span class="sxs-lookup"><span data-stu-id="fc380-112">Fields common to arrays:</span></span>

-   <span data-ttu-id="fc380-113">Gesamt \_ Größe</span><span class="sxs-lookup"><span data-stu-id="fc380-113">total\_size</span></span>

    <span data-ttu-id="fc380-114">Gesamtgröße des Arrays im Speicher in Bytes.</span><span class="sxs-lookup"><span data-stu-id="fc380-114">Total size of the array in memory, in bytes.</span></span> <span data-ttu-id="fc380-115">Dies entspricht der Netzwerkgröße nach der Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="fc380-115">This is the same as wire size after alignment.</span></span> <span data-ttu-id="fc380-116">Die Gesamtgröße wird für Kategorien berechnet, für die das Auffüll Problem nicht vorhanden ist, und die Größe ist die tatsächliche Array Größe.</span><span class="sxs-lookup"><span data-stu-id="fc380-116">The total size is calculated for categories for which the padding issue does not exist and the size is actual array size.</span></span>

-   <span data-ttu-id="fc380-117">Element \_ Größe</span><span class="sxs-lookup"><span data-stu-id="fc380-117">element\_size</span></span>

    <span data-ttu-id="fc380-118">Gesamtgröße des Arbeitsspeichers eines einzelnen Elements des Arrays, einschließlich Auffüll Zeichen (Dies kann nur bei komplexen Arrays Vorkommen).</span><span class="sxs-lookup"><span data-stu-id="fc380-118">Total size in memory of a single element of the array, including padding (this may happen for complex arrays only).</span></span>

-   <span data-ttu-id="fc380-119">Element \_ Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc380-119">element\_description</span></span>

    <span data-ttu-id="fc380-120">Die Beschreibung des Array Elementtyps.</span><span class="sxs-lookup"><span data-stu-id="fc380-120">Description of the array element type.</span></span>

-   <span data-ttu-id="fc380-121">Zeiger \_ Layout</span><span class="sxs-lookup"><span data-stu-id="fc380-121">pointer\_layout</span></span>

    <span data-ttu-id="fc380-122">Weitere Informationen finden Sie im Thema [Zeiger Layout](pointer-layout-tfs.md) .</span><span class="sxs-lookup"><span data-stu-id="fc380-122">See the [Pointer Layout](pointer-layout-tfs.md) topic for more information.</span></span>

## <a name="fixed-sized-arrays"></a><span data-ttu-id="fc380-123">Arrays mit fester Größe</span><span class="sxs-lookup"><span data-stu-id="fc380-123">Fixed-sized Arrays</span></span>

<span data-ttu-id="fc380-124">Eine Array Format Zeichenfolge mit fester Größe wird für Arrays mit einer bekannten Größe generiert und kann daher in den marshallingpuffer kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="fc380-124">A fixed-sized array format string is generated for arrays that have a known size, and therefore may be block-copied to the marshaling buffer.</span></span> <span data-ttu-id="fc380-125">Die beiden folgenden Formate für ein festes Array Deskriptor sind wie folgt.</span><span class="sxs-lookup"><span data-stu-id="fc380-125">The two fixed array descriptor formats are as follows.</span></span>

``` syntax
FC_SMFARRAY alignment<1> 
total_size<2> 
[pointer_layout<>]  
element_description<> 
FC_END
```

<span data-ttu-id="fc380-126">und</span><span class="sxs-lookup"><span data-stu-id="fc380-126">and</span></span>

``` syntax
FC_LGFARRAY alignment<1> 
total_size<4> 
[pointer_layout<>] 
element_description<> 
FC_END
```

## <a name="conformant-array"></a><span data-ttu-id="fc380-127">Konformes Array</span><span class="sxs-lookup"><span data-stu-id="fc380-127">Conformant Array</span></span>

<span data-ttu-id="fc380-128">Ein konformes Array kann blockiert werden, sobald die Array Größe bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="fc380-128">A conformant array can be block-copied once the size of the array is known.</span></span>

``` syntax
FC_CARRAY alignment<1>
element_size<2> 
conformance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="fc380-129">Die Übereinstimmungs \_ Beschreibung<> ist ein Korrelations Deskriptor, der abhängig davon, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes hat.</span><span class="sxs-lookup"><span data-stu-id="fc380-129">The conformance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

## <a name="conformant-varying-array"></a><span data-ttu-id="fc380-130">Konform mit variierendem Array</span><span class="sxs-lookup"><span data-stu-id="fc380-130">Conformant Varying Array</span></span>

<span data-ttu-id="fc380-131">Ein konformes variierendes Array kann auch mit Block Kopien kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="fc380-131">A conformant varying array can also be block-copied.</span></span>

``` syntax
FC_CVARRAY alignment<1> 
element_size<2> 
conformance_description<> 
variance_description<>  
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="fc380-132">Die Übereinstimmungs \_ Beschreibung<> und die Varianz \_ Beschreibung<> ist ein Korrelations Deskriptor, der abhängig davon, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes hat.</span><span class="sxs-lookup"><span data-stu-id="fc380-132">The conformance\_description<> and variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

## <a name="varying-array"></a><span data-ttu-id="fc380-133">Variierendes Array</span><span class="sxs-lookup"><span data-stu-id="fc380-133">Varying Array</span></span>

<span data-ttu-id="fc380-134">Die unterschiedlichen Arrays haben zwei Möglichkeiten, je nach Größe des Arrays.</span><span class="sxs-lookup"><span data-stu-id="fc380-134">The varying arrays have two possibilities depending on the size of the array.</span></span>

``` syntax
FC_SMVARRAY alignment<1>
total_size<2>  
number_elements<2> 
element_size<2> 
variance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END

FC_LGVARRAY alignment<1>
total_size<4>  
number_elements<4> 
element_size<2> 
variance_description<4>
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="fc380-135">Die Varianz \_ Beschreibung<> ist ein Korrelations Deskriptor und hat je nach verwendetem [**/robust**](/windows/desktop/Midl/-robust) 4 oder 6 Bytes.</span><span class="sxs-lookup"><span data-stu-id="fc380-135">The variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on the [**/robust**](/windows/desktop/Midl/-robust) being used.</span></span>

<span data-ttu-id="fc380-136">Bei unterschiedlichen Arrays, die in einer Struktur eingebettet sind, ist der Offset<2> Feld der Varianz \_ Beschreibung<> ein relativer Offset von der Position des unterschiedlichen Arrays in der-Struktur bis hin zum Beschreibungsfeld für die Varianz.</span><span class="sxs-lookup"><span data-stu-id="fc380-136">For varying arrays embedded inside of a structure, the offset<2> field of the variance\_description<> is a relative offset from the varying array's position in the structure to the variance describing field.</span></span> <span data-ttu-id="fc380-137">Der Offset ist in der Regel relativ zum Anfang der-Struktur.</span><span class="sxs-lookup"><span data-stu-id="fc380-137">The offset is typically relative to the beginning of the structure.</span></span>

## <a name="complex-arrays"></a><span data-ttu-id="fc380-138">Komplexe Arrays</span><span class="sxs-lookup"><span data-stu-id="fc380-138">Complex Arrays</span></span>

<span data-ttu-id="fc380-139">Bei einem komplexen Array handelt es sich um ein beliebiges Array mit einem Element, das verhindert, dass es blockiert wird. Daher müssen zusätzliche Aktionen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fc380-139">A complex array is any array with an element that prevents it from being block-copied, and as such, additional action needs to be taken.</span></span> <span data-ttu-id="fc380-140">Diese Elemente machen ein Array Komplex:</span><span class="sxs-lookup"><span data-stu-id="fc380-140">These elements make an array complex:</span></span>

-   <span data-ttu-id="fc380-141">einfache Typen: ENUM16, \_ \_ INT3264 (nur auf 64-Bit-Plattformen), eine Ganzzahl mit dem \[ [ **Bereich**](/windows/desktop/Midl/range)\]</span><span class="sxs-lookup"><span data-stu-id="fc380-141">simple types: ENUM16, \_\_INT3264 (on 64-bit platforms only), an integral with \[[**range**](/windows/desktop/Midl/range)\]</span></span>
-   <span data-ttu-id="fc380-142">Verweis-und Schnittstellen Zeiger (alle Zeiger auf 64-Bit-Plattformen)</span><span class="sxs-lookup"><span data-stu-id="fc380-142">reference and interface pointers (all pointers on 64-bit platforms)</span></span>
-   <span data-ttu-id="fc380-143">Unions</span><span class="sxs-lookup"><span data-stu-id="fc380-143">unions</span></span>
-   <span data-ttu-id="fc380-144">komplexe Strukturen (Weitere Informationen finden Sie im Thema Beschreibung der komplexen Struktur. eine vollständige Liste der Gründe für eine komplexe Struktur finden Sie unter.)</span><span class="sxs-lookup"><span data-stu-id="fc380-144">complex structures (see the Complex Structure Description topic for a full list of reasons for a structure to be complex)</span></span>
-   <span data-ttu-id="fc380-145">mit "über \[ [**tragen \_ als**](/windows/desktop/Midl/transmit-as)" definierte Elemente \] , \[ [**Benutzer \_ Mars**](/windows/desktop/Midl/user-marshal) Hallen\]</span><span class="sxs-lookup"><span data-stu-id="fc380-145">elements defined with \[[**transmit\_as**](/windows/desktop/Midl/transmit-as)\], \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\]</span></span>
-   <span data-ttu-id="fc380-146">Alle mehrdimensionalen Arrays mit mindestens einer konformen und/oder unterschiedlichen Dimension sind unabhängig vom zugrunde liegenden Elementtyp Komplex.</span><span class="sxs-lookup"><span data-stu-id="fc380-146">All multidimensional arrays with at least one conformant and/or varying dimension are complex regardless of the underlying element type.</span></span>

<span data-ttu-id="fc380-147">Die Beschreibung des komplexen Arrays lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fc380-147">The complex array description is as follows:</span></span>

``` syntax
FC_BOGUS_ARRAY alignment<1> 
number_of_elements<2> 
conformance_description<> 
variance_description<> 
element_description<> 
FC_END
```

<span data-ttu-id="fc380-148">Die Anzahl \_ der \_ Elemente<2> Feld ist 0 (null), wenn das Array konform ist.</span><span class="sxs-lookup"><span data-stu-id="fc380-148">The number\_of\_elements<2> field is zero if the array is conformant.</span></span>

<span data-ttu-id="fc380-149">Die Übereinstimmungs \_ Beschreibung<> und die Varianz \_ Beschreibung<> ist ein Korrelations Deskriptor, der abhängig davon, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes hat.</span><span class="sxs-lookup"><span data-stu-id="fc380-149">The conformance\_description<> and variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="fc380-150">Wenn das Array über Konformität und/oder Varianz verfügt, werden die Übereinstimmungs \_ Beschreibung<> und/oder Varianz \_ Beschreibung<> Felder gültige Beschreibungen aufweisen; andernfalls werden die ersten 4 Bytes des Korrelations Deskriptors auf "0xffffffff" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fc380-150">If the array has conformance and/or variance then the conformance\_description<> and/or variance\_description<> field(s) have valid descriptions, otherwise the first 4 bytes of the correlation descriptor are set to 0xFFFFFFFF.</span></span> <span data-ttu-id="fc380-151">Die Flags werden, falls vorhanden, auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fc380-151">The flags, when present, are set to zero.</span></span>

 

 
