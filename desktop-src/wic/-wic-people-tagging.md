---
description: In diesem Thema werden das neue XMP-Schema (Extensible Metadata Platform) und die Windows 7-Fotoeigenschaft System.Photo.PeopleNames beschrieben, die das Markieren von Personen in einem digitalen Foto ermöglicht.
ms.assetid: 557c3e9a-1756-4abb-8465-b12195ecbc91
title: Übersicht über Personentags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a262acd70474f75689e99a3bcd1087cd0117ae3602b78a90357aa932fdd7fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205704"
---
# <a name="people-tagging-overview"></a>Übersicht über Personentags

In diesem Thema werden das neue XMP-Schema (Extensible Metadata Platform) und die Windows 7-Fotoeigenschaft [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) beschrieben, die das Markieren von Personen in einem digitalen Foto ermöglicht. In diesem Thema wird auch erläutert, wie sie die Windows Imaging Component (WIC)-API zum Lesen und Schreiben der Metadaten verwendet, die für personentagging erforderlich sind.

Dieses Thema enthält folgende Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Introduction (Einführung)](#introduction)
-   [Personentagging](#people-tagging-overview)
    -   [Personennamen](#people-names)
    -   [Personenrechtecke](#people-rectangles)
-   [Schemareferenz](#schema-reference)
    -   [Microsoft Photo 1.2-Schema](#microsoft-photo-12-schema)
    -   [Microsoft Photo RegionInfo-Schema](#microsoft-photo-regioninfo-schema)
    -   [Microsoft-Fotobereichsschema](#microsoft-photo-regioninfo-schema)
    -   [Beispielmetadaten](#sample-metadata)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Um dieses Thema zu verstehen, sollten Sie mit den WIC-Decoderschnittstellen und den zugehörigen Component Object Model-Komponenten (COM) vertraut sein, wie in der Übersicht über Windows [Imaging-Komponenten beschrieben.](-wic-about-windows-imaging-codec.md) Außerdem ist es hilfreich, sich allgemein mit der Bildverarbeitung von Metadaten vertraut zu machen, insbesondere mit XMP.

## <a name="introduction"></a>Einführung

Microsoft hat ein neues XMP-Schema zum Markieren von Personen in einem digitalen Bild erstellt. Mit diesem Schema können Anwendungen die Namen und Speicherorte von Personen, die sich im Bild befinden, als Metadaten innerhalb des Bilds speichern. Zusätzlich zum neuen Schema ist die neue Fotoeigenschaft [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) in Windows 7 verfügbar. Mit dieser neuen Eigenschaft können Anwendungen die Namen der Einzelnen lesen, die in den Bildmetadaten gespeichert sind. WIC nutzt diese neuen Features, indem Es Anwendungen ermöglicht wird, Personen, die Metadaten auf digitalen Fotos markieren, einfach zu lesen und zu schreiben.

## <a name="people-tagging"></a>Personentagging

WIC stellt Anwendungsentwicklern COM-Komponenten bereit, die Bilddaten sowie Bildmetadaten lesen. Zum Lesen und Schreiben von Metadaten, z. B. dem neuen People-Tagging-Feature, stellt WIC die [**Schnittstellen IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) und [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) bereit. Diese Schnittstellen ermöglichen es Anwendungen, die [Metadatenabfragesprache zu verwenden,](-wic-codec-metadataquerylanguage.md) um Metadaten in die einzelnen Frames eines Bilds zu schreiben. Im folgenden Abschnitt wird veranschaulicht, wie sie mithilfe von WIC-Abfragelesern und Writern die Metadaten für das People-Tagging in die Metadaten eines Bilds lesen und schreiben.

### <a name="people-names"></a>Personennamen

Ein Teil des People-Tagging-Features ist die Möglichkeit, einfach eine Liste der Namen der Personen zu erhalten, die im Bild markiert sind. Dieser Teil des Features wird von den [Metadatenhandlern System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) und WIC unterstützt. Die [**IWICMetadataQueryReader-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) wird in Verbindung mit der System.Photo.PeopleNames-Eigenschaft verwendet, um die Namen von Personen zu lesen, die in einem Bild identifiziert und in den Bildmetadaten gespeichert werden.

Im folgenden Codebeispiel wird ein Abfrageleser veranschaulicht, der aus einem Bildrahmen ermittelt wurde, um die Metadaten eines Bilds nach markierten Namen der [System.Photo.PeopleNames-Eigenschaft](../properties/props-system-photo-peoplenames.md) abfragt.


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



Der Abfrageausdruck "System.Photo.PeopleNames" fragt den Frame für die -Eigenschaft ab. Wenn die People-Tagging-Metadaten vorhanden sind und die Namen von Personen enthalten, wird der [PROPVARIANT-Wert](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) auf VT LPWSTR festgelegt, und der Datenwert enthält die Liste der markierten \_ Namen. Weitere Informationen zum Lesen von Bildmetadaten finden Sie unter [Übersicht über das Lesen und Schreiben von Bildmetadaten.](-wic-codec-readingwritingmetadata.md)

Das Abfragen des Personennamentags ist nur nützlich, wenn das Bild tatsächlich die Metadaten zum Markieren von Personen enthält. Damit dies geschieht, muss eine Anwendung sie zuerst geschrieben haben. Verwenden Sie zum Schreiben der Metadaten für Personennamen [**einen IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) und den expliziten XMP-Pfad der Metadaten. Im folgenden Codebeispiel wird die Verwendung eines Abfragewriters zum Schreiben eines Namens in den Abfragepfad veranschaulicht.


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



Beachten Sie den Schritt zum Erstellen der XMP-Struktur und festlegen sie unter `MPRI:Regions/{ulong=0}` . Ohne diesen Schritt kann der WIC nicht ermitteln, wo das spätere platzieren `PersonDisplayName` wird. Beachten Sie auch, dass der explizite Abfragepfad anstelle von [System.Photo.PeopleNames](-wic-photoprop-system-photo-peoplenames.md)verwendet wird, dessen Metadatenrichtlinie das Schreiben von Metadaten nicht unterstützt.

### <a name="people-rectangles"></a>Personenrechtecke

Die Namen von Personen sind jedoch nur Teil des People-Tagging-Features. Zusätzlich zum Speichern der Namen von Personen in den Metadaten unterstützt das Schema auch Bereichsinformationen, die den spezifischen Bereich (ein Rechteck) identifizieren, in dem die Person im Bild angezeigt wird.

Die Rechteckinformationen werden durch vier kommastrennte Dezimalwerte dargestellt, z.B. "0,25, 0,25, 0,25, 0,25". Die ersten beiden Werte geben die obere linke Koordinate an. Die letzten beiden geben die Höhe und Breite des Rechtecks an. Die Abmessungen des Bilds zum Definieren von Personenrechtecke werden auf 1 normalisiert. Dies bedeutet, dass das Rechteck im Beispiel "0,25, 0,25, 0,25, 0,25" 1/4 des Abstands von oben und 1/4 des Abstands von links vom Bild beginnt. Sowohl die Höhe als auch die Breite des Rechtecks sind 1/4 der Größe der jeweiligen Bilddimensionen.

Die Rechteckinformationen, die Personen identifizieren, werden in derselben Struktur auf die gleiche Weise geschrieben wie die Namen von Personen. Verwenden Sie zum Schreiben der Rechteckmetadaten [**einen IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) und den expliziten XMP-Pfad der Metadaten. Im folgenden Codebeispiel wird das vorherige Beispiel fortgesetzt und den Metadaten des Bilds ein Rechteck hinzugefügt, das "John Doe" darstellt. Beachten Sie, dass der gleiche Index `{ulong=0}` verwendet wird, um dieses Rechteck "John Doe" zu zuordnen.


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

Die Microsoft XMP-Schemas für Personen mit Tags definieren einen Satz von Eigenschaften, um Personen in digitalen Fotos zu markieren.

Die folgenden Abschnitte enthalten die Schemadefinitionen, die zum Markieren von Personen erforderlich sind. Nach Möglichkeit verwenden die Schemadefinitionen die Konventionen, die von [den XMP-Spezifikationen (Extensible Metadata Platform) von Adobe bereitgestellt werden.](https://www.adobe.com/devnet/xmp/) Die Schemadefinitionen in diesem Thema zeigen den XML-Namespace Uniform Resource Identifier (URI), der das Schema und das bevorzugte Schemanamespacepräfix identifiziert, gefolgt von einer Tabelle, die alle für das Schema definierten Eigenschaften auflistet. Jede Tabelle verfügt über die folgenden Spalten:

-   **Eigenschaft:** Der Name der Eigenschaft, einschließlich des bevorzugten Namespacepräfixes.

-   **Werttyp:** Der Werttyp der Eigenschaft. Die People-Tagging-Unterstützungsschemas verwenden nach Möglichkeit die XMP-Werttypen, einschließlich Datum und Text. Arraytypen wird der Containertyp `alt` vorangegangen: `bag` , oder `seq` .

-   **Kategorie:** Schemaeigenschaften sind intern oder extern:

    -   Interne Metadaten müssen von der Anwendung festgelegt werden.

    -   Externe Metadaten müssen vom Benutzer festgelegt werden und sind unabhängig vom Inhalt des Dokuments.

-   **Beschreibung:** Die Beschreibung der Eigenschaft.

### <a name="microsoft-photo-12-schema"></a>Microsoft Photo 1.2-Schema

Das Microsoft Photo 1.2-Schema stellt einen Satz von Eigenschaften für Bildregionen zur Verfügung.

-   Der Schemanamespace-URI ist `https://ns.microsoft.com/photo/1.2/` .
-   Das bevorzugte Schemanamespacepräfix ist `MP` .



| Eigenschaft      | Werttyp | Kategorie | Beschreibung                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| MP:RegionInfo | Regioninfo | Intern | **required:** Speichert den Stamm der People-Tagging-Metadaten. Weitere Informationen finden Sie im Abschnitt Microsoft Photo RegionInfo Schema (Microsoft Photo RegionInfo-Schema). |



 

### <a name="microsoft-photo-regioninfo-schema"></a>Microsoft Photo RegionInfo-Schema

Das Microsoft Photo RegionInfo 1.2-Schema stellt einen Satz von Eigenschaften für die Informationen zur Region zur Verfügung.

-   Der Schemanamespace-URI ist `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` .
-   Das bevorzugte Schemanamespacepräfix ist `MPRI` .



| Eigenschaft              | Werttyp | Kategorie | Beschreibung                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| MPRI:DateRegionsValid | Date       | Extern | **optional:** Datum, an dem die letzte Region erstellt wurde.                                                          |
| MPRI: Regionen          | Bag-Bereich | Extern | **required:** Speichert die Personentagingregionen. Weitere Informationen finden Sie im Folgenden im Abschnitt Schema der Microsoft-Fotoregion. |



 

### <a name="microsoft-photo-region-schema"></a>Microsoft Photo Region Schema

Das Microsoft Photo Region 1.2-Schema stellt eine Reihe von Eigenschaften für Bildbereiche bereit.

-   Der Schemanamespace-URI ist `https://ns.microsoft.com/photo/1.2/t/Region#` .
-   Das bevorzugte Schemanamespacepräfix ist `MPReg` .



| MPReg:Property          | Werttyp | Kategorie | Beschreibung                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MPReg:PersonDisplayName | Text       | Extern | **required:** Speichert den Namen der Person im angegebenen Rechteck.                                                                                                                                                                                                                                            |
| MPReg:Rectangle         | Text       | Extern | **optional:** Speichert das Rechteck, das die Person innerhalb des Fotos identifiziert. Das Rechteck wird als vier durch Trennzeichen getrennte Dezimalwerte gespeichert. Die ersten beiden Werte geben die obere linke Koordinate an. Die letzten beiden geben die Höhe und Breite des Rechtecks an. Die Dezimalwerte müssen auf 1 normalisiert werden. |
| MPReg:PersonEmailDigest | Text       | Extern | **optional:** Speichert den SHA-1-verschlüsselten Nachrichtenhash der Live-E-Mail-Adresse der Person.                                                                                                                                                                                                                     |
| MPReg:PersonLiveIdCID   | Text       | Extern | **optional:** Speichert die Dezimaldarstellung der Live-CID der Person mit Vorzeichen, eine 64-Bit-Ganzzahl, die eine Liveidentität öffentlich identifiziert.                                                                                                                                                                     |



 

### <a name="sample-metadata"></a>Beispielmetadaten

Im Folgenden werden die XMP-Metadaten für das Tagging von Personen dargestellt.

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

**Konzeptionellen**
</dt> <dt>

[Windows Übersicht über Bildverarbeitungskomponenten](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Übersicht über WIC-Metadaten](-wic-about-metadata.md)
</dt> <dt>

[Übersicht über das Lesen und Schreiben von Bildmetadaten](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Übersicht über die Metadatenabfragesprache](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
