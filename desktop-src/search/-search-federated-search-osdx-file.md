---
description: Beschreibt, wie sie eine osdx-Datei (OpenSearch Description) erstellen, um externe Datenspeicher mit dem Windows-Client über das OpenSearch verbinden.
ms.assetid: 62cd88cd-e6ff-4e46-887d-e62f7018c065
title: Erstellen einer OpenSearch-Beschreibungsdatei in Windows Verbundsuche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f58b29a860c7d53583b7fd17ddd942bb21b08d649ea7e54d5b2278be2f8d4c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456862"
---
# <a name="creating-an-opensearch-description-file-in-windows-federated-search"></a>Erstellen einer OpenSearch-Beschreibungsdatei in Windows Verbundsuche

Beschreibt, wie sie eine osdx-Datei (OpenSearch Description) erstellen, um externe Datenspeicher über das Windows-Protokoll [mit dem](https://github.com/dewitt/opensearch) OpenSearch verbinden. Mit der Verbundsuche können Benutzer einen Remotedatenspeicher durchsuchen und die Ergebnisse im Windows anzeigen.

Dieses Thema enthält folgende Abschnitte:

-   [OpenSearch Beschreibungsdatei](#opensearch-description-file)
    -   [Erforderliche untergeordnete Mininum-Elemente](#mininum-required-child-elements)
-   [Standardelemente in Windows Verbundsuche](#standard-elements-in-windows-federated-search)
    -   [Shortname](#shortname)
    -   [Beschreibung](#description)
    -   [URL-Vorlage für RSS/Atom-Ergebnisse](#url-template-for-rssatom-results)
    -   [URL-Vorlage für Webergebnisse](#url-template-for-web-results)
    -   [URL-Vorlagenparameter](#url-template-parameters)
    -   [Auspagete Ergebnisse](#paged-results)
    -   [Paging mit dem Elementindex](#paging-using-the-item-index)
    -   [Paging mithilfe des Seitenindexes](#paging-using-the-page-index)
    -   [Seitengröße](#page-size)
-   [Erweiterte Elemente in Windows Verbundsuche](#extended-elements-in-windows-federated-search)
    -   [Maximale Ergebnisanzahl](#maximum-result-count)
    -   [Eigenschaftszuordnung](#property-mapping)
-   [Vorschau](#previews)
-   [Menüelement "Dateispeicherort öffnen"](#open-file-location-menu-item)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="opensearch-description-file"></a>OpenSearch Beschreibungsdatei

Eine OpenSearch Description-Datei (OSDX) für Windows Verbundsuche muss die folgenden Regeln einhalten:

-   Ein gültiges OpenSearch Description-Dokument, wie [](https://github.com/dewitt/opensearch) in der OpenSearch 1.1-Spezifikation definiert.
-   Geben Sie eine URL-Vorlage mit einem RSS- oder Atom-Formattyp an.
-   Verwenden Sie die Dateierweiterung .osdx, oder werden Sie beim Herunterladen aus dem Web mit der Dateierweiterung .osdx verknüpft. Beispielsweise ist ein Server nicht erforderlich, um OSDX zu verwenden. Ein Server kann die Datei mit einer beliebigen Dateinamenerweiterung zurückgeben, z. B. .xml, und so behandelt werden, als wäre es eine OSDX-Datei, wenn der richtige MIME-Typ für OpenSearch Description-Dokumente (OSDX-Dateien) verwendet wird.
-   Geben Sie einen **ShortName-Elementwert** an (empfohlen).

### <a name="mininum-required-child-elements"></a>Erforderliche untergeordnete Mininum-Elemente

Die folgende OSDX-Beispieldatei besteht aus **ShortName** und -Elementen, die `Url` die mindestens erforderlichen untergeordneten Elemente sind.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    <Url format="application/rss+xml" 
        template="https://example.com/rss.php?query=
        {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



## <a name="standard-elements-in-windows-federated-search"></a>Standardelemente in Windows Verbundsuche

Zusätzlich zu den untergeordneten Mindestelementen unterstützt die Verbundsuche die folgenden Standardelemente.

### <a name="shortname"></a>Shortname

Windows verwendet den **ShortName-Elementwert,** um die Datei .searchconnector-ms (Search Connector) zu benennen, die erstellt wird, wenn der Benutzer die OSDX-Datei öffnet. Windows wird sichergestellt, dass der generierte Dateiname nur Zeichen verwendet, die in Windows zulässig sind. Wenn kein **ShortName-Wert** angegeben wird, versucht die Datei .searchconnector-ms stattdessen, den Dateinamen der OSDX-Datei zu verwenden.

Der folgende Code veranschaulicht die Verwendung des **ShortName-Elements** in einer OSDX-Datei.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    <ShortName>My web Service</ShortName>
    ...
</OpenSearchDescription>
```



### <a name="description"></a>BESCHREIBUNG

Windows verwendet den  Description-Elementwert, um die Dateibeschreibung zu füllen, die im Detailbereich des Windows-Explorers angezeigt wird, wenn ein Benutzer eine SEARCHCONNECTOR-MS-Datei auswählt.


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Description>Searches the example company book catalog</Description>
</OpenSearchDescription>
```



### <a name="url-template-for-rssatom-results"></a>URL-Vorlage für RSS/Atom-Ergebnisse

Die OSDX-Datei muss ein **URL-Formatelement** und ein Vorlagenattribut (eine URL-Vorlage) enthalten, die Ergebnisse entweder im RSS- oder Atom-Format zurückgibt.  Das Formatattribut muss für RSS-formatierte Ergebnisse oder für Atom-formatierte Ergebnisse auf festgelegt werden, wie `application/rss+xml` im folgenden Code `application/atom+xml` gezeigt.

> [!Note]  
> Das **URL-Formatelement** **und das Vorlagenattribut** werden häufig als URL-Vorlage bezeichnet.

 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
   ...
        <Url format="application/rss+xml" template="https://example.com/rss.php?query=
            {searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
</OpenSearchDescription>
```



### <a name="url-template-for-web-results"></a>URL-Vorlage für Webergebnisse

Wenn eine Version der Suchergebnisse in einem Webbrowser angezeigt werden kann, sollten Sie ein **Url format=-Element** und ein Vorlagenattribut angeben, wie im folgenden `text/html` Code gezeigt. 


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
    ...
    <Url format="text/html" template="https://example.com/html.php?query={searchTerms}" />
</OpenSearchDescription>
```



Wenn Sie ein **Url format="text/html"-Element** und ein Vorlagenattribut angeben, wird in der Befehlsleiste des Windows-Explorers eine Schaltfläche angezeigt, wie im folgenden Screenshot gezeigt, mit der der Benutzer einen Webbrowser öffnen kann, um die Suchergebnisse anzuzeigen, wenn der Benutzer eine Abfrage ausführt. 

![Screenshot der Rolloverschaltfläche für die Websuche.](images/websearchroll-overcommandbarbutton.png)

Das Rollover der Abfrage zurück zur Webbenutzeroberfläche des Datenspeichers ist in einigen Szenarien wichtig. Beispielsweise kann ein Benutzer mehr als 100 Ergebnisse anzeigen (die Standardanzahl von Elementen, die der OpenSearch an fordert). Falls ja, kann der Benutzer auch Suchfunktionen verwenden, die nur auf der Website des Datenspeichers verfügbar sind, z. B. erneutes Abfragen mit einer anderen Sortierreihenfolge oder Pivotieren und Filtern der Abfrage mit verknüpften Metadaten.

### <a name="url-template-parameters&quot;></a>URL-Vorlagenparameter

Der OpenSearch-Anbieter führt immer die folgenden Aktionen aus:

1.  Verwendet die URL-Vorlage, um die Anforderung an den Webdienst zu senden.
2.  Versucht, die in der URL-Vorlage gefundenen Token zu ersetzen, bevor die Anforderung wie folgt an den Webdienst sendet:
    -   Ersetzt die Standardtoken OpenSearch, die in der folgenden Tabelle aufgeführt sind.
    -   Entfernt alle Token, die in der folgenden Tabelle nicht aufgeführt sind.



| Unterstütztes Token  | Verwendung durch OpenSearch Anbieter                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| {searchTerms}    | Ersetzt durch die Suchbegriffe, die der Benutzer in das Sucheingabefeld Windows Explorer ein gibt.<br/>                                         |
| {startIndex}     | Wird beim Abrufen von Ergebnissen in &quot;Seiten&quot; verwendet.<br/> Wird durch den Index für das erste Ergebniselement ersetzt, das zurückkommen soll.<br/>                        |
| {startPage}      | Wird beim Abrufen von Ergebnissen in &quot;Seiten&quot; verwendet.<br/> Ersetzt durch die Seitennummer des Sets von Suchergebnissen, die zurückgeben werden.<br/>               |
| {count}          | Wird beim Abrufen von Ergebnissen in &quot;Seiten&quot; verwendet.<br/> Ersetzt durch die Anzahl von Suchergebnissen pro Seite, die Windows Explorer-Anforderungen enthält.<br/> |
| {language}       | Wird durch eine Zeichenfolge ersetzt, die die Sprache der gesendeten Abfrage angibt.<br/>                                                          |
| {inputEncoding}  | Ersetzt durch eine Zeichenfolge (z. B. &quot;UTF-16"), die die Zeichencodierung der gesendeten Abfrage angibt.<br/>                                |
| {outputEncoding} | Ersetzt durch eine Zeichenfolge (z. B. "UTF-16"), die die gewünschte Zeichencodierung für die Antwort vom Webdienst angibt.<br/>       |



 

### <a name="paged-results"></a>Auspagete Ergebnisse

Möglicherweise möchten Sie die Anzahl der pro Anforderung zurückgegebenen Ergebnisse begrenzen. Sie können eine "Seite" der Ergebnisse gleichzeitig zurückgeben oder den OpenSearch-Anbieter dazu berechten, zusätzliche Seiten der Ergebnisse entweder nach Elementnummer oder Seitennummer zu erhalten. Wenn Sie beispielsweise 20 Ergebnisse pro Seite senden, beginnt die erste Seite, die Sie senden, bei Elementindex 1 und bei Seite 1. Die zweite Seite, die Sie senden, beginnt bei Elementindex 21 und bei Seite 2. Sie können definieren, wie der OpenSearch-Anbieter Elemente anfordern soll, indem Sie entweder das - oder das `{startItem}` `{startPage}` -Token in der URL-Vorlage verwenden.

### <a name="paging-using-the-item-index"></a>Paging mit dem Elementindex

Ein Elementindex identifiziert das erste Ergebniselement auf einer Ergebnisseite. Wenn Clients Anforderungen mithilfe eines Elementindexes senden möchten, können Sie das Token in Ihrem Url-Elementvorlagenattribut verwenden, wie `{startIndex}` im folgenden Code gezeigt.  


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}" />
```



Der [OpenSearch](https://github.com/dewitt/opensearch) ersetzt dann das Token in der URL durch einen Startindexwert. Die erste Anforderung beginnt mit dem ersten Element, wie im folgenden Beispiel veranschaulicht:


```
https://example.com/rss.php?query=frogs&start=1
```



Der OpenSearch kann zusätzliche Elemente erhalten, indem er den `{startIndex}` Parameterwert ändert und eine neue Anforderung ausgibt. Der Anbieter wiederholt diesen Prozess, bis er genügend Ergebnisse erhält, um seinen Grenzwert zu erfüllen, oder das Ende der Ergebnisse erreicht. Der OpenSearch-Anbieter untersucht die Anzahl der Elemente, die vom Webdienst auf der ersten Seite der Ergebnisse zurückgegeben werden, und legt die erwartete Seitengröße auf diese Anzahl fest. Sie verwendet diese Zahl, um den Wert `{startIndex}` für nachfolgende Anforderungen zu erhöhen. Wenn der Webdienst beispielsweise 20 Ergebnisse in der ersten Anforderung zurückgibt, legt der Anbieter die erwartete Seitengröße auf 20 fest. Bei der nächsten Anforderung ersetzt der Anbieter durch den Wert `{startIndex}` 21, um die nächsten 20 Elemente zu erhalten.

> [!Note]  
> Wenn eine Seite mit Ergebnissen, die vom Webdienst zurückgegeben wird, weniger Elemente als die erwartete Seitengröße enthält, geht der OpenSearch-Anbieter davon aus, dass er die letzte Ergebnisseite empfangen hat und keine Anforderungen mehr stellt.

 

### <a name="paging-using-the-page-index"></a>Paging mithilfe des Seitenindexes

Ein Seitenindex identifiziert die angegebene Ergebnisseite. Wenn Sie möchten, dass Clients Anforderungen mithilfe einer Seitenzahl senden, können Sie das Token im Vorlagenattribut des URL-Formatelements verwenden, um dies anzugeben, wie im folgenden `{startPage}` Beispiel veranschaulicht:  


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;page={startPage}" />
```



Der OpenSearch-Anbieter ersetzt dann das Token in der URL durch einen Seitennummernparameter. Die erste Anforderung beginnt mit der ersten Seite, wie im folgenden Beispiel gezeigt:


```
https://example.com/rss.php?query=frogs&page=1
```



> [!Note]  
> Wenn eine vom Webdienst zurückgegebene Seite mit Ergebnissen weniger Elemente als die erwartete Seitengröße enthält, geht der OpenSearch Anbieter davon aus, dass er die letzte Ergebnisseite empfangen hat und keine Anforderungen mehr stellt.

 

### <a name="page-size"></a>Page Size

Möglicherweise möchten Sie Ihren Webdienst so konfigurieren, dass eine Anforderung die Größe der Seiten mithilfe eines Parameters in der URL angeben kann. Eine Anforderung muss in der OSDX-Datei mithilfe des Tokens wie folgt angegeben `{count}` werden:


```
<Url format="application/rss+xml" 
    template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
```



Der [OpenSearch](https://github.com/dewitt/opensearch) Anbieter kann dann die gewünschte Seitengröße in Der Anzahl der Ergebnisse pro Seite festlegen, wie im folgenden Beispiel gezeigt:


```
https://example.com/rss.php?query=frogs&start=1&cnt=50
```



Standardmäßig stellt der OpenSearch-Anbieter Anforderungen mit einer Seitengröße von 50. Wenn Sie eine andere Seitengröße wünschen, geben Sie kein Token an, und platzieren Sie `{count}` stattdessen die gewünschte Zahl direkt im **Url-Vorlagenelement.**

Der OpenSearch-Anbieter bestimmt die Seitengröße basierend auf der Anzahl der Ergebnisse, die bei der ersten Anforderung zurückgegeben werden. Wenn die erste Seite der empfangenen Ergebnisse weniger Elemente enthält als die angeforderte Anzahl, setzt der Anbieter die Seitengröße für alle nachfolgenden Seitenanforderungen zurück. Wenn nachfolgende Seitenanforderungen weniger Elemente als angefordert zurückgeben, geht der OpenSearch Anbieter davon aus, dass er das Ende der Ergebnisse erreicht hat.

## <a name="extended-elements-in-windows-federated-search"></a>Erweiterte Elemente in Windows Verbundsuche

Zusätzlich zu den Standardelementen unterstützt die Verbundsuche die folgenden erweiterten Elemente: **MaximumResultCount** und **ResultsProcessing.**

Da diese erweiterten untergeordneten Elemente in der [OpenSearch](https://github.com/dewitt/opensearch) v1.1-Spezifikation nicht unterstützt werden, müssen sie mit dem folgenden Namespace hinzugefügt werden:


```
http://schemas.microsoft.com/opensearchext/2009/
```



### <a name="maximum-result-count"></a>Maximale Ergebnisanzahl

Standardmäßig sind Suchconnectors auf 100 Ergebnisse pro Benutzerabfrage beschränkt. Dieser Grenzwert kann angepasst werden, indem das **MaximumResultCount-Element** in die OSD-Datei eingeschlossen wird, wie im folgenden Beispiel gezeigt:


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/" 
    xmlns:ms-ose="http://schemas.microsoft.com/opensearchext/2009/">
        ...
        <ms-ose:MaximumResultCount>200</ms-ose:MaximumResultCount>
</OpenSearchDescription>
```



Im vorherigen Beispiel wird das Namespacepräfix `ms-ose` im **OpenSearchDescription-Element** der obersten Ebene deklariert und dann als Präfix im Elementnamen verwendet. Diese Deklaration ist erforderlich, da **MaximumResultCount** in der [OpenSearch](https://github.com/dewitt/opensearch) v1.1-Spezifikation nicht unterstützt wird.

### <a name="property-mapping"></a>Eigenschaftszuordnung

Wenn Ergebnisse vom Webdienst als RSS- oder Atom-Feed zurückgegeben werden, muss der OpenSearch Anbieter die Elementmetadaten in den Feeds Eigenschaften zuordnen, die die Windows Shell verwenden kann. Der folgende Screenshot veranschaulicht, wie der OpenSearch-Anbieter einige der RSS-Standardelemente zuschaut.

![Screenshot der integrierten Eigenschaftenzuordnungen "rss-to-windows-shell"](images/built-inrsstowindowsshellpropertymappings.png)

### <a name="default-mappings"></a>Standardzuordnungen

Die Standardzuordnungen von RSS-XML-Elementen zu Windows Shell-Systemeigenschaften sind in der folgenden Tabelle aufgeführt. XML-Pfade sind relativ zum Elementelement. Das `"media:"` Präfix wird durch den [Yahoo Search-Namespace](https://www.rssboard.org/media-rss) definiert.



| RSS-XML-Pfad                  | Windows Shell-Eigenschaft (kanonischer Name) |
|-------------------------------|-----------------------------------------|
| Link                          | System.ItemUrl                          |
| Titel                         | System.ItemName                         |
| Autor                        | System.Author                           |
| Pubdate                       | System.DateModified                     |
| BESCHREIBUNG                   | System.AutoSummary                      |
| Kategorie                      | System.Keywords                         |
| enclosure/@type               | System.MIMEType                         |
| enclosure/@length             | System.Size                             |
| enclosure/@url                | System.ContentUrl                       |
| media:category                | System.Keywords                         |
| media:content/@fileSize       | System.Size                             |
| media:content/@type           | System.MIMEType                         |
| media:content/@url            | System.ContentUrl                       |
| media:group/content/@fileSize | System.Size                             |
| media:group/content/@type     | System.MIMEType                         |
| media:group/content/@url      | System.ContentUrl                       |
| media:thumbnail/@url          | System.ItemThumbnailUrl                 |



 

> [!Note]  
> Zusätzlich zu den Standardzuordnungen von RSS- oder Atom-Standardelementen können Sie andere Windows Shell-Systemeigenschaften zuordnen, indem Sie zusätzliche XML-Elemente in den Windows Namespace für jede der Eigenschaften einschließen. Sie können auch Elemente aus anderen vorhandenen XML-Namespaces wie MediaRSS, iTunes usw. zuordnen, indem Sie der OSDX-Datei eine benutzerdefinierte Eigenschaftenzuordnung hinzufügen.

 

### <a name="custom-property-mappings"></a>Benutzerdefinierte Eigenschaftenzuordnungen

Sie können die Zuordnung von Elementen aus der RSS-Ausgabe zu Windows Shell-Systemeigenschaften anpassen, indem Sie die Zuordnung in der OSDX-Datei angeben.

Die RSS-Ausgabe gibt Folgendes an:

-   Einen XML-Namespace und
-   Für alle untergeordneten Elemente eines Elements ein Elementname, dem zugeordnet werden soll.

Die OSDX-Datei identifiziert eine Windows Shell-Eigenschaft für jeden Elementnamen in einem Namespace. Die Eigenschaftenzuordnungen, die Sie in Ihrer OSDX-Datei definieren, überschreiben die Standardzuordnungen für diese angegebenen Eigenschaften, sofern vorhanden.

Das folgende Diagramm veranschaulicht, wie eine RSS-Erweiterung Windows Eigenschaften (kanonischer Name) zugeordnet wird.

![Diagramm, das zeigt, dass die Kombination aus xml-Namespace und XML-Pfad den kanonischen Namen erzeugt](images/rssextensionsusexmlnamespaceandpathstomaptowindowsproperties.png)

### <a name="example-rss-results-and-osd-property-mapping"></a>Rss-Beispielergebnisse und OSD-Eigenschaftenzuordnung

Die folgende RSS-Beispielausgabe identifiziert `https://example.com/schema/2009` als XML-Namespace mit dem Präfix "example". Dieses Präfix muss erneut vor dem **E-Mail-Element** angezeigt werden.


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009">
   ...
    <item>
      <title>Someone</title>
      <example:email>Someone@example.com</example:email>
    </item>
```



In der folgenden OSDX-Beispieldatei wird das **XML-E-Mail-Element** der Windows Shell-Eigenschaft [System.Contact.EmailAddress](../properties/props-system-contact-emailaddress.md)zugeordnet.


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



Es gibt einige Eigenschaften, die nicht zugeordnet werden können, da werte für sie später entweder überschrieben oder nicht bearbeitet werden können. Beispielsweise können [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) oder [System.ItemPathDisplayNarrow](../properties/props-system-itempathdisplaynarrow.md) nicht zugeordnet werden, da sie aus dem URL-Wert berechnet werden, der entweder in den Link- oder Gehäuseelementen angegeben ist.

### <a name="thumbnails"></a>Miniaturbilder

UrLs für Miniaturansichtsbilder können für jedes Element bereitgestellt werden, indem das **element media:thumbnail url=""** verwendet wird. Die ideale Auflösung ist 150 x 150 Pixel. Die größten unterstützten Miniaturansichten sind 256 x 256 Pixel. Die Bereitstellung größerer Images nimmt mehr Bandbreite in Anspruch, ohne dass der Benutzer einen zusätzlichen Vorteil hat.

### <a name="open-file-location-context-menu"></a>Kontextmenü "Dateispeicherort öffnen"

Windows stellt ein Kontextmenü mit dem Namen **Dateispeicherort** öffnen für Ergebniselemente bereit. Wenn der Benutzer ein Element aus diesem Menü auswählt, wird die "übergeordnete" URL für das ausgewählte Element geöffnet. Wenn es sich bei der URL um eine Web-URL wie handelt, `https://...` wird der Webbrowser geöffnet und zu dieser URL navigiert. Ihr Feed sollte eine benutzerdefinierte URL für jedes Element bereitstellen, um sicherzustellen, dass Windows eine gültige URL öffnet. Dies kann erreicht werden, indem die URL in ein Element in den XML-Code des Elements eingeschlossen wird, wie im folgenden Beispiel veranschaulicht:


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



Wenn diese Eigenschaft nicht explizit im XML-Code des Elements festgelegt ist, legt der OpenSearch Anbieter sie auf den übergeordneten Ordner der URL des Elements fest. Im obigen Beispiel verwendet der OpenSearch-Anbieter den Linkwert und legt den [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md) Windows Shell-Eigenschaftswert auf `"https://example.com/"` fest.

### <a name="customize-windows-explorer-views-with-property-description-lists"></a>Anpassen Windows Explorer-Ansichten mit Eigenschaftenbeschreibungslisten

Einige Windows Explorer-Ansichtslayouts werden durch Eigenschaftenbeschreibungslisten oder Proplists definiert. Eine Proplist ist eine durch Semikolons getrennte Liste von Eigenschaften, z. B. `"prop:System.ItemName; System.Author"` , die verwendet wird, um zu steuern, wie Ihre Ergebnisse in Windows Explorer angezeigt werden.

Die Benutzeroberflächenbereiche von Windows Explorer, die mithilfe von Proplists angepasst werden können, werden im folgenden Screenshot veranschaulicht:

![Screenshot der Ui-Bereiche des Windows-Explorers, die mithilfe von Proplists angepasst werden können](images/areasofwindowsexplorerthatyoucancontrolwithproplists.png)

Jedem Bereich von Windows Explorer ist ein Satz von Proplists zugeordnet, die selbst als Eigenschaften angegeben werden. Sie können benutzerdefinierte Proplists für einzelne Elemente in Ihren Resultsets oder für alle Elemente in einem Satz von Ergebnissen angeben.



| Benutzeroberflächenbereich zum Anpassen               | Windows Shell-Eigenschaft, die die Anpassung implementiert |
|------------------------------------|----------------------------------------------------------|
| Inhaltsansichtsmodus (beim Suchen) | System.PropList.ContentViewModeForSearch                 |
| Inhaltsansichtsmodus (beim Durchsuchen)  | System.PropList.ContentViewModeForBrowse                 |
| Kachelansichtsmodus                     | System.PropList.TileInfo                                 |
| Detailbereich                       | System.PropList.PreviewDetails                           |
| Infotip (QuickInfo zum Hovern des Elements)     | System.PropList.Infotip                                  |



 

 

**So geben Sie eine eindeutige Proplist für ein einzelnes Element an:**

1.  Fügen Sie in der RSS-Ausgabe ein benutzerdefiniertes Element hinzu, das die Proplist darstellt, die Sie anpassen möchten. Im folgenden Beispiel wird beispielsweise die Liste für den Detailbereich definiert:
    ```
    <win:System.PropList.PreviewDetails>
        prop:System.ItemName;System.Author</win:System.PropList.PreviewDetails>
    ```

    

2.  Um eine Eigenschaft auf jedes Element in den Suchergebnissen anzuwenden, ohne die RSS-Ausgabe zu ändern, geben Sie eine Proplist innerhalb eines **ms-ose:PropertyDefaultValues-Elements** in der OSDX-Datei an, wie im folgenden Beispiel gezeigt:

    ```
    <ms-ose:ResultsProcessing format="application/rss+xml">
        <ms-ose:PropertyDefaultValues>
          <ms-ose:Property schema="http://schemas.microsoft.com/windows/2008/propertynamespace"
            name="System.PropList.ContentViewModeForSearch">prop:~System.ItemNameDisplay;System.Photo.DateTaken;
            ~System.ItemPathDisplay;~System.Search.AutoSummary;System.Size;System.Author;System.Keywords</ms-ose:Property>
        </ms-ose:PropertyDefaultValues>
      </ms-ose:ResultsProcessing>
    ```

    

### <a name="content-view-mode-layout-of-properties"></a>Layout der Eigenschaften im Inhaltsansichtsmodus

Die Liste der Eigenschaften, die in den Proplists **System.PropList.ContentViewModeForSearch** und **System.PropList.ContentViewModeForBrowse** angegeben sind, bestimmt, was im Inhaltsansichtsmodus angezeigt wird. Weitere Informationen zu Eigenschaftenlisten finden Sie unter [PropList](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).

Die Eigenschaften werden entsprechend den Zahlen im folgenden Layoutmuster festgelegt:

![Screenshot: Standardlayoutmuster in der Inhaltsansicht](images/propertiesnumberslayoutpattern.png)

Wenn wir die folgende Liste von Eigenschaften verwenden,


```
prop:~System.ItemNameDisplay;System.Author;System.ItemPathDisplay;~System.Search.AutoSummary;
    System.Size;System.Photo.DateTaken;System.Keywords
```



Dann wird die folgende Anzeige angezeigt:

![Screenshot, der das Layout der Beispieleigenschaft zeigt.](images/samplepropertylayout.png)

> [!Note]  
> Um die bestmögliche Lesbarkeit zu gewährleisten, sollten die in der Spalte ganz rechts angezeigten Eigenschaften mit bezeichnungiert werden.

 

### <a name="property-list-flags"></a>Eigenschaftenlistenflags

Nur eines der flags, die in der Proplists-Dokumentation definiert sind, gilt für die Anzeige von Elementen in Layouts im Inhaltsansichtsmodus: ` "~"` . In den vorherigen Beispielen bezeichnet Windows Explorer einige der Eigenschaften, z. B. `Tags: animals; zoo; lion` . Dies ist das Standardverhalten, wenn Sie eine Eigenschaft in der Liste angeben. Beispielsweise verfügt die Proplist über `"System.Author"` , die als angezeigt `"Authors: value"` wird. Wenn Sie die Eigenschaftenbezeichnung ausblenden möchten, platzieren Sie vor `"~"` dem Eigenschaftennamen eine . Wenn die Proplist z. B. auf hat, wird die Eigenschaft nur als Wert `"~System.Size"` ohne die Bezeichnung angezeigt.

## <a name="previews"></a>Vorschau

Wenn der Benutzer ein Ergebniselement im Windows Explorer auswählt und der Vorschaubereich geöffnet ist, wird der Inhalt des Elements in der Vorschau angezeigt.

Der inhalt, der in der Vorschau angezeigt werden soll, wird durch eine URL angegeben, die wie folgt bestimmt wird:

1.  Wenn die **Eigenschaft System.WebPreviewUrl** Windows Shell für das Element festgelegt ist, verwenden Sie diese URL.
    > [!Note]  
    > Die -Eigenschaft muss im RSS mithilfe des Windows Shell-Namespace bereitgestellt oder explizit in der OSDX-Datei zugeordnet werden.

     

2.  Falls nicht, verwenden Sie stattdessen die Link-URL.

Im folgenden Flussdiagramm wird diese Logik veranschaulicht.

![Flussdiagramm, das zeigt, wie der Windows-Explorer die URL auswählt, die für Vorschauversionen verwendet werden soll](images/howwindowsexploreridentifieswhichurltouseforpreviews.png)

Es ist möglich, für die Vorschauversion eine andere URL als für das Element selbst zu verwenden. Wenn Sie also unterschiedliche URLs für die Link-URL und das Gehäuse oder angeben, verwendet Windows Explorer die Link-URL für Vorschauen des Elements, verwendet jedoch die andere URL für die Erkennung, das Öffnen, Herunterladen `media:content URL` usw.

Wie Windows Explorer bestimmt, welche URL verwendet werden soll:

1.  Wenn Sie eine Zuordnung zu [System.ItemFolderPathDisplay](../properties/props-system-itemfolderpathdisplay.md)bereitstellen, verwendet Windows Explorer diese URL.
2.  Wenn Sie keine Zuordnung bereitstellen, ermittelt Windows Explorer, ob die Link- und Gehäuse-URLs unterschiedlich sind. Wenn ja, verwendet Windows Explorer die Link-URL.
3.  Wenn die URLs identisch sind oder es nur eine Link-URL gibt, analysiert Windows Explorer den Link, um den übergeordneten Container zu finden, indem der Dateiname aus der vollständigen URL entfernt wird.
    > [!Note]  
    > Wenn Sie erkennen, dass die URL-Analyse zu in dead-Links für Ihren Dienst führen würde, sollten Sie eine explizite Zuordnung für die Eigenschaft bereitstellen.

     

## <a name="open-file-location-menu-item"></a>Menüelement "Dateispeicherort öffnen"

Wenn ein mit der rechten Maustaste auf ein Element klickt, wird der **Menübefehl Dateispeicherort** öffnen angezeigt. Dieser Befehl führt den Benutzer zum Container für oder zum Speicherort dieses Elements. Wenn Sie in einer SharePoint beispielsweise diese Option für eine Datei in einer Dokumentbibliothek auswählen, wird das Stammverzeichnis der Dokumentbibliothek im Webbrowser geöffnet.

Wenn ein Benutzer auf Dateispeicherort **öffnen klickt,** Windows Explorer versucht, einen übergeordneten Container mithilfe der im folgenden Flussdiagramm gezeigten Logik zu finden:

![Flussdiagramm, das zeigt, wie der Windows-Explorer einen übergeordneten Container identifiziert](images/howwindowsexploreridentifiesaparentcontainer.png)

## <a name="additional-resources"></a>Weitere Ressourcen

Weitere Informationen zum Implementieren eines Suchverbunds in Remotedatenspeicher mithilfe von OpenSearch-Technologien in Windows 7 und höher finden Sie unter "Zusätzliche Ressourcen" unter Verbundsuche [in Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbundsuche in Windows 10](-search-federated-search-overview.md)
</dt> <dt>

[Erste Schritte mit Der Verbundsuche in Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Verbinden Ihres Webdiensts in Windows Verbundsuche](-search-federated-search-web-service.md)
</dt> <dt>

[Aktivieren Ihrer Store in Windows Verbundsuche](-search-federated-search-data-store.md)
</dt> <dt>

[Bewährte Methoden bei der Windows Verbundsuche](-search-fedsearch-best.md)
</dt> <dt>

[Bereitstellen von Suchconnectors in Windows Verbundsuche](-search-federated-search-deploying.md)
</dt> </dl>

 

 
