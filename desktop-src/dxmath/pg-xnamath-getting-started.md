---
title: Erste Schritte (DirectXMath)
description: Die DirectXMath-Bibliothek implementiert eine optimale und portable Schnittstelle für arithmetische und lineare Algebraoperationen für Gleitkommavektoren mit einfacher Genauigkeit (2D, 3D und 4D) oder Matrizen (3×3 und 4×4).
ms.assetid: 9972e382-7a0f-88a7-ad44-18521af3520d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ad7de99a462dc533d8010c45dfadcb1bcfa1b6f33317a941e91c16f30c3d2c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117500"
---
# <a name="getting-started-directxmath"></a>Erste Schritte (DirectXMath)

Die DirectXMath-Bibliothek implementiert eine optimale und portable Schnittstelle für arithmetische und lineare Algebraoperationen für Gleitkommavektoren mit einfacher Genauigkeit (2D, 3D und 4D) oder Matrizen (3×3 und 4×4). Die Bibliothek bietet eingeschränkte Unterstützung für Ganzzahlvektorvorgänge. Diese Vorgänge werden umfassend beim Rendern und Beiimieren von Grafikprogrammen verwendet. Vektoren mit doppelter Genauigkeit (einschließlich Longs, Shorts oder Bytes) und nur eingeschränkte Ganzzahlvektorvorgänge werden nicht unterstützt.

Die Bibliothek ist auf einer Vielzahl von Windows-Plattformen verfügbar. Da die Bibliothek Funktionen bereitstellt, die zuvor nicht verfügbar waren, ersetzt diese Version die folgenden Bibliotheken:

-   Xbox Math-Bibliothek, die vom Xboxmath.h-Header bereitgestellt wird
-   Von den D3DX 9-DLLs bereitgestellte D3DX 9-Bibliothek
-   Mathematische D3DX 10-Bibliothek, die über die D3DX 10-DLLs bereitgestellt wird
-   Vom Header "xnamath.h" im DirectX SDK und Xbox 360 XDK bereitgestellte XNA-Mathebibliothek

In diesen Abschnitten werden die Grundlagen der ersten Schritte beschrieben.

-   [Herunterladen](#download)
-   [Systemanforderungen zur Laufzeit](#run-time-system-requirements)
-   [Übersicht über den Entwurf](#design-overview)
-   [Matrixkonvention](#matrix-convention)
-   [Grundlegende Verwendung](#basic-usage)
-   [Richtlinien für die Typverwendung](#type-usage-guidelines)
-   [Erstellen von Vektoren](#creating-vectors)
    -   [KONSTANTE VEKTOREN](#constant-vectors)
    -   [VEKTOREN AUS VARIABLEN](#vectors-from-variables)
    -   [VEKTOREN AUS VEKTOREN](#vectors-from-vectors)
    -   [VEKTOREN AUS DEM ARBEITSSPEICHER](#vectors-from-memory)
-   [Extrahieren von Komponenten aus Vektoren](#extracting-components-from-vectors)
-   [Zugehörige Themen](#related-topics)

## <a name="download"></a>Download

Die DirectXMath-Bibliothek ist im Windows SDK enthalten. Alternativ können Sie sie von [GitHub/Microsoft/DirectXMath](https://github.com/Microsoft/DirectXMath)herunterladen. Diese Website enthält auch verwandte Beispielprojekte.

## <a name="run-time-system-requirements"></a>Run-Time Systemanforderungen

Die DirectXMath-Bibliothek verwendet spezialisierte Prozessoranweisungen für Vektorvorgänge, wenn sie verfügbar sind. Um zu vermeiden, dass ein Programm Fehler aufgrund unbekannter Anweisungsausnahmen generiert, überprüfen Sie die Prozessorunterstützung, indem Sie [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport) aufrufen, bevor Sie die DirectXMath-Bibliothek verwenden.

Dies sind die grundlegenden Supportanforderungen für die DirectXMath-Bibliothek zur Laufzeit:

-   Die Standardkompilierung auf einer Windows-Plattform (x86/x64) erfordert SSE/SSE2-Anweisungsunterstützung.
-   Die Standardkomplikation auf einer Windows RT-Plattform erfordert ARM-NEON-Anweisungsunterstützung.
-   Für die Kompilierung mit [**\_ definierten XM \_ NO \_ INTRINSICS \_**](ovw-xnamath-reference-directives.md) ist nur eine Standardmäßigunterstützung für Gleitkomma-Vorgänge erforderlich.

> [!Note]  
> Wenn Sie [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport)aufrufen, schließen Sie <windows.h-> ein, bevor Sie <DirectXMath.h-> einschließen. Dies ist die einzige Funktion in der Bibliothek, die Inhalte von <windows.h-> erfordert, sodass Sie nicht <windows.h-> in jedes Modul einschließen müssen, das <DirectXMath.h-> verwendet.

 

## <a name="design-overview"></a>Entwurfsübersicht

Die DirectXMath-Bibliothek unterstützt in erster Linie die Programmiersprache C++. Die Bibliothek wird mithilfe von Inlineroutinen in den Headerdateien DirectXMath \* .inl, DirectXPackedVector.inl und DirectXCollision.inl implementiert. Diese Implementierung nutzt systeminterne Compilerfunktionen mit hoher Leistung.

Die DirectXMath-Bibliothek bietet Folgendes:

-   Eine Implementierung, die systeminterne SSE/SSE2-Funktionen verwendet.
-   Eine Implementierung ohne systeminterne Funktionen.
-   Eine Implementierung, die arm-NEON-Systeminterne Funktionen verwendet.

Da die Bibliothek mithilfe von Headerdateien bereitgestellt wird, verwenden Sie den Quellcode, um Ihre eigene App anzupassen und zu optimieren.

## <a name="matrix-convention"></a>Matrixkonvention

DirectXMath verwendet Zeilenmatrizen, Zeilenvektoren und Prämultiplikation. Die Handkraft wird durch die verwendete Funktionsversion bestimmt (RH im Vergleich zu LSV), andernfalls funktioniert die Funktion entweder mit linkshändigen oder rechtshändigen Ansichtskoordinaten.

Direct3D hat bisher linkshändiges Koordinatensystem, Zeilenmatrizen, Zeilenvektoren und Prämultiplikation verwendet. Modern Direct3D hat keine starke Anforderung für linke und rechtshändige Koordinaten, und in der Regel nutzen HLSL-Shader standardmäßig Spaltenhauptmatrizen. Weitere Informationen finden Sie unter [HLSL-Matrixreihenfolge.](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-per-component-math)

## <a name="basic-usage"></a>Grundlegende Verwendung

Um DirectXMath-Bibliotheksfunktionen zu verwenden, schließen Sie die Header DirectXMath.h, DirectXPackedVector.h, DirectXColors.h und/oder DirectXCollision.h ein. Die Header befinden sich im Windows Software Development Kit für Windows Store-Apps.

## <a name="type-usage-guidelines"></a>Richtlinien für die Typverwendung

Die Typen [**XMVECTOR**](xmvector-data-type.md) und [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) sind der Arbeitsaufwand für die DirectXMath-Bibliothek. Jeder Vorgang nutzt oder erzeugt Daten dieser Typen. Das Arbeiten mit ihnen ist der Schlüssel zur Verwendung der Bibliothek. Da DirectXMath jedoch die SIMD-Anweisungssätze verwendet, unterliegen diese Datentypen einer Reihe von Einschränkungen. Es ist wichtig, dass Sie diese Einschränkungen verstehen, wenn Sie die DirectXMath-Funktionen gut nutzen möchten.

Sie sollten sich [**XMVECTOR**](xmvector-data-type.md) als Proxy für ein SIMD-Hardwareregister und [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) als Proxy für eine logische Gruppierung von vier SIMD-Hardwareregistern vorstellen. Diese Typen werden mit Anmerkungen versehen, um anzugeben, dass sie eine 16-Byte-Ausrichtung erfordern, um ordnungsgemäß zu funktionieren. Der Compiler speichert sie automatisch ordnungsgemäß auf dem Stapel, wenn sie als lokale Variable verwendet werden, oder fügt sie in das Datensegment ein, wenn sie als globale Variable verwendet werden. Mit den richtigen Konventionen können sie auch sicher als Parameter an eine Funktion übergeben werden (weitere Informationen finden Sie unter [Aufrufkonventionen).](pg-xnamath-internals.md)

Zuordnungen aus dem Heap sind jedoch komplizierter. Daher müssen Sie vorsichtig sein, wenn Sie [**XMVECTOR**](xmvector-data-type.md) oder [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) als Member einer Klasse oder Struktur verwenden, die vom Heap zugeordnet werden soll. Auf Windows x64 werden alle Heapzuordnungen auf 16 Byte ausgerichtet, aber für Windows x86 sind sie nur 8 Byte ausgerichtet. Es gibt Optionen zum Zuordnen von Strukturen aus dem Heap mit 16-Byte-Ausrichtung (siehe [Ordnungsgemäßes Ausrichten von Zuordnungen).](pg-xnamath-optimizing.md) Für C++-Programme können Sie operator new/delete/new \[ \] \[ \] /delete-Überladungen (entweder global oder klassenspezifisch) verwenden, um bei Bedarf eine optimale Ausrichtung zu erzwingen.

> [!Note]  
> Als Alternative zum Erzwingen der Ausrichtung in Ihrer C++-Klasse direkt durch Überladen von new/delete können Sie das [pImpl-Idiom](https://en.wikipedia.org/wiki/Opaque_pointer)verwenden. Wenn Sie sicherstellen, dass Ihre **Impl-Klasse** intern über [**\_ eine ausgerichtete \_ malloc-Klasse**](/cpp/c-runtime-library/reference/aligned-malloc) ausgerichtet ist, können Sie in der internen Implementierung frei ausgerichtete Typen verwenden. Dies ist eine gute Option, wenn die Klasse "public" eine Windows Runtime-Verweisklasse ist oder für die Verwendung mit [**std::shared \_ ptr<>**](/cpp/standard-library/shared-ptr-class)vorgesehen ist, wodurch andernfalls die sorgfältige Ausrichtung unterbrochen werden kann.

 

Häufig ist es jedoch einfacher und kompakter, die Verwendung von [**XMVECTOR**](xmvector-data-type.md) oder [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) direkt in einer Klasse oder Struktur zu vermeiden. Verwenden Sie stattdessen [**XMFLOAT3,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) [**XMFLOAT4,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) [**XMFLOAT4X3,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)usw. als Member Ihrer -Struktur. Darüber hinaus können Sie die Funktionen [Vector Loading](ovw-xnamath-reference-functions-load.md) und [Vector Storage](ovw-xnamath-reference-functions-storage.md) verwenden, um die Daten effizient in lokale **XMVECTOR-** oder **XMMATRIX-Variablen** zu verschieben, Berechnungen durchzuführen und die Ergebnisse zu speichern. Es gibt auch Streamingfunktionen [**(XMVector3TransformStream,**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream) [**XMVector4TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transformstream)usw.), die effizient direkt mit Arrays dieser Datentypen arbeiten.

## <a name="creating-vectors"></a>Erstellen von Vektoren

### <a name="constant-vectors"></a>KONSTANTE VEKTOREN

Viele Vorgänge erfordern die Verwendung von Konstanten in Vektorberechnungen, und es gibt eine Reihe von Möglichkeiten, einen [**XMVECTOR**](xmvector-data-type.md) mit den gewünschten Werten zu laden.

-   Wenn Sie eine Skalarkonstante in alle Elemente eines [**XMVECTOR**](xmvector-data-type.md)laden, verwenden Sie [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) oder [**XMVectorReplicateInt.**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint)
    ```
    XMVECTOR vFive = XMVectorReplicate( 5.f );
    ```

    

-   Wenn Sie eine Vektorkonstante mit unterschiedlichen festen Werten als [**XMVECTOR**](xmvector-data-type.md)verwenden, verwenden Sie die [**XMVECTORF32-,**](xmvectorf32-data-type.md) [**XMVECTORU32-,**](xmvectoru32-data-type.md) **XMVECTORI32-** oder [**XMVECTORU8-Strukturen.**](xmvectoru8-data-type.md) Auf diese kann dann direkt überall verwiesen werden, wo Sie einen **XMVECTOR-Wert** übergeben würden.
    ```
    static const XMVECTORF32 vFactors = { 1.0f, 2.0f, 3.0f, 4.0f };
    ```

    

    > [!Note]  
    > Verwenden Sie Initialisiererlisten nicht direkt mit [**XMVECTOR**](xmvector-data-type.md) (d.h. XMVECTOR v = { 1.0f, 2.0f, 3.0f, 4.0f }). Dieser Code ist ineffizient und nicht auf allen Plattformen portierbar, die von DirectXMath unterstützt werden.

     

-   DirectXMath enthält eine Reihe vordefinierter globaler Konstanten, die Sie in Ihrem Code verwenden können (g \_ XMOne, g \_ XMOne3, g \_ XMTwo, g \_ XMOneHalf, g \_ XMHalfPi, g \_ XMPi usw.). Suchen Sie den Header DirectXMath.h nach den **XMGLOBALCONSTANT-Werten.**
-   Es gibt eine Reihe von Vektorkonstanten für allgemeine RGB-Farben (Rot, Grün, Blau, Gelb usw.). Weitere Informationen zu diesen Vektorkonstanten finden Sie unter DirectXColors.h und der DirectX::Colors-Namespace.

### <a name="vectors-from-variables"></a>VEKTOREN AUS VARIABLEN

-   Wenn Sie einen Vektor aus einer einzelnen skalaren Variablen erstellen, finden Sie weitere Informationen unter [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) und [**XMVectorReplicateInt.**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint)
    ```
    XMVECTOR v = XMVectorReplicate( f  );
    ```

    

-   Wenn Sie einen Vektor aus vier skalaren Variablen erstellen, finden Sie weitere Informationen unter [**XMVectorSet**](/windows/win32/api/directxmath/nf-directxmath-xmvectorset) und [**XMVectorSetInt.**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetint)
    ```
    XMVECTOR v = XMVectorSet( fx, fy, fz, fw );
    ```

    

### <a name="vectors-from-vectors"></a>VEKTOREN AUS VEKTOREN

-   Wenn Sie einen Vektor aus einem anderen Vektor erstellen, bei dem eine bestimmte Komponente auf eine Variable festgelegt ist, können Sie die Verwendung von [Vector Accessor Functions](ovw-xnamath-reference-functions-accessors.md)in Betracht ziehen.
    ```
    XMVECTOR v2 = XMVectorSetW( v1, fw );
    ```

    

-   Wenn Sie einen Vektor aus einem anderen Vektor mit einer einzelnen replizierten Komponente erstellen, verwenden Sie [**XMVectorSplatX,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatx) [**XMVectorSplatY,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplaty) [**XMVectorSplatZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatz)und [**XMVectorSplatW**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatw).
    ```
    XMVECTOR vz = XMVectorSplatZ( v );
    ```

    

-   Wenn Sie einen Vektor aus einem anderen Vektor oder Vektorpaar mit neu angeordneten Komponenten erstellen, finden Sie weitere Informationen unter [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) und [**XMVectorPermute.**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)
    ```
    XMVECTOR v2 = XMVectorSwizzle<XM_SWIZZLE_Z, XM_SWIZZLE_Y, XM_SWIZZLE_W, XM_SWIZZLE_X>( v1 );

    XMVECTOR v3 = XMVectorPermute<XM_PERMUTE_0W, XM_PERMUTE_1X, XM_PERMUTE_0X, XM_PERMUTE_1Z>( v1, v2 );
    ```

    

### <a name="vectors-from-memory"></a>VEKTOREN AUS DEM ARBEITSSPEICHER

-   Informationen zum Laden eines einzelnen float-Werts aus dem Arbeitsspeicher finden Sie unter [**XMVectorReplicatePtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateptr), [**XMVectorReplicateIntPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateintptr), [**XMLoadFloat**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat)und [**XMLoadInt**](/windows/win32/api/directxmath/nf-directxmath-xmloadint).
-   Gängige Methoden zum Laden von float-Arrays [**sind: XMLoadFloat2**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat2), [**XMLoadFloat3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3), [**XMLoadFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4), [**XMLoadFloat3x3,**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3x3) [**XMLoadFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x3)und [**XMLoadFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x4).
-   DirectXMath enthält eine umfangreiche Reihe von Typen und zugehörigen Lasten und Speichern für die Verarbeitung verschiedener Datenstrukturen und gängiger GPU-Formate. Weitere Informationen [finden Sie unter Vector Load](ovw-xnamath-reference-functions-load.md) und Vector [Store](ovw-xnamath-reference-functions-storage.md).

## <a name="extracting-components-from-vectors"></a>Extrahieren von Komponenten aus Vektoren

Die SIMD-Verarbeitung ist am effizientesten, wenn Daten in die SIMD-Register geladen und vor dem Extrahieren der Ergebnisse vollständig verarbeitet werden. Die Konvertierung zwischen Skalar- und Vektorformen ist ineffizient, daher wird empfohlen, dies nur bei Bedarf zu tun. Aus diesem Grund werden Funktionen in der DirectXMath-Bibliothek, die einen Skalarwert erzeugen, in einer Vektorform zurückgegeben, in der das Skalarergebnis über den resultierenden Vektor repliziert wird (d. h. [**XMVector2Dot,**](/windows/win32/api/directxmath/nf-directxmath-xmvector2dot) [**XMVector3Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector3length)und so weiter). Wenn Sie jedoch Skalarwerte benötigen, finden Sie hier einige Möglichkeiten:

-   Wenn eine einzelne Skalarantwort berechnet wird, ist die Verwendung der [Vektorzugriffsfunktionen](ovw-xnamath-reference-functions-accessors.md) geeignet:
    ```
    float f = XMVectorGetX( v );
    ```

    

-   Wenn mehrere Komponenten des Vektors extrahiert werden müssen, sollten Sie den Vektor in einer Speicherstruktur speichern und zurücklesen. Beispiel:
    ```
    XMFLOAT4A t;
    XMStoreFloat4A( &t, v );
    // t.x, t.y, t.z, and t.w can be individually accessed now
    ```

    

-   Die effizienteste Form der Vektorverarbeitung ist die Verwendung des Speicher-zu-Arbeitsspeicher-Streamings, bei dem die Eingabedaten aus dem Arbeitsspeicher geladen [(mithilfe](ovw-xnamath-reference-functions-load.md)von Vektorladefunktionen), vollständig in SIMD-Form verarbeitet und dann in den Arbeitsspeicher geschrieben werden (mit [Vector Store Functions).](ovw-xnamath-reference-functions-storage.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectXMath-Programmierhandbuch](ovw-xnamath-progguide.md)
</dt> </dl>

 

 