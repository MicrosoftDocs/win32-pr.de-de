---
description: Erfahren Sie mehr über die Verbundsuche, die es Benutzern ermöglicht, auf ihre Remotedaten innerhalb von Windows-Explorer.
ms.assetid: c25dbc33-3f9a-4e40-965e-9be639ababed
title: Erste Schritte mit Der Verbundsuche in Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de3fc42686e94f2edc1c5d45bbb0374afe79535
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119065"
---
# <a name="getting-started-with-federated-search-in-windows"></a><span data-ttu-id="3ae1b-103">Erste Schritte mit Der Verbundsuche in Windows</span><span class="sxs-lookup"><span data-stu-id="3ae1b-103">Getting Started with Federated Search in Windows</span></span>

<span data-ttu-id="3ae1b-104">Die Windows 7-Unterstützung für den Suchverbund mit Remotedatenspeichern mithilfe von OpenSearch-Technologien ermöglicht Benutzern den Zugriff auf und die Interaktion mit ihren Remotedaten aus Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-104">Windows 7 support for search federation to remote data stores using OpenSearch technologies enables users to access and interact with their remote data from within Windows Explorer.</span></span> <span data-ttu-id="3ae1b-105">Sie können einen webbasierten Datenspeicher erstellen, der mithilfe der Windows-Verbundsuche durchsucht werden kann, und eine umfassende Integration Ihrer Remotedatenquellen mit Windows-Explorer ermöglichen, ohne clientseitigen Windows-Code schreiben oder bereitstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-105">You can build a web-based data store that can be searched using Windows federated search and enable rich integration of your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

<span data-ttu-id="3ae1b-106">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="3ae1b-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="3ae1b-107">Was ist die Verbundsuche?</span><span class="sxs-lookup"><span data-stu-id="3ae1b-107">What is Federated Search?</span></span>](#what-is-federated-search)
-   [<span data-ttu-id="3ae1b-108">Schritte zum Erstellen der Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-108">Steps for Building Federated Search</span></span>](#steps-for-building-federated-search)
-   [<span data-ttu-id="3ae1b-109">Funktionsweise der Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-109">How Federated Search Works</span></span>](#how-federated-search-works)
-   [<span data-ttu-id="3ae1b-110">Senden von Abfragen und Zurückgeben von Suchergebnissen in RSS oder Atom</span><span class="sxs-lookup"><span data-stu-id="3ae1b-110">Sending Queries and Returning Search Results in RSS or Atom</span></span>](#sending-queries-and-returning-search-results-in-rss-or-atom)
-   [<span data-ttu-id="3ae1b-111">Beispiele für die Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-111">Federated Search Examples</span></span>](#federated-search-examples)
-   [<span data-ttu-id="3ae1b-112">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3ae1b-112">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="3ae1b-113">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3ae1b-113">Related topics</span></span>](#related-topics)

## <a name="what-is-federated-search"></a><span data-ttu-id="3ae1b-114">Was ist die Verbundsuche?</span><span class="sxs-lookup"><span data-stu-id="3ae1b-114">What is Federated Search?</span></span>

<span data-ttu-id="3ae1b-115">Windows 7 unterstützt die Verbindung externer Quellen mit dem Windows-Client über das [OpenSearch-Protokoll.](https://github.com/dewitt/opensearch)</span><span class="sxs-lookup"><span data-stu-id="3ae1b-115">Windows 7 supports the connection of external sources to the Windows client through the [OpenSearch](https://github.com/dewitt/opensearch) protocol.</span></span> <span data-ttu-id="3ae1b-116">Auf diese Weise können Benutzer einen Remotedatenspeicher durchsuchen und Ergebnisse innerhalb Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-116">This enables users to search a remote data store and view results from within Windows Explorer.</span></span> <span data-ttu-id="3ae1b-117">Der [OpenSearch](https://github.com/dewitt/opensearch) v1.1-Standard definiert einfache Dateiformate, die verwendet werden können, um zu beschreiben, wie ein Client den Webdienst nach dem Datenspeicher abfragen soll und wie der Dienst Ergebnisse zurückgeben soll, die vom Client gerendert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-117">The [OpenSearch](https://github.com/dewitt/opensearch) v1.1 standard defines simple file formats that can be used to describe how a client should query the web service for the data store and how the service should return results to be rendered by the client.</span></span> <span data-ttu-id="3ae1b-118">Die Windows-Verbundsuche stellt eine Verbindung mit Webdiensten mit [OpenSearch-Abfragen](https://github.com/dewitt/opensearch) sicher und gibt Ergebnisse im RSS- oder Atom-XML-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-118">Windows federated search connects to web services that receive [OpenSearch](https://github.com/dewitt/opensearch) queries, and returns results in either the RSS or Atom XML format.</span></span>

<span data-ttu-id="3ae1b-119">Der folgende Screenshot veranschaulicht die Suchergebnisse, die nach der Remotesuche einer SharePoint-Website erzielt wurden.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-119">The following screen shot illustrates the search results obtained after remotely searching a SharePoint site.</span></span>

![Screenshot: Suchergebnisse von einer SharePoint-Website, wie sie im Windows-Explorer angezeigt werden](images/searchingasharepointsitefromwindowsexp.png)

## <a name="steps-for-building-federated-search"></a><span data-ttu-id="3ae1b-121">Schritte zum Erstellen der Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-121">Steps for Building Federated Search</span></span>

<span data-ttu-id="3ae1b-122">Führen Sie die folgenden Schritte aus, um eine Verbundsuche zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="3ae1b-122">To build federated search, perform the following steps:</span></span>

1.  <span data-ttu-id="3ae1b-123">Ermöglichen Sie das Durchsuchen Ihres Datenspeichers über Windows-Explorer, indem Sie einen [OpenSearch-kompatiblen](https://github.com/dewitt/opensearch)Webdienst bereitstellen, der Ergebnisse im RSS- oder Atom-Format zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-123">Enable your data store to be searched from Windows Explorer by providing an [OpenSearch](https://github.com/dewitt/opensearch)-compatible web service that can return results in RSS or Atom format.</span></span>
2.  <span data-ttu-id="3ae1b-124">Erstellen Sie eine OpenSearch-Beschreibungsdatei (OSDX), in der beschrieben wird, wie Sie eine Verbindung mit dem Webdienst herstellen und benutzerdefinierte Elemente in RSS oder Atom XML zuordnen.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-124">Create an OpenSearch Description (.osdx) file that describes how to connect to the web service and how to map any custom elements in your RSS or Atom XML.</span></span>
3.  <span data-ttu-id="3ae1b-125">Stellen Sie die Suchconnectors mit einer OSDX-Datei auf Windows-Clientcomputern zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-125">Deploy the search connectors to Windows client computers with an .osdx file.</span></span>

<span data-ttu-id="3ae1b-126">Das folgende Diagramm veranschaulicht die Schritte zum Erstellen der Verbundsuche.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-126">The following diagram illustrates the steps for building federated search.</span></span>

![Diagramm des Prozesses zum Erstellen einer Verbundsuche](images/queryinganewopensearchremotedatastore.png)

## <a name="how-federated-search-works"></a><span data-ttu-id="3ae1b-128">Funktionsweise der Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-128">How Federated Search Works</span></span>

<span data-ttu-id="3ae1b-129">Die Kommunikation zwischen Windows-Explorer und Ihrem [OpenSearch-Webdienst](https://github.com/dewitt/opensearch) erfolgt über die Windows-Datenebene.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-129">Communication between Windows Explorer and your [OpenSearch](https://github.com/dewitt/opensearch) web service is performed through the Windows Data Layer.</span></span> <span data-ttu-id="3ae1b-130">Die Windows-Datenschicht kann über Windows Store-Anbieter mit verschiedenen Arten von Datenspeichern kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-130">The Windows Data Layer can communicate with different types of data stores through Windows Store Providers.</span></span> <span data-ttu-id="3ae1b-131">Jeder Anbieter ist auf die Kommunikation mit Datenspeichern spezialisiert, die ein bestimmtes Protokoll unterstützen und über bestimmte Funktionen verfügen.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-131">Each provider specializes in communicating with data stores that support a particular protocol and have specific capabilities.</span></span> <span data-ttu-id="3ae1b-132">Die folgende Abbildung zeigt beispielsweise, wie der [OpenSearch-Anbieter](https://github.com/dewitt/opensearch) mit Datenspeichern kommuniziert, die einen Webdienst bereitstellen, der [den OpenSearch-Standard](https://github.com/dewitt/opensearch) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-132">For example, the following illustration sows how the [OpenSearch](https://github.com/dewitt/opensearch) provider communicates with data stores that provide a web service that supports the [OpenSearch](https://github.com/dewitt/opensearch) standard.</span></span>

![Diagramm, das die Kommunikation vom Windows-Explorer auf dem Client über den Opensearch-Datenspeicher auf dem Remoteserver zeigt](images/windowssearchfederationfunctionality.png)

<span data-ttu-id="3ae1b-134">Damit Ihr Datenspeicher die Verbundsuche in Windows 7 unterstützen kann, müssen Sie eine Reihe von Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-134">To enable your data store to support federated search in Windows 7, you must perform a number of tasks.</span></span> <span data-ttu-id="3ae1b-135">In der folgenden Tabelle sind die Aufgaben zum Aktivieren Ihres Datenspeichers, die erforderlichen Aufgaben und der Ort der Dokumentation aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-135">The following table lists tasks for enabling your data store, what is required to accomplish each task, and where to find documentation.</span></span>



| <span data-ttu-id="3ae1b-136">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="3ae1b-136">Task</span></span>                                                                                                     | <span data-ttu-id="3ae1b-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ae1b-137">Requirement</span></span>                                                                                                                                                                                            | <span data-ttu-id="3ae1b-138">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="3ae1b-138">Documentation</span></span>                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae1b-139">Aktivieren Sie die Suche nach Ihrem Datenspeicher durch Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-139">Enable your data store to be searched by Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="3ae1b-140">Erstellen Sie einen OpenSearch-kompatiblen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-140">Build an OpenSearch-compatible web service.</span></span><br/> <span data-ttu-id="3ae1b-141">Erstellen Sie eine OpenSearch-Beschreibungsdatei (.osdx).</span><span class="sxs-lookup"><span data-stu-id="3ae1b-141">Create an OpenSearch Description (.osdx) file.</span></span><br/>                                                                                       | [<span data-ttu-id="3ae1b-142">Verbinden Ihres Webdiensts in der Windows-Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-142">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/> [<span data-ttu-id="3ae1b-143">Aktivieren des Datenspeichers in der Windows-Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-143">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/> |
| <span data-ttu-id="3ae1b-144">Stellen Sie Ihren Webdienst aktiv für Benutzer in einem Unternehmen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-144">Actively deploy your web service to users within an enterprise.</span></span><br/>                               | <span data-ttu-id="3ae1b-145">Stellen Sie Ihren Benutzern eine OSDX-Datei zur Verfügung, kopieren Sie sie lokal, und machen Sie sie über eine Verknüpfung für den Benutzer zugänglich.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-145">Supply an .osdx file to your users, copy it locally, and make it accessible to the user via a shortcut.</span></span><br/>                                                                                     | [<span data-ttu-id="3ae1b-146">Bereitstellen von Suchconnectors in der Windows-Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-146">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)<br/>                                                                                                              |
| <span data-ttu-id="3ae1b-147">Aufzählen von Suchergebnissen in Windows-Explorer als Antwort auf eine Abfrage.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-147">Enumerate search results in Windows Explorer in response to a query.</span></span><br/>                          | <span data-ttu-id="3ae1b-148">Implementieren Sie einen Webdienst, der eine Abfragezeichenfolge akzeptiert und Ergebnisse im RSS- oder Atom-Format zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-148">Implement a web service that accepts a query string and returns results in RSS or Atom format.</span></span><br/>                                                                                              | [<span data-ttu-id="3ae1b-149">Verbinden Ihres Webdiensts in der Windows-Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-149">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)<br/>                                                                                                            |
| <span data-ttu-id="3ae1b-150">Ermöglichen Sie es Benutzern, Ihren Datenspeicher zu ihren Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-150">Enable users to add your data store to their Windows Explorer.</span></span><br/>                                | <span data-ttu-id="3ae1b-151">Erstellen Sie eine OSDX-Datei, und stellen Sie sie Ihren Benutzern zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-151">Create an .osdx file and supply it to your users.</span></span><br/>                                                                                                                                           | [<span data-ttu-id="3ae1b-152">Aktivieren des Datenspeichers in der Windows-Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-152">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="3ae1b-153">Zeigen Sie Ihre Elemente als dateispezifische Elemente in Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-153">Display your items as file-like items in Windows Explorer.</span></span><br/>                                    | <span data-ttu-id="3ae1b-154">Zurückgeben einer URL zur Datei oder zum Inhaltsstream mithilfe von **Gehäuse-** oder **media:content-Elementen**</span><span class="sxs-lookup"><span data-stu-id="3ae1b-154">Return a URL to the file or content stream by using **enclosure** or **media:content** elements</span></span><br/> <span data-ttu-id="3ae1b-155">Geben Sie eine Dateierweiterung oder einen MIME-Typ an, den der Clientcomputer erkennt.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-155">Supply a file name extension or a MIME type that the client computer recognizes.</span></span><br/> | [<span data-ttu-id="3ae1b-156">Aktivieren des Datenspeichers in der Windows-Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-156">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)<br/>                                                                                                                |
| <span data-ttu-id="3ae1b-157">Zeigen Sie benutzerdefinierte Eigenschaften in Windows-Explorer, die über die in RSS- oder Atom-Standards definierten hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-157">Display custom properties in Windows Explorer, beyond those defined in RSS or Atom standards.</span></span><br/> | <span data-ttu-id="3ae1b-158">Geben Sie zusätzliche Metadaten an, indem Sie einen anderen XML-Namespace in Ihrer RSS/Atom-Ausgabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-158">Provide additional metadata by using another XML namespace in your RSS/Atom output.</span></span><br/> <span data-ttu-id="3ae1b-159">Fügen Sie Ihrer OSDX-Datei eine Eigenschaftenzuordnung hinzu.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-159">Add a property map to your .osdx file.</span></span><br/>                                                       | [<span data-ttu-id="3ae1b-160">Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-160">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="3ae1b-161">Passen Sie die Eigenschaften an, die für Ihre Elemente in der Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-161">Customize the properties that are displayed for your items in Windows Explorer.</span></span><br/>               | <span data-ttu-id="3ae1b-162">Fügen Sie Ihrer OSDX-Datei Proplist-Zuordnungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-162">Add proplist mappings to your .osdx file.</span></span><br/>                                                                                                                                                   | [<span data-ttu-id="3ae1b-163">Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-163">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="3ae1b-164">Zeigen Sie eine benutzerdefinierte Webseitenansicht Ihrer Elemente im Vorschaubereich an.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-164">Display a custom webpage view of your items in the preview pane.</span></span><br/>                              | <span data-ttu-id="3ae1b-165">Gibt eindeutige Link- und Gehäusewerte zurück.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-165">Return distinct link and enclosure values.</span></span><br/> <span data-ttu-id="3ae1b-166">Ordnen Sie der Windows Shell-Eigenschaft **System.WebPreviewUrl** einen URL-Wert zu.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-166">Map a URL value to the **System.WebPreviewUrl** Windows Shell property.</span></span><br/>                                                               | [<span data-ttu-id="3ae1b-167">Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-167">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |
| <span data-ttu-id="3ae1b-168">Zeigen Sie eine Befehlsleistenschaltfläche in Windows-Explorer, die die Abfrage auf Ihre Website überrollt.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-168">Display a command bar button in Windows Explorer that rolls the query over to your website.</span></span><br/>   | <span data-ttu-id="3ae1b-169">Geben Sie `Url format="text/html"` eine Vorlage in der OSDX-Datei an.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-169">Provide a `Url format="text/html"` template in the .osdx file.</span></span><br/>                                                                                                                              | [<span data-ttu-id="3ae1b-170">Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-170">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)<br/>                                                                                                  |



 

## <a name="sending-queries-and-returning-search-results-in-rss-or-atom"></a><span data-ttu-id="3ae1b-171">Senden von Abfragen und Zurückgeben von Suchergebnissen in RSS oder Atom</span><span class="sxs-lookup"><span data-stu-id="3ae1b-171">Sending Queries and Returning Search Results in RSS or Atom</span></span>

<span data-ttu-id="3ae1b-172">Wenn der Benutzer einen Begriff in das Suchfeld in der oberen rechten Ecke von Windows-Explorer ein gibt, wird die Abfrage an den [OpenSearch-Anbieter](https://github.com/dewitt/opensearch) gesendet, der die Abfrage dann an den Remotedatenspeicher sendet.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-172">When the user types a term into the search box in the upper-right corner of Windows Explorer, the query is sent to the [OpenSearch](https://github.com/dewitt/opensearch) provider, which then sends the query to the remote data store.</span></span> <span data-ttu-id="3ae1b-173">Der Remotewebdienst antwortet auf die Abfrage, indem er Ergebnisse in einem XML-Dokument, das in der Regel als Feed bezeichnet wird, in einem von zwei unterstützten Formaten (RSS oder Atom) liefert.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-173">The remote web service responds to the query by providing results in an XML document, typically referred to as a feed, in one of two supported formats (RSS or Atom).</span></span> <span data-ttu-id="3ae1b-174">Jedes Ergebniselement im Feed enthält untergeordnete XML-Elemente, die Elementmetadaten darstellen oder beschreiben, z. B. Titel, URL, Beschreibung, Miniaturansicht usw.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-174">Each result item in the feed includes XML child elements to represent or describe item metadata, such as the title, URL, description, thumbnail image, and so forth.</span></span> <span data-ttu-id="3ae1b-175">Der [OpenSearch-Anbieter](https://github.com/dewitt/opensearch) ist für die Zuordnung der XML-Elementwerte zu Windows Shell-Systemeigenschaften verantwortlich, die von Windows-Anwendungen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-175">The [OpenSearch](https://github.com/dewitt/opensearch) provider is responsible for mapping the XML element values to Windows Shell system properties that can be used by Windows applications.</span></span>

## <a name="federated-search-examples"></a><span data-ttu-id="3ae1b-176">Beispiele für die Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-176">Federated Search Examples</span></span>

<span data-ttu-id="3ae1b-177">Die folgende OpenSearch Description(.osdx)-Beispieldatei besteht aus - und -Elementen, die die mindestens erforderlichen untergeordneten Elemente zum Verbinden eines externen Datenspeichers mit dem Windows-Client über das `ShortName` `Url` OpenSearch-Protokoll sind.</span><span class="sxs-lookup"><span data-stu-id="3ae1b-177">The following example OpenSearch Description (.osdx) file consists of `ShortName` and `Url` elements, which are the minimum required child elements to connect an external data store to the Windows client through the OpenSearch protocol.</span></span>


```
<OpenSearchDescription xmlns="https://a9.com/-/spec/opensearch/1.1/">
        <ShortName>My web Service</ShortName>
        <Url format="application/rss+xml" template="https://example.com/rss.php?query={searchTerms}&amp;start={startIndex}&amp;cnt={count}" />
        </OpenSearchDescription>
```



<span data-ttu-id="3ae1b-178">Im folgenden Beispiel wird veranschaulicht, wie sie einen webfähigen Datenspeicher im RSS-Format durchsuchbar machen und angeben, dass ein Suchelement zurückgegeben wird:</span><span class="sxs-lookup"><span data-stu-id="3ae1b-178">The following example illustrates how to make a web-enabled data store searchable in RSS format, and how to specify that one search item be returned:</span></span>


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



<span data-ttu-id="3ae1b-179">Das folgende Beispiel veranschaulicht das Zuordnen von Eigenschaften zu Standardsystemeigenschaften, sodass angezeigte Elemente sortiert und gruppiert werden:</span><span class="sxs-lookup"><span data-stu-id="3ae1b-179">The following example illustrates how to map properties to default system properties so that displayed items are sorted and grouped:</span></span>


```
<author>Sanjay Jacobs</author>
                <category>Nature</category>
                <pubDate>Thu, 24 Apr 2008 2003 21:34:38 GTMT</pubDate>
```



<span data-ttu-id="3ae1b-180">Im folgenden Beispiel wird veranschaulicht, wie jedem Element in der Datei eine Miniaturbildanzeige Windows-Explorer:</span><span class="sxs-lookup"><span data-stu-id="3ae1b-180">The following example illustrates how to adds a thumbnail image display to each item in Windows Explorer:</span></span>


```
<media:thumbnail>    
```



## <a name="additional-resources"></a><span data-ttu-id="3ae1b-181">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3ae1b-181">Additional Resources</span></span>

<span data-ttu-id="3ae1b-182">Weitere Informationen zum Implementieren des Suchverbunds in Remotedatenspeicher mit opensearch-Technologien in Windows 7 und höher finden Sie unter "Zusätzliche Ressourcen" unter [Verbundsuche in Windows.](-search-federated-search-overview.md)</span><span class="sxs-lookup"><span data-stu-id="3ae1b-182">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](-search-federated-search-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ae1b-183">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3ae1b-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ae1b-184">Verbundsuche in Windows 10</span><span class="sxs-lookup"><span data-stu-id="3ae1b-184">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="3ae1b-185">Verbinden Ihres Webdiensts in der Windows-Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-185">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="3ae1b-186">Aktivieren des Datenspeichers in der Windows-Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-186">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="3ae1b-187">Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-187">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="3ae1b-188">Bewährte Methoden bei der Windows-Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-188">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="3ae1b-189">Bereitstellen von Suchconnectors in der Windows-Verbundsuche</span><span class="sxs-lookup"><span data-stu-id="3ae1b-189">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 




