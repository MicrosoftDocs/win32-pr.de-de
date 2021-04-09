---
description: In diesem Thema werden die Schritte zum Verbinden eines Webdiensts zwischen dem Datenspeicher und der Windows-Verbund Suche beschrieben, und es wird beschrieben, wie Sie Abfragen senden und Suchergebnisse in RSS oder Atom zurückgeben.
ms.assetid: 4c8de310-49e6-4d90-a920-0c715351c86a
title: Verbinden des Webdiensts in der Windows-Verbund Suche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45632d1d3c7b820ab1f39db0896c9f2927b24ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128577"
---
# <a name="connecting-your-web-service-in-windows-federated-search"></a><span data-ttu-id="b403f-103">Verbinden des Webdiensts in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="b403f-103">Connecting Your Web Service in Windows Federated Search</span></span>

<span data-ttu-id="b403f-104">In diesem Thema werden die Schritte zum Verbinden eines Webdiensts zwischen dem Datenspeicher und der Windows-Verbund Suche beschrieben, und es wird beschrieben, wie Sie Abfragen senden und Suchergebnisse in RSS oder Atom zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b403f-104">This topic describes the steps involved in connecting a web service between your data store and Windows Federated Search, and how to send queries and return search results in RSS or Atom.</span></span>

<span data-ttu-id="b403f-105">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="b403f-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="b403f-106">Webdienst verbinden</span><span class="sxs-lookup"><span data-stu-id="b403f-106">Connect Your web Service</span></span>](#connect-your-web-service)
-   [<span data-ttu-id="b403f-107">Registrieren eines vorhandenen Remote Datenspeicher</span><span class="sxs-lookup"><span data-stu-id="b403f-107">Register an Existing Remote Data Store</span></span>](#register-an-existing-remote-data-store)
-   [<span data-ttu-id="b403f-108">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b403f-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="b403f-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b403f-109">Related topics</span></span>](#related-topics)

## <a name="connect-your-web-service"></a><span data-ttu-id="b403f-110">Webdienst verbinden</span><span class="sxs-lookup"><span data-stu-id="b403f-110">Connect Your web Service</span></span>

<span data-ttu-id="b403f-111">**Führen Sie die folgenden Schritte aus, um den Webdienst des Datenspeicher mit der Verbund Suche zu verbinden:**</span><span class="sxs-lookup"><span data-stu-id="b403f-111">**To connect the web service of your data store to federated search, perform the following steps:**</span></span>

1.  <span data-ttu-id="b403f-112">Erstellen Sie eine OSDX-Datei.</span><span class="sxs-lookup"><span data-stu-id="b403f-112">Create an .osdx file.</span></span>
2.  <span data-ttu-id="b403f-113">Stellen Sie die OSDX-Datei für Benutzer bereit, damit Sie den Dienst bei Bedarf hinzufügen können, indem Sie die OSDX-Datei öffnen.</span><span class="sxs-lookup"><span data-stu-id="b403f-113">Supply the .osdx file to users so that they can add the service on demand by opening the .osdx file.</span></span>
3.  <span data-ttu-id="b403f-114">Generieren Sie einen Suchconnector, und stellen Sie ihn aktiv in Ihrem Unternehmen bereit.</span><span class="sxs-lookup"><span data-stu-id="b403f-114">Generate a search connector and actively deploy it in your enterprise.</span></span>

## <a name="register-an-existing-remote-data-store"></a><span data-ttu-id="b403f-115">Registrieren eines vorhandenen Remote Datenspeicher</span><span class="sxs-lookup"><span data-stu-id="b403f-115">Register an Existing Remote Data Store</span></span>

<span data-ttu-id="b403f-116">Ein Benutzer registriert einen neuen Remote Datenspeicher bei der Windows-Verbund Suche, indem er eine OpenSearch-Beschreibungsdatei (OSDX-Datei) öffnet.</span><span class="sxs-lookup"><span data-stu-id="b403f-116">A user registers a new remote data store with Windows Federated Search by opening an OpenSearch Description (.osdx) file.</span></span> <span data-ttu-id="b403f-117">Wenn der Benutzer dies tut, treten die folgenden Ereignisse auf:</span><span class="sxs-lookup"><span data-stu-id="b403f-117">When the user does so, the following events occur:</span></span>

1.  <span data-ttu-id="b403f-118">Eine searchconnector-MS-Datei (Search-Connector) wird im Ordner Windows-Suchvorgänge (% User Profile%/searches) erstellt.</span><span class="sxs-lookup"><span data-stu-id="b403f-118">A .searchconnector-ms file (search connector) is created in the Windows Searches folder (%userprofile%/Searches).</span></span>
2.  <span data-ttu-id="b403f-119">Eine Verknüpfung mit der Datei. searchconnector-MS wird im Ordner Verknüpfungen erstellt (% User Profile%/links).</span><span class="sxs-lookup"><span data-stu-id="b403f-119">A shortcut to the .searchconnector-ms file is created in the Links folder (%userprofile%/Links).</span></span>
3.  <span data-ttu-id="b403f-120">Im Windows Explorer-Navigations **Favoriten** Bereich wird eine Verknüpfung angezeigt, die es dem Benutzer ermöglicht, in den neuen Datenspeicher zu navigieren und den Webdienst abzufragen.</span><span class="sxs-lookup"><span data-stu-id="b403f-120">A shortcut appears in the Windows Explorer navigation **Favorites** pane, enabling the user to navigate into the new data store, and query the web service.</span></span>

> [!Note]  
> <span data-ttu-id="b403f-121">Ein Datenspeicher, der bereits über einen [OpenSearch](https://github.com/dewitt/opensearch) -Webdienst verfügt, der mit der Windows-Verbund Suche kompatibel ist, kann Windows-Explorer hinzugefügt werden, wenn ein Benutzer eine OSDX-Datei öffnet.</span><span class="sxs-lookup"><span data-stu-id="b403f-121">A data store that already has an [OpenSearch](https://github.com/dewitt/opensearch) web service that is compatible with Windows Federated Search can be added to Windows Explorer when a user opens an .osdx file.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="b403f-122">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b403f-122">Additional Resources</span></span>

<span data-ttu-id="b403f-123">Weitere Informationen zum Implementieren eines Such Verbunds in Remote Datenspeicher mithilfe von OpenSearch-Technologien in Windows 7 und höher finden Sie unter "zusätzliche Ressourcen" bei der [Verbund Suche in Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b403f-123">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b403f-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b403f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b403f-125">Verbundsuche in Windows 10</span><span class="sxs-lookup"><span data-stu-id="b403f-125">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="b403f-126">Ersten Einstieg in die Verbund Suche in Windows</span><span class="sxs-lookup"><span data-stu-id="b403f-126">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="b403f-127">Aktivieren des Datenspeicher in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="b403f-127">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="b403f-128">Erstellen einer OpenSearch-Beschreibungsdatei in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="b403f-128">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="b403f-129">Bewährte Methoden bei der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="b403f-129">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="b403f-130">Bereitstellen von Suchconnectors in der Windows-Verbund Suche</span><span class="sxs-lookup"><span data-stu-id="b403f-130">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
