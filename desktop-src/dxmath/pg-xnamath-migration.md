---
description: In dieser Übersicht werden die Änderungen beschrieben, die erforderlich sind, um vorhandenen Code mithilfe der XNA Math-Bibliothek zur DirectXMath-Bibliothek zu migrieren.
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: Codemigration aus der XNA Math Library
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc7a48d30711a870c28b677e458a4f72c3b3c40
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549962"
---
# <a name="code-migration-from-the-xna-math-library"></a><span data-ttu-id="9123e-103">Codemigration aus der XNA Math Library</span><span class="sxs-lookup"><span data-stu-id="9123e-103">Code Migration from the XNA Math Library</span></span>

<span data-ttu-id="9123e-104">In dieser Übersicht werden die Änderungen beschrieben, die erforderlich sind, um vorhandenen Code mithilfe der XNA Math-Bibliothek zur DirectXMath-Bibliothek zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="9123e-104">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span>

## <a name="header-changes"></a><span data-ttu-id="9123e-105">Headeränderungen</span><span class="sxs-lookup"><span data-stu-id="9123e-105">Header Changes</span></span>

<span data-ttu-id="9123e-106">Die DirectXMath-Bibliothek verwendet einen neuen Satz von Headern.</span><span class="sxs-lookup"><span data-stu-id="9123e-106">The DirectXMath library uses a new set of headers.</span></span>

<span data-ttu-id="9123e-107">Ersetzen Sie den `xnamath.h` Header durch , und fügen Sie für die `DirectXMath.h` `DirectXPackedVector.h` *gpu-gepackten Typen* hinzu.</span><span class="sxs-lookup"><span data-stu-id="9123e-107">Replace the `xnamath.h` header with `DirectXMath.h`, and add `DirectXPackedVector.h` for the *GPU packed* types.</span></span>

<span data-ttu-id="9123e-108">Die Begrenzungstypen aus dem DirectX SDK Collision-Beispiel in sind jetzt Teil `xnacollision.h` der DirectXMath-Bibliothek in `DirectXCollision.h` .</span><span class="sxs-lookup"><span data-stu-id="9123e-108">The bounding types from the DirectX SDK Collision sample in `xnacollision.h` is now part of the DirectXMath library in `DirectXCollision.h`.</span></span> <span data-ttu-id="9123e-109">Diese wurden so geändert, dass C++-Klassen anstelle einer API im C-Stil verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9123e-109">These have been modified to use C++ classes rather than a C-style API.</span></span>

## <a name="constant-changes"></a><span data-ttu-id="9123e-110">Konstante Änderungen</span><span class="sxs-lookup"><span data-stu-id="9123e-110">Constant Changes</span></span>

<span data-ttu-id="9123e-111">XNAMATH \_ VERSION (200, 201, 202, 203, 204 und so weiter) wurde durch DIRECXTMATH \_ VERSION (300, 301, 302, 303 und so weiter) ersetzt.</span><span class="sxs-lookup"><span data-stu-id="9123e-111">XNAMATH\_VERSION (200, 201, 202, 203, 204, and so on) has been replaced with DIRECXTMATH\_VERSION (300, 301, 302, 303, and so on).</span></span>

> [!NOTE]  
> <span data-ttu-id="9123e-112">DirectXMath 3.00 und 3.02 wurden mit vorläufigen Versionen des Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9123e-112">DirectXMath 3.00 and 3.02 shipped with preliminary versions of the Windows SDK.</span></span> <span data-ttu-id="9123e-113">DirectXMath 3.03 befindet sich in der endgültigen Version des Windows 8 SDK.</span><span class="sxs-lookup"><span data-stu-id="9123e-113">DirectXMath 3.03 is in the final version of the Windows 8 SDK.</span></span>

## <a name="namespaces"></a><span data-ttu-id="9123e-114">Namespaces</span><span class="sxs-lookup"><span data-stu-id="9123e-114">Namespaces</span></span>

<span data-ttu-id="9123e-115">Die DirectXMath-Bibliothek verwendet C++-Namespaces, um die Typen zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="9123e-115">The DirectXMath library uses C++ namespaces to organize the types.</span></span> <span data-ttu-id="9123e-116">XNA Math hat nur den globalen Namespace verwendet.</span><span class="sxs-lookup"><span data-stu-id="9123e-116">XNA Math used only the global namespace.</span></span> <span data-ttu-id="9123e-117">Die DirectXMath-Typen, die XNA Math gemeinsam sind, befinden sich im **DirectX-** oder **DirectX::P ackedVector-Namespace.**</span><span class="sxs-lookup"><span data-stu-id="9123e-117">The DirectXMath types in common with XNA Math are in the **DirectX** or the **DirectX::PackedVector** namespace.</span></span>

<span data-ttu-id="9123e-118">In C++-Quelldateien besteht eine einfache Lösung im Hinzufügen von `using` -Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="9123e-118">In C++ source files, a simple solution is to add `using` statements.</span></span>

```cpp
#include "DirectXMath.h"
#include "DirectXPackedVector.h"

using namespace DirectX; 
using namespace DirectX::PackedVector;
```

<span data-ttu-id="9123e-119">Für Header gilt es nicht als bewährte Methode, using-Anweisungen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9123e-119">For headers, it is not considered best practice to add using statements.</span></span> <span data-ttu-id="9123e-120">Fügen Sie stattdessen vollqualifizierte Namespaces hinzu.</span><span class="sxs-lookup"><span data-stu-id="9123e-120">Instead, add fully-qualified namespaces.</span></span>

```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```

## <a name="partial-loads"></a><span data-ttu-id="9123e-121">Teillasten</span><span class="sxs-lookup"><span data-stu-id="9123e-121">Partial Loads</span></span>

<span data-ttu-id="9123e-122">Für verschiedene Funktionen, die weniger als 4 Elemente eines XMVECTOR laden, hat die XNA Math-Bibliothek die zusätzlichen Elemente nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="9123e-122">For various functions that load less than 4 elements of an XMVECTOR, the XNA Math library left the additional elements undefined.</span></span> <span data-ttu-id="9123e-123">DirectXMath füllt diese zusätzlichen Elemente immer mit 0 auf.</span><span class="sxs-lookup"><span data-stu-id="9123e-123">DirectXMath will always fill these additional elements with 0.</span></span>

## <a name="removal-of-xbox-360-specific-types"></a><span data-ttu-id="9123e-124">Entfernen von Xbox 360 Typen</span><span class="sxs-lookup"><span data-stu-id="9123e-124">Removal of Xbox 360 Specific Types</span></span>

<span data-ttu-id="9123e-125">Die folgenden mathematischen XNA-Bibliothekstypen, -Funktionen und -Konstanten sind in DirectXMath nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9123e-125">The following XNA Math library types, functions, and constants are not available in DirectXMath.</span></span>

-   <span data-ttu-id="9123e-126">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span><span class="sxs-lookup"><span data-stu-id="9123e-126">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span></span>
-   <span data-ttu-id="9123e-127">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span><span class="sxs-lookup"><span data-stu-id="9123e-127">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span></span>
-   <span data-ttu-id="9123e-128">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span><span class="sxs-lookup"><span data-stu-id="9123e-128">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span></span>
-   <span data-ttu-id="9123e-129">g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ XMAddDHen, g \_ XMMulHenD3, g \_ XMMulDHen3, g \_ XMXorHenD3, g \_ XMXorDHen3</span><span class="sxs-lookup"><span data-stu-id="9123e-129">g\_XMMaskHenD3, g\_XMMaskDHen3, g\_XMAddUHenD3, g\_XMAddHenD3, g\_XMAddDHen, g\_XMMulHenD3, g\_XMMulDHen3, g\_XMXorHenD3, g\_XMXorDHen3</span></span>
-   <span data-ttu-id="9123e-130">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span><span class="sxs-lookup"><span data-stu-id="9123e-130">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span></span>
-   <span data-ttu-id="9123e-131">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span><span class="sxs-lookup"><span data-stu-id="9123e-131">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span></span>
-   <span data-ttu-id="9123e-132">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span><span class="sxs-lookup"><span data-stu-id="9123e-132">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span></span>
-   <span data-ttu-id="9123e-133">g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g \_ XMAddIco4, g \_ XMMulIco4</span><span class="sxs-lookup"><span data-stu-id="9123e-133">g\_XMMaskIco4, g\_XMXorXIco4, g\_XMXorIco4, g\_XMAddXIco4, g\_XMAddUIco4, g\_XMAddIco4, g\_XMMulIco4</span></span>

<span data-ttu-id="9123e-134">\_\_vector4i ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="9123e-134">\_\_vector4i is deprecated.</span></span> <span data-ttu-id="9123e-135">Verwenden [**Sie stattdessen XMVECTORI32**](xmvectori32-data-type.md) oder [**XMVECTORU32.**](xmvectoru32-data-type.md)</span><span class="sxs-lookup"><span data-stu-id="9123e-135">Use [**XMVECTORI32**](xmvectori32-data-type.md) or [**XMVECTORU32**](xmvectoru32-data-type.md) instead.</span></span>

<span data-ttu-id="9123e-136">Die folgenden Funktionen und Typen sind veraltet, da sie nur Xbox 360 sind: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span><span class="sxs-lookup"><span data-stu-id="9123e-136">The following functions and types are deprecated as they are Xbox 360 only: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span></span>

## <a name="arm-neon-intrinsics"></a><span data-ttu-id="9123e-137">Systeminterne ARM-NEON-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9123e-137">ARM-NEON Intrinsics</span></span>

<span data-ttu-id="9123e-138">Das Deklarieren einer Vektorkonst constant mit diesem Code wird für XNA Math for SSE und NO-INTRINSICS kompiliert, aber für DirectXMath mit ARM-NEON ist ein Fehler.</span><span class="sxs-lookup"><span data-stu-id="9123e-138">Declaring a vector constant with this code will compile for XNA Math for SSE and NO-INTRINSICS, but will fail for DirectXMath using ARM-NEON.</span></span>

```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```

<span data-ttu-id="9123e-139">Im Allgemeinen wird diese Methode der Initialisierung von [**XMVECTOR**](xmvector-data-type.md)nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="9123e-139">In general, we don't recommend this method of initialization of an [**XMVECTOR**](xmvector-data-type.md).</span></span> <span data-ttu-id="9123e-140">Wenn Sie jedoch eine Vektorkonstive wünschen, unterstützt die [**XMVECTORF32-Klasse**](xmvectorf32-data-type.md) diesen Initialisierungsstil und gibt den **XMVECTOR-Typ** automatisch zurück, sodass Sie **XMVECTORF32** in den meisten der gleichen Kontexte verwenden können.</span><span class="sxs-lookup"><span data-stu-id="9123e-140">However, if you want a vector constant, the [**XMVECTORF32**](xmvectorf32-data-type.md) class supports this style of initialization and returns the **XMVECTOR** type automatically so you can use **XMVECTORF32** in most of the same contexts.</span></span> <span data-ttu-id="9123e-141">Alle Schreibvorgänge in eine **XMVECTORF32-Klasse** erfordern explizites Verweisen auf den **.v XMVECTOR-Member.**</span><span class="sxs-lookup"><span data-stu-id="9123e-141">Any write operations to an **XMVECTORF32** class require explicitly referencing the .v **XMVECTOR** member.</span></span>

## <a name="permute"></a><span data-ttu-id="9123e-142">Permute</span><span class="sxs-lookup"><span data-stu-id="9123e-142">Permute</span></span>

<span data-ttu-id="9123e-143">Die XNA Math-Bibliothek hatte das folgende Formular für allgemeine Vektor-Permute:</span><span class="sxs-lookup"><span data-stu-id="9123e-143">The XNA Math library had the following form for general vector permute:</span></span>

```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```

<span data-ttu-id="9123e-144">Für DirectXMath wurden **XMVectorPermuteControl** und XM \_ PERMUTE \_ 0X entfernt.</span><span class="sxs-lookup"><span data-stu-id="9123e-144">For DirectXMath, **XMVectorPermuteControl** has been eliminated and the XM\_PERMUTE\_0X ..</span></span> <span data-ttu-id="9123e-145">XM \_ PERMUTE \_ 1Z-Konstanten wurden als einfache 0-7-Indizes neu definiert.</span><span class="sxs-lookup"><span data-stu-id="9123e-145">XM\_PERMUTE\_1Z constants have been redefined to be simple 0-7 indices.</span></span> <span data-ttu-id="9123e-146">Dies ist die neue Signatur für [**XMVectorPermute:**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)</span><span class="sxs-lookup"><span data-stu-id="9123e-146">Here is the new signature for [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span></span>

```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```

<span data-ttu-id="9123e-147">Anstelle eines Steuerworts nimmt diese Funktion die 4 Indizes direkt als Parameter an, wodurch sie auch analog zur [**XMVectorSwizzle-Funktion**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) mit dem neuen XM \_ SWIZZLE \_ X .</span><span class="sxs-lookup"><span data-stu-id="9123e-147">Instead of a control word, this function directly takes the 4 indices as parameters, which also makes it analogous to the [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) function using the new XM\_SWIZZLE\_X ..</span></span> <span data-ttu-id="9123e-148">XM \_ SWIZZLE \_ W-Konstanten, die als einfache 0-3-Indizes definiert sind.</span><span class="sxs-lookup"><span data-stu-id="9123e-148">XM\_SWIZZLE\_W constants defined as simple 0-3 indices.</span></span>

```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```

> [!NOTE]
> <span data-ttu-id="9123e-149">Für konstante Werte gibt es eine viel effizientere Möglichkeit, Permute zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="9123e-149">For constant values, there is a much more efficient way to implement permute.</span></span> <span data-ttu-id="9123e-150">Verwenden Sie anstelle des Funktionsformulars [**von XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)das **Vorlagenformular:**</span><span class="sxs-lookup"><span data-stu-id="9123e-150">Instead of using the function form of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use the **template** form:</span></span>

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
```

## <a name="template-forms"></a><span data-ttu-id="9123e-151">Vorlagenformulare</span><span class="sxs-lookup"><span data-stu-id="9123e-151">Template Forms</span></span>

<span data-ttu-id="9123e-152">Im Allgemeinen ist die Verwendung eines Vorlagenformulars über eine Funktionsform der folgenden Funktionen wesentlich effizienter und ermöglicht es der Bibliothek, plattformspezifische Optimierungen durch Vorlagenspezialisierung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9123e-152">In general, using a template form over a function form of the following functions is much more efficient and allows the library to do platform specific optimizations through template specialization.</span></span>

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
    XMVECTOR XMVectorSwizzle(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateLeft(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateRight(FXMVECTOR V)

template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
    XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
```

## <a name="eliminated-functions"></a><span data-ttu-id="9123e-153">Entfernte Funktionen</span><span class="sxs-lookup"><span data-stu-id="9123e-153">Eliminated Functions</span></span>

| <span data-ttu-id="9123e-154">Entfernte Funktion</span><span class="sxs-lookup"><span data-stu-id="9123e-154">Eliminated Function</span></span>        | <span data-ttu-id="9123e-155">Ersetzung</span><span class="sxs-lookup"><span data-stu-id="9123e-155">Replacement</span></span>                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9123e-156">XMStoreFloat3x3NC</span><span class="sxs-lookup"><span data-stu-id="9123e-156">XMStoreFloat3x3NC</span></span>          | [<span data-ttu-id="9123e-157">**XMStoreFloat3x3**</span><span class="sxs-lookup"><span data-stu-id="9123e-157">**XMStoreFloat3x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
| <span data-ttu-id="9123e-158">XMStoreFloat4NC</span><span class="sxs-lookup"><span data-stu-id="9123e-158">XMStoreFloat4NC</span></span>            | [<span data-ttu-id="9123e-159">**XMStoreFloat4**</span><span class="sxs-lookup"><span data-stu-id="9123e-159">**XMStoreFloat4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
| <span data-ttu-id="9123e-160">XMStoreFloat4x3NC</span><span class="sxs-lookup"><span data-stu-id="9123e-160">XMStoreFloat4x3NC</span></span>          | [<span data-ttu-id="9123e-161">**XMStoreFloat4x3**</span><span class="sxs-lookup"><span data-stu-id="9123e-161">**XMStoreFloat4x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
| <span data-ttu-id="9123e-162">XMStoreFloat4x4NC</span><span class="sxs-lookup"><span data-stu-id="9123e-162">XMStoreFloat4x4NC</span></span>          | [<span data-ttu-id="9123e-163">**XMStoreFloat4x4**</span><span class="sxs-lookup"><span data-stu-id="9123e-163">**XMStoreFloat4x4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
| <span data-ttu-id="9123e-164">XMStoreInt4NC</span><span class="sxs-lookup"><span data-stu-id="9123e-164">XMStoreInt4NC</span></span>              | [<span data-ttu-id="9123e-165">**XMStoreInt4**</span><span class="sxs-lookup"><span data-stu-id="9123e-165">**XMStoreInt4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
| <span data-ttu-id="9123e-166">XMVector2InBoundsR</span><span class="sxs-lookup"><span data-stu-id="9123e-166">XMVector2InBoundsR</span></span>         | <span data-ttu-id="9123e-167">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="9123e-167">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span></span> <span data-ttu-id="9123e-168">[XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0</span><span class="sxs-lookup"><span data-stu-id="9123e-168">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="9123e-169">XMVector2TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="9123e-169">XMVector2TransformStreamNC</span></span> | [<span data-ttu-id="9123e-170">**XMVector2TransformStream**</span><span class="sxs-lookup"><span data-stu-id="9123e-170">**XMVector2TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
| <span data-ttu-id="9123e-171">XMVector3InBoundsR</span><span class="sxs-lookup"><span data-stu-id="9123e-171">XMVector3InBoundsR</span></span>         | <span data-ttu-id="9123e-172">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="9123e-172">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span></span> <span data-ttu-id="9123e-173">[XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0</span><span class="sxs-lookup"><span data-stu-id="9123e-173">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="9123e-174">XMVector3TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="9123e-174">XMVector3TransformStreamNC</span></span> | [<span data-ttu-id="9123e-175">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="9123e-175">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
| <span data-ttu-id="9123e-176">XMVector4InBoundsR</span><span class="sxs-lookup"><span data-stu-id="9123e-176">XMVector4InBoundsR</span></span>         | <span data-ttu-id="9123e-177">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="9123e-177">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span></span> <span data-ttu-id="9123e-178">[XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0</span><span class="sxs-lookup"><span data-stu-id="9123e-178">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
| <span data-ttu-id="9123e-179">XMVectorCosHEst</span><span class="sxs-lookup"><span data-stu-id="9123e-179">XMVectorCosHEst</span></span>            | [<span data-ttu-id="9123e-180">**XMVectorCosH**</span><span class="sxs-lookup"><span data-stu-id="9123e-180">**XMVectorCosH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
| <span data-ttu-id="9123e-181">XMVectorExpEst</span><span class="sxs-lookup"><span data-stu-id="9123e-181">XMVectorExpEst</span></span>             | [<span data-ttu-id="9123e-182">**XMVectorExp**</span><span class="sxs-lookup"><span data-stu-id="9123e-182">**XMVectorExp**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
| <span data-ttu-id="9123e-183">XMVectorLogEst</span><span class="sxs-lookup"><span data-stu-id="9123e-183">XMVectorLogEst</span></span>             | [<span data-ttu-id="9123e-184">**XMVectorLog**</span><span class="sxs-lookup"><span data-stu-id="9123e-184">**XMVectorLog**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
| <span data-ttu-id="9123e-185">XMVectorPowEst</span><span class="sxs-lookup"><span data-stu-id="9123e-185">XMVectorPowEst</span></span>             | [<span data-ttu-id="9123e-186">**XMVectorPow**</span><span class="sxs-lookup"><span data-stu-id="9123e-186">**XMVectorPow**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
| <span data-ttu-id="9123e-187">XMVectorSinHEst</span><span class="sxs-lookup"><span data-stu-id="9123e-187">XMVectorSinHEst</span></span>            | [<span data-ttu-id="9123e-188">**XMVectorSinH**</span><span class="sxs-lookup"><span data-stu-id="9123e-188">**XMVectorSinH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
| <span data-ttu-id="9123e-189">XMVectorTanHEst</span><span class="sxs-lookup"><span data-stu-id="9123e-189">XMVectorTanHEst</span></span>            | [<span data-ttu-id="9123e-190">**XMVectorTanH**</span><span class="sxs-lookup"><span data-stu-id="9123e-190">**XMVectorTanH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |

## <a name="related-topics"></a><span data-ttu-id="9123e-191">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9123e-191">Related topics</span></span>

[<span data-ttu-id="9123e-192">DirectXMath-Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="9123e-192">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
