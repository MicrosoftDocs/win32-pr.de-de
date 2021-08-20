---
description: Führt das Schema für die Beschreibung des Suchconnectors ein, das von Windows Explorer-Bibliotheken und Verbundsuchanbietern verwendet wird.
ms.assetid: b85a04c6-9398-4cc7-a894-881216600203
title: Suchconnectorbeschreibungsschema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e8d8ab60ba472cca961a4208b1c551679ef93eacd46e07cf5e080a3e73f3d14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226381"
---
# <a name="search-connector-description-schema"></a>Suchconnectorbeschreibungsschema

Führt das Schema für die Beschreibung des Suchconnectors ein, das von Windows Explorer-Bibliotheken und Verbundsuchanbietern verwendet wird. Das Schema gibt die Struktur und die Anforderungen für Search Connector Description-Dateien ( \* .searchConnector-ms) und für **searchConnectorDescriptionType-Elemente** der ShellBibliotheksbeschreibungsdateien \* (.library-ms) an.

In diesem Thema wird das Schema im Zusammenhang mit Connectors für die Verbundsuche beschrieben. Weitere Informationen zu Bibliotheken und zum Bibliotheksbeschreibungsschema finden Sie unter [Bibliotheksbeschreibungsschema.](../shell/library-schema-entry.md)

Dieses Thema enthält die folgenden Abschnitte:

-   [Was sind Suchconnectors?](#what-are-search-connectors)
-   [Wie funktionieren Die Beschreibungsdateien des Suchconnectors?](#search-connector-description-schema)
-   [Was ist das Beschreibungsschema des Suchconnectors?](#what-is-the-search-connector-description-schema)
-   [Was sind die Hauptkomponenten des Schemas?](#what-are-the-major-parts-of-the-schema)
-   [Beispiele für Suchconnectorbeschreibungsdateien](#examples-of-search-connector-description-files)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="what-are-search-connectors"></a>Was sind Suchconnectors?

Suchconnectors verbinden Benutzer mit Daten, die in Webdiensten oder Remotespeicherorten gespeichert sind. Mit Windows 7 können Benutzer Suchconnectors für Standorte wie Webdienste installieren, sodass sie diese Standorte direkt über Windows Explorer durchsuchen. Suchconnectors sind Search Connector Description-Dateien ( \* .searchConnector-ms), die angeben, wie eine Verbindung mit hergestellt, Abfragen gesendet und Ergebnisse vom Speicherort empfangen werden sollen.

Zusätzlich zu Webdiensten können Suchconnectors verwendet werden, um lokale Indexbereiche zu durchsuchen, die von Protokollhandlern erstellt werden. Beispielsweise können Benutzer lokal mit dem MAPI-Protokollhandler indizierte E-Mails durchsuchen, indem sie einen Suchconnector für diesen E-Mail-Speicher verwenden.

## <a name="how-do-search-connector-description-files-work"></a>Wie funktionieren Die Beschreibungsdateien des Suchconnectors?

Wenn Die Search Connector Description-Dateien auf den Systemen der Benutzer installiert sind, können Benutzer Windows Explorer öffnen, im Navigationsbereich auf den Suchconnector klicken und eine Suchabfrage eingeben. Windows Der Explorer sendet die Abfrage mithilfe von Informationen aus der Beschreibungsdatei des Suchconnectors, z. B. welchen Anbieter sie verwenden soll, und den Bereich der Suche. Die Ergebnisse werden als RSS- oder Atom-Feedelemente zurückgegeben und Benutzern so angezeigt, als wären sie reguläre Shell-Elemente.

Wie Sie Die Beschreibungsdatei des Suchconnectors bereitstellen, hängt vom Typ des Speicherorts ab, den der Suchconnector unterstützt:

-   In einer OpenSearch-Konfigurationsdatei \* (OSDX) für Ihren Webdienst
-   Im Rahmen der Installation des Protokollhandlers

Sie sollten sicherstellen, dass folgendes geschieht, wenn ein Benutzer die OSDX-Datei öffnet oder den Protokollhandler installiert:

-   Die Datei .searchconnector-ms wird im Ordner **Windows Searches** (%userprofile%/Searches) des Benutzers erstellt.
-   Eine Verknüpfung zur Datei .searchconnector-ms wird im Ordner **Links** des Benutzers (%userprofile%/Links) erstellt.

## <a name="what-is-the-search-connector-description-schema"></a>Was ist das Beschreibungsschema des Suchconnectors?

Das Search Connector Description-Schema ist ein XML-Schema, das die Struktur von Search Connector Description-Dateien \* (.searchConnector-ms) definiert. Jeder Suchconnector muss über eine Beschreibungsdatei für den Suchconnector verfügen, die angibt, wie eine Verbindung hergestellt, Abfragen gesendet und Ergebnisse vom Speicherort empfangen werden.

## <a name="what-are-the-major-parts-of-the-schema"></a>Was sind die Hauptkomponenten des Schemas?

In der folgenden Tabelle sind die Hauptteile des Schemas aufgeführt.



| Untergeordnete Elemente                                                                         | BESCHREIBUNG                                                                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isSearchOnlyItem](search-schema-sconn-issearchonlyitem.md)                           | Gibt an, ob die vom Suchconnector unterstützten Speicherorte such- oder such- und durchsuchend sind.                                                                                |
| [isDefaultSaveLocation](search-schema-sconn-isdefaultsavelocation.md)                 | Nur zur Bibliotheksverwendung.                                                                                                                                                                   |
| [isDefaultNonOwnerSaveLocation](search-schema-sconn-isdefaultnonownersavelocation.md) | Nur zur Bibliotheksverwendung.                                                                                                                                                                   |
| [description](search-schema-sconn-description.md)                                     | Beschreibt den Suchconnector.                                                                                                                                                         |
| [iconReference](search-schema-sconn-iconreference.md)                                 | Identifiziert den Speicherort eines benutzerdefinierten Symbols für den Suchconnector.                                                                                                                      |
| [imageLink](search-schema-sconn-imagelink.md)                                         | Identifiziert den Speicherort einer benutzerdefinierten Miniaturansicht für den Suchconnector.                                                                                                                 |
| [Autor](search-schema-sconn-author.md)                                               | Identifiziert den Autor des Suchconnectors.                                                                                                                                          |
| [Datecreated](search-schema-sconn-datecreated.md)                                     | Gibt das Datum an, an dem der Suchconnector erstellt wurde.                                                                                                                              |
| [templateInfo](search-schema-sconn-templateinfo.md)                                   | Gibt einen Ordnertyp für den Suchconnector an.                                                                                                                                       |
| [locationProvider](search-schema-sconn-locationprovider.md)                           | Gibt den Suchanbieter an, der von diesem Suchconnector verwendet werden soll.                                                                                                                      |
| [scope](search-schema-sconn-scope.md)                                                 | Gibt die Speicherorte an, die in den Suchbereich eingeschlossen und aus diesem ausgeschlossen werden sollen.                                                                                                                |
| [propertyStore](search-schema-sconn-propertystore.md)                                 | Gibt den Speicherort eines XML-basierten [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) für diesen Suchconnector an. **IPropertyStore** unterstützt die offenen Metadaten des Suchconnectors. |
| [includeInStartMenuScope](search-schema-sconn-includeinstartmenuscope.md)             | Gibt an, ob der vom Suchconnector dargestellte Speicherort im Suchbereich des Startmenü enthalten sein soll.                                                                 |
| [Domäne](search-schema-sconn-domain.md)                                               | Identifiziert die Domäne der obersten Ebene des Suchconnectors.                                                                                                                                     |
| [supportsAdvancedQuerySyntax](search-schema-sconn-supportsadvancedquerysyntax.md)     | Gibt an, ob der Suchconnector die erweiterte Abfragesyntax (Advanced Query Syntax, AQS) unterstützt.                                                                                                            |
| [isIndexed](search-schema-sconn-isindexed.md)                                         | Gibt an, ob der vom Suchconnector dargestellte Speicherort indiziert wird.                                                                                                          |



 

## <a name="examples-of-search-connector-description-files"></a>Beispiele für Suchconnectorbeschreibungsdateien

Im Folgenden finden Sie ein Beispiel für eine Beschreibungsdatei des Suchconnectors für einen Verbundsuchwebdienst.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



Im Folgenden finden Sie ein Beispiel für eine Beschreibungsdatei des Suchconnectors für einen MAPI-Protokollhandler.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="additional-resources"></a>Weitere Ressourcen

-   Weitere Informationen zum Bibliotheksbeschreibungsschema finden Sie unter [Bibliotheksbeschreibungsschema.](../shell/library-schema-entry.md)
-   Weitere Informationen zum Installieren eines Suchconnectors finden Sie unter [Verbundsuche in Windows](-search-federated-search-overview.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[searchConnectorDescriptionType-Element (Search Connector Schema)](search-schema-searchconnectordescription.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[OpenSearch](http://www.opensearch.org/Home)
</dt> <dt>

[Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx)
</dt> </dl>

 

 
