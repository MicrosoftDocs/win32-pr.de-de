---
description: Dieses Thema enthält eine Übersicht über die Abfragen der Abfragesprache Abfragen zum Lesen und Schreiben von Metadaten, die von GIF-, PNG-, TIFF-und JPEG-Bildern unterstützt werden
ms.assetid: a6ab1708-dd82-4960-b908-f1daef7374ef
title: Native Imageformat-Metadatenabfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be5e9c0f853e4c5e48fb5eb41f2d2ab27b4f4d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364119"
---
# <a name="native-image-format-metadata-queries"></a>Native Imageformat-Metadatenabfragen

Dieses Thema enthält eine Übersicht über die Abfragen der [Abfragesprache](-wic-codec-metadataquerylanguage.md) Abfragen zum Lesen und Schreiben von Metadaten, die von GIF-, PNG-, TIFF-und JPEG-Bildern unterstützt werden Sie enthält Metadaten, die für jedes Bildformat spezifisch sind, sowie Metadaten, die von mehreren Formaten unterstützt werden.

Dieses Thema enthält folgende Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Richtlinien Ausdruck für Foto-Metadaten](#photo-metadata-policy-expression)
-   [Datei Format spezifische Metadaten](#file-format-specific-metadata)
    -   [GIF-Metadaten](#gif-metadata)
    -   [PNG-Metadaten](#png-metadata)
    -   [TIFF-Metadaten](#tiff-metadata)
    -   [JPEG-Metadaten](#jpeg-metadata)
-   [Datei Format unabhängige Metadaten](#file-format-independent-metadata)
    -   [IFD-Metadaten](#ifd-metadata)
    -   [EXIF-Metadaten](#exif-metadata)
    -   [GPS-Metadaten](#gps-metadata)
    -   [XMP-Metadaten](#xmp-metadata)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Um dieses Thema zu verstehen, sollten Sie sich mit dem Metadatensystem der Windows Imaging Component (WIC) vertraut machen, wie in der [WIC-Metadatenübersicht](-wic-about-metadata.md)beschrieben. Sie sollten auch mit der Abfragesprache vertraut sein, die zum Lesen und Schreiben von Metadaten verwendet wird, wie unter [Übersicht über die metadatenquery-Sprache](-wic-codec-metadataquerylanguage.md)beschrieben.

## <a name="photo-metadata-policy-expression"></a>Richtlinien Ausdruck für Foto-Metadaten

Zusätzlich zur Unterstützung der Metadatenabfragesprache akzeptiert [WIC](-wic-api.md) auch kanonische Eigenschaftsnamen aus dem [Windows-Eigenschaften System](../properties/windows-properties-system.md). WIC unterstützt eine Teilmenge des Windows-Eigenschafts Namespace, der für Bildformate relevant ist, wie in [Photo Metadata Policies](photo-metadata-policies.md)beschrieben. Eine Windows-Eigenschaft, die als WIC-Metadatenabfrage verwendet wird, wird als ein Foto-metadatenrichtlinien-Ausdruck bezeichnet.

Der Photo Metadata Policy-Ausdruck für das EXIF-ausrichtungsflag lautet z. b. wie folgt:

-   [System. Photo. Orientation](-wic-photoprop-system-photo-orientation.md)

Im Allgemeinen werden Richtlinien Ausdrücke für Native Metadatenabfragen für allgemeine bildmetadatenelemente empfohlen, die vom Windows-Eigenschafts Namespace abgedeckt werden. Die Metadatenabfrage-Sprache eignet sich am besten für Fälle, in denen der Zugriff auf eine bestimmte bildmetadatenelemente auf niedriger Ebene erforderlich ist, oder für benutzerdefinierte oder erweiterte Metadatenelemente, die vom Windows-Eigenschaften System nicht unterstützt werden. Weitere Informationen finden Sie unter [Policy Expressions Photo Metadata](-wic-codec-metadataquerylanguage.md).

## <a name="file-format-specific-metadata"></a>Datei Format spezifische Metadaten

Die folgenden Abschnitte enthalten Tabellen, in denen die verfügbaren Metadatenabfragen für jeden Image Dateityp aufgeführt sind. Jede Tabelle weist die folgenden Spalten auf:

-   **Path** : der Abfrage Pfad, der zum Abrufen des Metadatenelements verwendet wird.
-   **Name** : der Name des Metadatenelements.
-   **Type** : der Typ des Metadatenelements, das aus dem Abfrage Pfad abgerufen wird. Metadaten, die von [WIC](-wic-api.md) abgerufen werden, werden in Form von PROPVARIANT zurückgegeben, das den Datentyp mithilfe der VarType-Enumeration meldet.

Die Abfrage Pfade werden von der WIC-metadatenapi verwendet, um auf die eingebetteten Metadaten eines Bilds zuzugreifen. Der folgende Beispielcode veranschaulicht die Verwendung eines [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) , um den IFD-Metadatenblock eines JPEG abzufragen.


```
// Not shown: image decoding 
IWICMetadataQueryReader *pQueryReader = NULL;
IWICMetadataQueryReader *pIFDReader = NULL;

// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

if (SUCCEEDED(hr))
{
    // Get the nested IFD reader.
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pIFDReader);
    }
    PropVariantClear(&value); // Clear value for new query.
}
```



### <a name="gif-metadata"></a>GIF-Metadaten

Das GIF-Bild Format (Graphics Interchange Format) unterstützt sowohl globale als auch auf Frame-Ebene-Metadaten. In den folgenden beiden Abschnitten werden die metadatenabfragepfade bereitgestellt, die für die globalen und auf Frame-Ebene der GIF

> [!Note]  
> Eine vollständige Liste der GIF-Metadaten sowie ausführlichere Informationen finden Sie im [GIF-Standard](https://www.w3.org/Graphics/GIF/spec-gif89a.txt) auf der W3C-Website.

 

### <a name="global-metadata"></a>Globale Metadaten

Die folgende Tabelle enthält die verfügbaren metadatenabfragepfade, die für den Zugriff auf globale GIF-Metadaten verwendet werden können.



| Pfad                                               | Name                       | type                                |
|----------------------------------------------------|----------------------------|-------------------------------------|
| /commentext or/ \[ \* \] commentext Where \* = 0 bis N | Kommentar Erweiterung          | VT \_ Unknown-A Query Reader/Writer |
| /commentext/TextEntry                              |                            | VT \_ LPSTR                           |
| /logscrdesc                                        | Beschreibung des logischen Bildschirms | VT \_ Unknown-A Query Reader/Writer |
| /logscrdesc/Signature                              |                            | VT \_ UI1 \| VT- \_ Vektor               |
| /logscrdesc/Width                                  |                            | VT \_ UI2                             |
| /logscrdesc/Height                                 |                            | VT \_ UI2                             |
| /logscrdesc/GlobalColorTableFlag                   |                            | VT \_ bool                            |
| /logscrdesc/ColorResolution                        |                            | VT \_ UI1                             |
| /logscrdesc/SortFlag                               |                            | VT \_ bool                            |
| /logscrdesc/GlobalColorTableSize                   |                            | VT \_ UI1                             |
| /logscrdesc/BackgroundColorIndex                   |                            | VT \_ UI1                             |
| /logscrdesc/PixelAspectRatio                       |                            | VT \_ UI1                             |
| /appext oder/ \[ \* \] appext \* , wobei = 0 bis N         | Anwendungs Erweiterung      | VT \_ Unknown-A Query Reader/Writer |
| /appext/Application                                |                            | VT \_ UI1 \| VT- \_ Vektor               |
| /appext/Data                                       |                            | VT \_ UI1 \| VT- \_ Vektor               |



 

### <a name="frame-metadata"></a>Frame-Metadaten

In der folgenden Tabelle sind die verfügbaren metadatenabfragepfade enthalten, die für den Zugriff auf GIF-Metadaten auf Frame-Ebene



| Pfad                            | Name                      | type                              |
|---------------------------------|---------------------------|-----------------------------------|
| /grctlext                       | Grafik Steuerelement-Erweiterung | VT \_ Unknown-Abfrage Leser/Writer |
| /grctlext/Disposal              |                           | VT \_ UI1                           |
| /grctlext/UserInputFlag         |                           | VT \_ bool                          |
| /grctlext/TransparencyFlag      |                           | VT \_ bool                          |
| /grctlext/Delay                 |                           | VT \_ UI2                           |
| /grctlext/TransparentColorIndex |                           | VT \_ UI1                           |
| /imgdesc                        | Bild Deskriptor          | VT \_ Unknown-Abfrage Leser/Writer |
| /imgdesc/Left                   |                           | VT \_ UI2                           |
| /imgdesc/Top                    |                           | VT \_ UI2                           |
| /imgdesc/Width                  |                           | VT \_ UI2                           |
| /imgdesc/Height                 |                           | VT \_ UI2                           |
| /imgdesc/LocalColorTableFlag    |                           | VT \_ bool                          |
| /imgdesc/InterlaceFlag          |                           | VT \_ bool                          |
| /imgdesc/SortFlag               |                           | VT \_ bool                          |
| /imgdesc/LocalColorTableSize    |                           | VT \_ UI1                           |



 

### <a name="png-metadata"></a>PNG-Metadaten

Das Bildformat Portable Network Graphics (PNG) unterstützt Metadaten auf Frame-Ebene.

> [!Note]  
> Eine vollständige Liste der PNG-Metadaten sowie ausführlichere Informationen finden Sie im [PNG-Standard](https://www.w3.org/TR/PNG/) auf der W3C-Website.

 

### <a name="frame-metadata"></a>Frame-Metadaten

In der folgenden Tabelle werden die verfügbaren metadatenabfragepfade bereitgestellt, die für den Zugriff auf die PNG-Metadaten von Frame



| Pfad                                                   | Name             | type                                      |
|--------------------------------------------------------|------------------|-------------------------------------------|
| /Text oder/ \[ \* \] Text Where \* = 0 bis N                 | Textteile       | VT \_ Unknown-Text Abfrage Leser/Writer    |
| /Text/{Str = \* } Where \* = identifizierendes Schlüsselwort für Text |                  | VT \_ LPSTR                                 |
| /gAMA                                                  | Gama-Block       | VT \_ Unknown-Gama Abfrage Leser/Writer    |
| /gAMA/ImageGamma                                       |                  | VT \_ UI4                                   |
| /iTXt oder/ \[ \* \] iTXt \* , wobei = 0 bis N                 | IText-Block      | VT \_ Unknown-iTXt-Abfrage Leser/Writer    |
| /iTXt/Keyword                                          |                  | VT \_ LPSTR                                 |
| /iTXt/CompressionFlag                                  |                  | VT \_ UI1                                   |
| /iTXt/LanguageTag                                      |                  | LPSTR                                     |
| /iTXt/TranslatedKeyword                                |                  | LPWSTR                                    |
| /iTXt/TextEntry                                        |                  | LPWSTR                                    |
| /cHRM                                                  | HRM-Block        | VT \_ Unknown-chrm-Abfrage Leser/Writer    |
| /cHRM/WhitePointX                                      |                  | VT \_ UI4                                   |
| /cHRM/WhitePointY                                      |                  | VT \_ UI4                                   |
| /cHRM/RedX                                             |                  | VT \_ UI4                                   |
| /cHRM/RedY                                             |                  | VT \_ UI4                                   |
| /cHRM/GreenX                                           |                  | VT \_ UI4                                   |
| /cHRM/GreenY                                           |                  | VT \_ UI4                                   |
| /cHRM/BlueX                                            |                  | VT \_ UI4                                   |
| /cHRM/BlueY                                            |                  | VT \_ UI4                                   |
| /sRGB                                                  | sRGB-Chuck       | VT \_ Unknown-sRGB-Abfrage Leser/Writer    |
| /sRGB/RenderingIntent                                  |                  | VT \_ UI1                                   |
| /Time                                                  | Zeit Block       | VT \_ unbekannter Zeit Abfrage Leser/Writer    |
| /tIME/Year                                             |                  | VT \_ UI2                                   |
| /tIME/Month                                            |                  | VT \_ UI1                                   |
| /tIME/Day                                              |                  | VT \_ UI1                                   |
| /tIME/Hour                                             |                  | VT \_ UI1                                   |
| /tIME/Minute                                           |                  | VT \_ UI1                                   |
| /tIME/Second                                           |                  | VT \_ UI1                                   |
| /bKGD                                                  | Hintergrund Segment | VT \_ Unknown-bkgb-Abfrage Leser/Writer    |
| /bKGD/BackgroundColor                                  |                  | VT- \_ UI1, VT \_ UI2 oder VT \_ UI2 VT- \| \_ Vektor |
| /hIST                                                  | Hist-Block       | VT \_ Unknown-Hist-Abfrage Leser/Writer    |
| /hIST/Frequencies                                      |                  | VT \_ Vector \| VT \_ UI2                     |
| /iCCP                                                  | ICCP-Block       | VT \_ Unknown-ICCP-Abfrage Leser/Writer    |
| /iCCP/ProfileName                                      |                  | VT \_ LPSTR                                 |
| /iCCP/ProfileData                                      |                  | VT \_ Vector \| VT \_ UI1                     |



 

### <a name="tiff-metadata"></a>TIFF-Metadaten

Das TIFF-Bild Format (Tagged Image File Format) unterstützt Metadaten auf Frame-Ebene.

> [!Note]  
> Eine vollständige Liste der TIFF-Metadaten sowie ausführlichere Informationen finden Sie [im TIFF-Standard](https://www.adobe.io/content/dam/udp/en/open/standards/tiff/TIFF6.pdf).

 

### <a name="frame-metadata"></a>Frame-Metadaten

In der folgenden Tabelle finden Sie die verfügbaren metadatenabfragepfade, die für den Zugriff auf TIFF-Metadaten auf Frame-Ebene



| Pfad                                          | Name            | type                                |
|-----------------------------------------------|-----------------|-------------------------------------|
| /ifd                                          | 0 IFD           | VT \_ Unknown-A Query Reader/Writer |
| /IFD/{ushort = \* } Where \* = 0 bis 65535        | IFD-Eintrag nach ID | Variable                            |
| /IFD/Thumb oder/IFD/{ushort = 330}               | Miniaturansicht-IFD   | VT \_ Unknown-A Query Reader/Writer |
| /IFD/XMP oder/IFD/{ushort = 700}                 | XMP             | VT \_ Unknown-A Query Reader/Writer |
| /IFD/EXIF oder/IFD/{ushort = 34665}              | EXIF            | VT \_ Unknown-A Query Reader/Writer |
| /IFD/GPS oder/IFD/{ushort = 34853}               | GPS             | VT \_ Unknown-A Query Reader/Writer |
| /IFD/EXIF/Interop oder/IFD/EXIF/{ushort = 40965} | Interop         | VT \_ Unknown-A Query Reader/Writer |
| /IFD/IPTC oder/IFD/{ushort = 33723}              | IPTC            | VT \_ Unknown-A Query Reader/Writer |
| /IFD/IPTC/{Str = \* } Where \* = IPTC-Schlüsselwort    | IPTC-Eintrag      | Variable                            |
| /ifd/irb/8bimiptc/iptc                        | IPTC            | VT \_ Unknown-A Query Reader/Writer |
| /IFD/IRB/8bimiptc/IPTC/{Str = \* }               | IPTC-Eintrag      | Variable                            |



 

### <a name="jpeg-metadata"></a>JPEG-Metadaten

Das JPEG-Bildformat unterstützt Metadaten auf Frame-Ebene.

> [!Note]  
> Eine vollständige Liste der JPEG-Metadaten sowie ausführlichere Informationen finden Sie unter dem [EXIF JPEG-Standard](http://www.cipa.jp/std/documents/e/DC-008-2010_E.pdf).

 

### <a name="frame-metadata"></a>Frame-Metadaten

In der folgenden Tabelle werden die verfügbaren metadatenabfragepfade bereitgestellt, die für den Zugriff auf die JPEG-Metadaten auf Frame



| Pfad                                                               | Name                 | type                                          |
|--------------------------------------------------------------------|----------------------|-----------------------------------------------|
| /app0                                                              | App0                 | VT \_ Unknown-App0 Query Reader/Writer        |
| /APP0/{ushort = 0}                                                   | Version              | VT \_ UI2                                       |
| /APP0/{ushort = 1}                                                   | Einheiten                | VT \_ UI1                                       |
| /APP0/{ushort = 2}                                                   | DpiX                 | VT \_ UI2                                       |
| /APP0/{ushort = 3}                                                   | DpiY                 | VT \_ UI2                                       |
| /APP0/{ushort = 4}                                                   | Xminiatur           | VT \_ UI1                                       |
| /APP0/{ushort = 5}                                                   | Yminiatur           | VT \_ UI1                                       |
| /APP0/{ushort = 6}                                                   | Thumbnaildata        | VT- \_ BLOB                                      |
| /App1                                                              | App1                 | VT \_ Unknown-App1 Query Reader/Writer        |
| /App1/IFD oder/App1/{ushort = 0}                                     | 0 IFD                | VT \_ Unknown-IFD Query Reader/Writer         |
| /App1/IFD/EXIF oder/App1/IFD/{ushort = 34665}                         | EXIF IFD             | VT \_ Unknown – EXIF Query Reader/Writer        |
| /App1/Thumb oder/App1/{ushort = 1}                                   | Miniaturansicht-IFD        | VT \_ Unknown-subifd-Abfrage Leser/Writer      |
| /app13                                                             | App13                | VT \_ Unknown-App13 Query Reader/Writer       |
| /app13/IRB oder/app13/{ushort = 0}                                    | UNB                  | VT \_ Unknown-UNB-Abfrage Leser/Writer         |
| /app13/IRB/{ULONGLONG = \* } Where \* = UNB Identifier (siehe "unb-Spezifikation") | UNB-Eintrag            | VT \_ unbekannt-unbekannter Abfrage Leser/Writer     |
| /app13/IRB/{ULONGLONG = \* }/{}                                       | Inhalt des UNB-Eintrags   | VT- \_ BLOB                                      |
| /app13/IRB/8bimiptc oder/app13/IRB/{ULONGLONG = 61857348781060}       | 8bimiptc             | VT \_ Unknown-8bimiptc Query Reader/Writer    |
| /app13/irb/8bimiptc/iptc                                           | IPTC                 | VT \_ Unknown-IPTC-Abfrage Leser/Writer        |
| /app13/IRB/8bimiptc/IPTC/{Str = \* }                                  | IPTC-Eintrag           | Variable                                      |
| /app13/IRB/8bimResInfo oder/app13/IRB/{ULONGLONG = 61857348781037}    | 8bim-Auflösungsinformationen | VT \_ Unknown-Abfrage Leser/Writer             |
| /app13/irb/8bimResInfo/PString                                     |                      | VT \_ LPSTR                                     |
| /app13/irb/8bimResInfo/HResolution                                 |                      | VT \_ UI4                                       |
| /app13/irb/8bimResInfo/VResolution                                 |                      | VT \_ UI4                                       |
| /app13/irb/8bimResInfo/WidthUnit                                   |                      | VT \_ UI2                                       |
| /app13/irb/8bimResInfo/HeightUnit                                  |                      | VT \_ UI2                                       |
| /app13/irb/8bimResInfo/HResolutionUnit                             |                      | VT \_ UI2                                       |
| /app13/irb/8bimResInfo/VResolutionUnit                             |                      | VT \_ UI2                                       |
| /com                                                               | JPEG-Kommentar         | VT \_ Unknown-Kommentar Abfrage Leser/Writer     |
| /com/TextEntry                                                     |                      | LPSTR                                         |
| /luminance                                                         | Luminance            | VT \_ Unknown-Abfrage Leser/Writer von Luminance   |
| /luminance/TableEntry                                              |                      | VT \_ UI1 \| VT- \_ Vektor                         |
| /chrominance                                                       | Chrominance          | VT \_ Unknown-Chrominance Query Reader/Writer |
| /chrominance/TableEntry                                            |                      | VT \_ UI1 \| VT- \_ Vektor                         |
| /xmp                                                               | XMP                  | VT \_ Unknown-XMP-Abfrage Leser/Writer         |



 

## <a name="file-format-independent-metadata"></a>Datei Format unabhängige Metadaten

Die folgenden Abschnitte enthalten Informationen zu Metadatenformaten, die von mehreren Bildformaten unterstützt werden. Jede Tabelle weist die folgenden Spalten auf:

-   **Relativer Pfad** : der Abfrage Pfad, der zum Abrufen des Metadatenelements relativ zum Metadatenblock verwendet wird.
-   **Name** : der Name des Metadatenelements.
-   **Type** : der Typ des Metadatenelements, das aus dem Abfrage Pfad abgerufen wird. Metadaten, die von [WIC](-wic-api.md) abgerufen werden, werden in Form von PROPVARIANT zurückgegeben, das den Datentyp mithilfe der VarType-Enumeration meldet.

> [!Note]  
> In den folgenden Tabellen wird nur der relative Pfad für den Zugriff auf ein Metadatenelement innerhalb des jeweiligen metadatenformats bereitgestellt. Um die voll qualifizierte Metadatenabfrage zu erhalten, fügen Sie diesen relativen Pfad an die metadatenblockabfrage für das jeweilige Metadatenformat an.

 

Um z. b. auf das ausrichtungsflag in einer JPEG-Datei zuzugreifen, verwenden [Sie den folgenden](-wic-photoprop-system-photo-orientation.md) Ausdruck:

-   /App1/IFD/{ushort = 274}

Verwenden Sie in einer TIFF-Datei den folgenden Ausdruck:

-   /IFD/{ushort = 274}

Beachten Sie in diesem Beispiel, dass unterschiedliche Bildformate einen bestimmten Metadatenblock unterschiedlich speichern können, sodass die voll qualifizierte Metadatenabfrage für den Zugriff auf ein bestimmtes Metadatenelement möglicherweise Bildformat spezifisch ist. In der Tabelle jedes Formats finden Sie die entsprechende Metadatenabfrage für den Zugriff auf einen bestimmten Metadatenblock.

### <a name="ifd-metadata"></a>IFD-Metadaten

Ein IFD-oder Image-Datei Verzeichnis ist eine im TIFF-Standard definierte Datenstruktur, die Bild Metadaten enthalten kann. Alle Metadatenelemente werden mithilfe eines Tags vom Typ ushort identifiziert. JPEG, TIFF und JPEG-XR unterstützen IFD-Metadaten. Drittanbieter Formate, wie z. b. einige Kamera Rohformate, unterstützen möglicherweise auch IFD-Metadaten.

In der folgenden Tabelle finden Sie relative Metadaten-Abfrage Pfade für den Zugriff auf einige häufig verwendete IFD-Metadatenelemente. Die IFD-Datenstruktur ermöglicht die Erweiterbarkeit von Drittanbietern, und diese Tabelle ist keine vollständige Liste. Weitere Informationen finden Sie im TIFF-Standard.

> [!Note]  
> Obwohl JPEG und andere Formate die IFD-Datenstruktur unterstützen, verwenden Sie möglicherweise nicht alle Metadatenelemente, die Sie definiert. Weitere Informationen finden Sie in den einzelnen Formaten.

 

> [!Note]  
> Bestimmte Metadatenelemente in der Tabelle erfordern zusätzliche Interpretation oder Informationen, um ordnungsgemäß zu verwenden. Weitere Informationen hierzu finden Sie im TIFF-Standard. Das Metadatenelement " [photomedimensioncinterpretation](-wic-photoprop-system-photo-photometricinterpretation.md) " gibt beispielsweise eine PROPVARIANT vom Typ "VT UI2" zurück \_ . Gemäß dem TIFF-Standard wird es jedoch als Enumeration interpretiert. Weitere Informationen finden Sie im TIFF-Standard.

 



| Relativer Pfad   | Name                      | type                                           |
|-----------------|---------------------------|------------------------------------------------|
| /{ushort = 256}   | ImageWidth                | VT \_ UI2 oder VT \_ UI4                             |
| /{ushort = 257}   | ImageLength               | VT \_ UI2 oder VT \_ UI4                             |
| /{ushort = 258}   | BitsPerSample             | VT \_ UI2                                        |
| /{ushort = 259}   | Komprimierung               | VT \_ UI2                                        |
| /{ushort = 262}   | Photomezcinterpretation | VT \_ UI2                                        |
| /{ushort = 274}   | Orientation               | VT \_ UI2                                        |
| /{ushort = 277}   | Samplesperpixel           | VT \_ UI2                                        |
| /{ushort = 284}   | Planarconfiguration       | VT \_ UI2                                        |
| /{ushort = 530}   | Ycbcrsubsampling          | VT \_ Vector \| VT \_ UI2                          |
| /{ushort = 531}   | Ycbcrpositionierung          | VT \_ UI2                                        |
| /{ushort = 282}   | XResolution               | VT \_ UI8                                        |
| /{ushort = 283}   | YResolution               | VT \_ UI8                                        |
| /{ushort = 296}   | ResolutionUnit            | VT \_ UI2                                        |
| /{ushort = 306}   | Datetime                  | VT \_ LPSTR                                      |
| /{ushort = 270}   | ImageDescription          | VT \_ LPSTR                                      |
| /{ushort = 271}   | Make                      | VT \_ LPSTR                                      |
| /{ushort = 272}   | Modell                     | VT \_ LPSTR                                      |
| /{ushort = 305}   | Software                  | VT \_ LPSTR                                      |
| /{ushort = 315}   | Interpret                    | VT \_ LPSTR                                      |
| /{ushort = 33432} | Copyright                 | VT \_ LPSTR                                      |
| /{ushort = 338}   | Extrasamples              | VT \_ UI2                                        |
| /{ushort = 254}   | Newsubfiletype            | VT \_ UI4                                        |
| /{ushort = 278}   | Rowsperstrip              | VT \_ UI2 oder VT \_ UI4                             |
| /{ushort = 279}   | Stripbytecounts           | VT \_ Vector \| VT \_ UI2 oder VT \_ Vector \| VT \_ UI4 |
| /{ushort = 273}   | Stripoffsets              | VT \_ Vector \| VT \_ UI2 oder VT \_ Vector \| VT \_ UI4 |



 

### <a name="exif-metadata"></a>EXIF-Metadaten

EXIF-Metadaten werden als Teil der EXIF JPEG-Spezifikation definiert. Die Metadaten von EXIF basieren auf der IFD-Datenstruktur, die im TIFF-Standard definiert ist, und stellen zusätzliche Attribute bereit, wie z. b. Informationen zu den Geräten und zum Erstellen des Bilds verwendete Foto Attribute. Alle Metadatenelemente werden mithilfe eines Tags vom Typ ushort identifiziert. JPEG, TIFF und JPEG-XR unterstützen EXIF-Metadaten. Drittanbieter Formate, wie z. b. einige Kamera Rohformate, unterstützen möglicherweise auch EXIF-Metadaten.

Die folgende Tabelle enthält relative metadatenabfragepfade für den Zugriff auf einige häufig verwendete EXIF-Metadatenelemente. Die EXIF-Datenstruktur ermöglicht die Erweiterbarkeit von Drittanbietern, und diese Tabelle ist keine vollständige Liste. Weitere Informationen finden Sie im EXIF-Standard.

> [!Note]  
> Viele EXIF-Metadatenelemente werden im EXIF-Standard mit dem Typ "rational" oder "srational" definiert. Ein "rational" besteht aus einem Zähler und einem Nenner, bei denen es sich bei beiden um 32-Bit-Ganzzahlen ohne Vorzeichen handelt. Der Zähler ist in den hohen 32 Bits und der Nenner in den unteren 32 Bits enthalten. In [WIC](-wic-api.md)werden diese als PROPVARIANT mit dem Typ "VT UI8" \_ bzw. "VT I8" zurückgegeben \_ . der tatsächliche Wert wird als "ularge \_ Integer" oder "Large Integer" gespeichert \_ . Um auf den Zähler und Nenner zuzugreifen, lesen Sie die Elemente highpart und LowPart des Werts ularge \_ Integer oder Large \_ Integer.

 

> [!Note]  
> Bestimmte Metadatenelemente in der folgenden Tabelle erfordern zusätzliche Interpretation oder Informationen, um ordnungsgemäß zu verwenden. Das [colorspace](-wic-photoprop-system-image-colorspace.md) -Metadatenelement gibt z. b. eine PROPVARIANT vom Typ VT \_ UI2 zurück. Gemäß dem EXIF-Standard wird es jedoch als Enumeration interpretiert. Weitere Informationen finden Sie im EXIF-Standard.

 



| Relativer Pfad   | Name                      | type                  |
|-----------------|---------------------------|-----------------------|
| /{ushort = 36864} | EXIF-Version               | VT- \_ BLOB              |
| /{ushort = 40960} | Flashpixversion           | VT- \_ BLOB              |
| /{ushort = 40961} | Colorspace                | VT \_ UI2               |
| /{ushort = 40962} | Pixelxdimension           | VT \_ UI2 oder VT \_ UI4    |
| /{ushort = 40963} | Pixelydimension           | VT \_ UI2 oder VT \_ UI4    |
| /{ushort = 37500} | Makernote                 | VT- \_ BLOB              |
| /{ushort = 37510} | UserComment               | VT \_ LPWSTR            |
| /{ushort = 36867} | DateTimeOriginal          | VT \_ LPSTR             |
| /{ushort = 36868} | Datetimedigisierte         | VT \_ LPSTR             |
| /{ushort = 42016} | ImageUniqueID             | VT \_ LPSTR             |
| /{ushort = 42032} | Camerabesitzname           | VT \_ LPSTR             |
| /{ushort = 42033} | Bodyserialnumber          | VT \_ LPSTR             |
| /{ushort = 42034} | Lensspecification         | VT \_ Vector \| VT \_ UI8 |
| /{ushort = 42035} | Lensmake                  | VT \_ LPSTR             |
| /{ushort = 42036} | Lensmodel                 | VT \_ LPSTR             |
| /{ushort = 42037} | Lensserialnumber          | VT \_ LPSTR             |
| /{ushort = 33434} | ExposureTime              | VT \_ UI8               |
| /{ushort = 33437} | F-Nummer                   | VT \_ UI8               |
| /{ushort = 34850} | ExposureProgram           | VT \_ UI2               |
| /{ushort = 34852} | Spectralsensitivität       | VT \_ LPSTR             |
| /{ushort = 34855} | Photographicsensitivität   | VT \_ Vector \| VT \_ UI2 |
| /{ushort = 34856} | Oecf                      | VT- \_ BLOB              |
| /{ushort = 34864} | Sensitivitytype           | VT \_ UI2               |
| /{ushort = 34865} | Standardoutputsensitivität | VT \_ UI4               |
| /{ushort = 34866} | Empfehlungs Element Empfehlungs-Index  | VT \_ UI4               |
| /{ushort = 34867} | Isospeed                  | VT \_ UI4               |
| /{ushort = 34868} | Isospeedlatitubinyyy       | VT \_ UI4               |
| /{ushort = 34869} | Isospeedlatitudecoz       | VT \_ UI4               |
| /{ushort = 37377} | Shutterspeedvalue         | VT \_ I8                |
| /{ushort = 37378} | Aperturevalue             | VT \_ UI8               |
| /{ushort = 37379} | Brightnessvalue           | VT \_ I8                |
| /{ushort = 37380} | ExposureBiasValue         | VT \_ I8                |
| /{ushort = 37381} | MaxApertureValue          | VT \_ UI8               |
| /{ushort = 37382} | Subjetdistance           | VT \_ UI8               |
| /{ushort = 37383} | Meteringmode              | VT \_ UI2               |
| /{ushort = 37384} | LightSource               | VT \_ UI2               |
| /{ushort = 37385} | Blinken                     | VT \_ UI2               |
| /{ushort = 37386} | FocalLength               | VT \_ UI8               |
| /{ushort = 37396} | Subjetarea               | VT \_ Vector \| VT \_ UI2 |
| /{ushort = 41483} | Flash Energie               | VT \_ UI8               |
| /{ushort = 41484} | Spatialfrequendcyresponse  | VT- \_ BLOB              |
| /{ushort = 41486} | Focalplanexresolution     | VT \_ UI8               |
| /{ushort = 41487} | Focalplaneyresolution     | VT \_ UI8               |
| /{ushort = 41488} | Focalplaneresolutionunit  | VT \_ UI2               |
| /{ushort = 41492} | Subjetlocation           | VT \_ Vector \| VT \_ UI2 |
| /{ushort = 41493} | Exposureindex             | VT \_ UI8               |
| /{ushort = 41495} | Sensingmethod             | VT \_ UI2               |
| /{ushort = 41728} | FileSource                | VT- \_ BLOB              |
| /{ushort = 41729} | SceneType                 | VT- \_ BLOB              |
| /{ushort = 41730} | Cfapattern                | VT- \_ BLOB              |
| /{ushort = 41985} | Customgerendert            | VT \_ UI2               |
| /{ushort = 41986} | Exposuremode              | VT \_ UI2               |
| /{ushort = 41987} | WhiteBalance              | VT \_ UI2               |
| /{ushort = 41988} | DigitalZoomRatio          | VT \_ UI8               |
| /{ushort = 41989} | FocalLengthIn35mmFilm     | VT \_ UI2               |
| /{ushort = 41990} | Scenecapturetype          | VT \_ UI2               |
| /{ushort = 41991} | Steuerelement               | VT \_ UI8               |
| /{ushort = 41992} | Vergleichen Sie                  | VT \_ UI2               |
| /{ushort = 41993} | Sättigung                | VT \_ UI2               |
| /{ushort = 41994} | Schärfe                 | VT \_ UI2               |
| /{ushort = 41995} | Geräte Einstellungs Beschreibung  | VT- \_ BLOB              |
| /{ushort = 41996} | Subjetdistancerange      | VT \_ UI2               |



 

### <a name="gps-metadata"></a>GPS-Metadaten

GPS-Metadaten enthalten geolozierungsinformationen und werden als Teil der EXIF JPEG-Spezifikation definiert. Alle Metadatenelemente werden mithilfe eines Tags vom Typ ushort identifiziert. JPEG, TIFF und JPEG-XR unterstützen GPS-Metadaten. Drittanbieter Formate, wie z. b. einige Kamera Rohformate, unterstützen möglicherweise auch GPS-Metadaten.

In der folgenden Tabelle finden Sie relative Metadaten-Abfrage Pfade für den Zugriff auf einige häufig verwendete GPS-Metadatenelemente. Diese Tabelle ist keine vollständige Liste. Weitere Informationen finden Sie im EXIF-Standard.

> [!Note]  
> Viele GPS-Metadatenelemente werden im EXIF-Standard als Typ "rational" definiert. Ein "rational" besteht aus einem Zähler und einem Nenner, bei denen es sich bei beiden um 32-Bit-Ganzzahlen ohne Vorzeichen handelt. Der Zähler ist in den hohen 32 Bits und der Nenner in den unteren 32 Bits enthalten. In [WIC](-wic-api.md)werden diese als PROPVARIANT mit dem Typ VT UI8 zurückgegeben \_ . Der tatsächliche Wert wird als ularge \_ Integer gespeichert. Um auf den Zähler und den Nenner zuzugreifen, lesen Sie die highpart-und LowPart-Member des ularge- \_ ganzzahligen Werts.

 

> [!Note]  
> Bestimmte Metadatenelemente in der Tabelle erfordern zusätzliche Interpretation oder Informationen, um ordnungsgemäß zu verwenden. Das gpslatituderef-Metadatenelement gibt z. b. eine PROPVARIANT vom Typ VT \_ LPSTR zurück. Gemäß dem EXIF-Standard ist diese Zeichenfolge "N" oder "S", die den Breitengrad "Nord" oder "Süd" darstellt. Weitere Informationen finden Sie im EXIF-Standard.

 



| Relativer Pfad | Name            | type                                          |
|---------------|-----------------|-----------------------------------------------|
| {ushort = 0}    | Gpsversionid    | VT \_ Vector \| VT \_ UI1                         |
| {ushort = 1}    | Gpslatituderef  | VT \_ LPSTR                                     |
| {ushort = 2}    | Gpslatitude     | VT \_ Vector \| VT \_ UI8                         |
| {ushort = 3}    | Gpslängs | VT \_ LPSTR                                     |
| {ushort = 4}    | Gpslängen Grad    | {ushort = 4} Gpslängen Grade VT \_ Vector \| VT \_ UI8 |
| {ushort = 5}    | Gpsaltituderef  | VT \_ UI1                                       |
| {ushort = 6}    | Gpsaltitude     | VT \_ UI8                                       |
| {ushort = 7}    | Gpstimestamp    | VT \_ Vector \| VT \_ UI8                         |
| {ushort = 8}    | Gpssatellites   | VT \_ LPSTR                                     |
| {ushort = 9}    | Gpsstatus       | VT \_ LPSTR                                     |
| {ushort = 10}   | Gpsmessremode  | VT \_ LPSTR                                     |
| {ushort = 11}   | Gpsdop          | VT \_ UI8                                       |
| {ushort = 12}   | Gpsspeedref     | VT \_ LPSTR                                     |
| {ushort = 13}   | Gpsspeed        | VT \_ UI8                                       |
| {ushort = 14}   | Gpstrackref     | VT \_ LPSTR                                     |
| {ushort = 15}   | Gpstrack        | VT \_ UI8                                       |



 

### <a name="xmp-metadata"></a>XMP-Metadaten

XMP ist ein XML-basierter erweiterbarer Metadatenstandard. Metadatenelemente können hierarchisch sein und komplexe Datenstrukturen enthalten. JPEG, TIFF und JPEG-XR unterstützen XMP-Metadaten. Drittanbieter Formate, wie z. b. einige Kamera Rohformate, unterstützen möglicherweise auch XMP-Metadaten.

Der XMP-Standard kann abgerufen werden aus: <https://www.adobe.com/devnet/xmp.html> .

XMP und ermöglicht es Drittanbietern, ihre eigenen Schemas oder Namespaces zu veröffentlichen, sodass Sie neue Metadatenelemente definieren können, ohne den XMP-Standard ändern zu müssen. Ein XMP-Schema wird eindeutig durch eine URL identifiziert, aber WIC stellt eine Reihe von benutzerfreundlichen [bezeichlen](-wic-api.md) für bekannte Schemas bereit.

XMP-Metadatenelemente werden durch einen Zeichen folgen Namen und einen Schema Bezeichner identifiziert. Als bewährte Vorgehensweise sollte jede XMP-Metadatenabfrage sowohl das Schema als auch den Namen angeben. Wenn die Schema-ID fehlt, versucht JPEG, den Metadatennamen für alle Namespaces abzugleichen, die im XMP-Metadatenpaket vorhanden sind.

Um beispielsweise die Bewertungs Eigenschaft wie im XMP-Schema in einem JPEG-Bild definiert zu erhalten, verwenden Sie die folgende Abfrage:

-   /XMP/{WSTR =https://ns.adobe.com/xap/1.0/}:Rating

Der erste Teil, "/XMP", Ruft den XMP-metadatenleser/-Writer für das Bild ab. " https://ns.adobe.com/xap/1.0/ " ist die URL des XMP-Schemas, wie im XMP-Standard definiert. Die URL wird in einen Daten Ausdruck eingeschlossen, um die Verwendung von Zeichen wie einem Schrägstrich (/) zu ermöglichen. Zum Schluss ist "Rating" der tatsächliche metadatenelementname, wie durch das XMP-Schema definiert, und er wird durch einen Doppelpunkt (:)) vom Schema Bezeichner getrennt.

In diesem Beispiel stellt WIC einen benutzerfreundlichen Bezeichner für das XMP-Schema bereit, das anstelle der vollständigen URL verwendet werden kann. Die vorherige Abfrage kann daher wie folgt umgeschrieben werden:

-   /XMP/XMP: Bewertung

[WIC](-wic-api.md) stellt benutzerfreundliche Schema Präfixe für die folgenden häufig verwendeten Schemas bereit:



| Schema Präfix  | Schema-URL                                        | Mit Standard verknüpfen                                         |
|----------------|---------------------------------------------------|----------------------------------------------------------|
| RDF            | https://www.w3.org/1999/02/22-rdf-syntax-ns\#      | <https://www.w3.org/TR/REC-rdf-syntax/>                   |
| dc             | https://purl.org/dc/elements/1.1/                  | <https://www.adobe.com/devnet/xmp.html>                   |
| XMP            | https://ns.adobe.com/xap/1.0/                      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpidq         | https://ns.adobe.com/xmp/Identifier/qual/1.0/      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmprights      | https://ns.adobe.com/xap/1.0/rights/               | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpmm          | https://ns.adobe.com/xap/1.0/mm/                   | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpbj          | https://ns.adobe.com/xap/1.0/bj/                   | <https://www.adobe.com/devnet/xmp.html>                   |
| xmptpg         | https://ns.adobe.com/xap/1.0/t/pg/                 | <https://www.adobe.com/devnet/xmp.html>                   |
| pdf            | https://ns.adobe.com/pdf/1.3/                      | <https://www.adobe.com/devnet/xmp.html>                   |
| Shop      | https://ns.adobe.com/photoshop/1.0/                | <https://www.adobe.com/devnet/xmp.html>                   |
| tiff           | https://ns.adobe.com/tiff/1.0/                     | <https://www.adobe.com/devnet/xmp.html>                   |
| EXIF           | https://ns.adobe.com/exif/1.0/                     | <https://www.adobe.com/devnet/xmp.html>                   |
| stdim          | https://ns.adobe.com/xap/1.0/sType/Dimensions\#    | <https://www.adobe.com/devnet/xmp.html>                   |
| xapgimg        | https://ns.adobe.com/xap/1.0/g/img/                | <https://www.adobe.com/devnet/xmp.html>                   |
| stevt          | https://ns.adobe.com/xap/1.0/sType/ResourceEvent\# | <https://www.adobe.com/devnet/xmp.html>                   |
| stref          | https://ns.adobe.com/xap/1.0/sType/ResourceRef\#   | <https://www.adobe.com/devnet/xmp.html>                   |
| stver          | https://ns.adobe.com/xap/1.0/sType/Version\#       | <https://www.adobe.com/devnet/xmp.html>                   |
| stjob          | https://ns.adobe.com/xap/1.0/sType/Job\#           | <https://www.adobe.com/devnet/xmp.html>                   |
| Boda            | https://ns.adobe.com/exif/1.0/aux/                 | <https://www.adobe.com/devnet/xmp.html>                   |
| Renn            | https://ns.adobe.com/camera-raw-settings/1.0/      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpdm          | https://ns.adobe.com/xmp/1.0/DynamicMedia/         | <https://www.adobe.com/devnet/xmp.html>                   |
| Iptc4xmpCore   | https://iptc.org/std/Iptc4xmpCore/1.0/xmlns/       | <https://www.iptc.org/cms/site/index.html?channel=CH0099> |
| Microsoftphoto | https://ns.microsoft.com/photo/1.0/                | [Übersicht über Personen Tags](-wic-people-tagging.md)       |
| MP             | https://ns.microsoft.com/photo/1.2/                | [Übersicht über Personen Tags](-wic-people-tagging.md)       |
| MPRI           | https://ns.microsoft.com/photo/1.2/t/RegionInfo\#  | [Übersicht über Personen Tags](-wic-people-tagging.md)       |
| Mpreg          | https://ns.microsoft.com/photo/1.2/t/Region\#      | [Übersicht über Personen Tags](-wic-people-tagging.md)       |



 

Wenn für ein bestimmtes Schema kein angezeigter Schema Präfix vorhanden ist, z. b. Wenn ein Bild XMP-Metadaten mit einem benutzerdefinierten Drittanbieter Schema enthält, sollte die Metadatenabfrage die vollständige Schema-URL verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über WIC-Metadaten](-wic-about-metadata.md)
</dt> <dt>

[Übersicht über die Metadaten-Abfragesprache](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Übersicht über die metadatenerweiterbarkeit](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Gewusst wie: Erneutes Codieren eines JPEG-Bilds mit Metadaten](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
