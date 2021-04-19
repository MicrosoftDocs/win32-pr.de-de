---
description: Erläutert, wie Sie den Zugriff auf Ihren Datenspeicher über einen OpenSearch-Webdienst aktivieren und wie Sie potenzielle Barrieren dafür vermeiden.
ms.assetid: 27d7676c-f4e8-43b4-856b-826e07afcd78
title: Aktivieren des Datenspeicher in der Windows-Verbund Suche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cef227cb82c64f391ec61b2a7fef0fe35acf131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346913"
---
# <a name="enabling-your-data-store-in-windows-federated-search"></a>Aktivieren des Datenspeicher in der Windows-Verbund Suche

Erläutert, wie Sie den Zugriff auf Ihren Datenspeicher über einen [OpenSearch](https://github.com/dewitt/opensearch) -Webdienst aktivieren und wie Sie potenzielle Barrieren dafür vermeiden.

Dieses Thema ist wie folgt organisiert:

-   [Bedingungen für die Akzeptanz von Suchanforderungen](#conditions-for-search-request-acceptance)
    -   [Unterstützte Abfrage Syntax](#supported-query-syntax)
    -   [Unterstützte Authentifizierungsprotokolle](#supported-authentication-protocols)
-   [Senden von Abfragen und Zurückgeben von Suchergebnissen in RSS oder Atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [Beispiel für eine RSS-Feed-Ausgabe](#example-of-an-rss-feed-output)
-   [Automatische Zuordnung zu Windows Shell-Eigenschaften](#automatic-mapping-to-windows-shell-properties)
-   [Grundlegendes zur Zuordnung von Elementen zu Dateitypen in Windows](#understanding-how-windows-maps-items-to-file-types)
-   [Vermeiden potenzieller Barrieren für die Aktivierung eines Datenspeicher](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a>Bedingungen für die Akzeptanz von Suchanforderungen

Der [OpenSearch](https://github.com/dewitt/opensearch) -Webdienst, den Sie auf dem Webserver erstellen, **muss** die folgenden zwei Anforderungen erfüllen:

-   Es ist möglich, eine `GET URL` Abfrage vom Client zu akzeptieren.
-   Erlauben Sie, dass die Suchbegriffe in die URL eingebettet werden.

    Im folgenden Beispiel wird gezeigt, wie ein Suchbegriff in eine URL eingebettet werden kann.

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> Die Verbund Suche unterstützt das Senden `POST` von Anforderungen an einen Webdienst nicht.

 

Weitere Informationen zum Erstellen einer URL finden Sie unter "URL-Vorlagen Parameter" unter [Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche](-search-federated-search-osdx-file.md).

### <a name="supported-query-syntax"></a>Unterstützte Abfrage Syntax

In Windows 7 wird keine bestimmte Abfrage Syntax erwartet. Der OpenSearch-Anbieter akzeptiert alle Bedingungen, die der Benutzer in das Eingabefeld in Windows-Explorer eingibt, und codiert ihn in die URL. Dies erfolgt entsprechend der URL-Vorlage, die unter "URL-Vorlagen Parameter" unter [Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche](-search-federated-search-osdx-file.md)beschrieben wird.

Benutzer erwarten, dass separate Begriffe als implizit und zusammen behandelt werden. Eine Abfrage für "Microsoft Windows" sollte z. b. nur Ergebnisse zurückgeben, die sowohl "Windows" als auch "Microsoft" enthalten.

### <a name="supported-authentication-protocols"></a>Unterstützte Authentifizierungsprotokolle

Windows Federated Search unterstützt die Windows-basierte Authentifizierung und kann über die folgenden Protokolle Anmelde Informationen für Webdienste bereitstellen:

-   NTLM.
-   Kerberos.
-   Basic (nur über HTTPS).
-   Andere unter Windows installierte SSPs (Security Support Providers), die zusätzliche Abfrage Kapazität bereitstellen. In der Dokumentation zum [SSP Interface](../secauthn/sspi.md) SDK finden Sie Informationen zum möglichen Hinzufügen anderer SSPs.

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Senden von Abfragen und Zurückgeben von Suchergebnissen in RSS oder Atom

Der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter ist für die Zuordnung der XML-Element Werte zu den Windows Shell-Systemeigenschaften zuständig, die von Windows-Anwendungen verwendet werden können. Sie sind jedoch nicht auf die Standard Zuordnungen von RSS-oder Atom-Standardelementen beschränkt und können benutzerdefinierte XML-Elemente in den Windows-Namespace für jede der Eigenschaften einschließen. Beispielsweise können Sie eigene benutzerdefinierte XML-Elemente innerhalb des **Item** -Elements hinzufügen, um Windows zusätzliche Metadaten bereitzustellen. Sie können auch Elemente aus anderen XML-Namespaces zuordnen, z. b. iTunes.

### <a name="example-of-an-rss-feed-output"></a>Beispiel für eine RSS-Feed-Ausgabe

In der folgenden Beispielausgabe des RSS-Feeds wird ein Element zurückgegeben.


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, you'd be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



Ausführlichere Informationen zur Eigenschaften Zuordnung finden Sie in den Abschnitten "Erweiterte Elemente in der Windows-Verbund Suche" und "benutzerdefinierte Eigenschafts Zuordnungen" unter [Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche](-search-federated-search-osdx-file.md).

## <a name="automatic-mapping-to-windows-shell-properties"></a>Automatische Zuordnung zu Windows Shell-Eigenschaften

Innerhalb der Elemente im RSS-Feed können Sie andere XML-Elemente einschließen, die automatisch den Windows Shell-Systemeigenschaften zugeordnet werden. Fügen Sie zu diesem Zweck ein Element mit dem Namen nach der Windows-shelleigenschaft ein, das dem Windows-shellsystem-Namespace vorangestellt ist. Das folgende Beispiel veranschaulicht die Namespace Deklaration `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` und die Einbindung eines Elements für die Eigenschaften Zuordnung `win:System.Contact.PrimaryEmailAddress` :


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



Das hier verwendete Namespace Präfix ( `"win"` ) ist ein Vorschlag. Sie können ein beliebiges Präfix verwenden. Allerdings müssen Sie die genauen Windows Shell-Eigenschaftsnamen verwenden und den exakten Uniform Resource Identifier (URI) einschließen, wie im folgenden Beispiel gezeigt:


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



**Informationen zu Windows Shell-System Eigenschaften**

Windows definiert eine komplette Liste der [System Eigenschaften](../properties/props.md) und das Werttyp Format, das für jede Eigenschaft erforderlich ist. Die Dokumentation für die Fenster shelleigenschaft [System. FileExtension](../properties/props-system-fileextension.md) gibt z. b. an, dass der Wert den führenden Punkt (". docx" und nicht "docx") enthalten muss.

**Werte für Datum und Uhrzeit**

Das bevorzugte Datums-und Uhrzeit Format ist ISO-8601, wie im folgenden Beispiel gezeigt:


```
2008-01-16T 19:20:30:.45+01:00
```



.NET-Entwickler sollten die DateTime-Klasse mit verwenden `ToString("R") ` , um das richtige Format auszugeben.

Ausführlichere Informationen zur Eigenschaften Zuordnung finden Sie unter "Erweiterte Elemente in der Windows-Verbund Suche" unter [Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche](-search-federated-search-osdx-file.md).

## <a name="understanding-how-windows-maps-items-to-file-types"></a>Grundlegendes zur Zuordnung von Elementen zu Dateitypen in Windows

Durch die Suche in der Windows-Explorer-Benutzeroberfläche können Benutzer Ergebnisse als Dateien behandeln, wenn ein RSS-Element auf eine remote gespeicherte Datei verweist. Der Benutzer kann Elemente per Drag & amp; Drop auf den Desktop verschieben, und die Windows-Explorer-Benutzeroberfläche zeigt das richtige Symbol an und stellt das entsprechende Kontextmenü bereit. Wenn das RSS-Element nicht auf eine remote gespeicherte Datei verweist, wird die Datei als Link behandelt, und Benutzer können Aktionen ausführen, z. b. das Erstellen einer Verknüpfung oder das Öffnen im Browser.

Im folgenden Flussdiagramm wird gezeigt, wie Windows den Dateityp eines Elements bestimmt.

![Flussdiagramm, das Pfade von einem Element zu Entscheidungen anzeigt, um es als weblinktyp Element oder als Dateityp zu behandeln](images/determineanitemfiletype.png)

Der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter führt die folgenden Schritte aus, um ein Element einem Dateityp zuzuordnen:

-   Identifizieren Sie, ob das Element als Datei oder Weblink behandelt werden soll.
-   Identifizieren Sie die korrekte zu verwendende Dateinamenerweiterung.

Wenn das Element z. b. über eine Link-URL verfügt, die einen Dateisystempfad verwendet (z `file:///\\server\share\etc\item.ext` . b.), behandelt der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter den Link als Datei und bestimmt den Typ anhand der Dateinamenerweiterung, die im Pfad verwendet wird (in diesem Beispiel. ext).

Wenn das Element das standardmäßige RSS-Gehäuse oder das **mediarss Media: Content** -Element verwendet, geht der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter davon aus, dass das Element eine Datei ist, und identifiziert die Dateinamenerweiterung wie folgt:

-   Wenn die Windows Shell-Eigenschaft [System. FileExtension](../properties/props-system-fileextension.md) dem Element zugeordnet wurde, verwendet der Anbieter diese Dateinamenerweiterung.
-   Wenn die Windows Shell-Eigenschaft [System. FileExtension](../properties/props-system-fileextension.md) nicht zugeordnet wurde, verwendet der Anbieter das **Type** -Attribut, das im Gehäuse-oder Content-Element angegeben ist. Dieses Element sollte eine `MIMEType` Zeichenfolge enthalten, z `"image/jpeg"` . b.. Wenn der `MIMEType` einer Dateinamenerweiterung zugeordnet ist, die auf dem Client Computer registriert ist, wird das Element als Datei dieses Typs angesehen. Wenn der `MIMEType` auf dem Client Computer registrierte Dateinamenerweiterung nicht zugeordnet ist, wird das Element als weblinktyp behandelt. Der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter versucht nicht, das **URL** -Attribut zu analysieren, um die Dateinamenerweiterung zu suchen.
-   Wenn `MIMEType` eine Dateinamenerweiterung zugeordnet ist, die auf dem Client Computer registriert ist, bestimmt der Anbieter, ob die Dateinamenerweiterung ein bekannter webdateityp ist (htm, HTML, ASP, aspx, PHP,. SWF,. stm). Wenn dies der Fall ist, wird der Dateityp als weblinktyp betrachtet. Andernfalls wird Sie als Dateityp betrachtet. Wenn dem z. b. die `MIMEType "text/html"` Dateinamenerweiterung. htm zugeordnet ist, wird dieses Element als Weblink anstelle von als htm-Dateityp betrachtet.

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a>Vermeiden potenzieller Barrieren für die Aktivierung eines Datenspeicher

Einige Datenspeicher stellen keinen mit [OpenSearch](https://github.com/dewitt/opensearch)kompatiblen Webdienst bereit, können aber weiterhin mit der Windows-Verbund Suche verbunden werden. Zu diesen Daten speichern gehören:

-   Remote Indizes mit Authentifizierungsmethoden, die in der Windows 7-Verbund Suche nicht unterstützt werden.

    Beispiele hierfür sind die Formular basierte Authentifizierung und andere benutzerdefinierte Authentifizierungsmethoden.

-   Wenn ein Öffentlicher Informationsspeicher über öffentliche Web-APIs verfügt, kann jeder einen anderen Webdienst schreiben, der mit [OpenSearch](https://github.com/dewitt/opensearch)kompatibel ist, und diese APIs im Hintergrund aufruft.

    Beispiele hierfür sind die Library of Congress und die medizinischen Forschungsdatenbanken.

-   Proprietäre Enterprise-Datenspeicher oder-Indizes sowie Legacy-Inhalts Verwaltungs Speicher, für die es möglicherweise unmöglich ist, ein Front-End zu implementieren.

Es gibt jedoch Alternativen, mit denen Barrieren zum Aktivieren eines Datenspeicher vermieden werden können. Im folgenden sind einige dieser Alternativen aufgeführt:

**Zum Schreiben eines Webdiensts für mittlere Menschen, wenn der Webdienst für die vorhandene Datenquelle nicht geändert werden kann oder wenn der Webdienst eine benutzerdefinierte API bereitstellt:**

1.  Schreiben eines Middle-man-Webdiensts, der eine Windows 7-Abfrage akzeptieren kann.
2.  Stellen Sie eine Verbindung mit Ihrer Datenquelle her, und rufen Sie die Abfrageergebnisse ab.
3.  Formatieren Sie die Ergebnisse im RSS-oder Atom-Format neu.
4.  Die Ergebnisse werden an den Windows 7-Client zurückgegeben.
5.  Beachten Sie, dass Sie bei Enterprise Data Services und vielen Internet Datendiensten ggf. die Benutzer Anmelde Informationen im Namen des Webdiensts übergeben müssen, um die Ergebnis Kürzung basierend auf den Berechtigungen des Benutzers durchzuführen.

**So verwenden Sie eine vorhandene Suchmaschine, wenn Sie einen öffentlichen Datenspeicher nicht aktivieren können:**

1.  Verwenden Sie eine öffentliche Suchmaschine, die [OpenSearch](https://github.com/dewitt/opensearch) mit RSS bereits unterstützt. Hierzu können Sie Ihren Benutzern eine OSDX-Datei mit einer URL-Vorlage bereitstellen, die die Ergebnisse auf die für Ihre bestimmte Domäne beschränkt.
2.  Sehen Sie sich das folgende Beispiel einer [OpenSearch](https://github.com/dewitt/opensearch) -Beschreibung an, um nur den Hilfe Inhalt für Windows zu suchen, indem Sie eine Abfrage für Live.com verwenden.

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
      <ShortName>Windows Help</ShortName>
      <Description>Search Windows Help using the live.com search engine</Description>
      <Language></Language>
      <Url type="text/html" template="https://windowshelp.microsoft.com/windows/search.aspx?=&amp;qu={searchTerms}"/>
      <Url type="application/rss+xml" template="https://api.search.live.com/rss.aspx?source=web&amp;query={searchTerms} site:windowshelp.microsoft.com&amp;web.count=50"/>
    </OpenSearchDescription>
    ```

    

**So verwenden Sie einen vorhandenen Index Server, der OpenSearch unterstützt, wenn Sie proprietäre Enterprise-Datenspeicher oder-Indizes nicht aktivieren können:**

1.  Wählen Sie einen vorhandenen Index Server aus, der [OpenSearch](https://github.com/dewitt/opensearch) zum Indizieren ihres Inhalts unterstützt, z. b. den SharePoint-Such Server.
2.  Erstellen Sie eine OSDX-Datei, die die Ergebnisse aus dem SharePoint-Index auf die von Ihrem Server beschränkt, indem Sie Ihre Schlüsselwort Syntax in der URL-Vorlage verwenden.

**So schreiben Sie einen Client seitigen Datenspeicher, wenn eine serverseitige Lösung nicht funktioniert:**

1.  Schreiben Sie eine Client seitige [OpenSearch](https://github.com/dewitt/opensearch) -Datenquelle, die sich zwischen dem Windows [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter und der externen Datenquelle befindet.
2.  Verwenden Sie die [iopensearchsource-Schnittstellen](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) -API im Windows SDK, um eine ordnungsgemäß konfigurierte. searchconnector-MS-Datei zu erstellen, über die Windows-Explorer Ihre Implementierung mit den Abfrage Parametern abrufen kann. Ihre Implementierung kann dann Ergebnisse im RSS-oder Atom-Format zurückgeben. Dadurch kann Ihre Implementierung benutzerdefinierte Benutzeroberfläche für die Authentifizierung bereitstellen und über die proprietäre API eine Verbindung mit der Datenquelle herstellen.

> [!Note]  
> Beim Öffnen einer OSDX-Datei wird eine searchconnector-MS-Datei (Search-Connector) im Verzeichnis "% User Profile%/searches" erstellt, und es wird ein Link zu dieser Datei im Verzeichnis "% User Profile%/Links" platziert.

 

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

[Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche](-search-federated-search-osdx-file.md)
</dt> <dt>

[Bewährte Methoden bei der Windows-Verbund Suche](-search-fedsearch-best.md)
</dt> <dt>

[Bereitstellen von Suchconnectors in der Windows-Verbund Suche](-search-federated-search-deploying.md)
</dt> </dl>

 

 
