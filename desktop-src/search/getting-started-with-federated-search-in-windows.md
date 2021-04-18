---
description: Die Unterstützung von Windows 7 zum Durchsuchen von Verbund zu Remote Daten speichern mithilfe von OpenSearch-Technologien ermöglicht Benutzern den Zugriff auf und die Interaktion mit ihren Remote Daten aus Windows-Explorer.
ms.assetid: c25dbc33-3f9a-4e40-965e-9be639ababed
title: Ersten Einstieg in die Verbund Suche in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058c1f887ff2bdba279cdd25e4910162dd9263d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525469"
---
# <a name="getting-started-with-federated-search-in-windows"></a><span data-ttu-id="7f697-103">Ersten Einstieg in die Verbund Suche in Windows</span><span class="sxs-lookup"><span data-stu-id="7f697-103">Getting Started with Federated Search in Windows</span></span>

<span data-ttu-id="7f697-104">Die Unterstützung von Windows 7 zum Durchsuchen von Verbund zu Remote Daten speichern mithilfe von OpenSearch-Technologien ermöglicht Benutzern den Zugriff auf und die Interaktion mit ihren Remote Daten aus Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="7f697-104">Windows 7 support for search federation to remote data stores using OpenSearch technologies enables users to access and interact with their remote data from within Windows Explorer.</span></span> <span data-ttu-id="7f697-105">Sie können einen webbasierten Datenspeicher erstellen, der mithilfe der Windows-Verbund Suche durchsucht werden kann, und eine umfassende Integration Ihrer Remote Datenquellen mit Windows-Explorer aktivieren, ohne dass Windows-Client seitiger Code geschrieben oder bereitgestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="7f697-105">You can build a web-based data store that can be searched using Windows federated search and enable rich integration of your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

<span data-ttu-id="7f697-106">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="7f697-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="7f697-107">Was ist eine Verbund Suche?</span><span class="sxs-lookup"><span data-stu-id="7f697-107">What is Federated Search?</span></span>](#what-is-federated-search)
-   [<span data-ttu-id="7f697-108">Schritte zum Aufbauen der Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-108">Steps for Building Federated Search</span></span>](#steps-for-building-federated-search)
-   [<span data-ttu-id="7f697-109">Funktionsweise der Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-109">How Federated Search Works</span></span>](#how-federated-search-works)
-   [<span data-ttu-id="7f697-110">Senden von Abfragen und Zurückgeben von Suchergebnissen in RSS oder Atom</span><span class="sxs-lookup"><span data-stu-id="7f697-110">Sending Queries and Returning Search Results in RSS or Atom</span></span>](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [<span data-ttu-id="7f697-111">Beispiele für die Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-111">Federated Search Examples</span></span>](#federated-search-examples)
-   [<span data-ttu-id="7f697-112">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7f697-112">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="7f697-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7f697-113">Related topics</span></span>](#related-topics)

## <a name="what-is-federated-search"></a><span data-ttu-id="7f697-114">Was ist eine Verbund Suche?</span><span class="sxs-lookup"><span data-stu-id="7f697-114">What is Federated Search?</span></span>

<span data-ttu-id="7f697-115">Windows 7 unterstützt die Verbindung externer Quellen mit dem Windows-Client über das [OpenSearch](https://github.com/dewitt/opensearch) -Protokoll.</span><span class="sxs-lookup"><span data-stu-id="7f697-115">Windows 7 supports the connection of external sources to the Windows client through the [OpenSearch](https://github.com/dewitt/opensearch) protocol.</span></span> <span data-ttu-id="7f697-116">Dies ermöglicht es Benutzern, in Windows-Explorer einen Remote Datenspeicher zu durchsuchen und Ergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7f697-116">This enables users to search a remote data store and view results from within Windows Explorer.</span></span> <span data-ttu-id="7f697-117">Der Standard [OpenSearch](https://github.com/dewitt/opensearch) v 1.1 definiert einfache Dateiformate, die verwendet werden können, um zu beschreiben, wie ein Client den Webdienst für den Datenspeicher Abfragen soll und wie der Dienst Ergebnisse zurückgeben soll, die vom Client gerendert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7f697-117">The [OpenSearch](https://github.com/dewitt/opensearch) v1.1 standard defines simple file formats that can be used to describe how a client should query the web service for the data store and how the service should return results to be rendered by the client.</span></span> <span data-ttu-id="7f697-118">Die Windows-Verbund Suche stellt eine Verbindung mit Webdiensten her, die [OpenSearch](https://github.com/dewitt/opensearch) -Abfragen empfangen, und gibt Ergebnisse entweder im RSS-oder Atom-XML-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="7f697-118">Windows federated search connects to web services that receive [OpenSearch](https://github.com/dewitt/opensearch) queries, and returns results in either the RSS or Atom XML format.</span></span>

<span data-ttu-id="7f697-119">Der folgende Screenshot veranschaulicht die Suchergebnisse, die nach der Remote Suche einer SharePoint-Website abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7f697-119">The following screen shot illustrates the search results obtained after remotely searching a SharePoint site.</span></span>

![Screenshot, der Suchergebnisse von einer SharePoint-Website anzeigt, wie in Windows-Explorer angezeigt](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a><span data-ttu-id="7f697-121">Schritte zum Aufbauen der Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-121">Steps for Building Federated Search</span></span>

<span data-ttu-id="7f697-122">Führen Sie die folgenden Schritte aus, um eine Verbund Suche zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="7f697-122">To build federated search, perform the following steps:</span></span>

1.  <span data-ttu-id="7f697-123">Aktivieren Sie den Datenspeicher in Windows-Explorer, indem Sie einen [OpenSearch](https://github.com/dewitt/opensearch)-kompatiblen Webdienst bereitstellen, der Ergebnisse im RSS-oder Atom-Format zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="7f697-123">Enable your data store to be searched from Windows Explorer by providing an [OpenSearch](https://github.com/dewitt/opensearch)-compatible web service that can return results in RSS or Atom format.</span></span>
2.  <span data-ttu-id="7f697-124">Erstellen Sie eine OpenSearch-Beschreibungsdatei (OSDX-Datei), in der beschrieben wird, wie eine Verbindung mit dem Webdienst hergestellt wird und wie benutzerdefinierte Elemente in der RSS-oder Atom-XML-Datei</span><span class="sxs-lookup"><span data-stu-id="7f697-124">Create an OpenSearch Description (.osdx) file that describes how to connect to the web service and how to map any custom elements in your RSS or Atom XML.</span></span>
3.  <span data-ttu-id="7f697-125">Stellen Sie die Suchconnectors auf Windows-Client Computern mit einer OSDX-Datei bereit.</span><span class="sxs-lookup"><span data-stu-id="7f697-125">Deploy the search connectors to Windows client computers with an .osdx file.</span></span>

<span data-ttu-id="7f697-126">Das folgende Diagramm veranschaulicht die Schritte zum Aufbau der Verbund Suche.</span><span class="sxs-lookup"><span data-stu-id="7f697-126">The following diagram illustrates the steps for building federated search.</span></span>

![Diagramm des Prozesses zum Aufbauen der Verbund Suche](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a><span data-ttu-id="7f697-128">Funktionsweise der Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-128">How Federated Search Works</span></span>

<span data-ttu-id="7f697-129">Die Kommunikation zwischen Windows-Explorer und Ihrem [OpenSearch](https://github.com/dewitt/opensearch) -Webdienst erfolgt über die Windows-Datenschicht.</span><span class="sxs-lookup"><span data-stu-id="7f697-129">Communication between Windows Explorer and your [OpenSearch](https://github.com/dewitt/opensearch) web service is performed through the Windows Data Layer.</span></span> <span data-ttu-id="7f697-130">Die Windows-Datenschicht kann über Windows Store-Anbieter mit unterschiedlichen Datenspeicher Typen kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="7f697-130">The Windows Data Layer can communicate with different types of data stores through Windows Store Providers.</span></span> <span data-ttu-id="7f697-131">Jeder Anbieter spezialisiert sich auf die Kommunikation mit Daten speichern, die ein bestimmtes Protokoll unterstützen und über bestimmte Funktionen verfügen.</span><span class="sxs-lookup"><span data-stu-id="7f697-131">Each provider specializes in communicating with data stores that support a particular protocol and have specific capabilities.</span></span> <span data-ttu-id="7f697-132">Die folgende Abbildung zeigt z. b., wie der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter mit Daten speichern kommuniziert, die einen Webdienst bereitstellen, der den [OpenSearch](https://github.com/dewitt/opensearch) -Standard unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7f697-132">For example, the following illustration sows how the [OpenSearch](https://github.com/dewitt/opensearch) provider communicates with data stores that provide a web service that supports the [OpenSearch](https://github.com/dewitt/opensearch) standard.</span></span>

![Diagramm, das die Kommunikation von Windows-Explorer auf dem Client über den OpenSearch-Datenspeicher auf dem Remote Server anzeigt](images/windowssearchfederationfunctionality.png)

<span data-ttu-id="7f697-134">Um dem Datenspeicher die Unterstützung der Verbund Suche in Windows 7 zu ermöglichen, müssen Sie eine Reihe von Tasks ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f697-134">To enable your data store to support federated search in Windows 7, you must perform a number of tasks.</span></span> <span data-ttu-id="7f697-135">In der folgenden Tabelle sind die Aufgaben zum Aktivieren des Datenspeicher, zum Ausführen der einzelnen Aufgaben und zum Speicherort der Dokumentation aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f697-135">The following table lists tasks for enabling your data store, what is required to accomplish each task, and where to find documentation.</span></span>



| <span data-ttu-id="7f697-136">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="7f697-136">Task</span></span>                                                                                                     | <span data-ttu-id="7f697-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f697-137">Requirement</span></span>                                                                                                                                                                                            | <span data-ttu-id="7f697-138">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="7f697-138">Documentation</span></span>                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f697-139">Aktivieren Sie den Datenspeicher, der von Windows Explorer durchsucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f697-139">Enable your data store to be searched by Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="7f697-140">Erstellen Sie einen mit OpenSearch kompatiblen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="7f697-140">Build an OpenSearch-compatible web service.</span></span><br/> <span data-ttu-id="7f697-141">Erstellen Sie eine OpenSearch-Beschreibungsdatei (OSDX-Datei).</span><span class="sxs-lookup"><span data-stu-id="7f697-141">Create an OpenSearch Description (.osdx) file.</span></span><br/>                                                                                       | [<span data-ttu-id="7f697-142">Verbinden des Webdiensts in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-142">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/> [<span data-ttu-id="7f697-143">Aktivieren des Datenspeicher in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-143">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/> |
| <span data-ttu-id="7f697-144">Stellen Sie Ihren Webdienst aktiv für Benutzer in einem Unternehmen bereit.</span><span class="sxs-lookup"><span data-stu-id="7f697-144">Actively deploy your web service to users within an enterprise.</span></span><br/>                               | <span data-ttu-id="7f697-145">Stellen Sie eine OSDX-Datei für Ihre Benutzer bereit, kopieren Sie Sie lokal, und machen Sie den Benutzer über eine Verknüpfung zugänglich.</span><span class="sxs-lookup"><span data-stu-id="7f697-145">Supply an .osdx file to your users, copy it locally, and make it accessible to the user via a shortcut.</span></span><br/>                                                                                     | [<span data-ttu-id="7f697-146">Bereitstellen von Suchconnectors in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-146">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)<br/>                                                                                                              |
| <span data-ttu-id="7f697-147">Listet die Suchergebnisse in Windows-Explorer als Antwort auf eine Abfrage auf.</span><span class="sxs-lookup"><span data-stu-id="7f697-147">Enumerate search results in Windows Explorer in response to a query.</span></span><br/>                          | <span data-ttu-id="7f697-148">Implementieren Sie einen Webdienst, der eine Abfrage Zeichenfolge akzeptiert und Ergebnisse im RSS-oder Atom-Format zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7f697-148">Implement a web service that accepts a query string and returns results in RSS or Atom format.</span></span><br/>                                                                                              | [<span data-ttu-id="7f697-149">Verbinden des Webdiensts in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-149">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/>                                                                                                            |
| <span data-ttu-id="7f697-150">Ermöglichen Sie es Benutzern, Ihren Datenspeicher Ihrem Windows-Explorer hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7f697-150">Enable users to add your data store to their Windows Explorer.</span></span><br/>                                | <span data-ttu-id="7f697-151">Erstellen Sie eine OSDX-Datei, und stellen Sie Sie für Ihre Benutzer bereit.</span><span class="sxs-lookup"><span data-stu-id="7f697-151">Create an .osdx file and supply it to your users.</span></span><br/>                                                                                                                                           | [<span data-ttu-id="7f697-152">Aktivieren des Datenspeicher in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-152">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="7f697-153">Zeigen Sie Ihre Elemente in Windows-Explorer als Datei ähnliche Elemente an.</span><span class="sxs-lookup"><span data-stu-id="7f697-153">Display your items as file-like items in Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="7f697-154">Zurückgeben einer URL zum Datei-oder Inhaltsstream mithilfe von **Gehäuse** oder **Medien: Inhalts** Elemente</span><span class="sxs-lookup"><span data-stu-id="7f697-154">Return a URL to the file or content stream by using **enclosure** or **media:content** elements</span></span><br/> <span data-ttu-id="7f697-155">Geben Sie eine Dateinamenerweiterung oder einen MIME-Typ an, der vom Client Computer erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="7f697-155">Supply a file name extension or a MIME type that the client computer recognizes.</span></span><br/> | [<span data-ttu-id="7f697-156">Aktivieren des Datenspeicher in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-156">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="7f697-157">Anzeigen benutzerdefinierter Eigenschaften in Windows-Explorer, außer den in den RSS-oder Atom-Standards definierten.</span><span class="sxs-lookup"><span data-stu-id="7f697-157">Display custom properties in Windows Explorer, beyond those defined in RSS or Atom standards.</span></span><br/> | <span data-ttu-id="7f697-158">Stellen Sie zusätzliche Metadaten bereit, indem Sie einen anderen XML-Namespace in der RSS/Atom-Ausgabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="7f697-158">Provide additional metadata by using another XML namespace in your RSS/Atom output.</span></span><br/> <span data-ttu-id="7f697-159">Fügen Sie der OSDX-Datei eine Eigenschaften Zuordnung hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f697-159">Add a property map to your .osdx file.</span></span><br/>                                                       | [<span data-ttu-id="7f697-160">Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-160">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="7f697-161">Passen Sie die Eigenschaften an, die für ihre Elemente in Windows-Explorer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7f697-161">Customize the properties that are displayed for your items in Windows Explorer.</span></span><br/>               | <span data-ttu-id="7f697-162">Fügen Sie der OSDX-Datei proplist-Zuordnungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f697-162">Add proplist mappings to your .osdx file.</span></span><br/>                                                                                                                                                   | [<span data-ttu-id="7f697-163">Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-163">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="7f697-164">Zeigen Sie eine benutzerdefinierte Webseiten Ansicht Ihrer Elemente im Vorschaubereich an.</span><span class="sxs-lookup"><span data-stu-id="7f697-164">Display a custom webpage view of your items in the preview pane.</span></span><br/>                              | <span data-ttu-id="7f697-165">Gibt eindeutige Link-und Gehäuse Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="7f697-165">Return distinct link and enclosure values.</span></span><br/> <span data-ttu-id="7f697-166">Ordnen Sie der Windows Shell-Eigenschaft **System. webpreviewurl** einen URL-Wert zu.</span><span class="sxs-lookup"><span data-stu-id="7f697-166">Map a URL value to the **System.WebPreviewUrl** Windows Shell property.</span></span><br/>                                                               | [<span data-ttu-id="7f697-167">Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-167">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="7f697-168">Anzeigen einer Befehls leisten Schaltfläche in Windows-Explorer, die die Abfrage auf Ihre Website überträgt.</span><span class="sxs-lookup"><span data-stu-id="7f697-168">Display a command bar button in Windows Explorer that rolls the query over to your website.</span></span><br/>   | <span data-ttu-id="7f697-169">Stellen Sie eine `Url format="text/html"` Vorlage in der OSDX-Datei bereit.</span><span class="sxs-lookup"><span data-stu-id="7f697-169">Provide a `Url format="text/html"` template in the .osdx file.</span></span><br/>                                                                                                                              | [<span data-ttu-id="7f697-170">Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-170">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a><span data-ttu-id="7f697-171">Senden von Abfragen und Zurückgeben von Suchergebnissen in RSS oder Atom</span><span class="sxs-lookup"><span data-stu-id="7f697-171">Sending Queries and Returning Search Results in RSS or Atom</span></span>

<span data-ttu-id="7f697-172">Wenn der Benutzer einen Begriff in das Suchfeld in der oberen rechten Ecke von Windows-Explorer eingibt, wird die Abfrage an den [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter gesendet, der die Abfrage dann an den Remote Datenspeicher sendet.</span><span class="sxs-lookup"><span data-stu-id="7f697-172">When the user types a term into the search box in the upper-right corner of Windows Explorer, the query is sent to the [OpenSearch](https://github.com/dewitt/opensearch) provider, which then sends the query to the remote data store.</span></span> <span data-ttu-id="7f697-173">Der Remoteweb Dienst antwortet auf die Abfrage, indem Ergebnisse in einem XML-Dokument (in der Regel als Feed bezeichnet) in einem von zwei unterstützten Formaten (RSS oder Atom) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7f697-173">The remote web service responds to the query by providing results in an XML document, typically referred to as a feed, in one of two supported formats (RSS or Atom).</span></span> <span data-ttu-id="7f697-174">Jedes Ergebnis Element im Feed enthält untergeordnete XML-Elemente, um Element Metadaten darzustellen oder zu beschreiben, wie z. b. Titel, URL, Beschreibung, Miniaturbild und so weiter.</span><span class="sxs-lookup"><span data-stu-id="7f697-174">Each result item in the feed includes XML child elements to represent or describe item metadata, such as the title, URL, description, thumbnail image, and so forth.</span></span> <span data-ttu-id="7f697-175">Der [OpenSearch](https://github.com/dewitt/opensearch) -Anbieter ist für die Zuordnung der XML-Element Werte zu den Windows Shell-Systemeigenschaften zuständig, die von Windows-Anwendungen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="7f697-175">The [OpenSearch](https://github.com/dewitt/opensearch) provider is responsible for mapping the XML element values to Windows Shell system properties that can be used by Windows applications.</span></span>

## <a name="federated-search-examples"></a><span data-ttu-id="7f697-176">Beispiele für die Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-176">Federated Search Examples</span></span>

<span data-ttu-id="7f697-177">Die folgende OpenSearch-Beispieldatei (OSDX-Datei) besteht aus `ShortName` -und- `Url` Elementen, bei denen es sich um die mindestens erforderlichen untergeordneten Elemente handelt, um einen externen Datenspeicher mit dem Windows-Client über das OpenSearch-Protokoll zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="7f697-177">The following example OpenSearch Description (.osdx) file consists of `ShortName` and `Url` elements, which are the minimum required child elements to connect an external data store to the Windows client through the OpenSearch protocol.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



<span data-ttu-id="7f697-178">Im folgenden Beispiel wird veranschaulicht, wie Sie einen webfähigen Datenspeicher im RSS-Format durchsuchbar machen und angeben, dass ein Suchelement zurückgegeben werden soll:</span><span class="sxs-lookup"><span data-stu-id="7f697-178">The following example illustrates how to make a web-enabled data store searchable in RSS format, and how to specify that one search item be returned:</span></span>


```
<rss version="2.0" xmlns:media="https://search.yahoo.com/mrss/" xmlns:example="https://example.com/namespace">
   <channel>
      <title>Search Results</title>
      <item>
         <title>An example result</title>
         <link>https://example.com/pictures.aspx?id=01</link>
         <description>This is a test of the emergency search results system. If this were a real emergency result, then you would be reading something more useful.</description>
         <pubDate>Wed, 1 Oct 2008 23:12:00 GMT</pubDate>
         <media:content url="https://example.com/pictures/picture01.jpg" fileSize="212889" type="image/jpeg" height="768" width="1024"/>
         <media:thumbnail url="https://example.com/thumbnails/picture01.jpg" height="120" width="160"/>
         <example:dateTaken>Mon, 22 Sep 2008 23:12:00 GMT</example:dateTaken>
      </item>
   </channel>
</rss>
```



<span data-ttu-id="7f697-179">Im folgenden Beispiel wird veranschaulicht, wie Eigenschaften zu Standardsystem Eigenschaften zugeordnet werden, damit angezeigte Elemente sortiert und gruppiert werden:</span><span class="sxs-lookup"><span data-stu-id="7f697-179">The following example illustrates how to map properties to default system properties so that displayed items are sorted and grouped:</span></span>


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



<span data-ttu-id="7f697-180">Im folgenden Beispiel wird veranschaulicht, wie jedem Element in Windows-Explorer eine Miniaturbild Anzeige hinzugefügt wird:</span><span class="sxs-lookup"><span data-stu-id="7f697-180">The following example illustrates how to adds a thumbnail image display to each item in Windows Explorer:</span></span>


```
<media:thumbnail>    
```



## <a name="additional-resources"></a><span data-ttu-id="7f697-181">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7f697-181">Additional Resources</span></span>

<span data-ttu-id="7f697-182">Weitere Informationen zum Implementieren eines Such Verbunds in Remote Datenspeicher mithilfe von OpenSearch-Technologien in Windows 7 und höher finden Sie unter "zusätzliche Ressourcen" bei der [Verbund Suche in Windows](-search-federated-search-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7f697-182">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](-search-federated-search-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f697-183">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7f697-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f697-184">Verbundsuche in Windows 10</span><span class="sxs-lookup"><span data-stu-id="7f697-184">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="7f697-185">Verbinden des Webdiensts in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-185">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="7f697-186">Aktivieren des Datenspeicher in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-186">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="7f697-187">Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-187">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="7f697-188">Bewährte Methoden bei der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-188">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="7f697-189">Bereitstellen von Suchconnectors in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="7f697-189">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 




