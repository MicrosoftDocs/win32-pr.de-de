---
title: Funktionen der HTTP-Server-API, Version 1,0
description: Die HTTP-Server-API stellt die folgenden Funktionen zum Schreiben von Anwendungen bereit.
ms.assetid: 1da9907d-a09d-41e1-aca1-9a8e2b91296f
keywords:
- Funktionen der HTTP-Server-API, Version 1,0
- Funktionen http, http-Server-API, Version 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050821e40695268d6e3fa2c946d2e8859748db2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207198"
---
# <a name="http-server-api-version-10-functions"></a><span data-ttu-id="6d200-105">Funktionen der HTTP-Server-API, Version 1,0</span><span class="sxs-lookup"><span data-stu-id="6d200-105">HTTP Server API Version 1.0 Functions</span></span>

<span data-ttu-id="6d200-106">Die HTTP-Server-API stellt die folgenden Funktionen zum Schreiben von Anwendungen bereit.</span><span class="sxs-lookup"><span data-stu-id="6d200-106">The HTTP Server API provides the following functions for writing applications.</span></span>

## <a name="general"></a><span data-ttu-id="6d200-107">Allgemein</span><span class="sxs-lookup"><span data-stu-id="6d200-107">General</span></span>



| <span data-ttu-id="6d200-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="6d200-108">Function</span></span>                                             | <span data-ttu-id="6d200-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d200-109">Description</span></span>                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d200-110">**Httpkreatehttphandle**</span><span class="sxs-lookup"><span data-stu-id="6d200-110">**HttpCreateHttpHandle**</span></span>](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) | <span data-ttu-id="6d200-111">Erstellt eine HTTP-Anforderungs Warteschlange und gibt ein Handle für diese zurück.</span><span class="sxs-lookup"><span data-stu-id="6d200-111">Creates an HTTP request queue and returns a handle to it.</span></span>                                                                         |
| [<span data-ttu-id="6d200-112">**Httpinitialize**</span><span class="sxs-lookup"><span data-stu-id="6d200-112">**HttpInitialize**</span></span>](/windows/desktop/api/Http/nf-http-httpinitialize)             | <span data-ttu-id="6d200-113">Initialisiert die HTTP-Server-API für die Verwendung durch den aufrufenden Prozess.</span><span class="sxs-lookup"><span data-stu-id="6d200-113">Initializes the HTTP Server API for use by the calling process.</span></span>                                                                   |
| [<span data-ttu-id="6d200-114">**Httpprepareurl**</span><span class="sxs-lookup"><span data-stu-id="6d200-114">**HttpPrepareUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpprepareurl)             | <span data-ttu-id="6d200-115">Analysiert, analysiert und normalisiert eine nicht normalisierte Unicode-oder Punycode-URL, sodass Sie sicher und in anderen HTTP-Funktionen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6d200-115">Parses, analyzes, and normalizes a non-normalized Unicode or punycode URL so it is safe and valid to use in other HTTP functions.</span></span> |
| [<span data-ttu-id="6d200-116">**Httpbeenden**</span><span class="sxs-lookup"><span data-stu-id="6d200-116">**HttpTerminate**</span></span>](/windows/desktop/api/Http/nf-http-httpterminate)               | <span data-ttu-id="6d200-117">Leitet die HTTP-Server-API an, um alle einem bestimmten Prozess zugeordneten Ressourcen zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="6d200-117">Directs the HTTP Server API to clean up any resources associated with a particular process.</span></span>                                       |



 

## <a name="cache-management"></a><span data-ttu-id="6d200-118">Cache Verwaltung</span><span class="sxs-lookup"><span data-stu-id="6d200-118">Cache Management</span></span>



| <span data-ttu-id="6d200-119">Funktion</span><span class="sxs-lookup"><span data-stu-id="6d200-119">Function</span></span>                                                       | <span data-ttu-id="6d200-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d200-120">Description</span></span>                                                                                            |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d200-121">**Httpaddfragmenttocache**</span><span class="sxs-lookup"><span data-stu-id="6d200-121">**HttpAddFragmentToCache**</span></span>](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache)       | <span data-ttu-id="6d200-122">Speichert ein Daten Fragment zwischen, sodass es verwendet werden kann, um eine dynamische Antwort ohne Lesevorgang vom Datenträger zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6d200-122">Caches a data fragment so that it can be used to compose a dynamic response without reading from disk.</span></span> |
| [<span data-ttu-id="6d200-123">**Httpflushresponlcache**</span><span class="sxs-lookup"><span data-stu-id="6d200-123">**HttpFlushResponseCache**</span></span>](/windows/desktop/api/Http/nf-http-httpflushresponsecache)       | <span data-ttu-id="6d200-124">Entfernt die angegebenen zwischengespeicherten Fragmente aus dem HTTP-Cache.</span><span class="sxs-lookup"><span data-stu-id="6d200-124">Removes specified cached fragments from the HTTP cache.</span></span>                                                |
| [<span data-ttu-id="6d200-125">**Httpreadfragmentfromcache**</span><span class="sxs-lookup"><span data-stu-id="6d200-125">**HttpReadFragmentFromCache**</span></span>](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) | <span data-ttu-id="6d200-126">Ruft ein angegebenes zwischen gespeicherter Antwort Fragment ab.</span><span class="sxs-lookup"><span data-stu-id="6d200-126">Retrieves a specified cached response fragment.</span></span>                                                        |



 

## <a name="configuration"></a><span data-ttu-id="6d200-127">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="6d200-127">Configuration</span></span>



| <span data-ttu-id="6d200-128">Funktion</span><span class="sxs-lookup"><span data-stu-id="6d200-128">Function</span></span>                                                                 | <span data-ttu-id="6d200-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d200-129">Description</span></span>                                                       |
|--------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="6d200-130">**Httpdelta eteserviceconfiguration**</span><span class="sxs-lookup"><span data-stu-id="6d200-130">**HttpDeleteServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) | <span data-ttu-id="6d200-131">Löscht die angegebenen Informationen aus dem http-Konfigurations Speicher.</span><span class="sxs-lookup"><span data-stu-id="6d200-131">Deletes specified information from the HTTP configuration store.</span></span>  |
| [<span data-ttu-id="6d200-132">**Httpqueryserviceconfiguration**</span><span class="sxs-lookup"><span data-stu-id="6d200-132">**HttpQueryServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration)   | <span data-ttu-id="6d200-133">Fragt den HTTP-Konfigurations Speicher nach angegebenen Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="6d200-133">Queries the HTTP configuration store for specified information.</span></span>   |
| [<span data-ttu-id="6d200-134">**Httpsetserviceconfiguration**</span><span class="sxs-lookup"><span data-stu-id="6d200-134">**HttpSetServiceConfiguration**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration)       | <span data-ttu-id="6d200-135">Legt die angegebenen Werte im Konfigurations Speicher der HTTP-Server-API fest.</span><span class="sxs-lookup"><span data-stu-id="6d200-135">Sets specified values in the HTTP Server API configuration store.</span></span> |



 

## <a name="input-and-output"></a><span data-ttu-id="6d200-136">Eingabe und Ausgabe</span><span class="sxs-lookup"><span data-stu-id="6d200-136">Input and Output</span></span>



| <span data-ttu-id="6d200-137">Funktion</span><span class="sxs-lookup"><span data-stu-id="6d200-137">Function</span></span>                                                             | <span data-ttu-id="6d200-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d200-138">Description</span></span>                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="6d200-139">**Httpreceivehttprequest**</span><span class="sxs-lookup"><span data-stu-id="6d200-139">**HttpReceiveHttpRequest**</span></span>](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)             | <span data-ttu-id="6d200-140">Ruft eine HTTP-Anforderung aus einer angegebenen Anforderungs Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="6d200-140">Retrieves an HTTP request from a specified request queue.</span></span>      |
| [<span data-ttu-id="6d200-141">**Httpreceiverequestentitybody**</span><span class="sxs-lookup"><span data-stu-id="6d200-141">**HttpReceiveRequestEntityBody**</span></span>](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) | <span data-ttu-id="6d200-142">Ruft Entitäts Text Daten einer bestimmten HTTP-Anforderung ab.</span><span class="sxs-lookup"><span data-stu-id="6d200-142">Retrieves entity-body data of a particular HTTP request.</span></span>       |
| [<span data-ttu-id="6d200-143">**HttpSendHttpResponse**</span><span class="sxs-lookup"><span data-stu-id="6d200-143">**HttpSendHttpResponse**</span></span>](/windows/desktop/api/Http/nf-http-httpsendhttpresponse)                 | <span data-ttu-id="6d200-144">Sendet eine HTTP-Antwort für eine bestimmte HTTP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6d200-144">Sends an HTTP response for a particular HTTP request.</span></span>          |
| [<span data-ttu-id="6d200-145">**Httpsendresponabentitybody**</span><span class="sxs-lookup"><span data-stu-id="6d200-145">**HttpSendResponseEntityBody**</span></span>](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)     | <span data-ttu-id="6d200-146">Sendet Entitäts Text Daten einer HTTP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="6d200-146">Sends entity-body data of an HTTP response.</span></span>                    |
| [<span data-ttu-id="6d200-147">**Httpwaitfordisconnect**</span><span class="sxs-lookup"><span data-stu-id="6d200-147">**HttpWaitForDisconnect**</span></span>](/windows/desktop/api/Http/nf-http-httpwaitfordisconnect)               | <span data-ttu-id="6d200-148">Benachrichtigt die Anwendung, wenn ein HTTP-Client eine Verbindungs Trennung durch hat.</span><span class="sxs-lookup"><span data-stu-id="6d200-148">Notifies the application when an HTTP client has disconnected.</span></span> |



 

## <a name="ssl"></a><span data-ttu-id="6d200-149">SSL</span><span class="sxs-lookup"><span data-stu-id="6d200-149">SSL</span></span>



| <span data-ttu-id="6d200-150">Funktion</span><span class="sxs-lookup"><span data-stu-id="6d200-150">Function</span></span>                                                             | <span data-ttu-id="6d200-151">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d200-151">Description</span></span>                                             |
|----------------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="6d200-152">**Httpreceiveclientcertificate**</span><span class="sxs-lookup"><span data-stu-id="6d200-152">**HttpReceiveClientCertificate**</span></span>](/windows/desktop/api/Http/nf-http-httpreceiveclientcertificate) | <span data-ttu-id="6d200-153">Ruft das Client Zertifikat für eine SSL-Verbindung ab.</span><span class="sxs-lookup"><span data-stu-id="6d200-153">Retrieves the client certificate for an SSL connection.</span></span> |



 

## <a name="url-registration"></a><span data-ttu-id="6d200-154">URL-Registrierung</span><span class="sxs-lookup"><span data-stu-id="6d200-154">URL Registration</span></span>



| <span data-ttu-id="6d200-155">Funktion</span><span class="sxs-lookup"><span data-stu-id="6d200-155">Function</span></span>                               | <span data-ttu-id="6d200-156">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d200-156">Description</span></span>                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d200-157">**Httpaddurl**</span><span class="sxs-lookup"><span data-stu-id="6d200-157">**HttpAddUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpaddurl)       | <span data-ttu-id="6d200-158">Registriert eine URL so, dass HTTP-Anforderungen für Sie an eine angegebene Anforderungs Warteschlange weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="6d200-158">Registers a URL so that HTTP requests for it are routed to a specified request queue.</span></span>           |
| [<span data-ttu-id="6d200-159">**Httpremoveurl**</span><span class="sxs-lookup"><span data-stu-id="6d200-159">**HttpRemoveUrl**</span></span>](/windows/desktop/api/Http/nf-http-httpremoveurl) | <span data-ttu-id="6d200-160">Hebt die Registrierung einer angegebenen URL auf, sodass keine Anforderungen mehr an eine angegebene Warteschlange weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="6d200-160">Unregisters a specified URL, so that requests for it are no longer routed to a specified queue.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6d200-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d200-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d200-162">HTTP Server-API, Version 1,0, Strukturen</span><span class="sxs-lookup"><span data-stu-id="6d200-162">HTTP Server API Version 1.0 Structures</span></span>](http-server-api-version-1-0-structures.md)
</dt> </dl>

 

 




