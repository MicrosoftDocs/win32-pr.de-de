---
title: Herunterfahren und bereinigen
description: Damit eine Anwendung ordnungsgemäß beendet wird, muss Sie die folgenden Bereinigungs Vorgänge ausführen.
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf1c59534b73fee21489439c7818c286874185d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037067"
---
# <a name="shutdown-and-cleanup"></a><span data-ttu-id="d59f2-103">Herunterfahren und bereinigen</span><span class="sxs-lookup"><span data-stu-id="d59f2-103">Shutdown and Cleanup</span></span>

<span data-ttu-id="d59f2-104">Damit eine Anwendung ordnungsgemäß beendet wird, muss Sie die folgenden Bereinigungs Vorgänge ausführen:</span><span class="sxs-lookup"><span data-stu-id="d59f2-104">For an application to terminate gracefully, it must perform the following cleanup operations:</span></span>

-   <span data-ttu-id="d59f2-105">Entfernen Sie alle registrierten URLs aus der URL-Gruppe, indem Sie die [**httpremoveurlfromurlgroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) -Funktion aufrufen, um die zuvor beim Aufruf von [**httpaddurltourlgroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup)registrierten URLs aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="d59f2-105">Remove all registered URLs from the URL group by calling the [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) function to deregister URLs previously registered in the call to [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).</span></span>
-   <span data-ttu-id="d59f2-106">Schließen Sie die URL-Gruppe, indem Sie die [**httpcloseurlgroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d59f2-106">Close the URL Group by calling the [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) function.</span></span> <span data-ttu-id="d59f2-107">Alle URL-Gruppen, die unter einer Server Sitzung erstellt wurden, müssen vor dem Schließen der Server Sitzung geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="d59f2-107">All the URL groups created under a server session must be closed before closing the server session.</span></span>
-   <span data-ttu-id="d59f2-108">Schließen Sie die Server Sitzung, indem Sie [**httpcloseserversession**](/windows/desktop/api/Http/nf-http-httpcloseserversession)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d59f2-108">Close the server session by calling [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).</span></span>
-   <span data-ttu-id="d59f2-109">Schließen Sie das Handle für die Anforderungs Warteschlange, indem Sie [**httpcloserequestqueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d59f2-109">Close the handle to the request queue by calling [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).</span></span>
-   <span data-ttu-id="d59f2-110">Beenden Sie die von der HTTP-Server-API erstellten Ressourcen, indem Sie die [**httpend**](/windows/desktop/api/Http/nf-http-httpterminate) -Funktion mit übereinstimmenden Flageinstellungen für jeden Aufruf der Anwendung aufrufen, die ursprünglich für [**httpinitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d59f2-110">Terminate the resources created by the HTTP Server API by calling the [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) function with matching flag settings for each call the application originally made to [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span></span> <span data-ttu-id="d59f2-111">Jeder dieser Aufrufe beendet alle Ressourcen, die im Aufruf von [**httpinitialize**](/windows/desktop/api/Http/nf-http-httpinitialize)erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="d59f2-111">Each of these calls terminates all resources created in the call to [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span></span>

 

 




