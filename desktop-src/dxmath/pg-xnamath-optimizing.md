---
description: In diesem Thema werden Überlegungen zur Optimierung und Strategien mit der DirectXMath-Bibliothek beschrieben.
ms.assetid: bcbf8ae1-ed49-fdf7-812d-b2089537ab28
title: Codeoptimierung mit der DirectXMath-Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15369ab36e199eb1a204cc4b761dc637f114f2a1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827254"
---
# <a name="code-optimization-with-the-directxmath-library"></a>Codeoptimierung mit der DirectXMath-Bibliothek

In diesem Thema werden Überlegungen zur Optimierung und Strategien mit der DirectXMath-Bibliothek beschrieben.

-   [Verwenden von Accessoren mit geringer Freundlichkeit](#use-accessors-sparingly)
-   [Verwenden der richtigen Kompilierungseinstellungen](#use-correct-compilation-settings)
-   [Verwenden von Est-Funktionen bei Bedarf](#use-est-functions-when-appropriate)
-   [Verwenden von ausgerichteten Datentypen und Vorgängen](#use-aligned-data-types-and-operations)
-   [Ordnungsgemäßes Ausrichten von Zuordnungen](#properly-align-allocations)
-   [Vermeiden von Operatorüberladungen nach Möglichkeit](#avoid-operator-overloads-when-possible)
-   [Abbrüche](#denormals)
-   [Nutzen der Dualität von ganzzahligen Gleitkommazahlen](#take-advantage-of-the-integer-floating-point-duality)
-   [Vorlagenformulare bevorzugen](#prefer-template-forms)
-   [Verwenden von DirectXMath mit Direct3D](#using-directxmath-with-direct3d)
-   [Verwandte Themen](#related-topics)

## <a name="use-accessors-sparingly"></a>Verwenden von Accessoren mit geringem Nutzen

Vektorbasierte Vorgänge verwenden die SIMD-Anweisungssätze, und diese verwenden spezielle Register. Für den Zugriff auf einzelne Komponenten muss von den SIMD-Registern zu den Skalarregistern und wieder zurück verschoben werden.

Nach Möglichkeit ist es effizienter, alle Komponenten eines [**XMVECTOR**](xmvector-data-type.md) gleichzeitig zu initialisieren, anstatt eine Reihe einzelner Vektoraccessoren zu verwenden.

## <a name="use-correct-compilation-settings"></a>Verwenden der richtigen Kompilierungseinstellungen

Aktivieren Sie für Windows x86-Ziele /arch:SSE2. Aktivieren Sie für alle Windows-Ziele /fp:fast.

Standardmäßig erfolgt die Kompilierung für die DirectXMath-Bibliothek für x86-Fensterziele mit \_ definierten XM \_ SSE \_ \_ INTRINSICS. Dies bedeutet, dass alle DirectXMath-Funktionen SSE2-Anweisungen verwenden. Dies gilt jedoch nicht für anderen Code.

Code außerhalb von DirectXMath wird mithilfe von Compilerstandard verwendet. Ohne diesen Schalter verwendet der generierte Code möglicherweise häufig den weniger effizienten x87-Code.

Es wird dringend empfohlen, immer die neueste verfügbare Version des Compilers zu verwenden.

## <a name="use-est-functions-when-appropriate"></a>Verwenden von Est-Funktionen bei Bedarf

Viele Funktionen verfügen über eine entsprechende Schätzfunktion, die auf Est endet. Diese Funktionen tauschen eine gewisse Genauigkeit für eine verbesserte Leistung aus. Est-Funktionen eignen sich für nicht kritische Berechnungen, bei denen die Genauigkeit auf geschwindigkeitsvergehend abgestellt werden kann. Die genaue Menge an genauigkeits- und geschwindigkeitsbedingten Verlusten hängt von der Plattform ab.

Beispielsweise könnte die [**XMVector3AngleBetweenNormalsEst-Funktion**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormalsest) anstelle der [**XMVector3AngleBetweenNormals-Funktion**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormals) verwendet werden.

## <a name="use-aligned-data-types-and-operations"></a>Verwenden von ausgerichteten Datentypen und Vorgängen

Die SIMD-Anweisungssätze für Versionen von Fenstern, die SSE2 unterstützen, verfügen in der Regel über ausgerichtete und nicht ausgerichtete Versionen von Speichervorgängen. Die Verwendung der ausgerichteten Vorgänge ist schneller und sollte nach Möglichkeit bevorzugt werden.

Die DirectXMath-Bibliothek bietet über Variantenvektortypen, -struktur und -funktionen zugriffsorientierte und nicht ausgerichtete Funktionen. Diese Varianten werden durch ein "A" am Ende des Namens angegeben.

Beispielsweise gibt es eine nicht ausgerichtete [**XMFLOAT4X4-Struktur**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) und eine ausgerichtete [**XMFLOAT4X4A-Struktur,**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) die von den [**Funktionen XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4) bzw. [**XMStoreFloat4A**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4a) verwendet werden.

## <a name="properly-align-allocations"></a>Ordnungsgemäßes Ausrichten von Zuordnungen

Die ausgerichteten Versionen der [systeminternen SSE-Funktionen,](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) die der DirectXMath-Bibliothek zugrunde liegen, sind schneller als die nicht ausgerichteten.

Aus diesem Grund gehen DirectXMath-Vorgänge, die [**XMVECTOR-**](xmvector-data-type.md) und [**XMMATRIX-Objekte**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) verwenden, davon aus, dass diese Objekte 16-Byte-ausgerichtet sind. Dies erfolgt automatisch für stapelbasierte Zuordnungen, wenn Code mithilfe der empfohlenen Windows-Compilereinstellungen für die DirectXMath-Bibliothek kompiliert wird (siehe [Verwenden der richtigen Kompilierungseinstellungen).](#use-correct-compilation-settings) Es ist jedoch wichtig sicherzustellen, dass die Heapzuordnung, die **XMVECTOR-** und **XMMATRIX-Objekte** oder Umwandlungen in diese Typen enthält, diese Ausrichtungsanforderungen erfüllt.

Während 64-Bit-Windows-Speicherbelegungen 16-Byte-ausgerichtet sind, wird bei 32-Bit-Versionen des zugeordneten Windows-Arbeitsspeichers standardmäßig nur 8 Byte ausgerichtet. Informationen zum Steuern der Speicherausrichtung finden Sie unter [ \_ aligned \_ malloc](https://docs.microsoft.com/cpp/c-runtime-library/reference/aligned-malloc).

Wenn Sie ausgerichtete DirectXMath-Typen mit der Standardvorlagenbibliothek (STL) verwenden, müssen Sie eine benutzerdefinierte Zuweisung bereitstellen, die die 16-Byte-Ausrichtung sicherstellt. Im [Blog](https://devblogs.microsoft.com/cppblog/the-mallocator/) Visual C++ Team finden Sie ein Beispiel für das Schreiben einer benutzerdefinierten Zuweisung (anstelle von malloc/free sollten Sie \_ in Ihrer Implementierung "aligned \_ malloc" und \_ "aligned \_ free" verwenden).

> [!Note]  
> Einige STL-Vorlagen ändern die Ausrichtung des bereitgestellten Typs. Wenn Sie z. [ \_ B. freigegebene<>](/cpp/standard-library/memory-functions?view=vs-2017&preserve-view=true) einige interne Nachverfolgungsinformationen hinzufügen, die die Ausrichtung des bereitgestellten Benutzertyps möglicherweise nicht berücksichtigen, führt dies zu nicht ausgerichteten Datenmembern. In diesem Fall müssen Sie nicht ausgerichtete Typen anstelle von ausgerichteten Typen verwenden. Wenn Sie von vorhandenen Klassen ableiten, einschließlich vieler Windows-Runtime-Objekte, können Sie auch die Ausrichtung einer Klasse oder Struktur ändern.

 

## <a name="avoid-operator-overloads-when-possible"></a>Vermeiden von Operatorüberladungen nach Möglichkeit

Zur Vereinfachung verfügen verschiedene Typen wie [**XMVECTOR**](xmvector-data-type.md) und [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) über Operatorüberladungen für allgemeine arithmetische Operationen. Solche Operatorüberladungen erstellen in der Regel zahlreiche temporäre Objekte. Es wird empfohlen, diese Operatorüberladungen in leistungsabhängigem Code zu vermeiden.

## <a name="denormals"></a>Abbrüche

Um Berechnungen in der Nähe von 0 zu unterstützen, enthält der IEEE 754-Gleitkomma-Standard Unterstützung für den schrittweisen Unterlauf. Der schrittweise Unterlauf wird durch die Verwendung denormalisierter Werte implementiert, und viele Hardwareimplementierungen sind bei der Behandlung von Denormals langsam. Eine zu berücksichtigende Optimierung besteht darin, die Behandlung von Denormals für die von DirectXMath verwendeten Vektorvorgänge zu deaktivieren.

Das Ändern der Behandlung von Denormals erfolgt mithilfe der [ \_ controlfp \_ s-Routine](/cpp/c-runtime-library/reference/controlfp-s) auf Präthreadbasis und kann zu Leistungsverbesserungen führen. Verwenden Sie diesen Code, um die Behandlung von Denormals zu ändern:


```
  #include <float.h>;
    unsigned int control_word;
    _controlfp_s( &control_word, _DN_FLUSH, _MCW_DN );
```



> [!Note]  
> In 64-Bit-Versionen von Windows werden [SSE-Anweisungen](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) für alle Berechnungen verwendet, nicht nur für vektorbasierte Vorgänge. Das Ändern der Denormalbehandlung wirkt sich auf alle Gleitkommaberechnungen in Ihrem Programm aus, nicht nur auf die von DirectXMath verwendeten Vektorvorgänge.

 

## <a name="take-advantage-of-the-integer-floating-point-duality"></a>Nutzen der Dualität von ganzzahligen Gleitkommazahlen

DirectXMath unterstützt Vektoren mit vier Gleitkommawerten mit einfacher Genauigkeit oder vier 32-Bit-Werten (mit oder ohne Vorzeichen).

Da die Anweisungssätze, die zum Implementieren der DirectXMath-Bibliothek verwendet werden, die gleichen Daten wie mehrere verschiedene Typen behandeln können, können sie beispielsweise denselben Vektor wie Gleitkomma- und Ganzzahldaten behandeln. Bestimmte Optimierungen können erreicht werden. Sie können diese Optimierungen abrufen, indem Sie die Initialisierungsroutinen für ganzzahlige Vektoren und bitweise Operatoren verwenden, um Gleitkommawerte zu bearbeiten.

Das binäre Format von Gleitkommazahlen mit einfacher Genauigkeit, das von der DirectXMath-Bibliothek verwendet wird, entspricht vollständig dem IEEE 764-Standard:

``` syntax
     SIGN    EXPONENT   MANTISSA
     X       XXXXXXXX   XXXXXXXXXXXXXXXXXXXXXXX
     1 bit   8 bits     23 bits
```

Bei der Arbeit mit der Ieee 764-Gleitkommazahl mit einfacher Genauigkeit ist es wichtig zu beachten, dass einige Darstellungen eine besondere Bedeutung haben (d. h., sie entsprechen nicht der vorherigen Beschreibung). Beispiele:

-   Positive Null ist 0
-   Negative Null ist 0x80000000
-   Q \_ NAN ist 07FC0000
-   +INF ist 0x7F800000
-   -INF ist 0xFF800000

## <a name="prefer-template-forms"></a>Vorlagenformulare bevorzugen

Das Vorlagenformular ist für [**XMVectorSwizzle,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) [**XMVectorPermute,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) [**XMVectorInsert,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) [**XMVectorShiftLeft,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft)und [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright)vorhanden. Wenn sie anstelle der allgemeinen Funktionsform verwendet werden, kann der Compiler wesentlich komplexere Implementierungen erstellen. Bei [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100))wird dies häufig auf einen oder zwei \_ mm \_ shuffle \_ ps-Werte reduziert. Für ARM-NEON kann die **XMVectorSwizzle-Vorlage** eine Reihe von Sonderfällen anstelle der allgemeineren VTBL-Swizzle/Permute verwenden.

## <a name="using-directxmath-with-direct3d"></a>Verwenden von DirectXMath mit Direct3D

Eine häufige Verwendung von DirectXMath ist die Durchführung von Grafikberechnungen für die Verwendung mit Direct3D. Mit Direct3D 10.x und Direct3D 11.x können Sie die DirectXMath-Bibliothek direkt verwenden:

-   Verwenden Sie die [Colors-Namespacekonstanten](ovw-xnamath-reference-constants.md) direkt im *ColorRGBA-Parameter* in einem Aufruf der [**ID3D11DeviceContext::ClearRenderTargetView-**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-clearrendertargetview) oder [**ID3D10Device::ClearRenderTargetView-Methode.**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-clearrendertargetview) Für Direct3D 9 müssen Sie in den [**XMCOLOR-Typ**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) konvertieren, um ihn als *Color-Parameter* in einem Aufruf der [**IDirect3DDevice9::Clear-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) zu verwenden.
-   Verwenden Sie die [**XMFLOAT4-XMVECTOR-**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) / [](xmvector-data-type.md) und [**XMFLOAT4X4-XMMATRIX-Typen,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)um konstante / [](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) Pufferstrukturen für den Verweis durch HLSL [**float4-**](../direct3dhlsl/dx-graphics-hlsl-scalar.md) oder [**matrix**](../direct3dhlsl/dx-graphics-hlsl-matrix.md)/float4x4-Typen einzurichten.
    > [!Note]  
    > [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) / [**XMMATRIX-Typen**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) liegen im Zeilen-Hauptformat vor. Wenn Sie daher den Compilerschalter /Zpr (das Kompilierungsflag [**D3DCOMPILE \_ PACK MATRIX COLUMN \_ \_ \_ MAJOR)**](../direct3dhlsl/d3dcompile-constants.md) verwenden oder das Schlüsselwort row \_ major weglassen, wenn Sie den Matrixtyp in HLSL deklarieren, müssen Sie die Matrix transponieren, wenn Sie sie in den Konstantenpuffer festlegen. [](../direct3dhlsl/dx-graphics-hlsl-appendix-keywords.md)

     

-   Bei Direct3D 10.x und Direct3D 11.x können Sie davon ausgehen, dass der von der Map-Methode (z. B. [**ID3D11DeviceContext::Map) zurückgegebene**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)Zeiger im **pData-Member** ([**D3D10 \_ MAPPED \_ TEXTURE2D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture2d)) ist.**pData**, [**D3D10 \_ MAPPED \_ TEXTURE3D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture3d).**pData** oder [**D3D11 \_ MAPPED \_ SUBRESOURCE**](/windows/win32/api/d3d11/ns-d3d11-d3d11_mapped_subresource).**pData**) ist auf 16 Byte ausgerichtet, wenn Sie [die Featureebene](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 10 \_ 0 oder höher oder [**D3D11 \_ USAGE \_ STAGING-Ressourcen**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectXMath-Programmierhandbuch](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
