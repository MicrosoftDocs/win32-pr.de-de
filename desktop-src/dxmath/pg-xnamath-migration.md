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
# <a name="code-migration-from-the-xna-math-library"></a>Code Migration aus der XNA-mathematischen Bibliothek

In dieser Übersicht werden die Änderungen beschrieben, die zum Migrieren von vorhandenem Code mithilfe der XNA-mathematischen Bibliothek zur directxmath-Bibliothek erforderlich sind.

-   [Header Änderungen](#header-changes)
-   [Konstante Änderungen](#constant-changes)
-   [Namespaces](#namespaces)
-   [Partielle Ladevorgänge](#partial-loads)
-   [Entfernen von Xbox 360-spezifischen Typen](#removal-of-xbox-360-specific-types)
-   [Systeminterne Arm-Neon-Funktionen](#arm-neon-intrinsics)
-   [Permute](#permute)
-   [Vorlagen Formulare](#template-forms)
-   [Eliminieren von Funktionen](#eliminated-functions)
-   [Zugehörige Themen](#related-topics)

## <a name="header-changes"></a>Header Änderungen

Die directxmath-Bibliothek verwendet einen neuen Satz von Headern.

Ersetzen Sie den xnamath. h-Header durch directxmath. h, und fügen Sie directxpackedvector. h für die "GPU-gepackten" Typen hinzu.

Die umgebenden Typen aus dem DirectX SDK-Kollisions Beispiel in xnacollision. h sind nun Teil der directxmath-Bibliothek in directxcollision. h. Diese wurden geändert, sodass anstelle einer API im C-Stil C++-Klassen verwendet werden.

## <a name="constant-changes"></a>Konstante Änderungen

Die xnamath- \_ Version (200, 201, 202, 203, 204 usw.) wurde durch die direcxtmath- \_ Version (300, 301, 302, 303 usw.) ersetzt.

> [!Note]  
> Directxmath 3,00 und 3,02 wurden mit vorläufigen Versionen des Windows SDK ausgeliefert. Directxmath 3,03 ist in der endgültigen Version des Windows 8 SDK.

 

## <a name="namespaces"></a>Namespaces

Die directxmath-Bibliothek verwendet C++-Namespaces, um die Typen zu organisieren. XNA Math hat nur den globalen Namespace verwendet. Die allgemeinen directxmath-Typen mit XNA Math befinden sich im "DirectX"-Namespace oder im "DirectX::P ackedvector"-Namespace.

In C++-Quelldateien besteht eine einfache Lösung darin, using-Anweisungen hinzuzufügen:


```
#include “DirectXMath.h”
#include “DirectXPackedVector.h”

using namespace DirectX; 
using namespace DirectX::PackedVector;
```



Bei Headern wird Sie nicht als "bewährte Vorgehensweise" betrachtet, um using-Anweisungen hinzuzufügen. Fügen Sie stattdessen voll qualifizierte Namespaces hinzu:


```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```



## <a name="partial-loads"></a>Partielle Ladevorgänge

Für verschiedene Funktionen, die weniger als vier Elemente eines xmvector laden, wurden die zusätzlichen Elemente in der mathematischen XNA-Bibliothek nicht definiert. Directxmath fügt diese zusätzlichen Elemente immer mit 0 (null) ein.

## <a name="removal-of-xbox-360-specific-types"></a>Entfernen von Xbox 360-spezifischen Typen

Die folgenden XNA-mathematischen Bibliothekstypen,-Funktionen und-Konstanten sind in directxmath nicht verfügbar.

-   HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3
-   XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()
-   XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()
-   g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ xmadddhen, g \_ XMMulHenD3, g \_ XMMulDHen3, g \_ XMXorHenD3, g \_ XMXorDHen3
-   XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4
-   XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()
-   XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()
-   g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g \_ XMAddIco4, g \_ XMMulIco4

\_\_vector4i ist veraltet. Verwenden Sie stattdessen [**XMVECTORI32**](xmvectori32-data-type.md) oder [**XMVECTORU32**](xmvectoru32-data-type.md) .

Die folgenden Funktionen und Typen sind als veraltet markiert, da Sie nur Xbox 360 sind: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.

## <a name="arm-neon-intrinsics"></a>Systeminterne Arm-Neon-Funktionen

Das Deklarieren einer Vektor Konstante mit diesem Code wird für XNA Math für SSE und keine systeminternen Funktionen kompiliert, schlägt jedoch für directxmath mit Arm-Neon fehl.


```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```



Im Allgemeinen wird diese Methode der Initialisierung eines [**xmvector**](xmvector-data-type.md)nicht empfohlen. Wenn Sie jedoch eine Vektor Konstante möchten, unterstützt die [**XMVECTORF32**](xmvectorf32-data-type.md) -Klasse diese Art von Initialisierung und gibt den **xmvector** -Typ automatisch zurück, sodass Sie **XMVECTORF32** in den meisten der gleichen Kontexte verwenden können. Alle Schreibvorgänge für eine **XMVECTORF32** -Klasse erfordern explizit Verweise auf das. v- **xmvector** -Element.

## <a name="permute"></a>Permute

Die mathematische XNA-Bibliothek enthielt die folgende Form für allgemeine Vektor perstumm Schaltung:


```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```



Für directxmath wurde **xmvector permutecontrol** entfernt, und das XM- \_ perstumm Zeichen \_ 0x.. XM- \_ perstumm- \_ 1Z-Konstanten wurden neu definiert, sodass Sie einfache 0-7-Indizes sind. Hier ist die neue Signatur für [**xmvectorperstumm**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):


```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```



Diese Funktion nimmt anstelle eines Steuer Worts direkt die vier Indizes als Parameter an, die Sie analog zur [**xmvectorswizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) -Funktion mit dem neuen XM- \_ Swizzle X verwenden \_ . XM- \_ SwiWrapper-Konstanten, die \_ als einfache 0-3-Indizes definiert sind.


```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```



> [!Note]  
> Für konstante Werte gibt es eine viel effizientere Methode zum Implementieren von perstumm. Verwenden Sie das **Vorlagen** Formular, anstatt das Funktions Formular von [**xmvectorperstumm**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)zu verwenden:
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
> ## <a name="template-forms"></a>Vorlagen Formulare
>
> Im Allgemeinen ist die Verwendung eines Vorlagen Formulars über eine Funktions Form der folgenden Funktionen weitaus effizienter und ermöglicht der Bibliothek das Durchführen von plattformspezifischen Optimierungen durch die Vorlagen Spezialisierung.
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
> ## <a name="eliminated-functions"></a>Eliminieren von Funktionen
>
> 
>
> | Funktion eliminiert        | Ersetzung                                                                                                       |
> |----------------------------|-------------------------------------------------------------------------------------------------------------------|
> | XMStoreFloat3x3NC          | [**XMStoreFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
> | XMStoreFloat4NC            | [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
> | XMStoreFloat4x3NC          | [**XMStoreFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
> | XMStoreFloat4x4NC          | [**XMStoreFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
> | XMStoreInt4NC              | [**XMStoreInt4**](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
> | XMVector2InBoundsR         | [**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ? [XM \_ Crmask \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0 |
> | XMVector2TransformStreamNC | [**XMVector2TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
> | XMVector3InBoundsR         | [**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ? [XM \_ Crmask \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0 |
> | XMVector3TransformStreamNC | [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
> | XMVector4InBoundsR         | [**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ? [XM \_ Crmask \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0 |
> | Xmvector coshest            | [**Xmvector**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
> | Xmvector Expest             | [**Xmvector Exp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
> | Xmvector loerfassung             | [**Xmvector Log**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
> | Xmvector powest             | [**Xmvector Pow**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
> | Xmvector sinhest            | [**Xmvector sinh**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
> | Xmvector tanhest            | [**Xmvector**](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |
>
> 
>
>  
>
> ## <a name="related-topics"></a>Zugehörige Themen
>
> <dl> <dt>

[Directxmath-Programmier Handbuch](ovw-xnamath-progguide.md)
</dt> </dl>
>
>  
>
>  
>
