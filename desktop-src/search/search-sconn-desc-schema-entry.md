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
# <a name="search-connector-description-schema"></a><span data-ttu-id="6cca7-103">Suchdienst-Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="6cca7-103">Search Connector Description Schema</span></span>

<span data-ttu-id="6cca7-104">Führt das Suchconnector-Beschreibungs Schema ein, das von Windows Explorer-Bibliotheken und Verbund Such Anbietern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6cca7-104">Introduces the Search Connector Description schema that is used by Windows Explorer libraries and federated search providers.</span></span> <span data-ttu-id="6cca7-105">Das Schema gibt die Struktur und die Anforderungen für \* suchconnectorbeschreibungs-Dateien (. searchconnector-MS) und für **searchconnectordescriptiontype** -Elemente der shellbibliotheks-Beschreibungs \* Dateien (. Library-MS) an.</span><span class="sxs-lookup"><span data-stu-id="6cca7-105">The schema specifies the structure and requirements for Search Connector Description files (\*.searchConnector-ms) and for **searchConnectorDescriptionType** elements of the Shell Library Description (\*.library-ms) files.</span></span>

<span data-ttu-id="6cca7-106">In diesem Thema wird das Schema im Zusammenhang mit Verbund Suchconnectors beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6cca7-106">This topic describes the schema as it relates to federated search connectors.</span></span> <span data-ttu-id="6cca7-107">Weitere Informationen zu Bibliotheken und zum Beschreibungs Schema der Bibliothek finden Sie unter [Bibliotheks Beschreibungs Schema](../shell/library-schema-entry.md).</span><span class="sxs-lookup"><span data-stu-id="6cca7-107">For more information about libraries and the Library Description schema, see [Library Description Schema](../shell/library-schema-entry.md).</span></span>

<span data-ttu-id="6cca7-108">Dieses Thema enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="6cca7-108">This topic includes the following sections:</span></span>

-   [<span data-ttu-id="6cca7-109">Was sind Suchconnectors?</span><span class="sxs-lookup"><span data-stu-id="6cca7-109">What Are Search Connectors?</span></span>](#what-are-search-connectors)
-   [<span data-ttu-id="6cca7-110">Funktionsweise von Suchconnector-Beschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="6cca7-110">How Do Search Connector Description Files Work?</span></span>](#search-connector-description-schema)
-   [<span data-ttu-id="6cca7-111">Was ist das Suchconnector-Beschreibungs Schema?</span><span class="sxs-lookup"><span data-stu-id="6cca7-111">What Is the Search Connector Description Schema?</span></span>](#what-is-the-search-connector-description-schema)
-   [<span data-ttu-id="6cca7-112">Worin bestehen die Hauptbestandteile des Schemas?</span><span class="sxs-lookup"><span data-stu-id="6cca7-112">What Are the Major Parts of the Schema?</span></span>](#what-are-the-major-parts-of-the-schema)
-   [<span data-ttu-id="6cca7-113">Beispiele für Suchconnector-Beschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="6cca7-113">Examples of Search Connector Description Files</span></span>](#examples-of-search-connector-description-files)
-   [<span data-ttu-id="6cca7-114">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6cca7-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="6cca7-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6cca7-115">Related topics</span></span>](#related-topics)

## <a name="what-are-search-connectors"></a><span data-ttu-id="6cca7-116">Was sind Suchconnectors?</span><span class="sxs-lookup"><span data-stu-id="6cca7-116">What Are Search Connectors?</span></span>

<span data-ttu-id="6cca7-117">Suchconnectors verbinden Benutzer mit Daten, die in Webdiensten oder Remote Speicherorten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="6cca7-117">Search connectors connect users with data stored in web services or remote storage locations.</span></span> <span data-ttu-id="6cca7-118">Mit Windows 7 können Benutzer Suchconnectors für Standorte wie z. b. Webdienste installieren, sodass Sie diese Speicherorte direkt im Windows-Explorer durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="6cca7-118">With Windows 7, users can install search connectors for locations, like web services, so that they search those locations directly from Windows Explorer.</span></span> <span data-ttu-id="6cca7-119">Suchconnectors sind suchconnectorbeschreibungs \* -Dateien (. searchconnector-MS), die angeben, wie eine Verbindung mit hergestellt, Abfragen gesendet und Ergebnisse vom Speicherort empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="6cca7-119">Search connectors are Search Connector Description files (\*.searchConnector-ms) that specify how to connect to, send queries to, and receive results from the location.</span></span>

<span data-ttu-id="6cca7-120">Zusätzlich zu den Webdiensten können Suchconnectors verwendet werden, um lokale Index Bereiche zu durchsuchen, die von Protokoll Handlern erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="6cca7-120">In addition to web services, search connectors can be used to search local index scopes created by protocol handlers.</span></span> <span data-ttu-id="6cca7-121">Beispielsweise können Benutzer mithilfe eines suchverbindungs Diensts für diesen e-Mail-Speicher lokale e-Mail-nach Speicherung mit dem MAPI-Protokollhandler suchen.</span><span class="sxs-lookup"><span data-stu-id="6cca7-121">For example, users can search email indexed locally with the MAPI protocol handler by using a search connector for that email store.</span></span>

## <a name="how-do-search-connector-description-files-work"></a><span data-ttu-id="6cca7-122">Funktionsweise von Suchconnector-Beschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="6cca7-122">How Do Search Connector Description Files Work?</span></span>

<span data-ttu-id="6cca7-123">Wenn die Suchconnector-Beschreibungsdateien auf den Benutzer Systemen installiert werden, können Benutzer Windows-Explorer öffnen, im Navigationsbereich auf den Suchconnector klicken und eine Suchabfrage eingeben.</span><span class="sxs-lookup"><span data-stu-id="6cca7-123">When Search Connector Description files are installed on users' systems, users can open Windows Explorer, click the search connector in the navigation pane, and enter a search query.</span></span> <span data-ttu-id="6cca7-124">Windows-Explorer sendet die Abfrage mithilfe von Informationen aus der Suchconnector-Beschreibungsdatei, z. b. dem zu verwendenden Anbieter und dem Suchbereich.</span><span class="sxs-lookup"><span data-stu-id="6cca7-124">Windows Explorer sends the query using information from the Search Connector Description file, such as which provider to use and the scope of the search.</span></span> <span data-ttu-id="6cca7-125">Die Ergebnisse werden als RSS-oder Atom-Feed-Elemente zurückgegeben und Benutzern angezeigt, als ob es sich um reguläre shellelemente handelt.</span><span class="sxs-lookup"><span data-stu-id="6cca7-125">The results are returned as RSS or Atom feed items and displayed to users as if they were regular Shell items.</span></span>

<span data-ttu-id="6cca7-126">Wie Sie Ihre Suchconnector-Beschreibungsdatei bereitstellen, hängt vom Typ des Standorts ab, den der Suchconnector unterstützt:</span><span class="sxs-lookup"><span data-stu-id="6cca7-126">How you deploy your Search Connector Description file depends on the type of location the search connector supports:</span></span>

-   <span data-ttu-id="6cca7-127">In einer OpenSearch-Konfigurations \* Datei (OSDX-Datei) für Ihren Webdienst</span><span class="sxs-lookup"><span data-stu-id="6cca7-127">In an OpenSearch configuration (\*.osdx) file for your web service</span></span>
-   <span data-ttu-id="6cca7-128">Als Teil ihrer protokollhandlerinstallation</span><span class="sxs-lookup"><span data-stu-id="6cca7-128">As part of your protocol handler installation</span></span>

<span data-ttu-id="6cca7-129">Stellen Sie sicher, dass Folgendes passiert, wenn ein Benutzer die OSDX-Datei öffnet oder den Protokollhandler installiert:</span><span class="sxs-lookup"><span data-stu-id="6cca7-129">You should ensure that the following things happen when a user opens the .osdx file or installs the protocol handler:</span></span>

-   <span data-ttu-id="6cca7-130">Die Datei. searchconnector-MS wird im Ordner **Windows-Such** Vorgänge (% User Profile%/searches) erstellt.</span><span class="sxs-lookup"><span data-stu-id="6cca7-130">The .searchconnector-ms file is created in the users' **Windows Searches** folder (%userprofile%/Searches).</span></span>
-   <span data-ttu-id="6cca7-131">Im Ordner **Verknüpfungen** der Benutzer (% User Profile%/links) wird eine Verknüpfung mit der Datei ". searchconnector-MS" erstellt.</span><span class="sxs-lookup"><span data-stu-id="6cca7-131">A shortcut to the .searchconnector-ms file is created in the users' **Links** folder (%userprofile%/Links).</span></span>

## <a name="what-is-the-search-connector-description-schema"></a><span data-ttu-id="6cca7-132">Was ist das Suchconnector-Beschreibungs Schema?</span><span class="sxs-lookup"><span data-stu-id="6cca7-132">What Is the Search Connector Description Schema?</span></span>

<span data-ttu-id="6cca7-133">Das Suchconnector-Beschreibungs Schema ist ein XML-Schema, das die Struktur der Suchconnector-Beschreibungsdateien ( \* searchconnector-MS) definiert.</span><span class="sxs-lookup"><span data-stu-id="6cca7-133">The Search Connector Description schema is an XML schema that defines the structure of Search Connector Description files (\*.searchConnector-ms).</span></span> <span data-ttu-id="6cca7-134">Jeder Suchconnector muss über eine Suchconnector-Beschreibungsdatei verfügen, die angibt, wie eine Verbindung mit dem Speicherort hergestellt, Abfragen an ihn gesendet und Ergebnisse vom Speicherort empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="6cca7-134">Each search connector must have a Search Connector Description file that specifies how to connect to, send queries to, and receive results from the location.</span></span>

## <a name="what-are-the-major-parts-of-the-schema"></a><span data-ttu-id="6cca7-135">Worin bestehen die Hauptbestandteile des Schemas?</span><span class="sxs-lookup"><span data-stu-id="6cca7-135">What Are the Major Parts of the Schema?</span></span>

<span data-ttu-id="6cca7-136">In der folgenden Tabelle sind die Hauptbestandteile des Schemas aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6cca7-136">The following table lists the major parts of the schema.</span></span>



| <span data-ttu-id="6cca7-137">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6cca7-137">Child elements</span></span>                                                                         | <span data-ttu-id="6cca7-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6cca7-138">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cca7-139">issearchonlyitem</span><span class="sxs-lookup"><span data-stu-id="6cca7-139">isSearchOnlyItem</span></span>](search-schema-sconn-issearchonlyitem.md)                           | <span data-ttu-id="6cca7-140">Gibt an, ob die vom Suchconnector unterstützten Speicherorte nur durchsuchen oder suchen und Durchsuchen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6cca7-140">Identifies whether the locations supported by the search connector are search-only or search and browse.</span></span>                                                                                |
| [<span data-ttu-id="6cca7-141">isdefaultsaveloation</span><span class="sxs-lookup"><span data-stu-id="6cca7-141">isDefaultSaveLocation</span></span>](search-schema-sconn-isdefaultsavelocation.md)                 | <span data-ttu-id="6cca7-142">Nur für die Bibliotheks Verwendung.</span><span class="sxs-lookup"><span data-stu-id="6cca7-142">For library use only.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="6cca7-143">isdefaultnonbesitzsaveloation</span><span class="sxs-lookup"><span data-stu-id="6cca7-143">isDefaultNonOwnerSaveLocation</span></span>](search-schema-sconn-isdefaultnonownersavelocation.md) | <span data-ttu-id="6cca7-144">Nur für die Bibliotheks Verwendung.</span><span class="sxs-lookup"><span data-stu-id="6cca7-144">For library use only.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="6cca7-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cca7-145">description</span></span>](search-schema-sconn-description.md)                                     | <span data-ttu-id="6cca7-146">Beschreibt den Suchconnector.</span><span class="sxs-lookup"><span data-stu-id="6cca7-146">Describes the search connector.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="6cca7-147">iconReference</span><span class="sxs-lookup"><span data-stu-id="6cca7-147">iconReference</span></span>](search-schema-sconn-iconreference.md)                                 | <span data-ttu-id="6cca7-148">Gibt den Speicherort eines benutzerdefinierten Symbols für den Suchconnector an.</span><span class="sxs-lookup"><span data-stu-id="6cca7-148">Identifies the location of a custom icon for the search connector.</span></span>                                                                                                                      |
| [<span data-ttu-id="6cca7-149">IMAGELINK</span><span class="sxs-lookup"><span data-stu-id="6cca7-149">imageLink</span></span>](search-schema-sconn-imagelink.md)                                         | <span data-ttu-id="6cca7-150">Gibt den Speicherort einer benutzerdefinierten Miniaturansicht für den Suchconnector an.</span><span class="sxs-lookup"><span data-stu-id="6cca7-150">Identifies the location of a custom thumbnail for the search connector.</span></span>                                                                                                                 |
| [<span data-ttu-id="6cca7-151">Schrift</span><span class="sxs-lookup"><span data-stu-id="6cca7-151">author</span></span>](search-schema-sconn-author.md)                                               | <span data-ttu-id="6cca7-152">Identifiziert den Autor des Suchconnector.</span><span class="sxs-lookup"><span data-stu-id="6cca7-152">Identifies the author of the search connector.</span></span>                                                                                                                                          |
| [<span data-ttu-id="6cca7-153">DateCreated</span><span class="sxs-lookup"><span data-stu-id="6cca7-153">dateCreated</span></span>](search-schema-sconn-datecreated.md)                                     | <span data-ttu-id="6cca7-154">Gibt das Datum an, an dem der Suchconnector erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6cca7-154">Identifies the date that the search connector was created.</span></span>                                                                                                                              |
| [<span data-ttu-id="6cca7-155">templateingefo</span><span class="sxs-lookup"><span data-stu-id="6cca7-155">templateInfo</span></span>](search-schema-sconn-templateinfo.md)                                   | <span data-ttu-id="6cca7-156">Gibt einen Ordnertyp für den Suchconnector an.</span><span class="sxs-lookup"><span data-stu-id="6cca7-156">Specifies a folder type for the search connector.</span></span>                                                                                                                                       |
| [<span data-ttu-id="6cca7-157">locationprovider</span><span class="sxs-lookup"><span data-stu-id="6cca7-157">locationProvider</span></span>](search-schema-sconn-locationprovider.md)                           | <span data-ttu-id="6cca7-158">Gibt den Suchanbieter an, der von diesem Suchconnector verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6cca7-158">Specifies the search provider to be used by this search connector.</span></span>                                                                                                                      |
| [<span data-ttu-id="6cca7-159">scope</span><span class="sxs-lookup"><span data-stu-id="6cca7-159">scope</span></span>](search-schema-sconn-scope.md)                                                 | <span data-ttu-id="6cca7-160">Gibt die Speicherorte an, die in den Suchbereich eingeschlossen und aus diesem ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6cca7-160">Specifies the locations to include in and exclude from the search scope.</span></span>                                                                                                                |
| [<span data-ttu-id="6cca7-161">PropertyStore</span><span class="sxs-lookup"><span data-stu-id="6cca7-161">propertyStore</span></span>](search-schema-sconn-propertystore.md)                                 | <span data-ttu-id="6cca7-162">Gibt den Speicherort eines XML-basierten [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) für diesen Suchconnector an.</span><span class="sxs-lookup"><span data-stu-id="6cca7-162">Specifies the location of an XML-based [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) for this search connector.</span></span> <span data-ttu-id="6cca7-163">Der **IPropertyStore** unterstützt die geöffneten Metadaten des Suchconnector.</span><span class="sxs-lookup"><span data-stu-id="6cca7-163">The **IPropertyStore** supports the search connector's open metadata.</span></span> |
| [<span data-ttu-id="6cca7-164">includeinstartmen-Cope</span><span class="sxs-lookup"><span data-stu-id="6cca7-164">includeInStartMenuScope</span></span>](search-schema-sconn-includeinstartmenuscope.md)             | <span data-ttu-id="6cca7-165">Gibt an, ob der durch den Suchconnector dargestellte Speicherort im Suchbereich des Start Menüs enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="6cca7-165">Specifies whether the location represented by the search connector should be included in the Start menu's search scope.</span></span>                                                                 |
| [<span data-ttu-id="6cca7-166">-</span><span class="sxs-lookup"><span data-stu-id="6cca7-166">domain</span></span>](search-schema-sconn-domain.md)                                               | <span data-ttu-id="6cca7-167">Identifiziert die Domäne der obersten Ebene des Suchconnector.</span><span class="sxs-lookup"><span data-stu-id="6cca7-167">Identifies the search connector's top-level domain.</span></span>                                                                                                                                     |
| [<span data-ttu-id="6cca7-168">supportsadvancedquerysyntax</span><span class="sxs-lookup"><span data-stu-id="6cca7-168">supportsAdvancedQuerySyntax</span></span>](search-schema-sconn-supportsadvancedquerysyntax.md)     | <span data-ttu-id="6cca7-169">Gibt an, ob der Suchconnector Erweiterte Abfrage Syntax (AQS) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6cca7-169">Specifies whether the search connector supports Advanced Query Syntax (AQS).</span></span>                                                                                                            |
| [<span data-ttu-id="6cca7-170">isindebug</span><span class="sxs-lookup"><span data-stu-id="6cca7-170">isIndexed</span></span>](search-schema-sconn-isindexed.md)                                         | <span data-ttu-id="6cca7-171">Gibt an, ob der durch den Suchconnector dargestellte Speicherort indiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6cca7-171">Specifies whether the location represented by the search connector is indexed.</span></span>                                                                                                          |



 

## <a name="examples-of-search-connector-description-files"></a><span data-ttu-id="6cca7-172">Beispiele für Suchconnector-Beschreibungsdateien</span><span class="sxs-lookup"><span data-stu-id="6cca7-172">Examples of Search Connector Description Files</span></span>

<span data-ttu-id="6cca7-173">Im folgenden finden Sie ein Beispiel für eine Suchconnector-Beschreibungsdatei für einen Verbund Suchweb Dienst.</span><span class="sxs-lookup"><span data-stu-id="6cca7-173">The following is an example of a Search Connector Description file for a federated search web service.</span></span>


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



<span data-ttu-id="6cca7-174">Im folgenden finden Sie ein Beispiel für eine Suchconnector-Beschreibungsdatei für einen MAPI-Protokollhandler.</span><span class="sxs-lookup"><span data-stu-id="6cca7-174">The following is an example of a Search Connector Description file for a MAPI protocol handler.</span></span>


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



## <a name="additional-resources"></a><span data-ttu-id="6cca7-175">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6cca7-175">Additional Resources</span></span>

-   <span data-ttu-id="6cca7-176">Weitere Informationen zum Bibliotheks Beschreibungs Schema finden Sie unter [Bibliotheks Beschreibungs Schema](../shell/library-schema-entry.md).</span><span class="sxs-lookup"><span data-stu-id="6cca7-176">For more information about the Library Description schema, see [Library Description Schema](../shell/library-schema-entry.md).</span></span>
-   <span data-ttu-id="6cca7-177">Weitere Informationen zum Installieren eines Suchconnector finden Sie unter [Federated Search in Windows](-search-federated-search-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6cca7-177">For more information on installing a search connector, see [Federated Search in Windows](-search-federated-search-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cca7-178">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6cca7-178">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6cca7-179">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="6cca7-179">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6cca7-180">searchconnectordescriptiontype-Element (suchconnectorschema)</span><span class="sxs-lookup"><span data-stu-id="6cca7-180">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md)
</dt> <dt>

<span data-ttu-id="6cca7-181">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="6cca7-181">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="6cca7-182">OpenSearch</span><span class="sxs-lookup"><span data-stu-id="6cca7-182">OpenSearch</span></span>](http://www.opensearch.org/Home)
</dt> <dt>

[<span data-ttu-id="6cca7-183">Microsoft Download Center</span><span class="sxs-lookup"><span data-stu-id="6cca7-183">Microsoft Download Center</span></span>](https://www.microsoft.com/DOWNLOADS/en/default.aspx)
</dt> </dl>

 

 
