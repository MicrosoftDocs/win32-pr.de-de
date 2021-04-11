---
description: Beschreibt, wie eine OpenSearch-Beschreibungsdatei (OSDX-Datei) erstellt wird, um externe Datenspeicher über das OpenSearch-Protokoll mit dem Windows-Client zu verbinden.
ms.assetid: 62cd88cd-e6ff-4e46-887d-e62f7018c065
title: Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406b166d6963517d692ef9de8292190d7eb92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958784"
---
# <a name="creating-an-opensearch-description-file-in-windows-federated-search"></a>Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche

Beschreibt, wie eine OpenSearch-Beschreibungsdatei (OSDX-Datei) erstellt wird, um externe Datenspeicher über das [OpenSearch](https://github.com/dewitt/opensearch) -Protokoll mit dem Windows-Client zu verbinden. Mit der Verbund Suche können Benutzer einen Remote Datenspeicher durchsuchen und die Ergebnisse innerhalb von Windows-Explorer anzeigen.

Dieses Thema enthält folgende Abschnitte:

-   [OpenSearch-Beschreibungsdatei](#opensearch-description-file)
    -   [Erforderliche untergeordnete Elemente für Mininum](#mininum-required-child-elements)
-   [Standard Elemente in der Windows-Verbund Suche](#standard-elements-in-windows-federated-search)
    -   [Kurznamen](#shortname)
    -   [Beschreibung](#description)
    -   [URL-Vorlage für RSS/Atom-Ergebnisse](#url-template-for-rssatom-results)
    -   [URL-Vorlage für Webergebnisse](#url-template-for-web-results)
    -   [URL-Vorlagen Parameter](#url-template-parameters)
    -   [Auslagerbare Ergebnisse](#paged-results)
    -   [Paging mit dem Element Index](#paging-using-the-item-index)
    -   [Paging mit dem Seiten Index](#paging-using-the-page-index)
    -   [Seitengröße](#page-size)
-   [Erweiterte Elemente in der Windows-Verbund Suche](#extended-elements-in-windows-federated-search)
    -   [Maximale Ergebnis Anzahl](#maximum-result-count)
    -   [Eigenschaftszuordnung](#property-mapping)
-   [Vorschauen](#previews)
-   [Menü Element "Datei Speicherort öffnen"](#open-file-location-menu-item)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="opensearch-description-file"></a>OpenSearch-Beschreibungsdatei

Eine OpenSearch-Beschreibungsdatei (OSDX-Datei) für die Windows-Verbund Suche muss die folgenden Regeln einhalten:

-   Ein gültiges OpenSearch-Beschreibungs Dokument, wie in der [OpenSearch](https://github.com/dewitt/opensearch) 1,1-Spezifikation definiert.
-   Stellen Sie eine URL-Vorlage mit einem RSS-oder Atom-Formattyp bereit.
-   Verwenden Sie die Dateinamenerweiterung. OSDX, oder lassen Sie sich beim Herunterladen aus dem Web mit der Dateinamenerweiterung. OSDX verknüpft. Beispielsweise ist es nicht erforderlich, dass ein Server. OSDX verwendet. Ein Server kann die Datei mit einer beliebigen Dateinamenerweiterung (z. b.. Xml) zurückgeben und so behandelt werden, als ob es sich um eine OSDX-Datei handelt, wenn Sie den richtigen MIME-Typ für OpenSearch-Beschreibungs Dokumente (OSDX-Dateien) verwendet.
-   Geben Sie einen Wert für das **Shortname** -Element an (empfohlen).

### <a name="mininum-required-child-elements"></a>Erforderliche untergeordnete Elemente für Mininum

Die folgende OSDX-Beispieldatei besteht aus **Kurzname** und `Url` Elementen, bei denen es sich um die mindestens erforderlichen untergeordneten Elemente handelt.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    <Url format="application/rss+xml" 
        template="https://example.com/rss.php?query=
        {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



## <a name="standard-elements-in-windows-federated-search"></a>Standard Elemente in der Windows-Verbund Suche

Zusätzlich zu den minimalen untergeordneten Elementen unterstützt die Verbund Suche die folgenden Standardelemente.

### <a name="shortname"></a>Kurznamen

Windows verwendet den **Shortname** -Elementwert, um die Datei ". searchconnector-MS" (Suchconnector) zu benennen, die erstellt wird, wenn der Benutzer die OSDX-Datei öffnet. Windows stellt sicher, dass für den generierten Dateinamen nur Zeichen verwendet werden, die in Windows-Dateinamen zulässig sind. Wenn kein **Shortname** -Wert angegeben wird, versucht die Datei ". searchconnector-MS" stattdessen, den Dateinamen der OSDX-Datei zu verwenden.

Der folgende Code veranschaulicht, wie das **Shortname** -Element in einer OSDX-Datei verwendet wird.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    ...
</OpenSearchDescription>
```



### <a name="description"></a>BESCHREIBUNG

Windows verwendet den Wert **Description** -Element, um die im Detailbereich von Windows-Explorer angezeigte Dateibeschreibung aufzufüllen, wenn ein Benutzer eine searchconnector-MS-Datei auswählt.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Description>Searches the example company book catalog</Description>
</OpenSearchDescription>
```



### <a name="url-template-for-rssatom-results"></a>URL-Vorlage für RSS/Atom-Ergebnisse

Die OSDX-Datei muss ein **URL-Format** Element und ein **Vorlagen** Attribut (eine URL-Vorlage) enthalten, das Ergebnisse im RSS-oder Atom-Format zurückgibt. Das Format-Attribut muss `application/rss+xml` für RSS-formatierte Ergebnisse oder `application/atom+xml` für Atom-formatierte Ergebnisse auf festgelegt werden, wie im folgenden Code gezeigt.

> [!Note]  
> Das **URL-Format** Element und das **Vorlagen** Attribut werden häufig als URL-Vorlage bezeichnet.

 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
   ...
        <Url format="application/rss+xml" template="https://example.com/rss.php?query=
            {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



### <a name="url-template-for-web-results"></a>URL-Vorlage für Webergebnisse

Wenn eine Version der Suchergebnisse vorhanden ist, die in einem Webbrowser angezeigt werden kann, sollten Sie ein URL- **Format =** `text/html` Element und ein **Vorlagen** Attribut angeben, wie im folgenden Code gezeigt.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Url format="text/html" template="https://example.com/html.php?query={searchTerms}" />
</OpenSearchDescription>
```



Wenn Sie ein **URL-Format = "Text/HTML"** -Element und ein **Vorlagen** Attribut angeben, wird in der Windows-Explorer-Befehlsleiste eine Schaltfläche angezeigt, die dem Benutzer ermöglicht, einen Webbrowser zu öffnen, um die Suchergebnisse anzuzeigen, wenn der Benutzer eine Abfrage ausführt.

![Screenshot der websuchschaltfläche.](images/websearchroll-overcommandbarbutton.png)

Das Rollback der Abfrage an die Webbenutzer Oberfläche des Daten Stores ist in einigen Szenarien wichtig. Beispielsweise kann ein Benutzer mehr als 100 Ergebnisse anzeigen (die Standard Anzahl der Elemente, die der OpenSearch-Anbieter anfordert). Wenn dies der Fall ist, kann der Benutzer auch Suchfunktionen verwenden, die nur auf der Website des Daten Stores verfügbar sind, wie z. b. das erneute Abfragen mit einer anderen Sortierreihenfolge oder das pivotieren und Filtern der Abfrage mit zugehörigen Metadaten.

### <a name="url-template-parameters"></a>URL-Vorlagen Parameter

Der OpenSearch-Anbieter führt immer die folgenden Aktionen aus:

1.  Verwendet die URL-Vorlage, um die Anforderung an den Webdienst zu senden.
2.  Versucht, die in der URL-Vorlage gefundenen Token vor dem Senden der Anforderung an den Webdienst wie folgt zu ersetzen:
    -   Ersetzt die in der folgenden Tabelle aufgeführten OpenSearch-Standard Token.
    -   Entfernt alle Token, die nicht in der folgenden Tabelle aufgeführt sind.



| Unterstütztes Token  | Verwendung durch den OpenSearch-Anbieter                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| {searchTerms}    | Ersetzt durch die Suchbegriffe, die vom Benutzer in das Eingabefeld für die Windows-Explorer-Suche eingegeben werden.<br/>                                         |
| Start Index     | Wird verwendet, wenn Ergebnisse in "Pages" erhalten werden.<br/> Ersetzt durch den Index für das erste Ergebnis Element, das zurückgegeben werden soll.<br/>                        |
| Startpage      | Wird verwendet, wenn Ergebnisse in "Pages" erhalten werden.<br/> Ersetzt durch die Seitenzahl der zurück zugebende Anzahl von Suchergebnissen.<br/>               |
| Countdown          | Wird verwendet, wenn Ergebnisse in "Pages" erhalten werden.<br/> Wird durch die Anzahl der Suchergebnisse pro Seite ersetzt, die Windows-Explorer anfordert.<br/> |
| Kurse       | Wird durch eine Zeichenfolge ersetzt, die die Sprache der gesendeten Abfrage angibt.<br/>                                                          |
| {InputEncoding}  | Ersetzt durch eine Zeichenfolge (z. b. UTF-16), die die Zeichencodierung der gesendeten Abfrage angibt.<br/>                                |
| outputEncoding | Ersetzt durch eine Zeichenfolge (z. b. "UTF-16"), die die gewünschte Zeichencodierung für die Antwort des Webdiensts angibt.<br/>       |



 

### <a name="paged-results"></a>Auslagerbare Ergebnisse

Möglicherweise möchten Sie die Anzahl der pro Anforderung zurückgegebenen Ergebnisse einschränken. Sie können eine "Seite" der Ergebnisse gleichzeitig zurückgeben oder festlegen, dass der OpenSearch-Anbieter zusätzliche Ergebnis Ergebnisse entweder nach Element Nummer oder Seitenzahl erhält. Wenn Sie z. b. 20 Ergebnisse pro Seite senden, beginnt die erste gesendete Seite an Element Index 1 und auf Seite 1. die zweite Seite, die Sie senden, beginnt an Element Index 21 und auf Seite 2. Sie können definieren, wie der OpenSearch-Anbieter Elemente anfordern soll, indem Sie entweder das- `{startItem}` oder das- `{startPage}` Token in der URL-Vorlage verwenden.

### <a name="paging-using-the-item-index"></a>Paging mit dem Element Index

Ein Element Index identifiziert das erste Ergebnis Element auf einer Seite mit Ergebnissen. Wenn Sie möchten, dass Clients Anforderungen mithilfe eines Element Indexes senden, können Sie das `{startIndex}` Token in Ihrem **URL** -Element **Vorlagen** Attribut verwenden, wie im folgenden Code gezeigt.


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}" />
```



Der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter ersetzt dann das Token in der URL durch einen Start Index Wert. Die erste Anforderung beginnt mit dem ersten Element, wie im folgenden Beispiel veranschaulicht:


```
https://example.com/rss.php?query=frogs&start=1
```



Der OpenSearch-Anbieter kann weitere Elemente erhalten, indem er den `{startIndex}` Parameterwert ändert und eine neue Anforderung ausgibt. Der Anbieter wiederholt diesen Prozess, bis er genügend Ergebnisse zum erfüllen seines Limits erhält oder das Ende der Ergebnisse erreicht. Der OpenSearch-Anbieter prüft die Anzahl der Elemente, die vom Webdienst auf der ersten Seite der Ergebnisse zurückgegeben werden, und legt die erwartete Seitengröße auf diese Zahl fest. Diese Zahl wird verwendet, um den `{startIndex}` Wert für nachfolgende Anforderungen zu erhöhen. Wenn der Webdienst z. b. 20 Ergebnisse in der ersten Anforderung zurückgibt, legt der Anbieter die erwartete Seitengröße auf 20 fest. Bei der nächsten Anforderung ersetzt der Anbieter `{startIndex}` durch den Wert 21, um die nächsten 20 Elemente zu erhalten.

> [!Note]  
> Wenn eine vom Webdienst zurückgegebene Ergebnisseite weniger Elemente aufweist als die erwartete Seitengröße, geht der OpenSearch-Anbieter davon aus, dass er die letzte Seite der Ergebnisse empfangen hat, und hält keine Anforderungen mehr an.

 

### <a name="paging-using-the-page-index"></a>Paging mit dem Seiten Index

Ein Seitenindex identifiziert die angegebene Seite der Ergebnisse. Wenn Sie möchten, dass Clients Anforderungen mithilfe einer Seitenzahl senden, können Sie das `{startPage}` Token in Ihrem **URL-Format** Element **Template** -Attribut verwenden, um anzugeben, wie im folgenden Beispiel veranschaulicht:


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;page={startPage}" />
```



Der OpenSearch-Anbieter ersetzt dann das Token in der URL durch einen page number-Parameter. Die erste Anforderung beginnt mit der ersten Seite, wie im folgenden Beispiel gezeigt:


```
https://example.com/rss.php?query=frogs&page=1
```



> [!Note]  
> Wenn eine vom Webdienst zurückgegebene Ergebnisseite weniger Elemente aufweist als die erwartete Seitengröße, geht der OpenSearch-Anbieter davon aus, dass er die letzte Seite der Ergebnisse empfangen hat, und hält keine Anforderungen mehr an.

 

### <a name="page-size"></a>Page Size

Möglicherweise möchten Sie den Webdienst so konfigurieren, dass eine Anforderung zum Angeben der Größe der Seiten mithilfe eines Parameters in der URL zulässig ist. Eine Anforderung muss in der OSDX-Datei angegeben werden, indem das `{count}` Token wie folgt verwendet wird:


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
```



Der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter kann dann die gewünschte Seitengröße in Anzahl der Ergebnisse pro Seite festlegen, wie im folgenden Beispiel gezeigt:


```
https://example.com/rss.php?query=frogs&start=1&cnt=50
```



Standardmäßig stellt der OpenSearch-Anbieter Anforderungen mithilfe einer Seitengröße von 50. Wenn Sie eine andere Seitengröße wünschen, geben Sie kein `{count}` Token an, und platzieren Sie die gewünschte Zahl stattdessen direkt im **URL-Vorlagen** Element.

Der OpenSearch-Anbieter bestimmt die Seitengröße basierend auf der Anzahl der Ergebnisse, die bei der ersten Anforderung zurückgegeben werden. Wenn die erste empfangene Ergebnisseite weniger Elemente enthält als die angeforderte Anzahl, setzt der Anbieter die Seitengröße für alle nachfolgenden Seiten Anforderungen zurück. Wenn nachfolgende Seiten Anforderungen weniger Elemente als angefordert zurückgeben, geht der OpenSearch-Anbieter davon aus, dass er das Ende der Ergebnisse erreicht hat.

## <a name="extended-elements-in-windows-federated-search"></a>Erweiterte Elemente in der Windows-Verbund Suche

Zusätzlich zu den Standardelementen unterstützt die Verbund Suche die folgenden erweiterten Elemente: **maximumresultcount** und **resultsprocessing.**

Da diese erweiterten untergeordneten Elemente in der [OpenSearch](https://github.com/dewitt/opensearch) v 1.1-Spezifikation nicht unterstützt werden, müssen Sie mithilfe des folgenden Namespace hinzugefügt werden:


```
http://schemas.microsoft.com/opensearchext/2009/
```



### <a name="maximum-result-count"></a>Maximale Ergebnis Anzahl

Standardmäßig sind Suchconnectors auf 100-Ergebnisse pro Benutzer Abfrage beschränkt. Diese Beschränkung kann angepasst werden, indem Sie das **maximumresultcount** -Element in die OSD-Datei einschließen, wie im folgenden Beispiel gezeigt:


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/" 
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
        ...
        <ms-ose:MaximumResultCount>200</ms-ose:MaximumResultCount>
</OpenSearchDescription>
```



Im vorangehenden Beispiel wird das Namespace Präfix `ms-ose` im **opensearchdescription** -Element der obersten Ebene deklariert und dann als Präfix im Elementnamen verwendet. Diese Deklaration ist erforderlich, weil **maximumresultcount** in der [OpenSearch](https://github.com/dewitt/opensearch) v 1.1-Spezifikation nicht unterstützt wird.

### <a name="property-mapping"></a>Eigenschaftszuordnung

Wenn Ergebnisse vom Webdienst als RSS-oder Atom-Feed zurückgegeben werden, muss der OpenSearch-Anbieter die Element Metadaten in den Feeds den Eigenschaften zuordnen, die von der Windows-Shell verwendet werden können. Der folgende Screenshot veranschaulicht, wie der OpenSearch-Anbieter einige der standardmäßigen RSS-Elemente zuordnet.

![Screenshot mit integrierten RSS-zu-Windows-shelleigenschaftenzuordnungen](images/built-inrsstowindowsshellpropertymappings.png)

### <a name="default-mappings"></a>Standardzuordnungen

In der folgenden Tabelle sind die Standard Zuordnungen von RSS-XML-Elementen zu den Windows Shell-Systemeigenschaften aufgeführt. XML-Pfade sind relativ zum Item-Element. Das `"media:"` Präfix wird vom [Namespace](https://www.rssboard.org/media-rss) Namespace für Yahoo-Suche definiert.



| RSS-XML-Pfad                  | Windows Shell-Eigenschaft (Kanonischer Name) |
|-------------------------------|-----------------------------------------|
| Link                          | System. itemurl                          |
| Titel                         | System. ItemName                         |
| Autor                        | System.Author                           |
| pubDate                       | System. DateModified                     |
| BESCHREIBUNG                   | System. autosummary                      |
| Category                      | System.Keywords                         |
| enclosure/@type               | System. MimeType                         |
| enclosure/@length             | System. Size                             |
| enclosure/@url                | System. contenturl                       |
| Medien: Kategorie                | System.Keywords                         |
| media:content/@fileSize       | System. Size                             |
| media:content/@type           | System. MimeType                         |
| media:content/@url            | System. contenturl                       |
| media:group/content/@fileSize | System. Size                             |
| media:group/content/@type     | System. MimeType                         |
| media:group/content/@url      | System. contenturl                       |
| media:thumbnail/@url          | System. itemthumbnailurl                 |



 

> [!Note]  
> Zusätzlich zu den Standard Zuordnungen von Standard-RSS-oder Atom-Elementen können Sie weitere Windows Shell-Systemeigenschaften zuordnen, indem Sie für jede der Eigenschaften zusätzliche XML-Elemente in den Windows-Namespace einschließen. Sie können auch Elemente aus anderen vorhandenen XML-Namespaces (z. b. mediarss, iTunes usw.) zuordnen, indem Sie eine benutzerdefinierte Eigenschaften Zuordnung in der OSDX-Datei hinzufügen.

 

### <a name="custom-property-mappings"></a>Zuordnungen von benutzerdefinierten Eigenschaften

Sie können die Zuordnung von Elementen aus der RSS-Ausgabe zu Windows Shell-Systemeigenschaften anpassen, indem Sie die Zuordnung in der OSDX-Datei angeben.

Die RSS-Ausgabe gibt Folgendes an:

-   Ein XML-Namespace und
-   Für alle untergeordneten Elemente eines Elements ein Elementname, der zugeordnet werden soll.

Die OSDX-Datei identifiziert eine Windows-shelleigenschaft für jeden Elementnamen in einem Namespace. Die Eigenschaften Zuordnungen, die Sie in ihrer OSDX-Datei definieren, überschreiben die Standard Zuordnungen, sofern vorhanden, für diese angegebenen Eigenschaften.

Im folgenden Diagramm wird veranschaulicht, wie eine RSS-Erweiterung Windows-Eigenschaften (Kanonischer Name) zugeordnet wird.

![Diagramm, das anzeigt, dass die Kombination aus XML-Namespace und XML-Pfad den kanonischen Namen erzeugt](images/rssextensionsusexmlnamespaceandpathstomaptowindowsproperties.png)

### <a name="example-rss-results-and-osd-property-mapping"></a>Beispiel-RSS-Ergebnisse und OSD-Eigenschaften Zuordnung

Die folgende RSS-Beispielausgabe identifiziert `https://example.com/schema/2009` als XML-Namespace mit dem Präfix "example". Dieses Präfix muss wieder vor dem **e-Mail-** Element angezeigt werden.


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009">
   ...
    <item>
      <title>Someone</title>
      <example:email>Someone@example.com</example:email>
    </item>
```



In der folgenden OSDX-Beispieldatei wird das XML **-e-Mail-** Element der Windows Shell-Eigenschaft [System. Contact. EmailAddress](../properties/props-system-contact-emailaddress.md)zugeordnet.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/"
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
...
 <ms-ose:ResultsProcessing format="application/rss+xml">
   <ms-ose:PropertyMapList>
     <ms-ose:PropertyMap sourceNamespaceURI="https://example.com/schema/2009/" >
       <ms-ose:Source path="email">
         <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace" name="System.Contact.EmailAddress" />
       </ms-ose:Source>
     </ms-ose:PropertyMap>
   </ms-ose:PropertyMapList>
 </ms-ose:ResultsProcessing>
...
</OpenSearchDescription>
```



Es gibt einige Eigenschaften, die nicht zugeordnet werden können, da die Werte für Sie entweder später überschrieben werden oder nicht bearbeitet werden können. Beispielsweise kann [System. itemfolderpathdisplay](../properties/props-system-itempathdisplay.md) oder [System. itempathdisplaynarrow](../properties/props-system-itempathdisplaynarrow.md) nicht zugeordnet werden, da Sie aus dem URL-Wert berechnet werden, der in den Link-oder Gehäuse Elementen bereitgestellt wird.

### <a name="thumbnails"></a>Miniaturbilder

Miniaturbild-URLs können für jedes Element mithilfe des Mediums " **Miniaturansicht URL =" "** angegeben werden. Die ideale Auflösung beträgt 150 x 150 Pixel. Die größten unterstützten Miniaturansichten sind 256 x 256 Pixel. Das Bereitstellen größerer Abbilder erfordert mehr Bandbreite, sodass der Benutzer keinen zusätzlichen Vorteil hat.

### <a name="open-file-location-context-menu"></a>Kontextmenü für Datei Speicherort öffnen

Windows stellt ein Kontextmenü mit dem Namen " **Open File Location** " für Ergebnis Elemente bereit. Wenn der Benutzer ein Element aus diesem Menü auswählt, wird die "übergeordnete" URL für das ausgewählte Element geöffnet. Wenn die URL eine Web-URL ist (z. b.) `https://...` , wird der Webbrowser geöffnet und zu dieser URL navigiert. Ihr Feed sollte für jedes Element eine benutzerdefinierte URL bereitstellen, um sicherzustellen, dass Windows eine gültige URL öffnet. Dies kann erreicht werden, indem die URL in ein Element innerhalb des XML-Elements eingeschlossen wird, wie im folgenden Beispiel veranschaulicht:


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" 
    xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <link>https://example.com/pictures.aspx?id=01</link>
      <win:System.ItemFolderPathDisplay>https://example.com/pictures_list.aspx
   </win:System.ItemFolderPathDisplay>
   </item>
...
```



Wenn diese Eigenschaft nicht explizit im XML-Code des Elements festgelegt ist, legt der OpenSearch-Anbieter diese auf den übergeordneten Ordner der URL des Elements fest. Im obigen Beispiel würde der OpenSearch-Anbieter den Linkwert verwenden und den Eigenschafts Wert [System. itemfolderpathdisplay](../properties/props-system-itemfolderpathdisplay.md) der Windows-Shell auf festlegen `"https://example.com/"` .

### <a name="customize-windows-explorer-views-with-property-description-lists"></a>Anpassen von Windows Explorer-Ansichten mit Eigenschaften Beschreibungs Listen

Einige Windows Explorer-Ansichts Layouts werden durch Eigenschafts Beschreibungs Listen oder proplists definiert. Eine proplist ist eine durch Semikolons getrennte Liste von Eigenschaften, z `"prop:System.ItemName; System.Author"` . b., die verwendet wird, um zu steuern, wie Ihre Ergebnisse in Windows-Explorer angezeigt werden.

Die Benutzeroberflächen Bereiche von Windows Explorer, die mithilfe von proplists angepasst werden können, werden im folgenden Screenshot veranschaulicht:

![Screenshot der Benutzeroberflächen Bereiche von Windows Explorer, die mithilfe von proplists angepasst werden können](images/areasofwindowsexplorerthatyoucancontrolwithproplists.png)

Jedem Bereich von Windows Explorer ist ein Satz von proplists zugeordnet, die selbst als Eigenschaften angegeben sind. Sie können benutzerdefinierte proplisten für einzelne Elemente in den Resultsets oder für alle Elemente in einem Resultset angeben.



| Benutzeroberflächen Bereich zum Anpassen               | Windows Shell-Eigenschaft, die die Anpassung implementiert |
|------------------------------------|----------------------------------------------------------|
| Inhalts Ansichtsmodus (bei der Suche) | System. proplist. contentviewmodeforsearch                 |
| Inhalts Ansichtsmodus (beim Durchsuchen)  | System. proplist. contentviewmodeforbrowse                 |
| Kachel Ansichtsmodus                     | System. proplist. tileingefo                                 |
| Detailbereich                       | System. proplist. previewdetails                           |
| Infotip (QuickInfo des Elements)     | System. proplist. infotip                                  |



 

 

**So geben Sie eine eindeutige proplist für ein einzelnes Element an:**

1.  Fügen Sie in der RSS-Ausgabe ein benutzerdefiniertes Element hinzu, das die anzufügende proplist darstellt. Im folgenden Beispiel wird z. b. die Liste für den Detailbereich festgelegt:
    ```
    <win:System.PropList.PreviewDetails>
        prop:System.ItemName;System.Author</win:System.PropList.PreviewDetails>
    ```

    

2.  Wenn Sie eine Eigenschaft auf alle Elemente in den Suchergebnissen anwenden möchten, ohne die RSS-Ausgabe zu ändern, geben Sie eine proplist innerhalb eines **MS-ose: propertydefaultvalues** -Elements in der OSDX-Datei an, wie im folgenden Beispiel gezeigt:

    ```
    <ms-ose:ResultsProcessing format="application/rss+xml">
        <ms-ose:PropertyDefaultValues>
          <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace"
            name="System.PropList.ContentViewModeForSearch">prop:~System.ItemNameDisplay;System.Photo.DateTaken;
            ~System.ItemPathDisplay;~System.Search.AutoSummary;System.Size;System.Author;System.Keywords</ms-ose:Property>
        </ms-ose:PropertyDefaultValues>
      </ms-ose:ResultsProcessing>
    ```

    

### <a name="content-view-mode-layout-of-properties"></a>Layout des Inhalts Ansichtsmodus von Eigenschaften

Die Liste der Eigenschaften, die in den " **System. proplist. contentviewmodeforsearch** " und " **System. proplist. contentviewmodeforbrowse** "-proplist angegeben sind, bestimmt, was im Inhalts Ansichtsmodus angezeigt wird. Weitere Informationen zu Eigenschafts Listen finden Sie unter [proplist](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).

Die Eigenschaften werden entsprechend den im folgenden Layoutmuster gezeigten Zahlen angeordnet:

![Screenshot mit dem standardlayoutmuster in der Inhaltsansicht](images/propertiesnumberslayoutpattern.png)

Wenn Sie die folgende Liste von Eigenschaften verwenden,


```
prop:~System.ItemNameDisplay;System.Author;System.ItemPathDisplay;~System.Search.AutoSummary;
    System.Size;System.Photo.DateTaken;System.Keywords
```



Anschließend wird die folgende Anzeige angezeigt:

![Screenshot mit Beispiel Eigenschaften Layout](images/samplepropertylayout.png)

> [!Note]  
> Um die beste Lesbarkeit zu erzielen, sollten die Eigenschaften, die in der Spalte ganz rechts angezeigt werden, mit der Bezeichnung gekennzeichnet werden.

 

### <a name="property-list-flags"></a>Eigenschaften Listen-Flags

Nur eines der Flags, das in der proplists-Dokumentation definiert ist, gilt für die Anzeige von Elementen im Content View Mode Layouts: ` "~"` . In den vorherigen Beispielen werden in der Windows-Explorer-Ansicht einige Eigenschaften wie z. b. Beschriftungen `Tags: animals; zoo; lion` . Dies ist das Standardverhalten, wenn Sie eine Eigenschaft in der Liste angeben. Beispielsweise enthält die proplist `"System.Author"` , die als angezeigt wird `"Authors: value"` . Wenn Sie die Eigenschaften Bezeichnung ausblenden möchten, platzieren Sie eine `"~"` vor dem Eigenschaftsnamen. Wenn die proplist beispielsweise ist `"~System.Size"` , wird die Eigenschaft nur als Wert ohne die Bezeichnung angezeigt.

## <a name="previews"></a>Vorschau

Wenn der Benutzer ein Ergebnis Element in Windows-Explorer auswählt und der Vorschaubereich geöffnet ist, wird der Inhalt des Elements in der Vorschau angezeigt.

Der Inhalt, der in der Vorschau angezeigt werden soll, wird durch eine URL angegeben, die wie folgt bestimmt wird:

1.  Wenn die Eigenschaft **System. webpreviewurl** Windows Shell für das Element festgelegt ist, verwenden Sie diese URL.
    > [!Note]  
    > Die-Eigenschaft muss in der RSS mithilfe des Windows Shell-Namespace oder explizit in der OSDX-Datei zugeordnet werden.

     

2.  Wenn dies nicht der Typ ist, verwenden Sie stattdessen die Link-URL.

Diese Logik wird im folgenden Flussdiagramm veranschaulicht.

![Flussdiagramm, das zeigt, wie Windows Explorer die URL für die Vorschau auswählt](images/howwindowsexploreridentifieswhichurltouseforpreviews.png)

Es ist möglich, eine andere URL als Vorschauversion für das Element selbst zu verwenden. Wenn Sie also unterschiedliche URLs für die Link-URL und das Gehäuse oder bereitstellen `media:content URL` , verwendet Windows Explorer die Link-URL für die Vorschau des Elements, verwendet jedoch die andere URL für die Dateityp Erkennung, das Öffnen, das Herunterladen usw.

Bestimmen der zu verwendenden URL durch Windows-Explorer:

1.  Wenn Sie eine Zuordnung zu [System. itemfolderpathdisplay](../properties/props-system-itemfolderpathdisplay.md)bereitstellen, verwendet Windows Explorer diese URL.
2.  Wenn Sie keine Zuordnung bereitstellen, identifiziert Windows Explorer, ob sich die Link-und die Gehäuse-URLs unterscheiden. Wenn dies der Fall ist, verwendet Windows Explorer die Link-URL.
3.  Wenn die URLs identisch sind oder nur eine Link-URL vorhanden ist, analysiert Windows Explorer den Link, um den übergeordneten Container zu suchen, indem der Dateiname aus der vollständigen URL entfernt wird.
    > [!Note]  
    > Wenn Sie erkennen, dass die URL-Verarbeitung zu inaktiven Links für den Dienst führen würde, sollten Sie eine explizite Zuordnung für die Eigenschaft bereitstellen.

     

## <a name="open-file-location-menu-item"></a>Menü Element "Datei Speicherort öffnen"

Wenn Sie mit der rechten Maustaste auf ein Element klicken, wird der Menübefehl **Datei Speicherort öffnen** angezeigt. Mit diesem Befehl wird der Benutzer in den Container für das Element oder den Speicherort dieses Elements gelangen. Wenn Sie z. b. in einer SharePoint-Suche diese Option für eine Datei in einer Dokumentbibliothek auswählen, wird der Stamm der Dokumentbibliothek im Webbrowser geöffnet.

Wenn ein Benutzer auf **Datei Speicherort öffnen** klickt, versucht Windows Explorer, mithilfe der im folgenden Flussdiagramm gezeigten Logik einen übergeordneten Container zu finden:

![Flussdiagramm, das zeigt, wie Windows Explorer einen übergeordneten Container identifiziert](images/howwindowsexploreridentifiesaparentcontainer.png)

## <a name="additional-resources"></a>Weitere Ressourcen

Weitere Informationen zum Implementieren eines Such Verbunds in Remote Datenspeicher mithilfe von OpenSearch-Technologien in Windows 7 und höher finden Sie unter "zusätzliche Ressourcen" bei der [Verbund Suche in Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbundsuche in Windows 10](-search-federated-search-overview.md)
</dt> <dt>

[Ersten Einstieg in die Verbund Suche in Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Verbinden des Webdiensts in der Windows-Verbund Suche](-search-federated-search-web-service.md)
</dt> <dt>

[Aktivieren des Datenspeicher in der Windows-Verbund Suche](-search-federated-search-data-store.md)
</dt> <dt>

[Bewährte Methoden bei der Windows-Verbund Suche](-search-fedsearch-best.md)
</dt> <dt>

[Bereitstellen von Suchconnectors in der Windows-Verbund Suche](-search-federated-search-deploying.md)
</dt> </dl>

 

 
