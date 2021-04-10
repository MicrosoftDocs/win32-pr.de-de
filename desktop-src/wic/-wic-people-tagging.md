---
description: Dieses Thema enthält eine Einführung in das neue Extensible Metadata Platform (XMP)-Schema und die Windows 7 Photo-Eigenschaft System. Photo. People Ames, die das Markieren von Einzelpersonen in einem digitalen Foto ermöglicht.
ms.assetid: 557c3e9a-1756-4abb-8465-b12195ecbc91
title: Übersicht über Personen Tags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64f2080e51d4d340474e0610fcce9512fc72429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131893"
---
# <a name="people-tagging-overview"></a>Übersicht über Personen Tags

Dieses Thema enthält eine Einführung in das neue Extensible Metadata Platform (XMP)-Schema und die Windows 7 Photo-Eigenschaft [System. Photo. People Ames](../properties/props-system-photo-peoplenames.md) , die das Markieren von Einzelpersonen in einem digitalen Foto ermöglicht. In diesem Thema wird auch erläutert, wie Sie die WIC-API (Windows Imaging Component) zum Lesen und Schreiben der Metadaten verwenden, die für das Tagging von Personen benötigt werden.

Dieses Thema enthält folgende Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Introduction (Einführung)](#introduction)
-   [Personen Tags](#people-tagging-overview)
    -   [Personennamen](#people-names)
    -   [Menschen Rechtecke](#people-rectangles)
-   [Schema Verweis](#schema-reference)
    -   [Microsoft-Foto 1,2-Schema](#microsoft-photo-12-schema)
    -   [Microsoft Photo RegionInfo-Schema](#microsoft-photo-regioninfo-schema)
    -   [Microsoft-Foto Regions Schema](#microsoft-photo-regioninfo-schema)
    -   [Beispiel Metadaten](#sample-metadata)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Um dieses Thema zu verstehen, sollten Sie mit den WIC-decoderschnittstellen und den zugehörigen COM-Komponenten (Related Component Object Model) vertraut sein, wie in der [Übersicht über Windows Imaging Component](-wic-about-windows-imaging-codec.md)beschrieben. Außerdem ist es hilfreich, eine allgemeine Vertrautheit mit der Erstellung von Metadaten zu erhalten, insbesondere mit XMP.

## <a name="introduction"></a>Einführung

Microsoft hat ein neues XMP-Schema zum Markieren von Personen in einem digitalen Image erstellt. Mit diesem Schema können Anwendungen die Namen und Speicherorte von Personen, die sich im Image befinden, als Metadaten innerhalb des Bilds speichern. Zusätzlich zum neuen Schema ist die neue Photo-Eigenschaft [System. Photo. People Ames](../properties/props-system-photo-peoplenames.md) in Windows 7 verfügbar. Diese neue Eigenschaft ermöglicht es Anwendungen, die in den Bild Metadaten gespeicherten Namen der einzelnen Personen zu lesen. WIC nutzt diese neuen Features, indem es Anwendungen ermöglicht, Personen zu lesen und zu schreiben, die Metadaten für digitale Fotos markieren.

## <a name="people-tagging"></a>Personen Tags

WIC bietet Anwendungsentwicklern com-Komponenten, die Bilddaten und Bild Metadaten lesen. Zum Lesen und Schreiben von Metadaten, wie z. b. das neue Feature "People Tagging", stellt WIC die Schnittstellen [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) und [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) bereit. Diese Schnittstellen ermöglichen es Anwendungen, die [Metadaten-Abfragesprache](-wic-codec-metadataquerylanguage.md) zu verwenden, um Metadaten in die einzelnen Frames eines Bilds zu schreiben. Der folgende Abschnitt veranschaulicht das Lesen und Schreiben der People-Tagging-Metadaten in die Metadaten eines Images mithilfe von WIC-Abfrage Lesern und-Writern.

### <a name="people-names"></a>Personennamen

Ein Teil der People-Tagging-Funktion ist die Möglichkeit, einfach eine Liste der Namen der im Image markierten Personen zu erhalten. Dieser Teil des Features wird von den metadatenhandlern [System. Photo. People Ames](../properties/props-system-photo-peoplenames.md) und WIC unterstützt. Die [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) -Schnittstelle wird in Verbindung mit der System. Photo. peoplenames-Eigenschaft verwendet, um die Namen der in einem Bild identifizierten Personen zu lesen und in den Bild Metadaten zu speichern.

Im folgenden Codebeispiel wird ein Abfrage Reader veranschaulicht, der aus einem Bild Rahmen abgerufen wurde, um die Metadaten eines Bilds nach markierten Namen der [System. Photo. peoplenames](../properties/props-system-photo-peoplenames.md) -Eigenschaft abzufragen.


```C++
// Not shown: image decoding, retrieving an image frame. 
...
PROPVARIANT value;
IWICMetadataQueryReader *pQueryReader = NULL;
...
// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

// Query for the System.Photo.PeopleNames property.
if (SUCCEEDED(hr))
{
    // Get the property metadata by property name.
    hr = pQueryReader->GetMetadataByName(L"System.Photo.PeopleNames", &value);
}
```



Der Abfrage Ausdruck "System. Photo. People Ames" fragt den Frame für die Eigenschaft ab. Wenn die Metadaten für Personen Tags vorhanden sind und die Namen der Personen enthalten, wird der [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Wert auf VT \_ LPWSTR festgelegt, und der Datenwert enthält die Liste der markierten Namen. Weitere Informationen zum Lesen von Bild Metadaten finden Sie unter Übersicht über das [Lesen und Schreiben von Bild Metadaten](-wic-codec-readingwritingmetadata.md).

Das Abfragen des People Names-Tags ist nur nützlich, wenn das Image tatsächlich die People-Tagging-Metadaten enthält. Damit dies geschehen kann, muss eine Anwendung Sie zuerst schreiben. Um die Metadaten für Personennamen zu schreiben, verwenden Sie eine [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) und den expliziten XMP-Pfad der Metadaten. Im folgenden Codebeispiel wird die Verwendung eines Abfrage-Writers zum Schreiben eines Namens in den Abfrage Pfad veranschaulicht.


```C++
// Not shown: image encoding, retrieving/creating the image frame,
// creating the IWICImagingFactory 
...
IWICImagingFactory *pFactory = NULL;
IWICMetadataQueryWriter *pQueryWriter = NULL;
...
// Get the query writer from the image frame.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pQueryWriter);
}

// A query writer specifically for this person's XMP struct
IWICMetadataQueryWriter *pXMPStructQueryWriter = NULL;

// Create a query writer specifically for an XMP Struct
hr = pFactory->CreateQueryWriter(
    GUID_MetadataFormatXMPStruct,
    NULL,
    &pXMPStructQueryWriter
    );

// Create a variant representing the structure created above
PROPVARIANT xmpStruct;
PropVariantInit(&xmpStruct);

// VT_UNKNOWN indicates that we're setting a COM object, in this case a XMPStruct
// which will hold the name and rectangle
xmpStruct.vt = VT_UNKNOWN; 
xmpStruct.punkVal = pXMPStructQueryWriter;

if(SUCCEEDED(hr))
{
    // WIC will automatically create the xmp base, the RegionInfo struct, and the Regions
    // bag (an unordered array) but structs within that bag need to be explicitly created.
    // The {ulong=0} in the query means to insert the new struct at the start of the bag,
    // {} could also be used to insert at the end of the bag.
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions/{ulong=0}",
        &xmpStruct
        );
}

// Set up the PROPVARIANT with the name information
PROPVARIANT personName;
PropVariantInit(&personName);
personName.vt = VT_LPWSTR;
personName.pwszVal = L"John Doe";

if(SUCCEEDED(hr))
{
    // Set the name metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:PersonDisplayName",
        &personName
        );  
}
```



Beachten Sie den Schritt zum Erstellen der XMP-Struktur, und legen Sie Sie unter fest `MPRI:Regions/{ulong=0}` . Ohne diesen Schritt kann der WIC nicht ermitteln, wo er später platziert werden soll `PersonDisplayName` . Beachten Sie außerdem, dass der explizite Abfrage Pfad anstelle von [System. Photo. People Ames](-wic-photoprop-system-photo-peoplenames.md)verwendet wird, dessen metadatenrichtlinie das Schreiben von Metadaten nicht unterstützt.

### <a name="people-rectangles"></a>Menschen Rechtecke

Die Namen der Personen sind jedoch nur Teil der People-Tagging-Funktion. Zusätzlich zum Speichern von Personennamen in den Metadaten unterstützt das Schema auch Regions Informationen, die den spezifischen Bereich (ein Rechteck) identifizieren, der im Bild angezeigt wird.

Die Rechteck Informationen werden durch vier durch Trennzeichen getrennte Dezimalwerte dargestellt, z. b. "0,25, 0,25, 0,25, 0,25". Die ersten beiden Werte geben die obere linke Koordinate an. die letzten beiden geben die Höhe und Breite des Rechtecks an. Die Dimensionen des Bilds zum Definieren von Menschen Rechtecke werden zu 1 normalisiert, was bedeutet, dass im Beispiel "0,25, 0,25, 0,25, 0,25" das Rechteck 1/4 der Entfernung von oben und 1/4 der Entfernung von der linken Seite des Bilds startet. Die Höhe und Breite des Rechtecks sind 1/4 der Größe ihrer jeweiligen Bild Dimensionen.

Die Rechteck Informationen, mit denen Einzelpersonen identifiziert werden, werden auf die gleiche Weise geschrieben wie die Namen von Personen in derselben Struktur. Verwenden Sie zum Schreiben der Rechteck Metadaten eine [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) und den expliziten XMP-Pfad der Metadaten. Im folgenden Codebeispiel wird das vorherige Beispiel fortgesetzt, und es wird ein Rechteck hinzugefügt, das ' John Doe ' für die Metadaten des Bilds darstellt. Beachten Sie, dass der gleiche `{ulong=0}` Index verwendet wird, um dieses Rechteck "John Doe" zuzuordnen.


```C++
// Set up the PROPVARIANT with the rectangle information
PROPVARIANT rectangle;
PropVariantInit(&rectangle);
rectangle.vt = VT_LPWSTR;
rectangle.pwszVal = L"0.0,0.0,0.25,0.25";

if(SUCCEEDED(hr))
{
    // Set the rectangle metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:Rectangle",
        &rectangle
        );
}
```



## <a name="schema-reference"></a>Schemareferenz

Die Microsoft XMP-Schemas für Personen Tags definieren einen Satz von Eigenschaften, um Einzelpersonen in digitalen Fotos zu markieren.

In den folgenden Abschnitten werden die Schema Definitionen bereitgestellt, die für Personen Tags erforderlich sind. Nach Möglichkeit verwenden die Schema Definitionen die Konventionen, die von den [XMP-Spezifikationen (Extensible Metadata Platform) von Adobe](https://www.adobe.com/devnet/xmp/)bereitgestellt werden. Die Schema Definitionen in diesem Thema zeigen den XML-Namespace Uniform Resource Identifier (URI), der das Schema und das bevorzugte Schema Namespace-Präfix identifiziert, gefolgt von einer Tabelle, die alle für das Schema definierten Eigenschaften auflistet. Jede Tabelle weist die folgenden Spalten auf:

-   **Property** : der Name der Eigenschaft, einschließlich des bevorzugten Namespace Präfixes.

-   **Werttyp** : der Werttyp der Eigenschaft. Das People-Tagging-Unterstützungs Schema verwendet nach Möglichkeit die XMP-Werttypen, einschließlich Datum und Text. Array Typen wird der Containertyp `alt` vorangestellt:, `bag` oder `seq` .

-   **Category** -Schema-Eigenschaften sind intern oder extern:

    -   Interne Metadaten müssen von der Anwendung festgelegt werden.

    -   Externe Metadaten müssen vom Benutzer festgelegt werden und sind unabhängig vom Inhalt des Dokuments.

-   **Description** : die Beschreibung der Eigenschaft.

### <a name="microsoft-photo-12-schema"></a>Microsoft-Foto 1,2-Schema

Das Microsoft Photo 1,2-Schema stellt einen Satz von Eigenschaften für Bildbereiche bereit.

-   Der Schema Namespace-URI ist `https://ns.microsoft.com/photo/1.2/` .
-   Das bevorzugte Schema Namespace-Präfix ist `MP` .



| Eigenschaft      | Werttyp | Category | BESCHREIBUNG                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| MP: RegionInfo | RegionInfo | Intern | **erforderlich** : speichert den Stamm der People-Tagging-Metadaten. Weitere Informationen finden Sie im folgenden Abschnitt des Microsoft Photo RegionInfo-Schemas. |



 

### <a name="microsoft-photo-regioninfo-schema"></a>Microsoft Photo RegionInfo-Schema

Das Microsoft Photo RegionInfo 1,2-Schema stellt einen Satz von Eigenschaften für Regions Informationen bereit.

-   Der Schema Namespace-URI ist `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` .
-   Das bevorzugte Schema Namespace-Präfix ist `MPRI` .



| Eigenschaft              | Werttyp | Category | BESCHREIBUNG                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| MPRI: dateregionsvalid | Date       | Extern | **optional** : Datum, an dem die letzte Region erstellt wurde.                                                          |
| MPRI: Regionen          | Behälter Bereich | Extern | **erforderlich** : speichert die People-taggingregionen. Weitere Informationen finden Sie im folgenden Abschnitt des Microsoft-Foto Regions Schemas. |



 

### <a name="microsoft-photo-region-schema"></a>Microsoft-Foto Regions Schema

Das Microsoft Photo Region 1,2-Schema stellt einen Satz von Eigenschaften für Bildbereiche bereit.

-   Der Schema Namespace-URI ist `https://ns.microsoft.com/photo/1.2/t/Region#` .
-   Das bevorzugte Schema Namespace-Präfix ist `MPReg` .



| Mpreg: Eigenschaft          | Werttyp | Category | BESCHREIBUNG                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mpreg: persondisplayname | Text       | Extern | **erforderlich** : speichert den Namen der Person im angegebenen Rechteck.                                                                                                                                                                                                                                            |
| Mpreg: Rechteck         | Text       | Extern | **optional** : speichert das Rechteck, das die Person innerhalb des Fotos identifiziert. Das Rechteck wird als vier durch Trennzeichen getrennte Dezimalwerte gespeichert. Die ersten beiden Werte geben die obere linke Koordinate an. die letzten beiden geben die Höhe und Breite des Rechtecks an. Die Dezimalwerte müssen auf 1 normalisiert werden. |
| Mpreg: personemaildigest | Text       | Extern | **optional** : speichert den SHA-1-verschlüsselten Nachrichten Hash der Live-e-Mail-Adresse der Person.                                                                                                                                                                                                                     |
| Mpreg: personliveidcid   | Text       | Extern | **optional** : speichert die signierte Dezimal Darstellung der Live-CID der Person, einer 64-Bit-Ganzzahl, die eine Live Identität öffentlich identifiziert.                                                                                                                                                                     |



 

### <a name="sample-metadata"></a>Beispiel Metadaten

Im folgenden finden Sie eine Darstellung der XMP-Metadaten für Personen Tags.

``` syntax
<rdf:Description rdf:about="" xmlns:MP="https://ns.microsoft.com/photo/1.2/">
<MP:RegionInfo> 
<rdf:Description xmlns:MPRI="https://ns.microsoft.com/photo/1.2/t/RegionInfo#">
   <MPRI:Regions> 
       <rdf:Bag> 
          <rdf:li> 
       <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#"> 
           <MPReg:Rectangle>0.790650, 0.441734, 0.209350, 0.279133
           </MPReg:Rectangle>
           <MPReg:PersonDisplayName>John Doe</MPReg:PersonDisplayName> 
           <MPReg:PersonEmailDigest>2FD4E1C67A2D28FCED849EE1BB76E7391B93EB13</MPReg:PersonEmailDigest> 
           <MPReg:PersonLiveIdCID>1234567890123456789</MPReg:PersonLiveIdCID> 
       </rdf:Description> 
         </rdf:li> 
         <rdf:li>
             <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#">
                  <MPReg:Rectangle>0.222656, 0.302083, 0.378906, 0.505208</MPReg:Rectangle> 
                  <MPReg:PersonDisplayName>Jane Doe</MPReg:PersonDisplayName> 
              </rdf:Description> 
         </rdf:li> 
<!-- Addition Regions --> ... 
<rdf:li>...
</rdf:li> 
</rdf:Bag> 
</MPRI:Regions> </rdf:Description> </MP:RegionInfo> </rdf:Description>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über WIC-Metadaten](-wic-about-metadata.md)
</dt> <dt>

[Übersicht über das Lesen und Schreiben von Bild Metadaten](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Übersicht über die Metadaten-Abfragesprache](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
