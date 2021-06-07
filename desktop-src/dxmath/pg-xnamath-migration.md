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
# <a name="code-migration-from-the-xna-math-library"></a>Codemigration aus der XNA Math Library

In dieser Übersicht werden die Änderungen beschrieben, die erforderlich sind, um vorhandenen Code mithilfe der XNA Math-Bibliothek zur DirectXMath-Bibliothek zu migrieren.

## <a name="header-changes"></a>Headeränderungen

Die DirectXMath-Bibliothek verwendet einen neuen Satz von Headern.

Ersetzen Sie den `xnamath.h` Header durch , und fügen Sie für die `DirectXMath.h` `DirectXPackedVector.h` *gpu-gepackten Typen* hinzu.

Die Begrenzungstypen aus dem DirectX SDK Collision-Beispiel in sind jetzt Teil `xnacollision.h` der DirectXMath-Bibliothek in `DirectXCollision.h` . Diese wurden so geändert, dass C++-Klassen anstelle einer API im C-Stil verwendet werden.

## <a name="constant-changes"></a>Konstante Änderungen

XNAMATH \_ VERSION (200, 201, 202, 203, 204 und so weiter) wurde durch DIRECXTMATH \_ VERSION (300, 301, 302, 303 und so weiter) ersetzt.

> [!NOTE]  
> DirectXMath 3.00 und 3.02 wurden mit vorläufigen Versionen des Windows SDK. DirectXMath 3.03 befindet sich in der endgültigen Version des Windows 8 SDK.

## <a name="namespaces"></a>Namespaces

Die DirectXMath-Bibliothek verwendet C++-Namespaces, um die Typen zu organisieren. XNA Math hat nur den globalen Namespace verwendet. Die DirectXMath-Typen, die XNA Math gemeinsam sind, befinden sich im **DirectX-** oder **DirectX::P ackedVector-Namespace.**

In C++-Quelldateien besteht eine einfache Lösung im Hinzufügen von `using` -Anweisungen.

```cpp
#include "DirectXMath.h"
#include "DirectXPackedVector.h"

using namespace DirectX; 
using namespace DirectX::PackedVector;
```

Für Header gilt es nicht als bewährte Methode, using-Anweisungen hinzuzufügen. Fügen Sie stattdessen vollqualifizierte Namespaces hinzu.

```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```

## <a name="partial-loads"></a>Teillasten

Für verschiedene Funktionen, die weniger als 4 Elemente eines XMVECTOR laden, hat die XNA Math-Bibliothek die zusätzlichen Elemente nicht definiert. DirectXMath füllt diese zusätzlichen Elemente immer mit 0 auf.

## <a name="removal-of-xbox-360-specific-types"></a>Entfernen von Xbox 360 Typen

Die folgenden mathematischen XNA-Bibliothekstypen, -Funktionen und -Konstanten sind in DirectXMath nicht verfügbar.

-   HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3
-   XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()
-   XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()
-   g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ XMAddDHen, g \_ XMMulHenD3, g \_ XMMulDHen3, g \_ XMXorHenD3, g \_ XMXorDHen3
-   XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4
-   XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()
-   XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()
-   g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g \_ XMAddIco4, g \_ XMMulIco4

\_\_vector4i ist veraltet. Verwenden [**Sie stattdessen XMVECTORI32**](xmvectori32-data-type.md) oder [**XMVECTORU32.**](xmvectoru32-data-type.md)

Die folgenden Funktionen und Typen sind veraltet, da sie nur Xbox 360 sind: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.

## <a name="arm-neon-intrinsics"></a>Systeminterne ARM-NEON-Eigenschaften

Das Deklarieren einer Vektorkonst constant mit diesem Code wird für XNA Math for SSE und NO-INTRINSICS kompiliert, aber für DirectXMath mit ARM-NEON ist ein Fehler.

```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```

Im Allgemeinen wird diese Methode der Initialisierung von [**XMVECTOR**](xmvector-data-type.md)nicht empfohlen. Wenn Sie jedoch eine Vektorkonstive wünschen, unterstützt die [**XMVECTORF32-Klasse**](xmvectorf32-data-type.md) diesen Initialisierungsstil und gibt den **XMVECTOR-Typ** automatisch zurück, sodass Sie **XMVECTORF32** in den meisten der gleichen Kontexte verwenden können. Alle Schreibvorgänge in eine **XMVECTORF32-Klasse** erfordern explizites Verweisen auf den **.v XMVECTOR-Member.**

## <a name="permute"></a>Permute

Die XNA Math-Bibliothek hatte das folgende Formular für allgemeine Vektor-Permute:

```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```

Für DirectXMath wurden **XMVectorPermuteControl** und XM \_ PERMUTE \_ 0X entfernt. XM \_ PERMUTE \_ 1Z-Konstanten wurden als einfache 0-7-Indizes neu definiert. Dies ist die neue Signatur für [**XMVectorPermute:**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)

```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```

Anstelle eines Steuerworts nimmt diese Funktion die 4 Indizes direkt als Parameter an, wodurch sie auch analog zur [**XMVectorSwizzle-Funktion**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) mit dem neuen XM \_ SWIZZLE \_ X . XM \_ SWIZZLE \_ W-Konstanten, die als einfache 0-3-Indizes definiert sind.

```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```

> [!NOTE]
> Für konstante Werte gibt es eine viel effizientere Möglichkeit, Permute zu implementieren. Verwenden Sie anstelle des Funktionsformulars [**von XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)das **Vorlagenformular:**

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
```

## <a name="template-forms"></a>Vorlagenformulare

Im Allgemeinen ist die Verwendung eines Vorlagenformulars über eine Funktionsform der folgenden Funktionen wesentlich effizienter und ermöglicht es der Bibliothek, plattformspezifische Optimierungen durch Vorlagenspezialisierung auszuführen.

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

## <a name="eliminated-functions"></a>Entfernte Funktionen

| Entfernte Funktion        | Ersetzung                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| XMStoreFloat3x3NC          | [**XMStoreFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
| XMStoreFloat4NC            | [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
| XMStoreFloat4x3NC          | [**XMStoreFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
| XMStoreFloat4x4NC          | [**XMStoreFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
| XMStoreInt4NC              | [**XMStoreInt4**](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
| XMVector2InBoundsR         | [**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0 |
| XMVector2TransformStreamNC | [**XMVector2TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
| XMVector3InBoundsR         | [**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0 |
| XMVector3TransformStreamNC | [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
| XMVector4InBoundsR         | [**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0 |
| XMVectorCosHEst            | [**XMVectorCosH**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
| XMVectorExpEst             | [**XMVectorExp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
| XMVectorLogEst             | [**XMVectorLog**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
| XMVectorPowEst             | [**XMVectorPow**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
| XMVectorSinHEst            | [**XMVectorSinH**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
| XMVectorTanHEst            | [**XMVectorTanH**](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |

## <a name="related-topics"></a>Zugehörige Themen

[DirectXMath-Programmierhandbuch](ovw-xnamath-progguide.md)
