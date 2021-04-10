---
title: Getting Started (directxmath)
description: Die directxmath-Bibliothek implementiert eine optimale und portabel-Schnittstelle für arithmetische und lineare Algebra-Vorgänge für Gleit Komma Vektoren mit einfacher Genauigkeit (2D, 3D und 4D) oder Matrizen (3 × 3 und 4 × 4).
ms.assetid: 9972e382-7a0f-88a7-ad44-18521af3520d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e599acfc498e28b33acfc5bbbba2bea5669d2a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351019"
---
# <a name="getting-started-directxmath"></a>Getting Started (directxmath)

Die directxmath-Bibliothek implementiert eine optimale und portabel-Schnittstelle für arithmetische und lineare Algebra-Vorgänge für Gleit Komma Vektoren mit einfacher Genauigkeit (2D, 3D und 4D) oder Matrizen (3 × 3 und 4 × 4). Die Bibliothek verfügt über eine begrenzte Unterstützung für ganzzahlige Vektor Vorgänge. Diese Vorgänge werden ausgiebig beim Rendering und bei der Animation durch Grafikprogramme verwendet. Es gibt keine Unterstützung für Vektoren mit doppelter Genauigkeit (einschließlich Longs, Shorts oder Bytes) und nur eingeschränkte ganzzahlige Vektor Vorgänge.

Die Bibliothek ist auf einer Vielzahl von Windows-Plattformen verfügbar. Da die Bibliothek Funktionen bereitstellt, die bisher nicht verfügbar waren, ersetzt diese Version die folgenden Bibliotheken:

-   Von der xboxmath. h-Kopfzeile bereitgestellte Xbox Math-Bibliothek
-   D3DX 9-Bibliothek von D3DX 9-DLLs bereitgestellt
-   D3DX 10 Math Library über die D3DX 10-DLLs bereitgestellt
-   XNA-mathematische Bibliothek, bereitgestellt vom xnamath. h-Header im DirectX SDK und Xbox 360 XDK

In diesen Abschnitten werden die Grundlagen der ersten Schritte erläutert.

-   [Download](#download)
-   [System Anforderungen für die Laufzeit](#run-time-system-requirements)
-   [Entwurfs Übersicht](#design-overview)
-   [Matrix Konvention](#matrix-convention)
-   [Grundlegende Verwendung](#basic-usage)
-   [Typverwendungs Richtlinien](#type-usage-guidelines)
-   [Erstellen von Vektoren](#creating-vectors)
    -   [Konstante Vektoren](#constant-vectors)
    -   [Vektoren aus Variablen](#vectors-from-variables)
    -   [Vektoren von Vektoren](#vectors-from-vectors)
    -   [Vektoren aus dem Arbeitsspeicher](#vectors-from-memory)
-   [Extrahieren von Komponenten aus Vektoren](#extracting-components-from-vectors)
-   [Zugehörige Themen](#related-topics)

## <a name="download"></a>Herunterladen

Die directxmath-Bibliothek ist in der Windows SDK enthalten. Alternativ können Sie es von [GitHub/Microsoft/directxmath](https://github.com/Microsoft/DirectXMath)herunterladen. Diese Site enthält auch Verwandte Beispiel Projekte.

## <a name="run-time-system-requirements"></a>System Anforderungen Run-Time

Die directxmath-Bibliothek verwendet spezielle Prozessor Anweisungen für Vektor Vorgänge, wenn diese verfügbar sind. Um zu vermeiden, dass ein Programmfehler vom Typ "unbekannte Anweisungs Ausnahme" generiert, überprüfen Sie die Prozessorunterstützung durch Aufrufen von [**xmverifycpusupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport) vor der Verwendung der directxmath-Bibliothek.

Dies sind die grundlegenden Anforderungen an die Laufzeitunterstützung der directxmath-Bibliothek:

-   Die Standard Kompilierung auf einer Windows-Plattform (x86/x64) erfordert die Unterstützung von SSE/SSE2-Anweisungen.
-   Standardmäßige compliationen auf einer Windows RT-Plattform erfordern eine Arm-Neon-Anweisungs Unterstützung.
-   Die Kompilierung mit XM, für die [**\_ \_ keine \_ \_**](ovw-xnamath-reference-directives.md) systeminternen Funktionen definiert sind, erfordert nur standardmäßige Gleit Komma Operationen

> [!Note]  
> Wenn Sie [**xmverifycpusupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport)aufgerufen haben, schließen Sie <Windows. h-> ein, bevor Sie <directxmath. h-> einschließen. Dies ist die einzige Funktion in der Bibliothek, die Inhalte aus <Windows. h benötigt> damit Sie nicht <Windows. h-> in jedes Modul einschließen müssen, das <directxmath. h> verwendet.

 

## <a name="design-overview"></a>Entwurfsübersicht

Die directxmath-Bibliothek unterstützt hauptsächlich die Programmiersprache C++. Die Bibliothek wird mithilfe von Inline Routinen in den Header Dateien, directxmath \* . INL, directxpackedvector. INL und directxcollision. INL implementiert. Diese Implementierung nutzt hochleistungsfähige Compilerfunktionen.

Die directxmath-Bibliothek bietet Folgendes:

-   Eine-Implementierung mit systeminternen SSE/SSE2-Funktionen.
-   Eine-Implementierung ohne systeminterne Funktionen.
-   Eine-Implementierung, die systeminterne Arm-Neon-Funktionen verwendet.

Da die Bibliothek mithilfe von Header Dateien übermittelt wird, verwenden Sie den Quellcode, um Ihre eigene APP anzupassen und zu optimieren.

## <a name="matrix-convention"></a>Matrix Konvention

Directxmath verwendet Zeilen hauptmatrizen, Zeilen Vektoren und prämultiplikation. Die Fälligkeit wird durch die verwendete Funktions Version (RH und LH) bestimmt; andernfalls funktioniert die Funktion entweder mit Links oder rechts gerichteten Ansichts Koordinaten.

Für den Verweis hat Direct3D in der Vergangenheit ein Links hängendes Koordinatensystem, Zeilen hauptmatrizen, Zeilen Vektoren und die prämultiplikation verwendet. Modern Direct3D hat keine starke Anforderung für linke und rechts gerichtete Koordinaten, und in der Regel werden HLSL-Shader standardmäßig für die Verwendung von Spalten hauptmatrizen verwendet. Weitere Informationen finden Sie unter [HLSL-Matrix Reihen](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-per-component-math) Folge.

## <a name="basic-usage"></a>Grundlegende Verwendung

Um directxmath-Bibliotheksfunktionen zu verwenden, schließen Sie die Header "directxmath. h", "directxpackedvector. h", "directxcolors. h" und "directxcollision. h" ein. Die Header finden Sie im Windows Software Development Kit für Windows Store-Apps.

## <a name="type-usage-guidelines"></a>Typverwendungs Richtlinien

Die [**xmvector**](xmvector-data-type.md) -und [**xmmatrix**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) -Typen sind die Arbeitspferde für die directxmath-Bibliothek. Jeder Vorgang verwendet oder erzeugt Daten dieser Typen. Das Arbeiten mit Ihnen ist der Schlüssel für die Verwendung der Bibliothek. Da directxmath jedoch die SIMD-Anweisungs Sätze nutzt, unterliegen diese Datentypen einer Reihe von Einschränkungen. Es ist wichtig, dass Sie diese Einschränkungen verstehen, wenn Sie die directxmath-Funktionen optimal verwenden möchten.

Sie sollten sich [**xmvector**](xmvector-data-type.md) als Proxy für ein SIMD-Hardware Register vorstellen, und [**xmmatrix**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) als Proxy für eine logische Gruppierung von vier SIMD-Hardware Registern. Diese Typen werden mit Anmerkungen versehen, um anzugeben, dass die 16-Byte-Ausrichtung für die ordnungsgemäße Ausführung erforderlich ist. Der Compiler platziert Sie automatisch ordnungsgemäß auf dem Stapel, wenn Sie als lokale Variable verwendet werden, oder platziert Sie im Daten Segment, wenn Sie als globale Variable verwendet werden. Mit ordnungsgemäßen Konventionen können Sie auch sicher als Parameter an eine Funktion übermittelt werden (Weitere Informationen finden Sie unter [Aufrufen von Konventionen](pg-xnamath-internals.md) ).

Zuordnungen aus dem Heap sind jedoch komplizierter. Daher müssen Sie sorgfältig vorgehen, wenn Sie entweder [**xmvector**](xmvector-data-type.md) oder [**xmmatrix**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) als Member einer Klasse oder Struktur verwenden, die vom Heap zugewiesen werden soll. Unter Windows x64 sind alle Heap Zuordnungen auf 16-Byte ausgerichtet, aber für Windows x86 sind Sie nur 8-Byte-ausgerichtet. Es gibt Optionen zum Zuordnen von Strukturen aus dem Heap mit 16-Byte-Ausrichtung (siehe [ordnungsgemäßes ausrichten](pg-xnamath-optimizing.md)von Zuordnungen). Für C++-Programme können Sie den Operator new/delete/New \[ \] /Delete \[ \] über Ladungen (entweder global oder klassenspezifisch) verwenden, um bei Bedarf optimale Ausrichtung zu erzwingen.

> [!Note]  
> Als Alternative zum direkten erzwingen der Ausrichtung in der C++-Klasse durch Überladen von New/DELETE können Sie das [pimpl-Ausdrucks Wort](https://en.wikipedia.org/wiki/Opaque_pointer)verwenden. Wenn Sie sicherstellen, dass Ihre **impl** -Klasse intern über [**\_ ausgerichteten \_ malloc**](/cpp/c-runtime-library/reference/aligned-malloc) ausgerichtet ist, können Sie in der internen Implementierung die ausgerichteten Typen frei verwenden. Dies ist eine gute Option, wenn die "Public"-Klasse eine Windows-Runtime Verweis Klasse ist oder für die Verwendung mit [**Std:: Shared \_ ptr<>**](/cpp/standard-library/shared-ptr-class)vorgesehen ist, die eine sorgfältige Ausrichtung andernfalls unterbrechen kann.

 

Häufig ist es jedoch einfacher und kompakter, die Verwendung von [**xmvector**](xmvector-data-type.md) oder [**xmmatrix**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) direkt in einer Klasse oder Struktur zu vermeiden. Verwenden Sie stattdessen [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3), [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4), [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3), [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)usw. als Member ihrer Struktur. Außerdem können Sie die Funktionen [Vector Load](ovw-xnamath-reference-functions-load.md) und [Vector Storage](ovw-xnamath-reference-functions-storage.md) verwenden, um die Daten effizient in lokale **xmvector** -oder **xmmatrix** -Variablen zu verschieben, Berechnungen auszuführen und die Ergebnisse zu speichern. Es gibt auch Streamingfunktionen ([**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream), [**XMVector4TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transformstream)usw.), die effizient direkt mit Arrays dieser Datentypen arbeiten.

## <a name="creating-vectors"></a>Erstellen von Vektoren

### <a name="constant-vectors"></a>Konstante Vektoren

Viele Vorgänge erfordern die Verwendung von Konstanten in Vektor Berechnungen, und es gibt eine Reihe von Möglichkeiten, [**xmvector**](xmvector-data-type.md) mit den gewünschten Werten zu laden.

-   Verwenden Sie [**xmvector replizieren**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) oder [**xmvector repligeint**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint), wenn Sie eine skalare Konstante in alle Elemente eines [**xmvector-Vektors**](xmvector-data-type.md)laden.
    ```
    XMVECTOR vFive = XMVectorReplicate( 5.f );
    ```

    

-   Verwenden Sie die [**XMVECTORF32**](xmvectorf32-data-type.md)-, [**XMVECTORU32**](xmvectoru32-data-type.md)-, **XMVECTORI32**-oder [**XMVECTORU8**](xmvectoru8-data-type.md) -Strukturen, wenn Sie eine Vektor Konstante mit unterschiedlichen Fixed-Werten als [**xmvector**](xmvector-data-type.md)verwenden. Diese können dann direkt überall referenziert werden, wenn Sie einen **xmvector** -Wert übergeben würden.
    ```
    static const XMVECTORF32 vFactors = { 1.0f, 2.0f, 3.0f, 4.0f };
    ```

    

    > [!Note]  
    > Verwenden Sie keine Initialisiererlisten direkt mit [**xmvector**](xmvector-data-type.md) (d. h. xmvector v = {1.0 f, 2.0 f, 3.0 f, 4.0 f}). Ein solcher Code ist ineffizient und auf allen Plattformen, die von directxmath unterstützt werden, nicht portabel.

     

-   Directxmath enthält eine Reihe vordefinierter globaler Konstanten, die Sie in Ihrem Code verwenden können (g \_ xmone, g \_ XMOne3, g \_ xmtwo, g \_ xmonehalf, g \_ xmhalfpi, g \_ xmpi usw.). Durchsuchen Sie den directxmath. h-Header nach den **xmglobalconstant** -Werten.
-   Es gibt eine Reihe von Vektor Konstanten für gängige RGB-Farben (rot, grün, blau, gelb usw.). Weitere Informationen zu diesen Vektor Konstanten finden Sie unter directxcolors. h und im DirectX:: Colors-Namespace.

### <a name="vectors-from-variables"></a>Vektoren aus Variablen

-   Wenn Sie einen Vektor aus einer einzelnen skalaren Variablen erstellen, finden Sie unter [**xmvector replizieren**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) und [**xmvector repligeint**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint)Weitere Informationen.
    ```
    XMVECTOR v = XMVectorReplicate( f  );
    ```

    

-   Wenn Sie einen Vektor aus vier skalaren Variablen erstellen, finden Sie unter [**xmvector Set**](/windows/win32/api/directxmath/nf-directxmath-xmvectorset) und [**xmvector setInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetint)Weitere Informationen.
    ```
    XMVECTOR v = XMVectorSet( fx, fy, fz, fw );
    ```

    

### <a name="vectors-from-vectors"></a>Vektoren von Vektoren

-   Wenn Sie einen Vektor aus einem anderen Vektor mit einer bestimmten Komponente erstellen, die auf eine Variable festgelegt ist, können Sie die Verwendung von [Vektor Zugriffs](ovw-xnamath-reference-functions-accessors.md)Methoden in Erwägung gezogen.
    ```
    XMVECTOR v2 = XMVectorSetW( v1, fw );
    ```

    

-   Wenn Sie einen Vektor aus einem anderen Vektor mit einer einzelnen replizierten Komponente erstellen, verwenden Sie [**xmvector splatx**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatx), [**xmvector splaty**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplaty), [**xmvector**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatz)und [**xmvector splatw**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatw).
    ```
    XMVECTOR vz = XMVectorSplatZ( v );
    ```

    

-   Wenn Sie einen Vektor aus einem anderen Vektor oder einem Vektoren Paar mit neu bestellten Komponenten erstellen, finden Sie weitere Informationen unter [**xmvectorswizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) und [**xmvectorperstumm**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute).
    ```
    XMVECTOR v2 = XMVectorSwizzle<XM_SWIZZLE_Z, XM_SWIZZLE_Y, XM_SWIZZLE_W, XM_SWIZZLE_X>( v1 );

    XMVECTOR v3 = XMVectorPermute<XM_PERMUTE_0W, XM_PERMUTE_1X, XM_PERMUTE_0X, XM_PERMUTE_1Z>( v1, v2 );
    ```

    

### <a name="vectors-from-memory"></a>Vektoren aus dem Arbeitsspeicher

-   Informationen zum Laden eines einzelnen Float-Werts aus dem Arbeitsspeicher finden Sie unter [**xmvector repliereptr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateptr), [**xmvector repliereintptr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateintptr), [**xmloadfloat**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat)und [**xmloadint**](/windows/win32/api/directxmath/nf-directxmath-xmloadint).
-   Gängige Methoden zum Laden von float-Arrays sind: [**XMLoadFloat2**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat2), [**XMLoadFloat3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3), [**XMLoadFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4), [**XMLoadFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3x3), [**XMLoadFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x3)und [**XMLoadFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x4).
-   Directxmath umfasst einen umfangreichen Satz von Typen und zugehörige Lade-und Speichervorgänge, um verschiedene Datenstrukturen und gängige GPU-Formate zu verarbeiten. Siehe [Vector Load](ovw-xnamath-reference-functions-load.md) and [Vector Store](ovw-xnamath-reference-functions-storage.md).

## <a name="extracting-components-from-vectors"></a>Extrahieren von Komponenten aus Vektoren

Die SIMD-Verarbeitung ist am effizientesten, wenn Daten in die SIMD-Register geladen und vor dem Extrahieren der Ergebnisse vollständig verarbeitet werden. Die Konvertierung zwischen skalaren und Vektor Formularen ist ineffizient. Daher wird empfohlen, dass Sie Sie nur bei Bedarf verwenden. Aus diesem Grund werden Funktionen in der directxmath-Bibliothek, die einen skalaren Wert erstellen, in einer Vektor Form zurückgegeben, in der das skalare Ergebnis über den resultierenden Vektor repliziert wird (d. h. [**XMVector2Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector2dot), [**XMVector3Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector3length)usw.). Wenn Sie jedoch skalare Werte benötigen, finden Sie hier einige Optionen für die Vorgehensweise:

-   Wenn eine einzelne skalare Antwort berechnet wird, ist die Verwendung der [vektoraccessorfunktionen](ovw-xnamath-reference-functions-accessors.md) angemessen:
    ```
    float f = XMVectorGetX( v );
    ```

    

-   Wenn mehrere Komponenten des Vektors extrahiert werden müssen, sollten Sie den Vektor in einer Speicherstruktur speichern und wieder lesen. Beispiel:
    ```
    XMFLOAT4A t;
    XMStoreFloat4A( &t, v );
    // t.x, t.y, t.z, and t.w can be individually accessed now
    ```

    

-   Die effizienteste Form der Vektor Verarbeitung ist die Verwendung von Speicher-zu-Speicher-Streaming, bei dem die Eingabedaten aus dem Arbeitsspeicher geladen werden (mithilfe von [Vektor Ladefunktionen](ovw-xnamath-reference-functions-load.md)), vollständig in SIMD-Form verarbeitet und anschließend in den Arbeitsspeicher geschrieben werden (mithilfe von [Vektor Speicherfunktionen](ovw-xnamath-reference-functions-storage.md)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Directxmath-Programmier Handbuch](ovw-xnamath-progguide.md)
</dt> </dl>

 

 