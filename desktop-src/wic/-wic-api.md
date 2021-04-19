---
description: Die Windows Imaging Component (WIC) stellt eine Component Object Model (com)-basierte API für die Verwendung in C und C++ bereit.
ms.assetid: 74b14b5e-70e9-410f-a6e6-d8873a5f4fa4
title: WIC-API-Übersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86e5a876010e52489adac9baa7ce57fdfdf80f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368815"
---
# <a name="wic-api-overview"></a>WIC-API-Übersicht

Die Windows Imaging Component (WIC) stellt eine Component Object Model (com)-basierte API für die Verwendung in C und C++ bereit. Die WIC-API bietet eine Vielzahl von Bild bezogenen Funktionen, einschließlich:

-   Integrierte Codecs für die Standardweb Bildformate.
-   Integrierte Unterstützung für standardmetadatenformate.
-   Unterstützung für eine breite Palette an Pixel Formaten.
-   Unterstützung für hohe Farben; Dazu zählen der erweiterte 30-Bit-Bereich, die 30-Bit-Genauigkeit mit hoher Genauigkeit und 48-Bit-Pixel Formate mit hoher Genauigkeit und Breite.
-   Erweiterbares Framework für Bild Codecs, Pixel Formate und Metadatenformate.

Dieses Thema enthält die folgenden Themen:

-   [WIC-Header Dateien](#wic-header-files)
-   [Bibliotheksdateien](#library-files)
-   [Klassenfactory](#class-factories)
-   [Bildverarbeitungskomponenten](#imaging-components)
-   [Siehe auch](#see-also)

## <a name="wic-header-files"></a>WIC-Header Dateien

Die WIC-APIs werden in den folgenden Header-und IDL-Dateien (Interface Definition Language) definiert:



| Datei              | BESCHREIBUNG                                          |
|-------------------|------------------------------------------------------|
| wincodec. h        | Definiert die C-und C++-Versionen der primären WIC-APIs.  |
| wincodec. idl      | Definiert die primären WIC-Schnittstellen.                  |
| wincodecsdk. h     | Definiert die C-und C++-Versionen der Metadaten-WIC-APIs. |
| wincodecsdk. idl   | Definiert die WIC-Metadatenschnittstellen.                 |
| wincodec- \_ Proxy. h | Definiert die WIC-Proxy Exporte.                       |



 

Um WIC verwenden zu können, müssen Ihre Anwendungen abhängig von der API, die Ihre Anwendung benötigt, wincodec. h und/oder wincodecsdk. h einschließen.

## <a name="library-files"></a>Bibliotheksdateien

Die WIC-Bibliotheksdateien:



| Datei              | BESCHREIBUNG                                                            |
|-------------------|------------------------------------------------------------------------|
| windowscodebug. lib | Import Bibliothek, die vom Windows Software Development Kit (SDK) bereitgestellt wird. |
| windowscodecs.dll | Vom Betriebssystem bereitgestellte Bestands Implementierungs Bibliothek.         |



 

Um einen Link zu WIC-APIs zu erhalten, muss Ihre Anwendung windowscodec. lib als zusätzliche Linker-Abhängigkeit einschließen.

## <a name="class-factories"></a>Klassenfactory

In der folgenden Tabelle werden die beiden com-Klassenfactorys beschrieben, die die WIC-APIs zum Erstellen von WIC-



| Factory-Schnittstelle                                               | BESCHREIBUNG                                                                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)     | Primäre Klassenfactory für die Anwendungsentwicklung mit WIC-Komponenten. Diese Factory erstellt Komponenten, z. b. Image-Decoders, Encoder und Streams.   |
| [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) | Klassenfactory, die für WIC-Komponenten Entwickler konzipiert ist. Komponenten, die aus dieser Factory erstellt werden, werden primär in der Codec-und metadatenhandlerentwicklung verwendet |



 

Verwenden Sie die [cokreateinstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -com-Funktion, um entweder eine Klassenfactory zu erstellen. Im folgenden Beispiel wird die Erstellung der WIC Imaging Factory veranschaulicht.


```C++
// Initialize COM
CoInitialize(NULL);

// The factory pointer
IWICImagingFactory *pFactory = NULL;

// Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&pFactory)
);
```



## <a name="imaging-components"></a>Bildverarbeitungskomponenten

Die WIC-APIs stellen verschiedene Arten von Abbild Erstellungs Komponenten bereit. In der folgenden Tabelle werden einige der gängigen WIC-Komponenten beschrieben. Eine vollständige Liste der verfügbaren Komponenten finden Sie unter [WIC-Schnittstellen](-wic-codec-ifaces.md).



| Komponententyp                                                      | BESCHREIBUNG                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**Bitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                             | Stellt eine beschreibbare Darstellung im Arbeitsspeicher einer [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)dar. |
| [**Decoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)                     | Wird zum Decodieren von Bilddaten aus einem Stream in ein Format verwendet, das für die Bildverarbeitung nützlich ist.                    |
| [**ASA**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)                     | Schreibt Bilddaten in einen Stream.                                                                                |
| [**Datenstrom**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)                             | Wird verwendet, um Daten aus einer Datei, einer Netzwerkressource, einem Speicherblock usw. zu lesen und zu schreiben.                      |
| [**Format Konverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)          | Wird verwendet, um ein Pixel Format in ein anderes zu konvertieren.                                                             |
| [**Metadatenabfrage-Reader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) | Wird zum Lesen von Metadaten eines Bilds oder Bilds verwendet.                                                             |
| [**Metadatenabfrage-Writer**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) | Wird verwendet, um Metadaten in einen Bild-oder Bild Rahmen zu schreiben.                                                            |



 

## <a name="see-also"></a>Weitere Informationen

[Referenzen](-wic-codec-reference.md)


[Beispiele und Code Beispiele](-wic-samples.md)


 

 
