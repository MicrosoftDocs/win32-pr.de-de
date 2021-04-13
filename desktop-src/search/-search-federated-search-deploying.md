---
description: In diesem Thema wird erläutert, wie ein Benutzer einen neuen Remote Datenspeicher bei der Verbund-Suche registriert, indem er eine OpenSearch-Beschreibungsdatei (OSDX-Datei) öffnet, eine OSDX-Datei bereitstellt und die Verwendung des OpenSearch-Dienstanbieter nachverfolgt.
ms.assetid: 9db0f970-4e17-492b-ab75-a8b0f8011d0a
title: Bereitstellen von Suchconnectors in der Windows-Verbund Suche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a870169cd6cca3537327a8631a15d61da78eb6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484438"
---
# <a name="deploying-search-connectors-in-windows-federated-search"></a><span data-ttu-id="9c29b-103">Bereitstellen von Suchconnectors in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="9c29b-103">Deploying Search Connectors in Windows Federated Search</span></span>

<span data-ttu-id="9c29b-104">In diesem Thema wird erläutert, wie ein Benutzer einen neuen Remote Datenspeicher bei der Verbund-Suche registriert, indem er eine OpenSearch-Beschreibungsdatei (OSDX-Datei) öffnet, eine OSDX-Datei bereitstellt und die Verwendung des [OpenSearch](https://github.com/dewitt/opensearch) -Dienstanbieter nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="9c29b-104">This topic explains how a user registers a new remote data store with federated search by opening an OpenSearch Description (.osdx) file, how to deploy an .osdx file, and how to track usage of your [OpenSearch](https://github.com/dewitt/opensearch) service.</span></span>

<span data-ttu-id="9c29b-105">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="9c29b-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="9c29b-106">Die Suchconnector-MS-Datei (Suchconnector)</span><span class="sxs-lookup"><span data-stu-id="9c29b-106">The .searchconnector-ms (Search Connector) File</span></span>](#the-searchconnector-ms-search-connector-file)
-   [<span data-ttu-id="9c29b-107">Bereitstellungs Methoden</span><span class="sxs-lookup"><span data-stu-id="9c29b-107">Deployment Methods</span></span>](#deployment-methods)
    -   [<span data-ttu-id="9c29b-108">Pull-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="9c29b-108">Pull Deployment</span></span>](#pull-deployment)
    -   [<span data-ttu-id="9c29b-109">Pushbereitstellung</span><span class="sxs-lookup"><span data-stu-id="9c29b-109">Push Deployment</span></span>](#push-deployment)
-   [<span data-ttu-id="9c29b-110">Nachverfolgung der Verwendung</span><span class="sxs-lookup"><span data-stu-id="9c29b-110">Tracking Usage</span></span>](#tracking-usage)
-   [<span data-ttu-id="9c29b-111">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9c29b-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="9c29b-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c29b-112">Related topics</span></span>](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a><span data-ttu-id="9c29b-113">Die Suchconnector-MS-Datei (Suchconnector)</span><span class="sxs-lookup"><span data-stu-id="9c29b-113">The .searchconnector-ms (Search Connector) File</span></span>

<span data-ttu-id="9c29b-114">Wenn Sie lediglich die OSDX-Datei öffnen, die beschreibt, wie Sie eine Verbindung mit dem Webdienst herstellen und benutzerdefinierte Elemente in ihrer RSS-oder Atom-XML-Datei zuordnen, wird der neue Remote Datenspeicher bei der Verbund Suche registriert.</span><span class="sxs-lookup"><span data-stu-id="9c29b-114">Merely opening the .osdx file that describes how to connect to the web service and how to map any custom elements in your RSS or Atom XML registers your new remote data store with federated search.</span></span> <span data-ttu-id="9c29b-115">Ein Datenspeicher, der bereits über einen [OpenSearch](https://github.com/dewitt/opensearch) -Webdienst verfügt, der mit der Verbund Suche kompatibel ist, kann Windows-Explorer hinzugefügt werden, wenn ein Benutzer eine OSDX-Datei öffnet.</span><span class="sxs-lookup"><span data-stu-id="9c29b-115">A data store that already has an [OpenSearch](https://github.com/dewitt/opensearch) web service that is compatible with federated search can be added to Windows Explorer when a user opens an .osdx file.</span></span>

<span data-ttu-id="9c29b-116">Nachdem Sie die OSDX-Datei an den Benutzer übergeben haben und der Benutzer die OSDX-Datei öffnet, treten die folgenden Ereignisse auf.</span><span class="sxs-lookup"><span data-stu-id="9c29b-116">After you have given the .osdx to your user and the user opens the .osdx file, the following events occur.</span></span>

1.  <span data-ttu-id="9c29b-117">Eine searchconnector-MS-Datei wird im Ordner **Windows-Such** Vorgänge (% User Profile%/searches) erstellt.</span><span class="sxs-lookup"><span data-stu-id="9c29b-117">A .searchconnector-ms file is created in the **Windows Searches** folder (%userprofile%/Searches).</span></span>
2.  <span data-ttu-id="9c29b-118">Eine Verknüpfung mit der Datei. searchconnector-MS wird im Ordner **Verknüpfungen** erstellt (% User Profile%/links).</span><span class="sxs-lookup"><span data-stu-id="9c29b-118">A shortcut to the .searchconnector-ms file is created in the **Links** folder (%userprofile%/Links).</span></span>
3.  <span data-ttu-id="9c29b-119">Im Windows Explorer-Navigations **Favoriten** Bereich wird eine Verknüpfung angezeigt, sodass der Benutzer in den neuen Datenspeicher navigieren und den Webdienst Abfragen kann.</span><span class="sxs-lookup"><span data-stu-id="9c29b-119">A shortcut appears in the Windows Explorer navigation **Favorites** pane, enabling the user to navigate into the new data store and query the web service.</span></span>

## <a name="deployment-methods"></a><span data-ttu-id="9c29b-120">Bereitstellungsmethoden</span><span class="sxs-lookup"><span data-stu-id="9c29b-120">Deployment Methods</span></span>

<span data-ttu-id="9c29b-121">Es gibt zwei Möglichkeiten zum Bereitstellen von Suchconnectors, der Pull-Bereitstellung und der pushbereitstellung.</span><span class="sxs-lookup"><span data-stu-id="9c29b-121">There are two ways to deploy search connectors, pull deployment and push deployment.</span></span>

### <a name="pull-deployment"></a><span data-ttu-id="9c29b-122">Pull-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="9c29b-122">Pull Deployment</span></span>

<span data-ttu-id="9c29b-123">Bei der Pull-Bereitstellung werden alle Bereitstellungs Arten beschrieben, bei denen der Endbenutzer die Initiative zum Installieren der Suchconnectors übernimmt.</span><span class="sxs-lookup"><span data-stu-id="9c29b-123">Pull deployment describes any type of deployment in which the end user takes the initiative to install the search connectors.</span></span> <span data-ttu-id="9c29b-124">Gängige Methoden der Pull-Bereitstellung sind:</span><span class="sxs-lookup"><span data-stu-id="9c29b-124">Common methods of pull deployment are:</span></span>

-   <span data-ttu-id="9c29b-125">Anfügen der OSDX-Datei in eine e-Mail.</span><span class="sxs-lookup"><span data-stu-id="9c29b-125">Attaching the .osdx file in an email.</span></span>
-   <span data-ttu-id="9c29b-126">Veröffentlichen der Datei auf einer Webseite.</span><span class="sxs-lookup"><span data-stu-id="9c29b-126">Posting the file on a webpage.</span></span>
-   <span data-ttu-id="9c29b-127">Bereitstellen eines dynamischen Links auf der Intranetsite Beispielsweise wird eine benutzerdefinierte OSDX-Datei erstellt, die auf der Benutzer Auswahl oder dem aktuellen Bereich innerhalb des Standorts basiert.</span><span class="sxs-lookup"><span data-stu-id="9c29b-127">Providing a dynamic link on your intranet site; for example, one that generates custom .osdx files based on user choices or the current scope within the site.</span></span>

<span data-ttu-id="9c29b-128">Damit die Datei heruntergeladen wird, wenn der Benutzer in Ihrem Browser auf den Link klickt, muss der Webserver, auf dem der Webdienst gehostet wird, so konfiguriert werden, dass die OSDX-Datei als Datei bereitstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9c29b-128">For the file to be downloaded when the user clicks the link in their browser, the web server hosting the web service must be configured to deliver the .osdx as a file.</span></span> <span data-ttu-id="9c29b-129">Daher müssen Sie die MIME-Typen auf dem Webserver so konfigurieren, dass OSDX-Dateien als behandelt werden `"application/opensearchdescription+xml"` .</span><span class="sxs-lookup"><span data-stu-id="9c29b-129">Hence, you must configure the MIME Types on the web server to treat .osdx files as `"application/opensearchdescription+xml"`.</span></span> <span data-ttu-id="9c29b-130">Optional können Sie das von Microsoft bereitgestellte Symbol zum Identifizieren des Suchconnector-Links verwenden.</span><span class="sxs-lookup"><span data-stu-id="9c29b-130">Optionally, you can use the icon supplied by Microsoft to identify search connector link.</span></span>

### <a name="push-deployment"></a><span data-ttu-id="9c29b-131">Pushbereitstellung</span><span class="sxs-lookup"><span data-stu-id="9c29b-131">Push Deployment</span></span>

<span data-ttu-id="9c29b-132">Pushbereitstellung beschreibt jede Art von Bereitstellung, die nicht von der Benutzer Initiative abhängt, um die Suchconnectors zu installieren.</span><span class="sxs-lookup"><span data-stu-id="9c29b-132">Push deployment describes any type of deployment that does not depend on user initiative to install the search connectors.</span></span> <span data-ttu-id="9c29b-133">Häufige Methoden der pushbereitstellung sind:</span><span class="sxs-lookup"><span data-stu-id="9c29b-133">Common methods of push deployment are:</span></span>

-   <span data-ttu-id="9c29b-134">Gruppenrichtlinie Einstellungen (GPP)</span><span class="sxs-lookup"><span data-stu-id="9c29b-134">Group Policy Preferences (GPP)</span></span>
-   <span data-ttu-id="9c29b-135">Anmeldeskript</span><span class="sxs-lookup"><span data-stu-id="9c29b-135">Logon script</span></span>
-   <span data-ttu-id="9c29b-136">Roamingprofile</span><span class="sxs-lookup"><span data-stu-id="9c29b-136">Roaming profiles</span></span>
-   <span data-ttu-id="9c29b-137">Bildverarbeitung</span><span class="sxs-lookup"><span data-stu-id="9c29b-137">Imaging</span></span>

## <a name="tracking-usage"></a><span data-ttu-id="9c29b-138">Nachverfolgung der Verwendung</span><span class="sxs-lookup"><span data-stu-id="9c29b-138">Tracking Usage</span></span>

<span data-ttu-id="9c29b-139">Um die Verwendung des [OpenSearch](https://github.com/dewitt/opensearch) -Diensts durch Benutzer zu verfolgen, die im Windows-Explorer suchen, Filtern Sie die Webserver-Protokolldateien für diese Benutzer-Agent-Zeichenfolge: `Windows-Search+(Windows+NT+6.1)` .</span><span class="sxs-lookup"><span data-stu-id="9c29b-139">To track the usage of your [OpenSearch](https://github.com/dewitt/opensearch) service by users searching from Windows Explorer, filter your web server log files for this user agent string: `Windows-Search+(Windows+NT+6.1)`.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9c29b-140">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9c29b-140">Additional Resources</span></span>

<span data-ttu-id="9c29b-141">Weitere Informationen zum Implementieren eines Such Verbunds in Remote Datenspeicher mithilfe von OpenSearch-Technologien in Windows 7 und höher finden Sie unter "zusätzliche Ressourcen" bei der [Verbund Suche in Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9c29b-141">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c29b-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c29b-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c29b-143">Verbundsuche in Windows 10</span><span class="sxs-lookup"><span data-stu-id="9c29b-143">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="9c29b-144">Ersten Einstieg in die Verbund Suche in Windows</span><span class="sxs-lookup"><span data-stu-id="9c29b-144">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="9c29b-145">Verbinden des Webdiensts in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="9c29b-145">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="9c29b-146">Aktivieren des Datenspeicher in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="9c29b-146">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="9c29b-147">Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="9c29b-147">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="9c29b-148">Bewährte Methoden bei der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="9c29b-148">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> </dl>

 

 
