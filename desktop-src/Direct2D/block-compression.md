---
title: Blockkomprimierung
description: Beschreibt die Funktionsweise der Blockkomprimierung und deren Verwendung in WIC und Direct2D.
ms.assetid: 52AF86A5-16E8-4AC8-BB67-CC2F1A3635B5
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e8ee83911cc7be1ab6e611a735a7a5b3a7397c472b78e3192468d2e323ed0c4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331745"
---
# <a name="block-compression"></a>Blockkomprimierung

Ab Windows 8.1 unterstützt Direct2D mehrere blockkomprimierte Pixelformate. Darüber hinaus enthält Windows 8.1 einen neuen WIC-DDS-Codec (Windows Imaging Component), um das Laden und Speichern von komprimierten Blockbildern im DDS-Dateiformat zu ermöglichen. Blockkomprimierung ist ein Verfahren zum Reduzieren des Grafikspeichers, der von Bitmapinhalten verbraucht wird. Mithilfe der Blockkomprimierung kann Ihre App den Arbeitsspeicherverbrauch und die Ladezeiten für die gleichen Auflösungsbilder reduzieren. Oder Ihre App kann Bilder mit mehr oder höherer Auflösung verwenden und gleichzeitig den gleichen GPU-Speicherbedarf nutzen.

Die Blockkomprimierung wird seit langem von Direct3D-Anwendungen verwendet, und mit Windows 8.1 ist auch für Entwickler von Mainstream- und Direct2D-Anwendungen verfügbar.

In diesem Thema wird beschrieben, wie die Blockkomprimierung funktioniert und wie sie in WIC und Direct2D verwendet wird.

## <a name="about-block-compression"></a>Informationen zur Blockkomprimierung

[Blockkomprimierung](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression) (BC) bezieht sich auf eine Klasse von Komprimierungstechniken zum Reduzieren von Texturgrößen. Direct3D 11 unterstützt je nach Featureebene bis zu 7 verschiedene BC-Formate. In Windows 8.1 Direct2D Unterstützung für die Formate BC1, BC2 und BC3 ein, die auf allen Featureebenen verfügbar sind.

### <a name="how-block-compression-works"></a>Funktionsweise der Blockkomprimierung

Die komprimierten Blockformate verwenden alle das gleiche grundlegende Verfahren, um den von Farbdaten verbrauchten Speicherplatz zu reduzieren. In diesem Abschnitt wird der einfachste Algorithmus BC1 zusammengefasst. Eine ausführlichere Erläuterung finden Sie unter [Blockkomprimierung](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11).

Zunächst wird das Bild in Blöcke von 4 x 4 Pixel unterteilt. Jeder Block wird separat komprimiert.

> [!Note]  
> Dies bedeutet, dass die Breite und Höhe eines Bilds jeweils ein Vielfaches von 4 Pixeln sein muss, damit es blockkomprimiert werden kann.

 

Dieses Beispielbild zeigt einen 4x4-Pixel-Block innerhalb eines Bilds.

![Ein Beispielbild zeigt einen 4x4-Pixel-Block innerhalb eines Bilds.](images/dds1.png)

Als Nächstes werden innerhalb eines 4 mal 4-Blocks zwei "Verweisfarben" ausgewählt und als zwei 16-Bit-Werte (5 Bits rot, 6 Bits grün, 5 Bits blau) codiert. Die Auswahl dieser Farben wirkt sich erheblich auf die Qualität des Bilds aus und ist nicht trivial. Zwei Zwischenfarben werden berechnet, indem zwischen den beiden Verweisfarben im RGB-Farbraum linear interpoliert wird. Dadurch werden insgesamt vier verschiedene mögliche Farben erzeugt. Jeder Farbe wird ein Zwei-Bit-Indexwert zugewiesen. Beachten Sie jedoch, dass nur die beiden Endpunktfarben gespeichert werden müssen, wenn die Interpolation korrigiert ist.

In dieser Abbildung werden die Farben 0 und 3 als "Verweisfarben" für den Block ausgewählt, während die Farben 1 und 2 mit linearer Interpolation berechnet werden.

![Diagramm, das die Berechnung von 4 Farbwerten zur Darstellung des Blocks zeigt.](images/dds2.png)

Schließlich wird jedes Pixel im -Block einer der vier zuvor berechneten Farben zugeordnet, und jedes Pixel wird mit dem Zwei-Bit-Indexwert codiert.

Die Gesamtmenge der Daten, die zur Darstellung dieser 16 Pixel verwendet werden, ist:

`16 bits [to define a reference color] * 2 + 2 bits * 16 [number of pixels]  = 64 bits`

Dies führt zu einer durchschnittlichen Dichte von 4 Bits pro Pixel. Zum Vergleich: Das allgemeine DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM-Pixelformat verbraucht 32 Bits pro Pixel.

Dieses Diagramm zeigt, dass jedes Pixel als 2-Bit-Index codiert ist. Der gesamte Block wird in 64 Bits codiert.

![Berechnen von 4 Farbwerten zur Darstellung des Blocks.](images/dds3.png)

Es gibt Variationen zur Unterstützung von Alphadaten und unterschiedlicher Anzahl von Farbkanälen. BC6H und BC7 verwenden deutlich unterschiedliche Algorithmen, um HDR-Inhalte (High Dynamic Range) zu unterstützen und die Qualität der Bilder zu erhöhen.

### <a name="directdraw-surface-dds-file-format"></a>DirectDraw Surface-Dateiformat (DDS)

Komprimierte Blockdaten werden in der Regel in [DirectDraw Surface-Dateien (DDS)](/windows/desktop/direct3ddds/dx-graphics-dds-reference) gespeichert. Als Direct3D-Entwickler sind Sie möglicherweise mit DDS-Dateien vertraut. Beachten Sie, dass Direct2D nur bestimmte DDS-Features unterstützt. Weitere Informationen finden Sie unter [DDS-Anforderungen.](#dds-requirements)

### <a name="advantages-of-block-compression"></a>Vorteile der Blockkomprimierung

Blockkomprimierungsformate unterscheiden sich von gängigen Branchenbildkomprimierungsformaten wie JPEG, da BC-Formate nativ von modernen GPUs unterstützt werden. Dies bedeutet, dass Sie ein komprimiertes Blockbild ohne Decodierung oder Dekomprimierung direkt auf die GPU laden können. BC-Formate verbrauchen durchschnittlich 4 bis 8 Bits pro Pixel; Im Vergleich zu einer typischen unkomprimierten BGRA-Bitmap mit 32 Bit pro Pixel führt dies zu Speichereinsparungen von 75 % bis 87,5 %. Da es keinen Decodierungsschritt gibt, wird die Zeit zum Laden eines BC-Bilds im Vergleich zu Formaten wie JPEG erheblich reduziert.

### <a name="when-to-use-block-compression"></a>Verwendung der Blockkomprimierung

Sie sollten die Verwendung von blockkomprimierten Bildern in Ihrer App anstelle anderer Formate wie JPEG in Betracht ziehen, wenn Sie den Arbeitsspeicherverbrauch von Bitmaps reduzieren oder die Decodierungs- und Ladezeiten reduzieren möchten.

Die Blockkomprimierung ist jedoch nicht für alle Fälle geeignet und erfordert einige Vor- und Abstellungen. Erstens sind die Algorithmen für die Blockkomprimierung verlustfrei. Die Blockkomprimierung funktioniert gut mit natürlichen Fotoinhalten, kann jedoch unerwünschte visuelle Artefakte in Bilder mit starken, hohen Kontrastgrenzen einführen, z. B. computergenerierte Screenshots. Sie sollten sicherstellen, dass Ihre blockkomprimierten Bildressourcen eine akzeptable Imagequalität haben, bevor Sie sie verwenden.

Zweitens verbrauchen blockkomprimierte DDS-Dateien im Allgemeinen mehr Speicherplatz auf dem Datenträger als vergleichbare JPEG-Bilder. Dies wiederum erhöht die Paketgröße und die Anforderungen an die Netzwerkbandbreite Ihrer App.

## <a name="using-block-compression"></a>Verwenden der Blockkomprimierung

In diesem Abschnitt wird erläutert, wie Sie komprimierte Blockressourcen in einer Direct2D-App generieren und verwenden.

### <a name="overview"></a>Übersicht

Komprimierte DDS-Dateien blockieren sind ein laufzeitoptimiertes Format, d. h., sie sind speziell für eine gute Leistung zur App-Runtime optimiert. Es wird empfohlen, ihre vorhandene Pipeline zum Erstellen und Bearbeiten von Ressourcen weiterhin zu verwenden und nur in ein blockkomprimiertes Format zu konvertieren, wenn Sie sie in Ihr Anwendungsprojekt oder zur Buildzeit importieren.

### <a name="dds-requirements"></a>DDS-Anforderungen

Das DDS-Dateiformat wurde entwickelt, um eine Vielzahl von Features zu unterstützen, die in Direct3D verwendet werden. Direct2D verwendet nur eine Teilmenge dieser Features. Wenn Sie DDS-Images für die Verwendung mit Direct2D erstellen, müssen Sie daher die folgenden Einschränkungen beachten:

-   Nur die folgenden [**DXGI \_ FORMAT-Werte**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) sind zulässig:
    -   DXGI \_ FORMAT \_ BC1 \_ UNORM
    -   DXGI \_ FORMAT \_ BC2 \_ UNORM
    -   \_DXGI-FORMAT \_ BC3 \_ UNORM
-   Prämultipliierte Alphadaten müssen verwendet werden. Dies schließt Legacy-DDS-Dateien mit Formaten ein, die prämultipliierte Alphas (DXT1, DXT2, DXT4) explizit definieren, sowie DDS-Dateien, die die DDS HEADER DX10-Struktur mit den \_ \_ DDS \_ ALPHA MODE \_ \_ OPAQUE- und DDS \_ ALPHA MODE \_ \_ PREMULTIPLIED-Werten verwenden.
-   Die Abmessungen X und Y müssen ein Vielfaches von 4 Pixeln sein.
-   Volumetexturen, Cubemaps, Mipmaps oder Texturarrays sind nicht zulässig. Sie sollten nur Einzelframe-Quellbilder verwenden.

### <a name="generating-block-compressed-assets"></a>Generieren von komprimierten Blockressourcen

Es gibt eine Vielzahl von DDS-Erstellungstools zum Erstellen oder Konvertieren von blockkomprimierten DDS-Dateien. Beachten Sie, dass nicht alle Tools die Anforderungen für die Verwendung von DDS-Dateien mit Direct2D unterstützen, wie im vorherigen Abschnitt beschrieben.

Ab Visual Studio 2013 können Sie vorhandene visuelle Visual Studio wie JPEG und PNG als automatischen Teil Ihres Buildprozesses in das richtige komprimierte DDS-Blockformat konvertieren. Dies erfolgt mithilfe des benutzerdefinierten Buildschritts für den Bildinhalts-Task.

Informationen dazu, wie Sie dies für Ihr Projekt einrichten, finden Sie unter: [How to: Export a Texture for Use with Direct2D or Javascipt Apps](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120))(How to: Exportieren einer Textur für die Verwendung mit Direct2D oder Javascipt Apps).

### <a name="direct2d-apis"></a>Direct2D-APIs

Direct2D wird in Windows 8.1 aktualisiert, um die folgenden Pixelformate zu unterstützen:

-   DXGI \_ FORMAT \_ BC1 \_ UNORM
-   DXGI \_ FORMAT \_ BC2 \_ UNORM
-   \_DXGI-FORMAT \_ BC3 \_ UNORM

Für die oben genannten Formate müssen Sie prämultipliierte Alphas verwenden. Darüber hinaus sind diese Formate nur für die Verwendung als Quelle und nicht als Ziel gültig. Dies bedeutet beispielsweise, dass Sie eine Direct2D-Bitmap mit BC1 erstellen können, aber keinen Gerätekontext.

Die folgenden Methoden werden in Windows 8.1 aktualisiert, um BC-Formate zu unterstützen:

-   [**ID2D1DeviceContext::IsDxgiFormatSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported)
-   [**ID2D1DeviceContext::CreateBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1))
-   [**ID2D1RenderTarget::CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)
-   [**ID2D1RenderTarget::CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md)
-   [**ID2D1Bitmap::CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)
-   [**ID2D1Bitmap::CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**ID2D1Bitmap1::GetSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-getsurface)

Beachten [**Sie, dass CreateBitmapFromWicBitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md) [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) als Schnittstelle verwendet. in Windows 8.1 WIC jedoch das Abrufen von blockkomprimierten Daten aus **IWICBitmapSource** nicht unterstützt, und es gibt kein WIC-Pixelformat, das DXGI \_ FORMAT \_ BC1 \_ UNORM usw. entspricht. Stattdessen bestimmt **CreateBitmapFromWicBitmap,** ob **IWICBitmapSource** ein gültiger DDS [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) ist, und lädt die komprimierten Blockdaten direkt. Sie können entweder explizit das Pixelformat in der [**D2D1 \_ BITMAP \_ PROPERTIES1-Struktur**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) angeben oder zulassen, dass Direct2D automatisch das richtige Format bestimmt.

### <a name="windows-imaging-component-apis"></a>Windows Imaging-Komponenten-APIs

Die Windows Imaging Component (WIC) fügt einen neuen DDS-Codec in Windows 8.1 hinzu. Darüber hinaus werden neue Schnittstellen hinzugefügt, die den Zugriff auf DDS-spezifische Daten unterstützen, einschließlich blockkomprimierten Pixeldaten:

-   [**IWICDdsDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsdecoder)
-   [**IWICDdsEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsencoder)
-   [**IWICDdsFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="block-compressed-wic-pixel-formats"></a>Block Compressed WIC pixel formats (Komprimierte WIC-Pixelformate blockieren)

Es gibt keine neuen Formate für komprimierte WIC-Blockpixel in Windows 8.1. Wenn Sie stattdessen einen [**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) aus dem DDS-Decoder abrufen und [**CopyPixels**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels)aufrufen, erhalten Sie unkomprimierte Standardpixel wie WICPixelFormat32bppPBGRA. Sie können [**IWICDdsFrameDecode::CopyBlocks**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsframedecode-copyblocks) verwenden, um die komprimierten Rohdaten des Blocks in Form eines Speicherpuffers aus einer DDS-Datei abzurufen.

### <a name="multi-frame-dds-access"></a>DDS-Zugriff mit mehreren Frames

Das DDS-Dateiformat ermöglicht das Speichern mehrerer verwandter Bilder in einer einzelnen Datei. Beispielsweise kann eine DDS-Datei eine Cubemap, eine Volumetextur oder ein Texturarray enthalten, die alle mipmapped sein können. In Direct3D werden diese mehreren Images als Unterressourcen verfügbar gemacht. In WIC werden mehrere Bilder als Frames verfügbar gemacht ([**IWICBitmapFrameDecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode) und [**IWICBitmapFrameEncode**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode)).

WIC unterstützt nur das Konzept eines eindimensionalen Arrays von Frames, während DDS drei unabhängige Dimensionen unterstützt (obwohl nur zwei in einer Datei verwendet werden können). WIC bietet Hilfsmethoden zur Unterstützung bei der Zuordnung zwischen einer DDS-Unterressource und einem WIC-Frame. Für die Decodierung können Sie mit [**IWICDdsDecoder::GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsdecoder-getframe) den Arrayindex, die Mipebene und den Sliceindex der Unterressource angeben und den richtigen WIC-Frame zurückgegeben.

Für die Codierung berechnet [**IWICDdsEncoder::CreateNewFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-createnewframe) den resultierenden Arrayindex, die MIP-Ebene und den Sliceindex, wenn Sie einen neuen Frame erstellen. Sie müssen zuerst [**IWICDdsEncoder::SetParameters**](/windows/desktop/api/wincodec/nf-wincodec-iwicddsencoder-setparameters) aufgerufen haben, um die DDS-spezifischen Dateiparameter zu definieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Gewusst wie: Exportieren einer Textur für die Verwendung mit Direct2D- oder Javascript-Apps](/previous-versions/visualstudio/visual-studio-2013/dn392693(v=vs.120))
</dt> <dt>

[Referenz für DDS](/windows/desktop/direct3ddds/dx-graphics-dds-reference)
</dt> <dt>

[Blockkomprimierung](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression)
</dt> </dl>

 

 