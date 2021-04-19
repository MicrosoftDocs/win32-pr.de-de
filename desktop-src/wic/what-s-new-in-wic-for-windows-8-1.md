---
description: Windows Imaging Component (WIC) wurde mit neuen Versionen von Windows aktualisiert. Dieses Thema bietet eine kurze Einführung in diese neuen Features.
ms.assetid: 710B71CE-6FCC-46DA-A65C-6E4FC6A04275
title: Neues in WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b8b3783ac2fd8ef6a971f785cec80f868a6b80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352370"
---
# <a name="whats-new-in-wic"></a>Neues in WIC

Windows Imaging Component (WIC) wurde mit neuen Versionen von Windows aktualisiert. Dieses Thema bietet eine kurze Einführung in diese neuen Features.

## <a name="whats-new-for-windows-10-version-1507"></a>Neuerungen in Windows 10, Version 1507

### <a name="access-to-low-level-jpeg-data-for-wic-decoding-and-encoding"></a>Zugriff auf Low-Level-JPEG-Daten für WIC-Decodierung und-Codierung

Ab Windows 10, Version 1507, bietet WIC Zugriff auf Low-Level-JPEG-Datenstrukturen, wie z. b. die Daten von Huffman und Quantisierung. Weitere Informationen finden Sie unter den folgenden Themen:

-   [**Iwicjpgframedecode**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframedecode) -Schnittstelle
-   [**Iwicjpgframekocode**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframeencode) -Schnittstelle

### <a name="jpeg-indexing"></a>JPEG-Indizierung

Die JPEG-Indizierung ist eine Technik, mit der die Leistung des zufälligen Zugriffs auf kleine Teilbereiche eines großen JPEG-Bilds erheblich verbessert wird. Dies ist eine zusätzliche Speicherauslastung. Die JPEG-Indizierung kann von jedem Aufrufer von WIC genutzt werden.

Die [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) -Schnittstelle ist für die Verwendung von JPEG-Indizierung konzipiert, wenn Sie aktiviert ist. Beispielsweise fordert die ID2D1ImageSource-API nur die erforderlichen Abschnitte des Bilds in einem Szenario wie "Pan" und "Zoom" für ein großes Auflösungs Bild an. Weitere Informationen finden Sie unter den folgenden Themen:

-   [**Iwicjpgframedecode:: setindizierungs**](/windows/win32/api/Wincodec/nf-wincodec-iwicjpegframedecode-setindexing) -Methode
-   [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) -Schnittstelle

## <a name="whats-new-for-windows-81"></a>Neuerungen bei Windows 8.1

### <a name="support-for-jpeg-ycbcr-images"></a>Unterstützung für JPEG YCbCr-Bilder

Ab Windows 8.1 bietet WIC Unterstützung für das decodieren, Transformieren und Codieren von JPEG-Daten im systemeigenen Format. Dadurch können Apps die Verarbeitungszeit und die Arbeitsspeicher Nutzung für bestimmte Abbild Erstellungs Vorgänge erheblich verringern, wenn Sie mit "y' CbCr-codiertem jpeer arbeiten. Weitere Informationen finden Sie unter den folgenden Themen:

-   [Direct2D](-wic-sample-d2d-viewer.md)[YCbCr-Effekt](../direct2d/ycbcr-effect.md)
-   [**Iwicplanarbitmapsourcetransform**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) -Schnittstelle
-   [**Iwicplanarbitmapframekocode**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) -Schnittstelle

### <a name="support-for-block-compressed-formats-dds-files"></a>Unterstützung für Block komprimierte Formate (DDS-Dateien)

Ab Windows 8.1 fügt WIC einen neuen Codec hinzu, der DDS-Images unterstützt, die in den folgenden Formaten codiert sind: DXGI- \_ Format \_ BC1 \_ unorm, DXGI \_ \_ -Format BC2 \_ unorm und DXGI- \_ Format \_ BC3 \_ unorm. Auf DDS-Block komprimierte Daten kann in einem decodierten Formular mithilfe von Standard-WIC-Schnittstellen zugegriffen werden, oder der Zugriff erfolgt direkt mithilfe neuer DDS-spezifischer Schnittstellen Weitere Informationen finden Sie unter den folgenden Themen:

-   [**Iwicddsdecoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsdecoder) -Schnittstelle
-   [**Iwicddsencoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsencoder) -Schnittstelle

## <a name="whats-new-for-windows-8"></a>Neuerungen in Windows 8

In Windows 8 wurde WIC mit mehreren neuen Features aktualisiert. Die aktualisierte Version von WIC ist auch unter Windows 7 und Windows Server 2008 R2 über das [Platt Form Update für Windows 7](../direct3darticles/platform-update-for-windows-7.md)verfügbar, das über das [Platt Form Update für Windows 7](https://support.microsoft.com/kb/2670838)verfügbar ist.

### <a name="improved-direct2d-integration"></a>Verbesserte Direct2D-Integration

WIC in Windows 8 bietet diese APIs, um die Direct2D-Integration in WIC zu verbessern:

-   [**Iwicimageencoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicimageencoder) : eine neue Schnittstelle, die Direct2D [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) -Inhalt in einen [iwicbitmapframecocode](-wic-imp-iwicbitmapframeencode.md)codieren kann. Die Methoden dieser Schnittstelle übernehmen einen Zeiger auf [**wicimageparameters**](/windows/win32/api/Wincodec/ns-wincodec-wicimageparameters), die Parameter zum Steuern der Codierung sind.
-   [**IWICImagingFactory2**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory2) -neue WIC-Factory mit der Methode " [**kreateimageencoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder) ". Diese Schnittstelle erbt von der ursprünglichen WIC-Factory [**IWICImagingFactory**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory)und wird auf die gleiche Weise erstellt.

### <a name="changes-to-bmp-codec-alpha-support"></a>Änderungen an der BMP-Codec-Alpha Unterstützung

WIC in Windows 8 unterstützt das Laden von [**BITMAPV5HEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) -Bilddateien als [WICPixelFormat32bppBGRA](-wic-codec-native-pixel-formats.md)-formatierte Bilder. Außerdem unterstützt der BMP-Encoder eine neue boolesche Codierungs Option "EnableV5Header32bppBGRA", die den Encoder anweist, ein **BITMAPV5HEADER** mit den 32bppbgra-Bilddaten zu schreiben.

Weitere Informationen zu BMP-Formaten finden Sie unter Übersicht über das [BMP-Format](bmp-format-overview.md).

### <a name="new-pixel-formats"></a>Neue Pixel Formate

WIC in Windows 8 definiert diese neuen Pixel Formate:

-   GUID \_ WICPixelFormat32bppRGB
-   GUID \_ WICPixelFormat64bppRGB
-   GUID \_ WICPixelFormat96bppRGBFloat
-   GUID \_ WICPixelFormat64bppPRGBAHalf

> [!Note]  
> Der integrierte TIFF-Codec gibt GUID WICPixelFormat96bppRGBFloat- \_ Daten zurück. Die anderen drei Formate werden von integrierten Codecs nicht verwendet.

 

### <a name="restrictions-to-component-extensibility-in-appcontainer"></a>Einschränkungen für die Erweiterbarkeit von Komponenten in appcontainer

Wenn Sie in einem appcontainer-Prozess ausgeführt werden, der alle Windows Store-Apps umfasst, verwendet WIC nur von Windows bereitgestellte Komponenten, unabhängig davon, ob auf dem System zusätzliche Komponenten installiert sind. Die APP, die nicht in appcontainer ausgeführt wird, ist nicht betroffen.

Apps müssen keine Codeänderungen vornehmen, um Sie in appcontainger auszuführen, aber das Flag [**wiccomponentenumerateoptions**](/windows/win32/api/Wincodec/ne-wincodec-wiccomponentenumerateoptions) und die GUID-Parameter des Anbieters haben keine Auswirkungen. WIC kann ein Abbild nicht laden, wenn es nicht von einem von Windows bereitgestellten Codec decodiert werden kann, und wenn die [**createcomponentenumschlag**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentenumerator) -Methode aufgerufen wird, werden nur von Windows bereitgestellte Komponenten zurückgegeben.

### <a name="changes-to-clsid_wicpngdecoder-and-png-decoder-color-context-support"></a>Änderungen an der Unterstützung von CLSID \_ wicpngdecoder und PNG-decoderfarben

**CLSID \_ WICPngDecoder1** wurde mit der gleichen GUID wie **CLSID \_ wicpngdecoder** und **CLSID \_ WICPngDecoder2** hinzugefügt.

Bei der Kompilierung für das Windows 8-SDK ist **CLSID \_ wicpngdecoder** \# auf **CLSID \_ WICPngDecoder2** definiert, um neu kompilierte apps mit dem neuen PNG-decoderverhalten zu Stufen. Apps sollten weiterhin **CLSID \_ wicpngdecoder** angeben.

Durch Angeben der **CLSID- \_ WICPngDecoder2** wird eine Version des WIC PNG-Decoders erstellt, der einen [**IWICColorContext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) aus chrm-und Gama-Blöcken generiert. Dadurch können diese Farbraum-Metadaten mit anderen Windows-APIs für die Farbverwaltung des Quell Bilds verwendet werden. Ein **IWICColorContext** wird nicht aus den Blöcken "Gama" und "chrm" generiert, wenn ein ICCP-Block vorhanden ist, wenn ein sRGB-Block vorhanden ist, oder wenn die Segmente "Gama" und "chrm" einen sRGB-Farbraum angeben.

Eine APP kann **CLSID- \_ WICPngDecoder1** angeben, um eine Version des WIC PNG-Decoders zu erstellen, die keinen [**IWICColorContext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) aus den Blöcken "Gama" und "chrm" generiert. Dies entspricht dem Verhalten des PNG-Decoders in früheren Versionen von Windows.

### <a name="changes-to-wincodec_sdk_version"></a>Änderungen an der Version des wincodec \_ SDK \_

Bei der Kompilierung für das Windows 8 SDK wird die **wincodec \_ SDK- \_ Version** \# für das **wincodec \_ SDK \_ Version2** definiert, um neu kompilierte apps mit dem neuen PNG-decoderverhalten höher zu Stufen. Andernfalls wird es \# für das **wincodec \_ SDK \_ Version1** definiert. Apps sollten weiterhin die **wincodec \_ SDK- \_ Version** angeben.

Die Angabe der **wincodec \_ SDK- \_ Version** beim Aufrufen von [**wiccreateimagingfactory \_ Proxy**](-wic-codec-wiccreateimagingfactory-proxy.md) zum Erstellen der Imaging Factory bewirkt, dass **CLSID- \_ WICPngDecoder2** anstelle von **CLSID \_ WICPngDecoder1** von der [**CreateDecoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder) -Methode und den zugehörigen Varianten erstellt werden. Außerdem gibt ein decoderkomponenteninfoenumerator **CLSID \_ WICPngDecoder2** Component Info, aber keine **CLSID \_ WICPngDecoder1** Info zurück.

Das Angeben des **wincodec \_ SDK \_ Version1** bewirkt, dass **CLSID \_ WICPngDecoder1** anstelle von **CLSID \_ WICPngDecoder2** in den obigen Fällen verwendet wird.

### <a name="changes-to-clsid_wicimagingfactory"></a>Änderungen an CLSID \_ wicimagingfactory

**CLSID \_ WICImagingFactory1** wurde mit der gleichen GUID wie **CLSID \_ wicimagingfactory** und **CLSID \_ WICImagingFactory2** hinzugefügt.

Bei der Kompilierung für das Windows 8 SDK ist **CLSID \_ wicimagingfactory** \# auf **CLSID \_ WICImagingFactory2** definiert, um neu kompilierte Apps mithilfe des neuen PNG-decoderverhaltens zu Stufen. Apps sollten weiterhin **CLSID \_ wicimagingfactory** angeben.

Durch Angeben der **CLSID- \_ WICImagingFactory2** beim Aufrufen von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Erstellen der Imaging Factory wird die Erstellung von **CLSID \_ WICPngDecoder2** anstelle der **CLSID- \_ WICPngDecoder1** aus der [**CreateDecoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder) -Methode und den zugehörigen Varianten verursacht. Außerdem gibt ein decoderkomponenteninfoenumerator **CLSID \_ WICPngDecoder2** Component Info, aber keine **CLSID \_ WICPngDecoder1** Info zurück.

Das Angeben von **CLSID \_ WICImagingFactory1** bewirkt, dass **CLSID \_ WICPngDecoder1** anstelle von **CLSID \_ WICPngDecoder2** in den obigen Fällen verwendet wird.

## <a name="whats-new-for-windows-7"></a>Neuerungen in Windows 7

In Windows 7 wurde WIC mit mehreren neuen Features aktualisiert. Dieses Thema bietet eine kurze Einführung in diese neuen Features.

### <a name="updates-to-the-tiff-codec"></a>Updates für den TIFF-Codec

Der WIC TIFF-Codec wurde für Windows 7 aktualisiert, um mehrere Features zu unterstützen, die von der vorherigen Version von WIC nicht unterstützt werden.

-   Unterstützung für große TIFF-Dateien.
-   Decodieren von gekachelten TIFF-Bildern.
-   Decodieren Sie flache (planare) TIFF-Bilder.
-   Decodieren von JPEG-codierten TIFF-Bildern.

### <a name="progressive-decoding"></a>Progressive Decodierung

Die Progressive Decodierung bietet die Möglichkeit, Teile eines Bilds inkrementell zu decodieren und zu Rendering, bevor das gesamte Bild heruntergeladen wird. Diese Funktion verbessert die Benutzer Funktionalität beim Anzeigen von Images aus dem Internet erheblich, da der Benutzer nicht warten muss, bis das gesamte Image heruntergeladen wird, bevor die Decodierung beginnen kann. Mit progressiver Decodierung können Benutzer eine Bildvorschau mit verfügbaren Daten anzeigen, bevor das gesamte Image heruntergeladen wird. Diese Funktion ist für alle Anwendungen, die zum Anzeigen von Images aus dem Internet oder für Datenquellen mit eingeschränkter Bandbreite verwendet werden, von entscheidender Bedeutung.

Weitere Informationen finden Sie in der [Übersicht über die Progressive Decodierung](-wic-progressive-decoding.md).

### <a name="extended-metadata-support-for-jpeg-png-and-gif"></a>Erweiterte Metadatenunterstützung für JPEG, PNG und GIF

In Windows 7 hat WIC seine Metadatenunterstützung für JPEG-, PNG-und GIF-Images erweitert.

-   Unterstützung für animierte GIF-und GIF-Eigenschaften hinzugefügt.
-   Die JPG-Metadatenhandler wurden zur Unterstützung von Chrominance-, Leuchtkraft-und Kommentar Metadaten erweitert.
-   Die PNG-Metadatenhandler wurden erweitert, um die Metadaten Time, sRGB, ICCP, Hist, chrm, iTXt, bkgd und Gama zu unterstützen.
-   Neue 8bim-Metadatenhandler für "resolutioninfo"-Metadaten und IPTC-Digest-Metadaten hinzugefügt.
-   Neue Metadatenhandler für den logischen Bildschirm Deskriptor (LSD), Bild Deskriptor (IMD), Grafik Steuerelement-Erweiterungen (GCE) und Anwendungs Erweiterungen (APE)-Metadaten hinzugefügt.
-   Unterstützung für Metadaten, die APPN-Blöcke umfassen.

### <a name="multi-threaded-apartment-support"></a>Multithread-Apartment Unterstützung

Objekte in einem Multithread-Apartment (MTA) können gleichzeitig durch eine beliebige Anzahl von Threads innerhalb des MTA aufgerufen werden, was eine bessere Leistung für Multikernsysteme und bestimmte Server Szenarien ermöglicht. Darüber hinaus können WIC-Codecs, die innerhalb eines MTA Leben, andere Objekte aufrufen, die innerhalb des MTA Leben, ohne die Marshallingkosten im Zusammenhang mit dem Aufruf zwischen Threads, die in unterschiedlichen STA-Wohnungen leben. In Windows 7 wurden alle in-Box-WIC-Codecs aktualisiert, um MTA zu unterstützen, einschließlich JPEG, TIFF, PNG, GIF, ICO und BMP. Es wird dringend empfohlen, dass Codecs für die Unterstützung von MTA geschrieben werden. Codecs, die MTA nicht unterstützen, führen aufgrund von Marshalling zu erheblichen Leistungsdaten in Multithreadanwendungen. Zum Aktivieren der MTA-Unterstützung muss eine ordnungsgemäße Synchronisierung im Codec implementiert werden. Die genaue Implementierung dieser Synchronisierungs Verfahren geht über den Rahmen dieses Artikels hinaus. Eine allgemeine Referenz zum Synchronisieren von Component Object Model (com)-Objekten finden Sie unten.

### <a name="metadata-working-group-implementations"></a>Metadaten-Arbeitsgruppen Implementierungen

Zurzeit gibt es eine Vielzahl von metadatenspeicherformaten, die überlappende Eigenschaften enthalten, ohne einen eindeutigen Industriestandard oder Anleitungen für konsistente Methoden zum Lesen und Schreiben dieser Metadatenformate. Zur Unterstützung dieser Vielzahl von Formaten und Eigenschaften wurde die metadatenarbeitsgruppe (MWG) gebildet. Das Ziel der MWG besteht darin, Richtlinien bereitzustellen, die die Interoperabilität zwischen einer Vielzahl von Plattformen, Anwendungen und Geräten gewährleisten. Die Richtlinien, die von der MWG festgelegt werden, gelten für die Metadatenfelder XMP, EXIF und IPTC sowie für die Bildformate JPEG, TIFF und PSD.

In Windows 7 wurden der Foto-Metadatenhandler und die metadatenrichtlinienschicht aktualisiert, um die Bild Metadaten gemäß den von der MWG festgelegten Richtlinien zu lesen und zu schreiben. Weitere Informationen zur metadatenarbeitgruppe (MWG) finden Sie in den [Richtlinien für die festgelegte Metadaten](https://s3.amazonaws.com/software.tagthatphoto.com/docs/mwg_guidance.pdf).

### <a name="windows-7-features-supported-on-windows-vista-and-windows-server-2008"></a>Windows 7-Features unter Windows Vista und Windows Server 2008

Das [Platt Form Update für Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md) ist eine Reihe von Laufzeitbibliotheken, die es Entwicklern ermöglichen, Anwendungen für Windows 7 und Windows Vista als Ziel festzulegen. Das Platt Form Update für Windows Server 2008 ist eine Reihe von Laufzeitbibliotheken, die es Entwicklern ermöglichen, Anwendungen für Windows Server 2008 R2 und Windows Server 2008 als Ziel festzulegen. Das Platt Form Update für Windows Vista und das Platt Form Update für Windows Server 2008 werden für alle Windows Vista-und Windows Server 2008-Kunden über Windows Update verfügbar sein. Anwendungen von Drittanbietern, die ein Platt Form Update für Windows Vista oder ein Platt Form Update für Windows Server 2008 erfordern, können Windows Update erkennen, ob das erforderliche aktualisierte installiert ist. Wenn dies nicht der Fall ist, wird Windows Update im Hintergrund heruntergeladen und installiert. Weitere Informationen zu beiden Updates finden Sie unter Platt Form Update für Windows Vista.

 

 
