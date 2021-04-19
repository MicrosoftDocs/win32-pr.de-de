---
description: In diesem Thema werden Überlegungen zur Optimierung und Strategien mit der directxmath-Bibliothek beschrieben.
ms.assetid: bcbf8ae1-ed49-fdf7-812d-b2089537ab28
title: Code Optimierung mit der directxmath-Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11b331077e3d6538952a2f7956641b8b3919e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356586"
---
# <a name="code-optimization-with-the-directxmath-library"></a>Code Optimierung mit der directxmath-Bibliothek

In diesem Thema werden Überlegungen zur Optimierung und Strategien mit der directxmath-Bibliothek beschrieben.

-   [Verwenden Sie Accessoren sparsam](#use-accessors-sparingly)
-   [Korrekte Kompilierungs Einstellungen verwenden](#use-correct-compilation-settings)
-   [Verwenden Sie bei Bedarf EST-Funktionen](#use-est-functions-when-appropriate)
-   [Verwenden von ausgerichteten Datentypen und-Vorgängen](#use-aligned-data-types-and-operations)
-   [Ordnungsgemäße Ausrichtung von Zuweisungen](#properly-align-allocations)
-   [Vermeiden von Operator Überladungen, wenn möglich](#avoid-operator-overloads-when-possible)
-   [Abbrüche](#denormals)
-   [Ausnutzen der ganzzahligen Gleit Komma Zahl](#take-advantage-of-the-integer-floating-point-duality)
-   [Vorlagen Formulare bevorzugen](#prefer-template-forms)
-   [Verwenden von directxmath mit Direct3D](#using-directxmath-with-direct3d)
-   [Zugehörige Themen](#related-topics)

## <a name="use-accessors-sparingly"></a>Verwenden Sie Accessoren sparsam

Bei vektorbasierten Vorgängen werden die SIMD-Anweisungs Sätze verwendet, von denen spezielle Register verwendet werden. Der Zugriff auf einzelne Komponenten erfordert, dass der Wechsel von der SIMD in die skalaren und wieder zurückgeht.

Wenn möglich, ist es effizienter, alle Komponenten eines [**xmvector**](xmvector-data-type.md) gleichzeitig zu initialisieren, anstatt eine Reihe einzelner Vektor Accessoren zu verwenden.

## <a name="use-correct-compilation-settings"></a>Korrekte Kompilierungs Einstellungen verwenden

Aktivieren Sie für Windows x86-Ziele/Arch: SSE2. Aktivieren Sie für alle Windows-Ziele/fp: fast.

Standardmäßig erfolgt die Kompilierung für die directxmath-Bibliothek für Windows x86-Ziele mit den \_ vordefinierten XM SSE-Funktionen \_ \_ \_ . Dies bedeutet, dass für alle directxmath-Funktionen die SSE2-Anweisungen verwendet werden. Das gleiche gilt jedoch nicht für anderen Code.

Code außerhalb von directxmath wird mithilfe von compilerstandardwerten behandelt. Ohne diesen Schalter kann der generierte Code häufig den weniger effizienten x87-Code verwenden.

Es wird dringend empfohlen, immer die neueste verfügbare Version des Compilers zu verwenden.

## <a name="use-est-functions-when-appropriate"></a>Verwenden Sie bei Bedarf EST-Funktionen

Viele Funktionen weisen eine äquivalente Schätz Funktion auf, die auf EST endet. Diese Funktionen Messen eine gewisse Genauigkeit, um die Leistung zu verbessern. EST-Funktionen eignen sich für nicht kritische Berechnungen, bei denen die Genauigkeit für die Geschwindigkeit geopfert werden kann. Die genaue Menge an verlorener Genauigkeit und Geschwindigkeitssteigerung ist plattformabhängig.

Beispielsweise kann die [**XMVector3AngleBetweenNormalsEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormalsest) -Funktion anstelle der [**XMVector3AngleBetweenNormals**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormals) -Funktion verwendet werden.

## <a name="use-aligned-data-types-and-operations"></a>Verwenden von ausgerichteten Datentypen und-Vorgängen

Die SIMD-Anweisungen für Windows-Versionen, die SSE2 unterstützen, verfügen in der Regel über ausgerichtete und nicht ausgerichtete Versionen von Speicher Vorgängen. Die Verwendung der ausgerichteten Vorgänge ist schneller und sollte möglichst bevorzugt werden.

Die directxmath-Bibliothek bietet Zugriff auf ausgerichtete und nicht ausgerichtete Funktionen durch Variant-Vektor Typen,-Strukturen und-Funktionen. Diese Varianten werden durch ein "A" am Ende des Namens angegeben.

Beispielsweise gibt es eine nicht ausgerichtete [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) -Struktur und eine ausgerichtete [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) -Struktur, die von den Funktionen [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4) und [**XMStoreFloat4A**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4a) verwendet werden.

## <a name="properly-align-allocations"></a>Ordnungsgemäße Ausrichtung von Zuweisungen

Die ausgerichteten Versionen der SSE-systeminternen [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) , die der directxmath-Bibliothek zugrunde liegen, sind schneller als die nicht ausgerichtete.

Aus diesem Grund wird von directxmath-Vorgängen mit [**xmvector**](xmvector-data-type.md) -und [**xmmatrix**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) -Objekten angenommen, dass diese Objekte 16-Byte-ausgerichtet sind. Dies erfolgt automatisch bei Stapel basierten Zuordnungen, wenn Code mithilfe der empfohlenen Fenster für die directxmath-Bibliothek kompiliert wird (siehe [verwenden korrekter Kompilierungs Einstellungen](#use-correct-compilation-settings)) Compilereinstellungen. Es ist jedoch wichtig sicherzustellen, dass die Heap Zuordnung, die **xmvector** -und **xmmatrix** -Objekte enthält, oder Umwandlungen in diese Typen diese Ausrichtungs Anforderungen erfüllen.

Während 64-Bit-Windows-Speicher Belegungen mit 16 Byte ausgerichtet sind, ist für 32-Bit-Versionen von zugewiesener Windows-Speicher standardmäßig nur eine 8-Byte-Ausrichtung vorgesehen. Informationen zum Steuern der Arbeitsspeicher Ausrichtung finden Sie unter [ \_ Ausrichten von \_ malloc](https://msdn.microsoft.com/library/8z34s9c6(VS.80).aspx).

Bei der Verwendung von ausgerichteten directxmath-Typen mit der Standard Vorlagen Bibliothek (Standard Template Library, STL) müssen Sie eine benutzerdefinierte Zuweisung bereitstellen, die die 16-Byte-Ausrichtung sicherstellt. Im Visual C++ [Teamblog](https://devblogs.microsoft.com/cppblog/the-mallocator/) finden Sie ein Beispiel für das Schreiben eines benutzerdefinierten zuordcators (anstelle von "malloc" oder "Free" sollten Sie \_ ausgerichtete \_ malloc verwenden und \_ \_ in ihrer Implementierung kostenlos ausrichten).

> [!Note]  
> Einige STL-Vorlagen ändern die Ausrichtung des bereitgestellten Typs. Nehmen Sie beispielsweise an, dass frei [ \_ gegebene<>](/cpp/standard-library/memory-functions?view=vs-2017&preserve-view=true) einige interne Verfolgungs Informationen hinzufügt, die die Ausrichtung des bereitgestellten Benutzer Typs berücksichtigen oder nicht, was zu nicht ausgerichteten Datenmembern führt. In diesem Fall müssen Sie nicht ausgerichtete Typen anstelle von ausgerichteten Typen verwenden. Wenn Sie von vorhandenen Klassen, einschließlich vielen Windows-Runtime Objekten, ableiten, können Sie auch die Ausrichtung einer Klasse oder Struktur ändern.

 

## <a name="avoid-operator-overloads-when-possible"></a>Vermeiden von Operator Überladungen, wenn möglich

Als praktische Funktion haben eine Anzahl von Typen wie [**xmvector**](xmvector-data-type.md) und [**xmmatrix**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) Operator Überladungen für gängige arithmetische Operationen. Diese Operator Überladungen erstellen tendenziell zahlreiche temporäre Objekte. Es wird empfohlen, diese Operator Überladungen in Leistungs sensiblem Code zu vermeiden.

## <a name="denormals"></a>Abbrüche

Um Berechnungen in der Nähe von 0 zu unterstützen, bietet der IEEE 754-float-Point-Standard Unterstützung für einen schrittweisen Unterlauf. Der schrittweise Unterlauf wird durch die Verwendung von denormalisierten Werten implementiert, und viele Hardware Implementierungen sind langsam, wenn denormals verarbeitet werden. Eine zu berücksichtigende Optimierung besteht darin, die Handhabung von denormals für die von directxmath verwendeten Vektor Vorgänge zu deaktivieren.

Das Ändern der Handhabung von denormals erfolgt mithilfe der [ \_ controlfp \_ s](/cpp/c-runtime-library/reference/controlfp-s) -Routine auf vorthreadbasis und kann zu Leistungsverbesserungen führen. Verwenden Sie diesen Code, um die Handhabung von denormals zu ändern:


```
  #include <float.h>;
    unsigned int control_word;
    _controlfp_s( &control_word, _DN_FLUSH, _MCW_DN );
```



> [!Note]  
> Auf 64-Bit-Versionen von Windows werden [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) -Anweisungen für alle Berechnungen verwendet, nicht nur für die Vektor Vorgänge. Das Ändern der denormalen Behandlung wirkt sich nicht nur auf die von directxmath verwendeten Vektor Vorgänge, sondern auf alle Gleit Komma Berechnungen in Ihrem Programm aus.

 

## <a name="take-advantage-of-the-integer-floating-point-duality"></a>Ausnutzen der ganzzahligen Gleit Komma Zahl

Directxmath unterstützt Vektoren mit einem Gleit Komma-oder 4 32-Bit-Wert (mit oder ohne Vorzeichen) mit einfacher Genauigkeit.

Da die Anweisungs Sätze, die zum Implementieren der directxmath-Bibliothek verwendet werden, die gleichen Daten wie mehrere verschiedene Typen behandeln können, um z. b. denselben Vektor wie Gleit Komma-und ganzzahlige Daten zu behandeln, können bestimmte Optimierungen erreicht werden. Sie können diese Optimierungen mit den ganzzahligen Vektor Initialisierungs Routinen und bitweisen Operatoren zum Bearbeiten von Gleit Komma Werten erhalten.

Das binäre Format von Gleit Komma Zahlen mit einfacher Genauigkeit, das von der directxmath-Bibliothek verwendet wird, entspricht vollständig dem IEEE 764-Standard:

``` syntax
     SIGN    EXPONENT   MANTISSA
     X       XXXXXXXX   XXXXXXXXXXXXXXXXXXXXXXX
     1 bit   8 bits     23 bits
```

Beim Arbeiten mit der IEEE 764-Gleit Komma Zahl mit einfacher Genauigkeit ist es wichtig zu beachten, dass einige Darstellungen eine besondere Bedeutung haben (d. h., Sie entsprechen nicht der vorangehenden Beschreibung). Beispiele:

-   Positive NULL ist 0
-   Minus 0 ist 0x80000000
-   Q \_ NaN ist 07fc0000
-   + Inf ist 0x7F 800000
-   -Inf ist 0xff800000

## <a name="prefer-template-forms"></a>Vorlagen Formulare bevorzugen

Das Vorlagen Formular ist für [**xmvector**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle), [**xmvector perstumm**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), [**xmvector INSERT**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert), [**xmvector shiftleft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft), [**xmvector rotateleft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft)und [**xmvector rotateright**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright)vorhanden. Wenn Sie diese anstelle des allgemeinen Funktions Formulars verwenden, kann der Compiler weitaus mehr effiziente Implementierungen erstellen. Für [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100))reduziert dies häufig einen oder zwei \_ mm-shuffle- \_ PS- \_ Werte. Bei Arm-Neon kann die **xmvector Swizzle** -Vorlage eine Reihe von besonderen Fällen anstelle des allgemeineren VTBL-escapesels/der allgemeineren Verwendung nutzen.

## <a name="using-directxmath-with-direct3d"></a>Verwenden von directxmath mit Direct3D

Directxmath wird häufig verwendet, um Grafik Berechnungen für die Verwendung mit Direct3D auszuführen. Mit Direct3D 10. x und Direct3D 11. x können Sie die directxmath-Bibliothek auf folgende Weise verwenden:

-   Verwenden Sie die Namespace [Konstanten](ovw-xnamath-reference-constants.md) Colors direkt im *colorrgba* -Parameter in einem Aufrufen der [**Verknüpfung id3d11devicecontext aus:: clearrendertargetview**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-clearrendertargetview) -Methode oder der [**ID3D10Device:: clearrendertargetview**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-clearrendertargetview) -Methode. Für Direct3D 9 müssen Sie in den [**xmcolor**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) -Typ konvertieren, um ihn als *Farb* Parameter in einem Aufrufen der [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) -Methode zu verwenden.
-   Verwenden Sie die Typen [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) / [**xmvector**](xmvector-data-type.md) und [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) / [**xmmatrix**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) zum Einrichten konstanter Puffer Strukturen für Verweise durch die Typen HLSL [**float4**](../direct3dhlsl/dx-graphics-hlsl-scalar.md) oder [**Matrix**](../direct3dhlsl/dx-graphics-hlsl-matrix.md)/float4x4.
    > [!Note]  
    > [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) / [**Xmmatrix**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) -Typen weisen das Zeilen Hauptformat auf. Wenn Sie daher den/ZPR-Compilerschalter (das Haupt Kompilierungs Kennzeichen der [**D3DCOMPILE \_ Pack- \_ \_ \_ Matrix**](../direct3dhlsl/d3dcompile-constants.md) ) verwenden oder das \_ Schlüssel schlüsselschlüsselwort weglassen, wenn Sie den Matrixtyp in HLSL deklarieren, müssen Sie die Matrix bei der Festlegung in den konstanten Puffer umlagern. [](../direct3dhlsl/dx-graphics-hlsl-appendix-keywords.md)

     

-   Mit Direct3D 10. x und Direct3D 11. x können Sie davon ausgehen, dass der von der Map-Methode (z. b. [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)) zurückgegebene Zeiger im **pData** -Member (d3d10 zugeordneter [**\_ \_ TEXTURE2D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture2d).**pData**, [**d3d10 \_ zugeordnet \_ TEXTURE3D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture3d).**pData** oder D3D11 zugeordnete unter [**\_ \_ geordnete Quelle**](/windows/win32/api/d3d11/ns-d3d11-d3d11_mapped_subresource).**pData**) ist eine 16-Byte-Ausrichtung, wenn Sie die [Featureebene](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 10 \_ 0 oder höher verwenden oder wenn Sie [**D3D11 \_ Usage \_**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) -stagingressourcen verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Directxmath-Programmier Handbuch](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
