---
description: Windows-Bilderstellungskomponente (WIC) wurde mit neuen Versionen von Windows aktualisiert. Dieses Thema bietet eine kurze Einführung in diese neuen Features.
ms.assetid: 710B71CE-6FCC-46DA-A65C-6E4FC6A04275
title: Neues in WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 420d501dd495081764a7fba89f73d21077c04b05d92e7c2b47c3c2c2d51d7d10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204015"
---
# <a name="whats-new-in-wic"></a>Neues in WIC

Windows-Bilderstellungskomponente (WIC) wurde mit neuen Versionen von Windows aktualisiert. Dieses Thema bietet eine kurze Einführung in diese neuen Features.

## <a name="whats-new-for-windows-10-version-1507"></a>Neues bei Windows 10 Version 1507

### <a name="access-to-low-level-jpeg-data-for-wic-decoding-and-encoding"></a>Zugriff auf JPEG-Daten auf niedriger Ebene für die WIC-Decodierung und -Codierung

Ab Version Windows 10 Version 1507 bietet WIC Zugriff auf JPEG-Datenstrukturen auf niedriger Ebene, einschließlich Huffman- und Quantisierungstabellen. Weitere Informationen finden Sie in den folgenden Themen:

-   [**IWICJpegFrameDecode-Schnittstelle**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframedecode)
-   [**IWICJpegFrameEncode-Schnittstelle**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframeencode)

### <a name="jpeg-indexing"></a>JPEG-Indizierung

Die JPEG-Indizierung ist eine Technik, die die Leistung des zufälligen Zugriffs auf kleine Unterregionen eines großen JPEG-Bilds erheblich verbessert, und dies auf Kosten einer zusätzlichen Speicherauslastung. Die JPEG-Indizierung kann von jedem Aufrufer von WIC genutzt werden.

Die [**ID2D1ImageSourceFromWic-Schnittstelle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) ist für die Nutzung der JPEG-Indizierung konzipiert, wenn sie aktiviert ist. Beispielsweise fordert die ID2D1ImageSource-API nur die erforderlichen Abschnitte des Bilds in einem Szenario an, z. B. Schwenken und Zoomen für ein Bild mit großer Auflösung. Weitere Informationen finden Sie in den folgenden Themen:

-   [**IWICJpegFrameDecode::SetIndexing-Methode**](/windows/win32/api/Wincodec/nf-wincodec-iwicjpegframedecode-setindexing)
-   [**ID2D1ImageSourceFromWic-Schnittstelle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)

## <a name="whats-new-for-windows-81"></a>Neues bei Windows 8.1

### <a name="support-for-jpeg-ycbcr-images"></a>Unterstützung für JPEG-YCbCr-Bilder

Ab Windows 8.1 bietet WIC Unterstützung für das Decodieren, Transformieren und Codieren von JPEG Y'CbCr-Bilddaten im nativen Format. Dadurch können Apps die Verarbeitungszeit und den Arbeitsspeicherverbrauch für bestimmte Imagingvorgänge bei der Arbeit mit Y'CbCr-codierten JPEGs erheblich verringern. Weitere Informationen finden Sie in den folgenden Themen:

-   [](-wic-sample-d2d-viewer.md)[Direct2D-YCbCr-Effekt](../direct2d/ycbcr-effect.md)
-   [**IWICPlanarBitmapSourceTransform-Schnittstelle**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)
-   [**IWICPlanarBitmapFrameEncode-Schnittstelle**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode)

### <a name="support-for-block-compressed-formats-dds-files"></a>Unterstützung für blockkomprimierte Formate (DDS-Dateien)

Ab Windows 8.1 fügt WIC einen neuen Codec hinzu, der DDS-Bilder unterstützt, die in den folgenden Formaten codiert sind: DXGI \_ FORMAT \_ BC1 \_ UNORM, DXGI \_ FORMAT \_ BC2 \_ UNORM und DXGI \_ FORMAT \_ BC3 \_ UNORM. Auf komprimierte DDS-Blockdaten kann in decodiertem Format über WIC-Standardschnittstellen oder direkt über neue DDS-spezifische Schnittstellen zugegriffen werden. Weitere Informationen finden Sie in den folgenden Themen:

-   [**IWICDdsDecoder-Schnittstelle**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsdecoder)
-   [**IWICDdsEncoder-Schnittstelle**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsencoder)

## <a name="whats-new-for-windows-8"></a>Neues bei Windows 8

In Windows 8 wurde WIC mit mehreren neuen Features aktualisiert. Die aktualisierte Version von WIC ist auch unter Windows 7 und Windows Server 2008 R2 über das Plattformupdate für [Windows 7](../direct3darticles/platform-update-for-windows-7.md)verfügbar, das über das Plattformupdate für [Windows 7 verfügbar ist.](https://support.microsoft.com/kb/2670838)

### <a name="improved-direct2d-integration"></a>Verbesserte Direct2D-Integration

WIC in Windows 8 bietet diese APIs zur Verbesserung der Direct2D-Integration mit WIC:

-   [**IWICImageEncoder:**](/windows/win32/api/Wincodec/nn-wincodec-iwicimageencoder) Eine neue Schnittstelle, die Direct2D [**ID2D1Image-Inhalte**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) in [einen IWICBitmapFrameEncode codieren kann.](-wic-imp-iwicbitmapframeencode.md) Die Methoden dieser Schnittstelle verwenden einen Zeiger auf [**WICImageParameters,**](/windows/win32/api/Wincodec/ns-wincodec-wicimageparameters)bei denen es sich um Parameter zum Steuern der Codierung handelt.
-   [**IWICImagingFactory2:**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory2) Neue WIC-Factory mit der [**CreateImageEncoder-Methode.**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder) Diese Schnittstelle erbt von der ursprünglichen WIC-Factory [**IWICImagingFactory**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory)und wird auf die gleiche Weise erstellt.

### <a name="changes-to-bmp-codec-alpha-support"></a>Änderungen an der BMP-Codec-Alphaunterstützung

WIC in Windows 8 unterstützt das Laden von [**BITMAPV5HEADER-Bilddateien**](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) als Bilder im [WICPixelFormat32bppBGRA-Format.](-wic-codec-native-pixel-formats.md) Darüber hinaus unterstützt der BMP-Encoder eine neue boolesche Encoderoption "EnableV5Header32bppBGRA", die den Encoder anweisen soll, einen **BITMAPV5HEADER** mit den 32bppBGRA-Bilddaten zu schreiben.

Weitere Informationen zu BMP-Formaten finden Sie unter [Übersicht über das BMP-Format.](bmp-format-overview.md)

### <a name="new-pixel-formats"></a>Neue Pixelformate

WIC in Windows 8 definiert diese neuen Pixelformate:

-   GUID \_ WICPixelFormat32bppRGB
-   GUID \_ WICPixelFormat64bppRGB
-   GUID \_ WICPixelFormat96bppRGBFloat
-   GUID \_ WICPixelFormat64bppPRGBAHalf

> [!Note]  
> Der integrierte TIFF-Codec gibt \_ GUID-WICPixelFormat96bppRGBFloat-Daten zurück. Die anderen drei Formate werden von integrierten Codecs nicht verwendet.

 

### <a name="restrictions-to-component-extensibility-in-appcontainer"></a>Einschränkungen der Komponentenerweiterbarkeit in AppContainer

Bei der Ausführung in einem AppContainer-Prozess, der alle Windows Store-Apps umfasst, verwendet WIC nur von Windows bereitgestellte Komponenten, unabhängig davon, ob zusätzliche Komponenten auf dem System installiert sind. Apps, die nicht in AppContainer ausgeführt werden, sind nicht betroffen.

Apps müssen keine Codeänderungen vornehmen, um in einer AppContainger-Datei ausgeführt zu werden, aber das [**WICComponentEnumerateOptions-Flag**](/windows/win32/api/Wincodec/ne-wincodec-wiccomponentenumerateoptions) und die Anbieter-GUID-Parameter haben keine Auswirkungen. WIC kann ein Image nicht laden, wenn es nicht von einem von Windows bereitgestellten Codec decodiert werden kann, und beim Aufrufen der [**CreateComponentEnumerator-Methode**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentenumerator) werden nur von Windows bereitgestellte Komponenten zurückgerufen.

### <a name="changes-to-clsid_wicpngdecoder-and-png-decoder-color-context-support"></a>Änderungen an der Farbkontextunterstützung für \_ CLSID WICPngDecoder und PNG-Decoder

**CLSID \_ WICPngDecoder1** wurde mit der gleichen GUID wie **CLSID \_ WICPngDecoder** hinzugefügt, und **CLSID \_ WICPngDecoder2** wurde hinzugefügt.

Bei der Kompilierung mit dem Windows 8 SDK wird **CLSID \_ WICPngDecoder** in \# **CLSID \_ WICPngDecoder2** definiert, um neu kompilierte Apps mithilfe des neuen PNG-Decoderverhaltens zu promoten. Apps sollten weiterhin **CLSID \_ WICPngDecoder angeben.**

Wenn **Sie CLSID \_ WICPngDecoder2** angeben, wird eine Version des WIC PNG-Decoders erstellt, der [**einen IWICColorContext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) aus cHRM- und gAMA-Block generiert. Dadurch können diese Farbraummetadaten mit anderen Windows-APIs für die Farbverwaltung des Quellbilds verwendet werden. Ein **IWICColorContext** wird nicht aus den gAMA- und cHRM-Blocken generiert, wenn ein iCCP-Block vorhanden ist, wenn ein sRGB-Block vorhanden ist oder wenn die gAMA- und cHRM-Block einen sRGB-Farbraum angeben.

Eine App kann **CLSID \_ WICPngDecoder1** angeben, um eine Version des WIC PNG-Decoders zu erstellen, die [**keinen IWICColorContext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) aus den gAMA- und cHRM-Blocken generiert. Dies entspricht dem Verhalten des PNG-Decoders in früheren Versionen von Windows.

### <a name="changes-to-wincodec_sdk_version"></a>Änderungen an der WINCODEC \_ \_ SDK-VERSION

Bei der Kompilierung mit dem Windows 8 SDK wird **WINCODEC \_ \_ SDK-VERSION** in \# **WINCODEC \_ SDK \_ VERSION2** definiert, um neu kompilierte Apps mithilfe des neuen PNG-Decoderverhaltens zu promoten. Andernfalls wird \# sie in **WINCODEC \_ SDK \_ VERSION1 definiert.** Apps sollten weiterhin **WINCODEC \_ SDK VERSION \_ angeben.**

Die Angabe der **WINCODEC \_ \_ SDK-VERSION** beim Aufrufen des [**WICCreateImagingFactory-Proxys \_**](-wic-codec-wiccreateimagingfactory-proxy.md) zum Erstellen der Imaging Factory bewirkt, dass **CLSID \_ WICPngDecoder2** anstelle von **CLSID \_ WICPngDecoder1** aus der [**CreateDecoder-Methode**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder) und ihren Varianten erstellt wird. Außerdem gibt ein Decoderkomponenteninformations-Enumerator **CLSID \_ WICPngDecoder2-Komponenteninformationen** zurück, jedoch keine **CLSID \_ WICPngDecoder1-Informationen.**

Die Angabe **von WINCODEC \_ SDK \_ VERSION1** verursacht in den obigen Fällen die Verwendung von **CLSID \_ WICPngDecoder1** anstelle von **CLSID \_ WICPngDecoder2.**

### <a name="changes-to-clsid_wicimagingfactory"></a>Änderungen an CLSID \_ WICImagingFactory

**CLSID \_ WICImagingFactory1** wurde mit der gleichen GUID wie **CLSID \_ WICImagingFactory** hinzugefügt, und **CLSID \_ WICImagingFactory2** wurde hinzugefügt.

Bei der Kompilierung mit dem Windows 8 SDK wird **CLSID \_ WICImagingFactory** in \# **CLSID \_ WICImagingFactory2** definiert, um neu kompilierte Apps mit dem neuen PNG-Decoderverhalten zu promoten. Apps sollten weiterhin **CLSID \_ WICImagingFactory angeben.**

Das Angeben der **CLSID \_ WICImagingFactory2** beim Aufrufen von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Erstellen der Imaging Factory bewirkt, dass **CLSID \_ WICPngDecoder2** anstelle von **CLSID \_ WICPngDecoder1** aus der [**CreateDecoder-Methode**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder) und ihren Varianten erstellt wird. Außerdem gibt ein Decoderkomponenteninformations-Enumerator **CLSID \_ WICPngDecoder2-Komponenteninformationen** zurück, jedoch keine **CLSID \_ WICPngDecoder1-Informationen.**

Die Angabe **der CLSID \_ WICImagingFactory1** verursacht in den obigen Fällen die Verwendung von **CLSID \_ WICPngDecoder1** anstelle von **CLSID \_ WICPngDecoder2.**

## <a name="whats-new-for-windows-7"></a>Neues bei Windows 7

In Windows 7 wurde WIC mit mehreren neuen Features aktualisiert. Dieses Thema bietet eine kurze Einführung in diese neuen Features.

### <a name="updates-to-the-tiff-codec"></a>Updates des TIFF-Codecs

Der WIC TIFF-Codec wurde für Windows 7 aktualisiert, um mehrere Features zu unterstützen, die von der vorherigen Version von WIC nicht unterstützt werden.

-   Unterstützung für große TIFF-Dateien.
-   Decodieren sie gekachelte TIFF-Bilder.
-   Decodieren sie flache (planare) TIFF-Bilder.
-   Decodieren sie JPEG-codierte TIFF-Bilder.

### <a name="progressive-decoding"></a>Progressive Decodierung

Die progressive Decodierung bietet die Möglichkeit, Teile eines Bilds inkrementell zu decodieren und zu rendern, bevor das gesamte Bild heruntergeladen wurde. Dieses Feature verbessert die Benutzerfreundlichkeit beim Anzeigen von Bildern aus dem Internet erheblich, da der Benutzer nicht warten muss, bis das gesamte Bild heruntergeladen wird, bevor die Decodierung beginnen kann. Bei der progressiven Decodierung können Benutzer eine Imagevorschau mit verfügbaren Daten sehen, lange bevor das gesamte Bild heruntergeladen wird. Dieses Feature ist wichtig für jede Anwendung, die zum Anzeigen von Bildern aus dem Internet oder aus Datenquellen mit begrenzter Bandbreite verwendet wird.

Weitere Informationen finden Sie unter [Progressive Decoding Overview (Übersicht über die progressive Decodierung).](-wic-progressive-decoding.md)

### <a name="extended-metadata-support-for-jpeg-png-and-gif"></a>Erweiterte Metadatenunterstützung für JPEG, PNG und GIF

In Windows 7 hat WIC die Metadatenunterstützung für JPEG-, PNG- und GIF-Bilder erweitert.

-   Unterstützung für animierte GIF- und GIF-Eigenschaften hinzugefügt.
-   Erweiterte JPG-Metadatenhandler zur Unterstützung von Chrominance-, Luminanz- und Kommentarmetadaten.
-   Erweiterte PNG-Metadatenhandler zur Unterstützung von tIME-, sRGB-, iCCP-, hIST-, cHRM-, iTXt-, bKGD- und gAMA-Metadaten.
-   Neue 8BIM-Metadatenhandler für ResolutionInfo-Metadaten und IPTC-Digestmetadaten hinzugefügt.
-   Es wurden neue Metadatenhandler für die Metadaten logical screen descriptor (LSD), Image Descriptor (IMD), Graphic Control Extensions (GCE) und Application Extensions (APE) hinzugefügt.
-   Unterstützung für Metadaten, die APPn-Blöcke umfassen.

### <a name="multi-threaded-apartment-support"></a>Multithread-Apartmentunterstützung

Objekte in einem Multithread-Apartment (MTA) können gleichzeitig von einer beliebigen Anzahl von Threads innerhalb des MTA aufgerufen werden, was eine bessere Leistung auf Systemen mit mehreren Kernen und bestimmten Serverszenarien ermöglicht. Darüber hinaus können WIC-Codecs, die in einem MTA leben, andere Objekte aufrufen, die innerhalb des MTA leben, ohne die Marshallingkosten, die mit dem Aufruf zwischen Threads verbunden sind, die in verschiedenen STA-Apartments leben. In Windows 7 wurden alle In-Box-WIC-Codecs aktualisiert, um MTA zu unterstützen, einschließlich JPEG, TIFF, PNG, GIF, ICO und BMP. Es wird dringend empfohlen, Codecs zur Unterstützung von MTA zu schreiben. Codecs, die MTA nicht unterstützen, führen aufgrund von Marshalling zu einer erheblichen Leistungsdegredation in Multithreadanwendungen. Das Aktivieren der MTA-Unterstützung erfordert, dass eine ordnungsgemäße Synchronisierung im Codec implementiert wird. Die genaue Implementierung dieser Synchronisierungstechniken geht über den Rahmen dieses Whitepapers hinaus. Eine allgemeine Referenz zum Synchronisieren Component Object Model -Objekten (COM) finden Sie unten.

### <a name="metadata-working-group-implementations"></a>Implementierungen von Metadatenarbeitsgruppe

Es gibt derzeit eine Vielzahl von Metadatenspeicherformaten, die überlappende Eigenschaften enthalten, ohne dass ein eindeutiger Branchenstandard oder eine Anleitung zu konsistenten Methoden zum Lesen und Schreiben dieser Metadatenformate vorhanden ist. Um bei dieser Vielzahl von Formaten und Eigenschaften zu helfen, wurde die Metadatenarbeitsgruppe (Metadata Working Group, SOLLTENG) gebildet. Das Ziel des TSIG besteht im Bereitstellen von Richtlinien, die die Interoperabilität zwischen einer Vielzahl von Plattformen, Anwendungen und Geräten sicherstellen. Die richtlinien, die vom PROTOKOLLG festgelegt werden, gelten für die XMP-, Exif- und IPTC-Metadatenfelder sowie für die Jpeg-, TIFF- und PSD-Bildformate.

In Windows 7 wurden der Handler für Fotometadaten und die Metadatenrichtlinienebene aktualisiert, um Bildmetadaten gemäß den Richtlinien des 2016-2016-2016-2016-Elements zu lesen und zu schreiben. Weitere Informationen zur Metadata Working Group (IIIG) finden Sie in den [festgelegten Metadatenrichtlinien.](https://s3.amazonaws.com/software.tagthatphoto.com/docs/mwg_guidance.pdf)

### <a name="windows-7-features-supported-on-windows-vista-and-windows-server-2008"></a>Windows 7-Features, die unter Windows Vista und Windows Server 2008 unterstützt werden

Das [Plattformupdate für Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md) ist eine Reihe von Laufzeitbibliotheken, mit denen Entwickler Anwendungen sowohl auf Windows 7 als auch auf Windows Vista Windows können. Das Plattformupdate für Windows Server 2008 ist eine Reihe von Laufzeitbibliotheken, mit denen Entwickler Anwendungen sowohl auf Windows Server 2008 R2 als auch auf Windows Server 2008 als Ziel verwenden können. Das Plattformupdate für Windows Vista und das Plattformupdate für Windows Server 2008 sind für alle Windows Vista- und Windows Server 2008-Kunden über Windows Update verfügbar. Bei Anwendungen von Drittanbietern, für die ein Plattformupdate für Windows Vista oder ein Plattformupdate für Windows Server 2008 erforderlich ist, kann Windows Update erkennen, ob das erforderliche Update installiert ist. Ist dies nicht der Windows Update wird es heruntergeladen und im Hintergrund installiert. Weitere Informationen zu beiden Updates finden Sie unter Plattformupdate für Windows Vista.

 

 
