---
description: In dieser Übersicht werden die Änderungen beschrieben, die zum Migrieren von vorhandenem Code mithilfe der XNA-mathematischen Bibliothek zur directxmath-Bibliothek erforderlich sind.
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: Code Migration aus der XNA-mathematischen Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c446165d3d0b6b7303424959f96ddf48bc75b5fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528040"
---
# <a name="code-migration-from-the-xna-math-library"></a><span data-ttu-id="47643-103">Code Migration aus der XNA-mathematischen Bibliothek</span><span class="sxs-lookup"><span data-stu-id="47643-103">Code Migration from the XNA Math Library</span></span>

<span data-ttu-id="47643-104">In dieser Übersicht werden die Änderungen beschrieben, die zum Migrieren von vorhandenem Code mithilfe der XNA-mathematischen Bibliothek zur directxmath-Bibliothek erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="47643-104">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span>

-   [<span data-ttu-id="47643-105">Header Änderungen</span><span class="sxs-lookup"><span data-stu-id="47643-105">Header Changes</span></span>](#header-changes)
-   [<span data-ttu-id="47643-106">Konstante Änderungen</span><span class="sxs-lookup"><span data-stu-id="47643-106">Constant Changes</span></span>](#constant-changes)
-   [<span data-ttu-id="47643-107">Namespaces</span><span class="sxs-lookup"><span data-stu-id="47643-107">Namespaces</span></span>](#namespaces)
-   [<span data-ttu-id="47643-108">Partielle Ladevorgänge</span><span class="sxs-lookup"><span data-stu-id="47643-108">Partial Loads</span></span>](#partial-loads)
-   [<span data-ttu-id="47643-109">Entfernen von Xbox 360-spezifischen Typen</span><span class="sxs-lookup"><span data-stu-id="47643-109">Removal of Xbox 360 Specific Types</span></span>](#removal-of-xbox-360-specific-types)
-   [<span data-ttu-id="47643-110">Systeminterne Arm-Neon-Funktionen</span><span class="sxs-lookup"><span data-stu-id="47643-110">ARM-NEON Intrinsics</span></span>](#arm-neon-intrinsics)
-   [<span data-ttu-id="47643-111">Permute</span><span class="sxs-lookup"><span data-stu-id="47643-111">Permute</span></span>](#permute)
-   [<span data-ttu-id="47643-112">Vorlagen Formulare</span><span class="sxs-lookup"><span data-stu-id="47643-112">Template Forms</span></span>](#template-forms)
-   [<span data-ttu-id="47643-113">Eliminieren von Funktionen</span><span class="sxs-lookup"><span data-stu-id="47643-113">Eliminated Functions</span></span>](#eliminated-functions)
-   [<span data-ttu-id="47643-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47643-114">Related topics</span></span>](#related-topics)

## <a name="header-changes"></a><span data-ttu-id="47643-115">Header Änderungen</span><span class="sxs-lookup"><span data-stu-id="47643-115">Header Changes</span></span>

<span data-ttu-id="47643-116">Die directxmath-Bibliothek verwendet einen neuen Satz von Headern.</span><span class="sxs-lookup"><span data-stu-id="47643-116">The DirectXMath library uses a new set of headers.</span></span>

<span data-ttu-id="47643-117">Ersetzen Sie den xnamath. h-Header durch directxmath. h, und fügen Sie directxpackedvector. h für die "GPU-gepackten" Typen hinzu.</span><span class="sxs-lookup"><span data-stu-id="47643-117">Replace the xnamath.h header with DirectXMath.h and add DirectXPackedVector.h for the “GPU packed” types.</span></span>

<span data-ttu-id="47643-118">Die umgebenden Typen aus dem DirectX SDK-Kollisions Beispiel in xnacollision. h sind nun Teil der directxmath-Bibliothek in directxcollision. h.</span><span class="sxs-lookup"><span data-stu-id="47643-118">The bounding types from the DirectX SDK Collision sample in xnacollision.h is now part of the DirectXMath library in DirectXCollision.h.</span></span> <span data-ttu-id="47643-119">Diese wurden geändert, sodass anstelle einer API im C-Stil C++-Klassen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47643-119">These have been modified to use C++ classes rather than a C-style API.</span></span>

## <a name="constant-changes"></a><span data-ttu-id="47643-120">Konstante Änderungen</span><span class="sxs-lookup"><span data-stu-id="47643-120">Constant Changes</span></span>

<span data-ttu-id="47643-121">Die xnamath- \_ Version (200, 201, 202, 203, 204 usw.) wurde durch die direcxtmath- \_ Version (300, 301, 302, 303 usw.) ersetzt.</span><span class="sxs-lookup"><span data-stu-id="47643-121">XNAMATH\_VERSION (200, 201, 202, 203, 204, and so on) has been replaced with DIRECXTMATH\_VERSION (300, 301, 302, 303, and so on).</span></span>

> [!Note]  
> <span data-ttu-id="47643-122">Directxmath 3,00 und 3,02 wurden mit vorläufigen Versionen des Windows SDK ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="47643-122">DirectXMath 3.00 and 3.02 shipped with preliminary versions of the Windows SDK.</span></span> <span data-ttu-id="47643-123">Directxmath 3,03 ist in der endgültigen Version des Windows 8 SDK.</span><span class="sxs-lookup"><span data-stu-id="47643-123">DirectXMath 3.03 is in the final version of the Windows 8 SDK.</span></span>

 

## <a name="namespaces"></a><span data-ttu-id="47643-124">Namespaces</span><span class="sxs-lookup"><span data-stu-id="47643-124">Namespaces</span></span>

<span data-ttu-id="47643-125">Die directxmath-Bibliothek verwendet C++-Namespaces, um die Typen zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="47643-125">The DirectXMath library uses C++ namespaces to organize the types.</span></span> <span data-ttu-id="47643-126">XNA Math hat nur den globalen Namespace verwendet.</span><span class="sxs-lookup"><span data-stu-id="47643-126">XNA Math used only the global namespace.</span></span> <span data-ttu-id="47643-127">Die allgemeinen directxmath-Typen mit XNA Math befinden sich im "DirectX"-Namespace oder im "DirectX::P ackedvector"-Namespace.</span><span class="sxs-lookup"><span data-stu-id="47643-127">The DirectXMath types in common with XNA Math are in the “DirectX” or the “DirectX::PackedVector” namespace.</span></span>

<span data-ttu-id="47643-128">In C++-Quelldateien besteht eine einfache Lösung darin, using-Anweisungen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="47643-128">In C++ source files, a simple solution is to add ‘using’ statements:</span></span>


```
#include “DirectXMath.h”
#include “DirectXPackedVector.h”

using namespace DirectX; 
using namespace DirectX::PackedVector;
```



<span data-ttu-id="47643-129">Bei Headern wird Sie nicht als "bewährte Vorgehensweise" betrachtet, um using-Anweisungen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="47643-129">For headers, it is not considered ‘best practice’ to add using statements.</span></span> <span data-ttu-id="47643-130">Fügen Sie stattdessen voll qualifizierte Namespaces hinzu:</span><span class="sxs-lookup"><span data-stu-id="47643-130">Instead, add fully qualified namespaces:</span></span>


```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```



## <a name="partial-loads"></a><span data-ttu-id="47643-131">Partielle Ladevorgänge</span><span class="sxs-lookup"><span data-stu-id="47643-131">Partial Loads</span></span>

<span data-ttu-id="47643-132">Für verschiedene Funktionen, die weniger als vier Elemente eines xmvector laden, wurden die zusätzlichen Elemente in der mathematischen XNA-Bibliothek nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="47643-132">For various functions that load less than 4 elements of an XMVECTOR, the XNA Math library left the additional elements undefined.</span></span> <span data-ttu-id="47643-133">Directxmath fügt diese zusätzlichen Elemente immer mit 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="47643-133">DirectXMath will always fill these additional elements with 0.</span></span>

## <a name="removal-of-xbox-360-specific-types"></a><span data-ttu-id="47643-134">Entfernen von Xbox 360-spezifischen Typen</span><span class="sxs-lookup"><span data-stu-id="47643-134">Removal of Xbox 360 Specific Types</span></span>

<span data-ttu-id="47643-135">Die folgenden XNA-mathematischen Bibliothekstypen,-Funktionen und-Konstanten sind in directxmath nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="47643-135">The following XNA Math library types, functions, and constants are not available in DirectXMath.</span></span>

-   <span data-ttu-id="47643-136">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span><span class="sxs-lookup"><span data-stu-id="47643-136">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span></span>
-   <span data-ttu-id="47643-137">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span><span class="sxs-lookup"><span data-stu-id="47643-137">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span></span>
-   <span data-ttu-id="47643-138">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span><span class="sxs-lookup"><span data-stu-id="47643-138">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span></span>
-   <span data-ttu-id="47643-139">g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ xmadddhen, g \_ XMMulHenD3, g \_ XMMulDHen3, g \_ XMXorHenD3, g \_ XMXorDHen3</span><span class="sxs-lookup"><span data-stu-id="47643-139">g\_XMMaskHenD3, g\_XMMaskDHen3, g\_XMAddUHenD3, g\_XMAddHenD3, g\_XMAddDHen, g\_XMMulHenD3, g\_XMMulDHen3, g\_XMXorHenD3, g\_XMXorDHen3</span></span>
-   <span data-ttu-id="47643-140">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span><span class="sxs-lookup"><span data-stu-id="47643-140">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span></span>
-   <span data-ttu-id="47643-141">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span><span class="sxs-lookup"><span data-stu-id="47643-141">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span></span>
-   <span data-ttu-id="47643-142">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span><span class="sxs-lookup"><span data-stu-id="47643-142">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span></span>
-   <span data-ttu-id="47643-143">g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g \_ XMAddIco4, g \_ XMMulIco4</span><span class="sxs-lookup"><span data-stu-id="47643-143">g\_XMMaskIco4, g\_XMXorXIco4, g\_XMXorIco4, g\_XMAddXIco4, g\_XMAddUIco4, g\_XMAddIco4, g\_XMMulIco4</span></span>

<span data-ttu-id="47643-144">\_\_vector4i ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="47643-144">\_\_vector4i is deprecated.</span></span> <span data-ttu-id="47643-145">Verwenden Sie stattdessen [**XMVECTORI32**](xmvectori32-data-type.md) oder [**XMVECTORU32**](xmvectoru32-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="47643-145">Use [**XMVECTORI32**](xmvectori32-data-type.md) or [**XMVECTORU32**](xmvectoru32-data-type.md) instead.</span></span>

<span data-ttu-id="47643-146">Die folgenden Funktionen und Typen sind als veraltet markiert, da Sie nur Xbox 360 sind: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span><span class="sxs-lookup"><span data-stu-id="47643-146">The following functions and types are deprecated as they are Xbox 360 only: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span></span>

## <a name="arm-neon-intrinsics"></a><span data-ttu-id="47643-147">Systeminterne Arm-Neon-Funktionen</span><span class="sxs-lookup"><span data-stu-id="47643-147">ARM-NEON Intrinsics</span></span>

<span data-ttu-id="47643-148">Das Deklarieren einer Vektor Konstante mit diesem Code wird für XNA Math für SSE und keine systeminternen Funktionen kompiliert, schlägt jedoch für directxmath mit Arm-Neon fehl.</span><span class="sxs-lookup"><span data-stu-id="47643-148">Declaring a vector constant with this code will compile for XNA Math for SSE and NO-INTRINSICS, but will fail for DirectXMath using ARM-NEON.</span></span>


```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```



<span data-ttu-id="47643-149">Im Allgemeinen wird diese Methode der Initialisierung eines [**xmvector**](xmvector-data-type.md)nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="47643-149">In general, we don't recommend this method of initialization of an [**XMVECTOR**](xmvector-data-type.md).</span></span> <span data-ttu-id="47643-150">Wenn Sie jedoch eine Vektor Konstante möchten, unterstützt die [**XMVECTORF32**](xmvectorf32-data-type.md) -Klasse diese Art von Initialisierung und gibt den **xmvector** -Typ automatisch zurück, sodass Sie **XMVECTORF32** in den meisten der gleichen Kontexte verwenden können.</span><span class="sxs-lookup"><span data-stu-id="47643-150">However, if you want a vector constant, the [**XMVECTORF32**](xmvectorf32-data-type.md) class supports this style of initialization and returns the **XMVECTOR** type automatically so you can use **XMVECTORF32** in most of the same contexts.</span></span> <span data-ttu-id="47643-151">Alle Schreibvorgänge für eine **XMVECTORF32** -Klasse erfordern explizit Verweise auf das. v- **xmvector** -Element.</span><span class="sxs-lookup"><span data-stu-id="47643-151">Any write operations to an **XMVECTORF32** class require explicitly referencing the .v **XMVECTOR** member.</span></span>

## <a name="permute"></a><span data-ttu-id="47643-152">Permute</span><span class="sxs-lookup"><span data-stu-id="47643-152">Permute</span></span>

<span data-ttu-id="47643-153">Die mathematische XNA-Bibliothek enthielt die folgende Form für allgemeine Vektor perstumm Schaltung:</span><span class="sxs-lookup"><span data-stu-id="47643-153">The XNA Math library had the following form for general vector permute:</span></span>


```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```



<span data-ttu-id="47643-154">Für directxmath wurde **xmvector permutecontrol** entfernt, und das XM- \_ perstumm Zeichen \_ 0x..</span><span class="sxs-lookup"><span data-stu-id="47643-154">For DirectXMath, **XMVectorPermuteControl** has been eliminated and the XM\_PERMUTE\_0X ..</span></span> <span data-ttu-id="47643-155">XM- \_ perstumm- \_ 1Z-Konstanten wurden neu definiert, sodass Sie einfache 0-7-Indizes sind.</span><span class="sxs-lookup"><span data-stu-id="47643-155">XM\_PERMUTE\_1Z constants have been redefined to be simple 0-7 indices.</span></span> <span data-ttu-id="47643-156">Hier ist die neue Signatur für [**xmvectorperstumm**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span><span class="sxs-lookup"><span data-stu-id="47643-156">Here is the new signature for [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span></span>


```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```



<span data-ttu-id="47643-157">Diese Funktion nimmt anstelle eines Steuer Worts direkt die vier Indizes als Parameter an, die Sie analog zur [**xmvectorswizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) -Funktion mit dem neuen XM- \_ Swizzle X verwenden \_ .</span><span class="sxs-lookup"><span data-stu-id="47643-157">Instead of a control word, this function directly takes the 4 indices as parameters, which also makes it analogous to the [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) function using the new XM\_SWIZZLE\_X ..</span></span> <span data-ttu-id="47643-158">XM- \_ SwiWrapper-Konstanten, die \_ als einfache 0-3-Indizes definiert sind.</span><span class="sxs-lookup"><span data-stu-id="47643-158">XM\_SWIZZLE\_W constants defined as simple 0-3 indices.</span></span>


```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```



> [!Note]  
> <span data-ttu-id="47643-159">Für konstante Werte gibt es eine viel effizientere Methode zum Implementieren von perstumm.</span><span class="sxs-lookup"><span data-stu-id="47643-159">For constant values, there is a much more efficient way to implement permute.</span></span> <span data-ttu-id="47643-160">Verwenden Sie das **Vorlagen** Formular, anstatt das Funktions Formular von [**xmvectorperstumm**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="47643-160">Instead of using the function form of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use the **template** form:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
> </tr>
> </tbody>
> </table>
>  
>
> ## <a name="template-forms"></a><span data-ttu-id="47643-161">Vorlagen Formulare</span><span class="sxs-lookup"><span data-stu-id="47643-161">Template Forms</span></span>
>
> <span data-ttu-id="47643-162">Im Allgemeinen ist die Verwendung eines Vorlagen Formulars über eine Funktions Form der folgenden Funktionen weitaus effizienter und ermöglicht der Bibliothek das Durchführen von plattformspezifischen Optimierungen durch die Vorlagen Spezialisierung.</span><span class="sxs-lookup"><span data-stu-id="47643-162">In general, using a template form over a function form of the following functions is much more efficient and allows the library to do platform specific optimizations through template specialization.</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
>     XMVECTOR XMVectorSwizzle(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateLeft(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateRight(FXMVECTOR V)
>
> template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
>     XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> ## <a name="eliminated-functions"></a><span data-ttu-id="47643-163">Eliminieren von Funktionen</span><span class="sxs-lookup"><span data-stu-id="47643-163">Eliminated Functions</span></span>
>
> 
>
> | <span data-ttu-id="47643-164">Funktion eliminiert</span><span class="sxs-lookup"><span data-stu-id="47643-164">Eliminated Function</span></span>        | <span data-ttu-id="47643-165">Ersetzung</span><span class="sxs-lookup"><span data-stu-id="47643-165">Replacement</span></span>                                                                                                       |
> |----------------------------|-------------------------------------------------------------------------------------------------------------------|
> | <span data-ttu-id="47643-166">XMStoreFloat3x3NC</span><span class="sxs-lookup"><span data-stu-id="47643-166">XMStoreFloat3x3NC</span></span>          | [<span data-ttu-id="47643-167">**XMStoreFloat3x3**</span><span class="sxs-lookup"><span data-stu-id="47643-167">**XMStoreFloat3x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
> | <span data-ttu-id="47643-168">XMStoreFloat4NC</span><span class="sxs-lookup"><span data-stu-id="47643-168">XMStoreFloat4NC</span></span>            | [<span data-ttu-id="47643-169">**XMStoreFloat4**</span><span class="sxs-lookup"><span data-stu-id="47643-169">**XMStoreFloat4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
> | <span data-ttu-id="47643-170">XMStoreFloat4x3NC</span><span class="sxs-lookup"><span data-stu-id="47643-170">XMStoreFloat4x3NC</span></span>          | [<span data-ttu-id="47643-171">**XMStoreFloat4x3**</span><span class="sxs-lookup"><span data-stu-id="47643-171">**XMStoreFloat4x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
> | <span data-ttu-id="47643-172">XMStoreFloat4x4NC</span><span class="sxs-lookup"><span data-stu-id="47643-172">XMStoreFloat4x4NC</span></span>          | [<span data-ttu-id="47643-173">**XMStoreFloat4x4**</span><span class="sxs-lookup"><span data-stu-id="47643-173">**XMStoreFloat4x4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
> | <span data-ttu-id="47643-174">XMStoreInt4NC</span><span class="sxs-lookup"><span data-stu-id="47643-174">XMStoreInt4NC</span></span>              | [<span data-ttu-id="47643-175">**XMStoreInt4**</span><span class="sxs-lookup"><span data-stu-id="47643-175">**XMStoreInt4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
> | <span data-ttu-id="47643-176">XMVector2InBoundsR</span><span class="sxs-lookup"><span data-stu-id="47643-176">XMVector2InBoundsR</span></span>         | <span data-ttu-id="47643-177">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="47643-177">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span></span> <span data-ttu-id="47643-178">[XM \_ Crmask \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="47643-178">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="47643-179">XMVector2TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="47643-179">XMVector2TransformStreamNC</span></span> | [<span data-ttu-id="47643-180">**XMVector2TransformStream**</span><span class="sxs-lookup"><span data-stu-id="47643-180">**XMVector2TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
> | <span data-ttu-id="47643-181">XMVector3InBoundsR</span><span class="sxs-lookup"><span data-stu-id="47643-181">XMVector3InBoundsR</span></span>         | <span data-ttu-id="47643-182">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="47643-182">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span></span> <span data-ttu-id="47643-183">[XM \_ Crmask \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="47643-183">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="47643-184">XMVector3TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="47643-184">XMVector3TransformStreamNC</span></span> | [<span data-ttu-id="47643-185">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="47643-185">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
> | <span data-ttu-id="47643-186">XMVector4InBoundsR</span><span class="sxs-lookup"><span data-stu-id="47643-186">XMVector4InBoundsR</span></span>         | <span data-ttu-id="47643-187">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="47643-187">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span></span> <span data-ttu-id="47643-188">[XM \_ Crmask \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="47643-188">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="47643-189">Xmvector coshest</span><span class="sxs-lookup"><span data-stu-id="47643-189">XMVectorCosHEst</span></span>            | [<span data-ttu-id="47643-190">**Xmvector**</span><span class="sxs-lookup"><span data-stu-id="47643-190">**XMVectorCosH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
> | <span data-ttu-id="47643-191">Xmvector Expest</span><span class="sxs-lookup"><span data-stu-id="47643-191">XMVectorExpEst</span></span>             | [<span data-ttu-id="47643-192">**Xmvector Exp**</span><span class="sxs-lookup"><span data-stu-id="47643-192">**XMVectorExp**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
> | <span data-ttu-id="47643-193">Xmvector loerfassung</span><span class="sxs-lookup"><span data-stu-id="47643-193">XMVectorLogEst</span></span>             | [<span data-ttu-id="47643-194">**Xmvector Log**</span><span class="sxs-lookup"><span data-stu-id="47643-194">**XMVectorLog**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
> | <span data-ttu-id="47643-195">Xmvector powest</span><span class="sxs-lookup"><span data-stu-id="47643-195">XMVectorPowEst</span></span>             | [<span data-ttu-id="47643-196">**Xmvector Pow**</span><span class="sxs-lookup"><span data-stu-id="47643-196">**XMVectorPow**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
> | <span data-ttu-id="47643-197">Xmvector sinhest</span><span class="sxs-lookup"><span data-stu-id="47643-197">XMVectorSinHEst</span></span>            | [<span data-ttu-id="47643-198">**Xmvector sinh**</span><span class="sxs-lookup"><span data-stu-id="47643-198">**XMVectorSinH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
> | <span data-ttu-id="47643-199">Xmvector tanhest</span><span class="sxs-lookup"><span data-stu-id="47643-199">XMVectorTanHEst</span></span>            | [<span data-ttu-id="47643-200">**Xmvector**</span><span class="sxs-lookup"><span data-stu-id="47643-200">**XMVectorTanH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |
>
> 
>
>  
>
> ## <a name="related-topics"></a><span data-ttu-id="47643-201">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47643-201">Related topics</span></span>
>
> <dl> <dt>

[<span data-ttu-id="47643-202">Directxmath-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="47643-202">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> </dl>
>
>  
>
>  
>
