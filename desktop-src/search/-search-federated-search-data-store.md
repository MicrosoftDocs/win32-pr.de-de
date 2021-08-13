---
description: Erläutert, wie Sie den Zugriff auf Ihren Datenspeicher durch einen OpenSearch Webdienst ermöglichen und potenzielle Barrieren dafür vermeiden können.
ms.assetid: 27d7676c-f4e8-43b4-856b-826e07afcd78
title: Aktivieren Ihrer Daten Store in Windows Federated Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26feb231f17dbaacb9656f2ef91e1cdb64bc598831a1e4808327dff7e5787bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456755"
---
# <a name="enabling-your-data-store-in-windows-federated-search"></a>Aktivieren Ihrer Daten Store in Windows Federated Search

Erläutert, wie Sie den Zugriff auf Ihren Datenspeicher durch einen [OpenSearch](https://github.com/dewitt/opensearch) Webdienst ermöglichen und potenzielle Barrieren dafür vermeiden können.

Dieses Thema ist wie folgt organisiert:

-   [Bedingungen für die Annahme von Suchanforderungen](#conditions-for-search-request-acceptance)
    -   [Unterstützte Abfragesyntax](#supported-query-syntax)
    -   [Unterstützte Authentifizierungsprotokolle](#supported-authentication-protocols)
-   [Senden von Abfragen und Zurückgeben von Suchergebnissen in RSS oder Atom](#sending-queries-and-returning-search-results-in-rss-or-atom)
    -   [Beispiel für eine RSS-Feedausgabe](#example-of-an-rss-feed-output)
-   [Automatische Zuordnung zu Windows Shelleigenschaften](#automatic-mapping-to-windows-shell-properties)
-   [Grundlegendes zum Windows-Karten von Elementen in Dateitypen](#understanding-how-windows-maps-items-to-file-types)
-   [Vermeiden potenzieller Barrieren für die Aktivierung eines Daten-Store](#avoiding-potential-barriers-to-enabling-a-data-store)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="conditions-for-search-request-acceptance"></a>Bedingungen für die Annahme von Suchanforderungen

Der [OpenSearch](https://github.com/dewitt/opensearch) Webdienst, den Sie auf Ihrem Webserver **erstellen, muss** die folgenden beiden Anforderungen erfüllen:

-   Sie können eine `GET URL` Abfrage vom Client akzeptieren.
-   Lassen Sie zu, dass die Suchbegriffe in die URL eingebettet werden.

    Das folgende Beispiel zeigt, wie ein Suchbegriff in eine URL eingebettet werden kann.

    ```
    https://example.com/search.aspx?query=terms&param=mysearchword
    ```

    

> [!Note]  
> Die Verbundsuche unterstützt das Senden von `POST` Anforderungen an einen Webdienst nicht.

 

Weitere Informationen zum Erstellen einer URL finden Sie unter "URL-Vorlagenparameter" unter [Erstellen einer OpenSearch Beschreibungsdatei in Windows Verbundsuche.](-search-federated-search-osdx-file.md)

### <a name="supported-query-syntax"></a>Unterstützte Abfragesyntax

In Windows 7 wird keine spezifische Abfragesyntax erwartet. Der OpenSearch Anbieter akzeptiert alle Begriffe, die der Benutzer im Eingabefeld in Windows Explorer eingibt, und codiert sie in die URL. Dies entspricht der URL-Vorlage, die in "URL-Vorlagenparameter" unter [Erstellen einer OpenSearch Beschreibungsdatei in Windows Verbundsuche](-search-federated-search-osdx-file.md)beschrieben wird.

Benutzer erwarten, dass separate Begriffe implizit als ANDed behandelt werden. Beispielsweise sollte eine Abfrage für "Microsoft Windows" nur Ergebnisse zurückgeben, die sowohl "Windows" als auch "Microsoft" enthalten.

### <a name="supported-authentication-protocols"></a>Unterstützte Authentifizierungsprotokolle

Windows Die Verbundsuche unterstützt Windows-basierte Authentifizierung und kann Webdiensten über die folgenden Protokolle Anmeldeinformationen bereitstellen:

-   NTLM.
-   Kerberos.
-   Basic (nur über HTTPS).
-   Andere SSPs (Security Support Providers), die auf Windows installiert sind und zusätzliche Abfragekapazität bereitstellen. Informationen zum möglichen Hinzufügen anderer SSPs finden Sie in der [SSP Interface](../secauthn/sspi.md) SDK-Dokumentation.

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a>Senden von Abfragen und Zurückgeben von Suchergebnissen in RSS oder Atom

Der [OpenSearch-Anbieter](https://github.com/dewitt/opensearch) ist dafür verantwortlich, die XML-Elementwerte Windows Shell-Systemeigenschaften zuzuordnen, die von Windows Anwendungen verwendet werden können. Sie sind jedoch nicht auf die Standardzuordnungen von RSS- oder Atom-Standardelementen beschränkt und können benutzerdefinierte XML-Elemente in den Windows Namespace für jede der Eigenschaften einschließen. Sie können z. B. eigene benutzerdefinierte XML-Elemente innerhalb des **Elementelements** hinzufügen, um zusätzliche Metadaten für Windows bereitzustellen. Sie können auch Elemente aus anderen XML-Namespaces zuordnen, z. B. iTunes.

### <a name="example-of-an-rss-feed-output"></a>Beispiel für eine RSS-Feedausgabe

Im folgenden Beispiel gibt die RSS-Feedausgabe ein Element zurück.


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



Ausführlichere Informationen zur Eigenschaftenzuordnung finden Sie in den Abschnitten "Erweiterte Elemente in der WIndows-Verbundsuche" und "Benutzerdefinierte Eigenschaftenzuordnungen" unter [Erstellen einer OpenSearch Beschreibungsdatei in Windows Verbundsuche.](-search-federated-search-osdx-file.md)

## <a name="automatic-mapping-to-windows-shell-properties"></a>Automatische Zuordnung zu Windows Shelleigenschaften

Innerhalb der Elemente im RSS-Feed können Sie andere XML-Elemente einschließen, die automatisch Windows Shell-Systemeigenschaften zugeordnet werden. Fügen Sie hierzu ein Element ein, das nach der Windows Shell-Eigenschaft benannt ist und dem Windows Shell-Systemnamespace vorangestellt ist. Das folgende Beispiel veranschaulicht die Namespacedeklaration `win=" http://schemas.microsoft.com/windows/2008/propertynamespace"` und die Einbeziehung eines Elements für die Eigenschaftenzuordnung: `win:System.Contact.PrimaryEmailAddress`


```
<rss version="2.0" xmlns:example="https://example.com/schema/2009" xmlns:win="http://schemas.microsoft.com/windows/2008/propertynamespace">
...
   <item>
      <title>Someone</title>
      <win:System.Contact.PrimaryEmailAddress>someone@example.com
   </win:System.Contact.PrimaryEmailAddress>
   </item>
```



Das hier verwendete Namespacepräfix ( `"win"` ) ist ein Vorschlag. Sie können ein beliebiges Präfix verwenden. Sie müssen jedoch die genauen Windows Shell-Eigenschaftsnamen verwenden und den genauen Uniform Resource Identifier (URI) enthalten, wie im folgenden Beispiel gezeigt:


```
http://schemas.microsoft.com/windows/2008/propertynamespace
```



**Informationen zu Windows Shell-Systemeigenschaften**

Windows definiert eine vollständige Liste der [Systemeigenschaften](../properties/props.md) und das für jede Eigenschaft erforderliche Werttypformat. Die Dokumentation für die [Eigenschaft System.FileExtension](../properties/props-system-fileextension.md) Window Shell gibt beispielsweise an, dass der Wert den führenden Punkt (".docx" und nicht "docx") enthalten muss.

**Werte für Datum und Uhrzeit**

Das bevorzugte Datums- und Uhrzeitformat ist ISO-8601, wie im folgenden Beispiel gezeigt:


```
2008-01-16T 19:20:30:.45+01:00
```



.NET-Entwickler sollten die DateTime-Klasse mit `ToString("R") ` verwenden, um das richtige Format auszugeben.

Ausführlichere Informationen zur Eigenschaftenzuordnung finden Sie unter "Erweiterte Elemente in Windows Verbundsuche" unter [Erstellen einer OpenSearch Beschreibungsdatei in Windows Verbundsuche.](-search-federated-search-osdx-file.md)

## <a name="understanding-how-windows-maps-items-to-file-types"></a>Grundlegendes zum Windows-Karten von Elementen in Dateitypen

Die Suche auf der Benutzeroberfläche des Windows-Explorers ermöglicht Benutzern, Ergebnisse als Dateien zu behandeln, wenn ein RSS-Element auf eine remote gespeicherte Datei verweist. Der Benutzer kann Elemente per Drag & Drop auf den Desktop ziehen, und die Windows-Explorer-Benutzeroberfläche zeigt das richtige Symbol an und stellt das entsprechende Kontextmenü bereit. Wenn das RSS-Element nicht auf eine remote gespeicherte Datei verweist, wird die Datei als Link behandelt, und Benutzer können Aktionen dafür ausführen, z. B. das Erstellen einer Verknüpfung oder das Öffnen im Browser.

Das folgende Flussdiagramm zeigt, wie Windows den Dateityp eines Elements bestimmt.

![Flussdiagramm mit Pfaden von einem Element zu Entscheidungen zur Behandlung als Weblinktypelement oder Dateityp](images/determineanitemfiletype.png)

Der [OpenSearch](https://github.com/dewitt/opensearch) Anbieter führt die folgenden Schritte aus, um ein Element einem Dateityp zuzuordnen:

-   Bestimmen Sie, ob das Element als Datei oder Weblink behandelt werden soll.
-   Identifizieren Sie die richtige zu verwendende Dateinamenerweiterung.

Wenn das Element beispielsweise über eine Link-URL verfügt, die einen Dateisystempfad verwendet (z. B. `file:///\\server\share\etc\item.ext` ), behandelt der [OpenSearch-Anbieter](https://github.com/dewitt/opensearch) den Link als Datei und bestimmt den Typ anhand der im Pfad verwendeten Dateinamenerweiterung (.ext in diesem Beispiel).

Wenn das Element das STANDARDMÄßIGE RSS-Gehäuse oder **mediaRSS media:content-Element** verwendet, geht der [OpenSearch-Anbieter](https://github.com/dewitt/opensearch) davon aus, dass es sich bei dem Element um eine Datei handelt, und identifiziert die Dateinamenerweiterung wie folgt:

-   Wenn die [Eigenschaft System.FileExtension](../properties/props-system-fileextension.md) Windows Shell für das Element zugeordnet wurde, verwendet der Anbieter diese Dateinamenerweiterung.
-   Wenn die [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell-Eigenschaft nicht zugeordnet wurde, verwendet der Anbieter das im Gehäuse- oder Inhaltselement angegebene **Type-Attribut.** Dieses Element sollte eine `MIMEType` Zeichenfolge enthalten, `"image/jpeg"` z. B. . Wenn dem `MIMEType` eine Dateierweiterung zugeordnet ist, die auf dem Clientcomputer registriert ist, wird das Element als Datei dieses Typs betrachtet. Wenn der `MIMEType` keiner auf dem Clientcomputer registrierten Dateinamenerweiterung zugeordnet ist, wird das Element als Weblinktyp behandelt. Der [OpenSearch](https://github.com/dewitt/opensearch) Anbieter versucht nicht, das **URL-Attribut** zu analysieren, um die Dateinamenerweiterung zu finden.
-   Wenn dem `MIMEType` eine auf dem Clientcomputer registrierte Dateinamenerweiterung zugeordnet ist, bestimmt der Anbieter, ob die Dateinamenerweiterung ein bekannter Webdateityp ist (.htm, .html, ASP, ASPX, PHP, SWF, STM). Wenn ja, wird der Dateityp als Weblinktyp betrachtet. andernfalls wird sie als Dateityp betrachtet. Wenn z. B. `MIMEType "text/html"` der .htm Dateinamenerweiterung zugeordnet ist, wird dieses Element als Weblink und nicht als .htm Dateityp betrachtet.

## <a name="avoiding-potential-barriers-to-enabling-a-data-store"></a>Vermeiden potenzieller Barrieren für die Aktivierung eines Daten-Store

Einige Datenspeicher stellen keinen [mit OpenSearch](https://github.com/dewitt/opensearch)kompatiblen Webdienst bereit, können aber weiterhin mit Windows Verbundsuche verbunden werden. Zu diesen Datenspeichern gehören:

-   Remoteindizes mit Authentifizierungsmethoden, die in Windows 7 Federated Search nicht unterstützt werden.

    Beispiele hierfür sind die formularbasierte Authentifizierung und andere benutzerdefinierte Authentifizierungsmethoden.

-   Wenn ein öffentlicher Speicher mit hohem Wert über öffentliche Web-APIs verfügt, kann jeder einen anderen Webdienst schreiben, [der mit OpenSearch](https://github.com/dewitt/opensearch)kompatibel ist, und diese APIs im Hintergrund aufrufen.

    Beispiele hierfür sind die Library ofStandardisierung und datenbanken für die medizinische Forschung.

-   Proprietäre Unternehmensdatenspeicher oder -indizes sowie Legacyspeicher für die Inhaltsverwaltung, für die es möglicherweise nicht möglich ist, ein Front-End zu implementieren.

Es gibt jedoch Alternativen, die Barrieren für die Aktivierung eines Datenspeichers vermeiden können. Es folgen einige dieser Alternativen:

**So schreiben Sie einen Middle-Man-Webdienst, wenn Sie den Webdienst für die vorhandene Datenquelle nicht ändern können oder der Webdienst eine benutzerdefinierte API bereitstellt:**

1.  Schreiben Sie einen Middle-Man-Webdienst, der eine Windows 7-Abfrage akzeptieren kann.
2.  Verbinden zu Ihrer Datenquelle, und rufen Sie die Abfrageergebnisse ab.
3.  Formatieren Sie die Ergebnisse im RSS- oder Atom-Format neu.
4.  Gibt die Ergebnisse an den Windows 7-Client zurück.
5.  Beachten Sie, dass Sie für Unternehmensdatendienste und viele Internetdatendienste möglicherweise die Benutzeranmeldeinformationen im Auftrag des Webdiensts übergeben müssen, um die Ergebniskürzung basierend auf den Berechtigungen des Benutzers durchzuführen.

**So verwenden Sie eine vorhandene Suchmaschine, wenn Sie keinen öffentlichen Datenspeicher aktivieren können:**

1.  Verwenden Sie eine öffentliche Suchmaschine, die bereits [OpenSearch](https://github.com/dewitt/opensearch) mit RSS unterstützt. Sie können dies erreichen, indem Sie Ihren Benutzern eine OSDX-Datei mit einer URL-Vorlage zur Verfügung stellen, die die Ergebnisse auf die Ergebnisse für Ihre spezifische Domäne beschränkt.
2.  Im folgenden Beispiel einer [OpenSearch](https://github.com/dewitt/opensearch) Beschreibung können Sie nur den Hilfeinhalt nach Windows durchsuchen, indem Sie eine Abfrage für live.com verwenden.

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

    

**So verwenden Sie einen vorhandenen Indizierungsserver, der OpenSearch unterstützt, wenn Sie proprietäre Unternehmensdatenspeicher oder -indizes nicht aktivieren können:**

1.  Wählen Sie einen vorhandenen Indizierungsserver aus, [der OpenSearch](https://github.com/dewitt/opensearch) unterstützt, um Ihren Inhalt zu indizieren, z. B. den SharePoint Suchserver.
2.  Erstellen Sie eine OSDX-Datei, die die Ergebnisse aus dem SharePoint Index auf die Ergebnisse ihres Servers beschränkt, indem Sie die KeyWord-Syntax in der URL-Vorlage verwenden.

**So schreiben Sie einen clientseitigen Datenspeicher, wenn eine serverseitige Lösung nicht funktioniert:**

1.  Schreiben Sie eine clientseitige [OpenSearch](https://github.com/dewitt/opensearch) Datenquelle, die sich zwischen dem Windows [OpenSearch](https://github.com/dewitt/opensearch) und der externen Datenquelle befindet.
2.  Verwenden Sie die [IOpenSearchSource-Schnittstellen-API](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iopensearchsource) im Windows SDK, um eine entsprechend konfigurierte Searchconnector-ms-Datei zu erstellen, über die Windows Explorer Ihre Implementierung mit den Abfrageparametern aufrufen kann. Ihre Implementierung kann dann Ergebnisse zurückgeben, die im RSS- oder Atom-Format formatiert sind. Dadurch kann Ihre Implementierung eine benutzerdefinierte Authentifizierungsbenutzeroberfläche bereitstellen und mithilfe der proprietären API eine Verbindung mit der Datenquelle herstellen.

> [!Note]  
> Beim Öffnen einer OSDX-Datei wird eine SEARCHCONNECTOR-MS-Datei (Suchconnector) im Verzeichnis %userprofile%/searches erstellt und ein Link zu ihr im Verzeichnis %userprofile%/links platziert.

 

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

[Erstellen einer OpenSearch-Beschreibungsdatei in Windows Verbundsuche](-search-federated-search-osdx-file.md)
</dt> <dt>

[Bewährte Methoden bei der Windows Verbundsuche](-search-fedsearch-best.md)
</dt> <dt>

[Bereitstellen von Suchconnectors in Windows Verbundsuche](-search-federated-search-deploying.md)
</dt> </dl>

 

 
