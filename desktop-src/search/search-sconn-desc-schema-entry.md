---
description: Führt das Suchconnector-Beschreibungs Schema ein, das von Windows Explorer-Bibliotheken und Verbund Such Anbietern verwendet wird.
ms.assetid: b85a04c6-9398-4cc7-a894-881216600203
title: Suchdienst-Beschreibungs Schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f502f67cdc933bf4d27a3475cd6adef70c00fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345669"
---
# <a name="search-connector-description-schema"></a>Suchdienst-Beschreibungs Schema

Führt das Suchconnector-Beschreibungs Schema ein, das von Windows Explorer-Bibliotheken und Verbund Such Anbietern verwendet wird. Das Schema gibt die Struktur und die Anforderungen für \* suchconnectorbeschreibungs-Dateien (. searchconnector-MS) und für **searchconnectordescriptiontype** -Elemente der shellbibliotheks-Beschreibungs \* Dateien (. Library-MS) an.

In diesem Thema wird das Schema im Zusammenhang mit Verbund Suchconnectors beschrieben. Weitere Informationen zu Bibliotheken und zum Beschreibungs Schema der Bibliothek finden Sie unter [Bibliotheks Beschreibungs Schema](../shell/library-schema-entry.md).

Dieses Thema enthält die folgenden Abschnitte:

-   [Was sind Suchconnectors?](#what-are-search-connectors)
-   [Funktionsweise von Suchconnector-Beschreibungsdateien](#search-connector-description-schema)
-   [Was ist das Suchconnector-Beschreibungs Schema?](#what-is-the-search-connector-description-schema)
-   [Worin bestehen die Hauptbestandteile des Schemas?](#what-are-the-major-parts-of-the-schema)
-   [Beispiele für Suchconnector-Beschreibungsdateien](#examples-of-search-connector-description-files)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="what-are-search-connectors"></a>Was sind Suchconnectors?

Suchconnectors verbinden Benutzer mit Daten, die in Webdiensten oder Remote Speicherorten gespeichert sind. Mit Windows 7 können Benutzer Suchconnectors für Standorte wie z. b. Webdienste installieren, sodass Sie diese Speicherorte direkt im Windows-Explorer durchsuchen. Suchconnectors sind suchconnectorbeschreibungs \* -Dateien (. searchconnector-MS), die angeben, wie eine Verbindung mit hergestellt, Abfragen gesendet und Ergebnisse vom Speicherort empfangen werden.

Zusätzlich zu den Webdiensten können Suchconnectors verwendet werden, um lokale Index Bereiche zu durchsuchen, die von Protokoll Handlern erstellt wurden. Beispielsweise können Benutzer mithilfe eines suchverbindungs Diensts für diesen e-Mail-Speicher lokale e-Mail-nach Speicherung mit dem MAPI-Protokollhandler suchen.

## <a name="how-do-search-connector-description-files-work"></a>Funktionsweise von Suchconnector-Beschreibungsdateien

Wenn die Suchconnector-Beschreibungsdateien auf den Benutzer Systemen installiert werden, können Benutzer Windows-Explorer öffnen, im Navigationsbereich auf den Suchconnector klicken und eine Suchabfrage eingeben. Windows-Explorer sendet die Abfrage mithilfe von Informationen aus der Suchconnector-Beschreibungsdatei, z. b. dem zu verwendenden Anbieter und dem Suchbereich. Die Ergebnisse werden als RSS-oder Atom-Feed-Elemente zurückgegeben und Benutzern angezeigt, als ob es sich um reguläre shellelemente handelt.

Wie Sie Ihre Suchconnector-Beschreibungsdatei bereitstellen, hängt vom Typ des Standorts ab, den der Suchconnector unterstützt:

-   In einer OpenSearch-Konfigurations \* Datei (OSDX-Datei) für Ihren Webdienst
-   Als Teil ihrer protokollhandlerinstallation

Stellen Sie sicher, dass Folgendes passiert, wenn ein Benutzer die OSDX-Datei öffnet oder den Protokollhandler installiert:

-   Die Datei. searchconnector-MS wird im Ordner **Windows-Such** Vorgänge (% User Profile%/searches) erstellt.
-   Im Ordner **Verknüpfungen** der Benutzer (% User Profile%/links) wird eine Verknüpfung mit der Datei ". searchconnector-MS" erstellt.

## <a name="what-is-the-search-connector-description-schema"></a>Was ist das Suchconnector-Beschreibungs Schema?

Das Suchconnector-Beschreibungs Schema ist ein XML-Schema, das die Struktur der Suchconnector-Beschreibungsdateien ( \* searchconnector-MS) definiert. Jeder Suchconnector muss über eine Suchconnector-Beschreibungsdatei verfügen, die angibt, wie eine Verbindung mit dem Speicherort hergestellt, Abfragen an ihn gesendet und Ergebnisse vom Speicherort empfangen werden.

## <a name="what-are-the-major-parts-of-the-schema"></a>Worin bestehen die Hauptbestandteile des Schemas?

In der folgenden Tabelle sind die Hauptbestandteile des Schemas aufgeführt.



| Untergeordnete Elemente                                                                         | BESCHREIBUNG                                                                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [issearchonlyitem](search-schema-sconn-issearchonlyitem.md)                           | Gibt an, ob die vom Suchconnector unterstützten Speicherorte nur durchsuchen oder suchen und Durchsuchen angezeigt werden.                                                                                |
| [isdefaultsaveloation](search-schema-sconn-isdefaultsavelocation.md)                 | Nur für die Bibliotheks Verwendung.                                                                                                                                                                   |
| [isdefaultnonbesitzsaveloation](search-schema-sconn-isdefaultnonownersavelocation.md) | Nur für die Bibliotheks Verwendung.                                                                                                                                                                   |
| [Beschreibung](search-schema-sconn-description.md)                                     | Beschreibt den Suchconnector.                                                                                                                                                         |
| [iconReference](search-schema-sconn-iconreference.md)                                 | Gibt den Speicherort eines benutzerdefinierten Symbols für den Suchconnector an.                                                                                                                      |
| [IMAGELINK](search-schema-sconn-imagelink.md)                                         | Gibt den Speicherort einer benutzerdefinierten Miniaturansicht für den Suchconnector an.                                                                                                                 |
| [Schrift](search-schema-sconn-author.md)                                               | Identifiziert den Autor des Suchconnector.                                                                                                                                          |
| [DateCreated](search-schema-sconn-datecreated.md)                                     | Gibt das Datum an, an dem der Suchconnector erstellt wurde.                                                                                                                              |
| [templateingefo](search-schema-sconn-templateinfo.md)                                   | Gibt einen Ordnertyp für den Suchconnector an.                                                                                                                                       |
| [locationprovider](search-schema-sconn-locationprovider.md)                           | Gibt den Suchanbieter an, der von diesem Suchconnector verwendet werden soll.                                                                                                                      |
| [scope](search-schema-sconn-scope.md)                                                 | Gibt die Speicherorte an, die in den Suchbereich eingeschlossen und aus diesem ausgeschlossen werden sollen.                                                                                                                |
| [PropertyStore](search-schema-sconn-propertystore.md)                                 | Gibt den Speicherort eines XML-basierten [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) für diesen Suchconnector an. Der **IPropertyStore** unterstützt die geöffneten Metadaten des Suchconnector. |
| [includeinstartmen-Cope](search-schema-sconn-includeinstartmenuscope.md)             | Gibt an, ob der durch den Suchconnector dargestellte Speicherort im Suchbereich des Start Menüs enthalten sein soll.                                                                 |
| [-](search-schema-sconn-domain.md)                                               | Identifiziert die Domäne der obersten Ebene des Suchconnector.                                                                                                                                     |
| [supportsadvancedquerysyntax](search-schema-sconn-supportsadvancedquerysyntax.md)     | Gibt an, ob der Suchconnector Erweiterte Abfrage Syntax (AQS) unterstützt.                                                                                                            |
| [isindebug](search-schema-sconn-isindexed.md)                                         | Gibt an, ob der durch den Suchconnector dargestellte Speicherort indiziert wird.                                                                                                          |



 

## <a name="examples-of-search-connector-description-files"></a>Beispiele für Suchconnector-Beschreibungsdateien

Im folgenden finden Sie ein Beispiel für eine Suchconnector-Beschreibungsdatei für einen Verbund Suchweb Dienst.


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



Im folgenden finden Sie ein Beispiel für eine Suchconnector-Beschreibungsdatei für einen MAPI-Protokollhandler.


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

-   Weitere Informationen zum Bibliotheks Beschreibungs Schema finden Sie unter [Bibliotheks Beschreibungs Schema](../shell/library-schema-entry.md).
-   Weitere Informationen zum Installieren eines Suchconnector finden Sie unter [Federated Search in Windows](-search-federated-search-overview.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[searchconnectordescriptiontype-Element (suchconnectorschema)](search-schema-searchconnectordescription.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[OpenSearch](http://www.opensearch.org/Home)
</dt> <dt>

[Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx)
</dt> </dl>

 

 
