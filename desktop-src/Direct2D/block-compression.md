---
title: Blockkomprimierung
description: Beschreibt, wie die Block Komprimierung funktioniert und wie Sie in WIC und Direct2D verwendet wird.
ms.assetid: 52AF86A5-16E8-4AC8-BB67-CC2F1A3635B5
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: aeb6ba9427a04f7a251a1d59062be508e4249b41
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104530410"
---
# <a name="block-compression"></a>Blockkomprimierung

Beginnend mit Windows 8.1 unterstützt Direct2D mehrere Block komprimierte Pixel Formate. Außerdem enthält Windows 8.1 einen neuen Windows Imaging Component (WIC) DDS-Codec, um das Laden und Speichern von komprimierten Images im DDS-Dateiformat zu ermöglichen. Die Block Komprimierung ist eine Technik, mit der der Umfang des Grafik Speichers reduziert wird, der von Bitmapinhalten genutzt wird. Wenn Sie die Block Komprimierung verwenden, kann Ihre APP Arbeitsspeicher Nutzung und Ladezeiten für die gleichen Auflösungs Images verringern. Oder Ihre APP kann mehr oder höhere Auflösungs Images verwenden, während gleichzeitig der gleiche GPU-Speicherbedarf beansprucht wird.

Die Block Komprimierung wurde von Direct3D-Anwendungen lange Zeit verwendet, und mit Windows 8.1 ist auch für gängige und Direct2D-Anwendungsentwickler verfügbar.

In diesem Thema wird beschrieben, wie die Block Komprimierung funktioniert und wie Sie in WIC und Direct2D verwendet wird.

## <a name="about-block-compression"></a>Informationen zur Block Komprimierung

[Block Komprimierung](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression) (BC) bezieht sich auf eine Klasse von Komprimierungs Techniken zum Reduzieren von Textur Größen. Direct3D 11 unterstützt abhängig von der Funktionsebene bis zu 7 verschiedene BC-Formate. In Windows 8.1 Direct2D wird die Unterstützung für die Formate BC1, BC2 und BC3 eingeführt, die auf allen Funktionsebenen verfügbar sind.

### <a name="how-block-compression-works"></a>Funktionsweise der Block Komprimierung

In den komprimierten Block Formaten wird die gleiche grundlegende Technik verwendet, um den von Farbdaten genutzten Speicherplatz zu reduzieren. In diesem Abschnitt wird der einfachste Algorithmus, BC1, zusammengefasst. Eine ausführlichere Erläuterung finden Sie unter [Block Komprimierung](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11).

Zuerst ist das Bild in Blöcke von 4 x 4 Pixel unterteilt. Jeder Block wird separat komprimiert.

> [!Note]  
> Dies bedeutet, dass die Breite und Höhe eines Bilds jeweils ein Vielfaches von 4 Pixeln sein muss, damit es blockiert werden kann.

 

Diese Beispiel Abbildung zeigt einen 4 x 4-Pixel Block innerhalb eines Bilds.

![ein Beispiel Bild zeigt einen 4 x 4-Pixel Block innerhalb eines Bilds.](images/dds1.png)

Anschließend werden in einem 4-bis 4-Block zwei "Reference"-Farben ausgewählt und als 2 16-Bit-Werte codiert (5 Bits rot, 6 Bits grün, 5 Bits blau). Die Auswahl dieser Farben wirkt sich erheblich auf die Bildqualität aus und ist nicht trivial. Zwei zwischen Farben werden durch linfrühe Interpolation zwischen den beiden Verweis Farben im RGB-Farbraum berechnet. Dies ergibt insgesamt vier verschiedene mögliche Farben. jeder Farbe wird ein zwei-Bit-Indexwert zugewiesen. Beachten Sie jedoch, dass nur die beiden Endpunkt Farben gespeichert werden müssen, wenn die Interpolations Zeit korrigiert ist.

In dieser Abbildung werden die Farben 0 und 3 als "Verweis Farben" für den Block ausgewählt, während die Farben 1 und 2 mithilfe von linearer Interpolationen berechnet werden.

![Diagramm, das die Berechnung von 4 Farbwerten anzeigt, die den Block darstellen.](images/dds2.png)

Schließlich wird jedes Pixel im Block einer der vier zuvor berechneten Farben zugeordnet, und jedes Pixel wird mit dem zwei-Bit-Indexwert codiert.

Die Gesamtmenge der Daten, die zur Darstellung dieser 16 Pixel verwendet werden, ist:

`16 bits [to define a reference color] * 2 + 2 bits * 16 [number of pixels]  = 64 bits`

Dies ergibt eine durchschnittliche Dichte von 4 Bits pro Pixel. Im Vergleich dazu verbraucht das Common DXGI- \_ Format \_ B8G8R8A8 \_ unorm Pixel Format 32 Bits pro Pixel.

Dieses Diagramm zeigt, dass jedes Pixel als 2-Bit-Index codiert ist. Der gesamte-Block wird in 64 Bits codiert.

![Berechnen von 4 Farbwerten, die den Block darstellen.](images/dds3.png)

Es gibt Variationen zur Unterstützung von Alpha Daten und unterschiedlicher Anzahl von Farbkanälen. BC6H und bzw bc7 verwenden deutlich unterschiedliche Algorithmen, um den Inhalt von hohem dynamischen Bereich (HDR) zu unterstützen und die Bildqualität zu erhöhen.

### <a name="directdraw-surface-dds-file-format"></a>DirectDraw Surface (DDS)-Dateiformat

Block komprimierte Daten werden in der Regel in [DDS-Dateien (DirectDraw Surface)](/windows/desktop/direct3ddds/dx-graphics-dds-reference) gespeichert. Wenn Sie ein Direct3D-Entwickler sind, sind Sie möglicherweise mit DDS-Dateien vertraut. Beachten Sie, dass Direct2D nur bestimmte DDS-Features unterstützt. Weitere Informationen finden Sie unter [DDS Requirements](#dds-requirements).

### <a name="advantages-of-block-compression"></a>Vorteile der Block Komprimierung

Block komprimierte Formate unterscheiden sich von allgemeinen Komprimierungs Formaten für Industrie Images, wie z. b Dies bedeutet, dass Sie ein komprimiertes Block-Bild direkt ohne Decodierung oder Dekomprimierung auf die GPU laden können. Die BC-Formate verbrauchen im Durchschnitt zwischen 4 und 8 Bits pro Pixel. im Vergleich zu einer typischen unkomprimierten BGRA-Bitmap mit 32 Bit pro Pixel führt dies zu einer Speicherersparnis von 75% bis 87,5%. Da es keinen Decodierungs Schritt gibt, wird die Zeit zum Laden eines BC-Bilds im Vergleich zu Formaten wie JPEG erheblich reduziert.

### <a name="when-to-use-block-compression"></a>Verwendungszwecke der Block Komprimierung

Sie sollten die Verwendung von Block komprimierten Images in der APP anstelle anderer Formate (z. b. JPEG) in Erwägung gezogen, wenn Sie die Arbeitsspeicher Nutzung von Bitmaps reduzieren oder die Decodierungs-und Ladezeiten reduzieren möchten.

Die Block Komprimierung ist jedoch nicht für alle Fälle geeignet und erfordert Kompromisse. Zunächst sind die Block Komprimierungs Algorithmen verlustfrei. Die Block Komprimierung funktioniert gut mit natürlichen Foto Inhalten, kann jedoch unerwünschte visuelle Elemente in Bilder mit scharfen Grenzen mit hohem Kontrast, wie z. b. computergenerierte Screenshots, einbringen. Stellen Sie sicher, dass die von einem Block komprimierten Image Ressourcen eine akzeptable Bildqualität aufweisen, bevor Sie Sie verwenden.

Zweitens verbrauchen komprimierte DDS-Dateien im Allgemeinen mehr Speicherplatz auf dem Datenträger als vergleichbare JPEG-Images. Dies wiederum erhöht die Paketgröße und die Anforderungen an die Netzwerkbandbreite Ihrer APP.

## <a name="using-block-compression"></a>Verwenden von Block Komprimierung

In diesem Abschnitt wird erläutert, wie Block komprimierte Assets in einer Direct2D-App generiert und verwendet werden.

### <a name="overview"></a>Übersicht

Block komprimierte DDS-Dateien sind ein Lauf Zeitoptimiertes Format, was bedeutet, dass Sie bei der APP-Laufzeit speziell für eine gute Leistung optimiert werden. Es wird empfohlen, dass Sie weiterhin Ihre vorhandene Pipeline zum Erstellen und Bearbeiten von Medienobjekten verwenden und nur in ein komprimiertes Block Format konvertieren, wenn Sie Sie in das Anwendungsprojekt importieren, oder während der Buildzeit.

### <a name="dds-requirements"></a>DDS-Anforderungen

Das DDS-Dateiformat wurde entwickelt, um eine breite Palette von Features zu unterstützen, die in Direct3D verwendet werden. Direct2D verwendet nur eine Teilmenge dieser Features. Wenn Sie also DDS-Images für die Verwendung mit Direct2D erstellen, müssen Sie die folgenden Einschränkungen beachten:

-   Nur die folgenden [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Werte sind zulässig:
    -   DXGI- \_ Format \_ BC1 \_ unorm
    -   DXGI- \_ Format \_ BC2 \_ unorm
    -   DXGI- \_ Format \_ BC3 \_ unorm
-   Es müssen prämultiplizierte Alpha Daten verwendet werden. Dies schließt Legacy-DDS-Dateien mit Formaten ein, die explizit ein prämultipliziertes Alpha (DXT1, DXT2, DXT4) definieren, sowie DDS-Dateien, die die DDS \_ -Header- \_ Struktur "DX10" mit dem DDS \_ \_ -Alpha Modus " \_ \_ \_ \_ .
-   Die X-und Y-Dimensionen müssen ein Vielfaches von 4 Pixel sein.
-   Volumetexturen, Cubemaps, Mipmaps oder Textur Arrays sind nicht zulässig. Sie sollten nur einzelne Frame-Quell Images verwenden.

### <a name="generating-block-compressed-assets"></a>Block komprimierte Assets werden erzeugt.

Es gibt eine Vielzahl von DDS-Erstellungs Tools, die zum Erstellen oder Konvertieren von komprimierten DDS-Block Dateien verfügbar sind. Beachten Sie, dass nicht alle Tools die Anforderungen für die Verwendung von DDS-Dateien mit Direct2D unterstützen, wie im vorherigen Abschnitt beschrieben.

Ab Visual Studio 2013 können Sie Visual Studio vorhandene visuelle Objekte wie JPEG und PNG in das korrekte komprimierte DDS-Block Format als automatischen Teil des Buildprozesses konvertieren. Dies erfolgt mithilfe des benutzerdefinierten Buildschritts "Bildinhalts Aufgabe".

Informationen dazu, wie Sie dies für Ihr Projekt einrichten, finden Sie unter Gewusst [wie: Exportieren einer Textur für die Verwendung mit Direct2D-oder Javascipt-apps](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120)).

### <a name="direct2d-apis"></a>Direct2D-APIs

Direct2D wird in Windows 8.1 aktualisiert, um die folgenden Pixel Formate zu unterstützen:

-   DXGI- \_ Format \_ BC1 \_ unorm
-   DXGI- \_ Format \_ BC2 \_ unorm
-   DXGI- \_ Format \_ BC3 \_ unorm

In den vorangehenden Formaten müssen Sie ein prämultipliziertes Alpha verwenden. Außerdem sind diese Formate nur für die Verwendung als Quelle, nicht als Ziel zulässig. Dies bedeutet beispielsweise, dass Sie eine Direct2D-Bitmap mit BC1 erstellen können, jedoch keinen Gerätekontext.

Die folgenden Methoden werden in Windows 8.1 aktualisiert, um die BC-Formate zu unterstützen:

-   [**ID2D1DeviceContext:: isdxgiformatsupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported)
-   [**ID2D1DeviceContext:: kreatebitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1DeviceContext:: kreatebitmapfromdxgisurface**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1RenderTarget:: kreatesharedbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)
-   [**ID2D1RenderTarget:: kreatebitmapfromwicbitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)
-   [**ID2D1Bitmap:: copyfrommemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)
-   [**ID2D1Bitmap:: copyfrombitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**ID2D1Bitmap1:: getSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-getsurface)

Beachten Sie [**, dass die**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md) " [**IWICBitmapSource"-Schnittstelle "IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) " in "" als Schnittstelle in Windows 8.1 WIC jedoch keine Unterstützung für das Abrufen von Block komprimierten Daten aus **IWICBitmapSource**, und es gibt kein WIC-Pixel Format, das dem DXGI- \_ Format \_ BC1 \_ unorm usw. entspricht. Stattdessen bestimmt " **kreatebitmapfromwicbitmap** ", ob **IWICBitmapSource** ein gültiger DDS [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) ist und die komprimierten Daten direkt lädt. Sie können das Pixel Format entweder explizit in der [**D2D1 \_ Bitmap \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) -Struktur angeben oder zulassen, dass Direct2D automatisch das richtige Format bestimmt.

### <a name="windows-imaging-component-apis"></a>Windows Imaging-Komponenten-APIs

Die Windows Imaging Component (WIC) fügt in Windows 8.1 einen neuen DDS-Codec hinzu. Außerdem werden neue Schnittstellen hinzugefügt, die den Zugriff auf DDS-spezifische Daten unterstützen, einschließlich Block komprimierter Pixeldaten:

-   [**Iwicddsdecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsdecoder)
-   [**Iwicddsencoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsencoder)
-   [**Iwicddsframedecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="block-compressed-wic-pixel-formats"></a>Komprimierte WIC-Pixel Formate blockieren

In Windows 8.1 sind keine neuen, in einem WIC-Block komprimierten Pixel Formate vorhanden. Wenn Sie stattdessen eine [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) -Schnittstelle aus dem DDS-Decoder abrufen und [**CopyPixels**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels)aufzurufen, erhalten Sie standardmäßige unkomprimierte Pixel, wie z. b. WICPixelFormat32bppPBGRA. Sie können [**iwicddsframedecode:: copyblocks**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsframedecode-copyblocks) verwenden, um die komprimierten Blockdaten in Form eines Speicherpuffers aus einer DDS-Datei abzurufen.

### <a name="multi-frame-dds-access"></a>DDS-Zugriff (Multi-Frame)

Das DDS-Dateiformat ermöglicht, dass mehrere verwandte Images in einer einzigen Datei gespeichert werden. Eine DDS-Datei kann z. b. eine cubemap, eine Volumestruktur oder ein Textur Array enthalten, die alle mipzugeordnet werden können. In Direct3D werden diese mehrere Bilder als unter Ressourcen verfügbar gemacht. In WIC werden mehrere Bilder als Frames ([**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) und [**IWICBitmapFrameEncode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode)) verfügbar gemacht.

WIC unterstützt nur das Konzept eines eindimensionalen Arrays von Frames, während DDS drei unabhängige Dimensionen unterstützt (obwohl nur zwei in einer Datei verwendet werden können). WIC bietet Hilfsmethoden zur Unterstützung der Zuordnung zwischen einer DDS-unter Quelle und WIC-Frame. Beim Decodieren können Sie mit [**iwicddsdecoder:: GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsdecoder-getframe) den Array Index, die MIP-Ebene und den Slice-Index der unter Berichte angeben und den korrekten WIC-Frame zurückgeben.

Bei der Codierung berechnet [**iwicddsencoder:: featenewframe**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-createnewframe) den resultierenden Array Index, die MIP-Ebene und den Slice-Index, wenn Sie einen neuen Frame erstellen. Sie müssen zuerst [**iwicddsencoder:: SetParameters**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-setparameters) aufgerufen haben, um die DDS-spezifischen Datei Parameter zu definieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gewusst wie: Exportieren einer Textur für die Verwendung mit Direct2D- oder Javascript-Apps](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120))
</dt> <dt>

[Verweis für DDS](/windows/desktop/direct3ddds/dx-graphics-dds-reference)
</dt> <dt>

[Block Komprimierung](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> </dl>

 

 