---
description: Network DDE wird zum initiieren und Verwalten der Netzwerkverbindungen verwendet, die für DDE-Konversationen zwischen Anwendungen benötigt werden, die auf verschiedenen Computern in einem Netzwerk ausgeführt werden.
ms.assetid: f9eee391-2b4a-4c17-bea5-72cda5124e1c
title: Informationen zu Network DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412971f6bef8d2782dce38b5aef413e4d073f6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345088"
---
# <a name="about-network-dde"></a><span data-ttu-id="15ba9-103">Informationen zu Network DDE</span><span class="sxs-lookup"><span data-stu-id="15ba9-103">About Network DDE</span></span>

<span data-ttu-id="15ba9-104">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="15ba9-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="15ba9-105">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="15ba9-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="15ba9-106">Network DDE wird zum initiieren und Verwalten der Netzwerkverbindungen verwendet, die für DDE-Konversationen zwischen Anwendungen benötigt werden, die auf verschiedenen Computern in einem Netzwerk ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="15ba9-106">Network DDE is used to initiate and maintain the network connections needed for DDE conversations between applications running on different computers in a network.</span></span> <span data-ttu-id="15ba9-107">Eine DDE- *Konversation* ist die Interaktion zwischen Client-und Server Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="15ba9-107">A DDE *conversation* is the interaction between client and server applications.</span></span> <span data-ttu-id="15ba9-108">Sie verwenden Network DDE zusammen mit DDE und der DDE Management Library (Ddeml) in Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="15ba9-108">You use network DDE along with DDE and the DDE management library (DDEML) in your application.</span></span>

<span data-ttu-id="15ba9-109">DDE ist eine Form der prozessübergreifenden Kommunikation, die gemeinsam genutzten Speicher zum Austauschen von Daten zwischen Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="15ba9-109">DDE is a form of interprocess communication that uses shared memory to exchange data between applications.</span></span> <span data-ttu-id="15ba9-110">Anwendungen können DDE für einen einmaligen Datentransfer oder für den laufenden Austausch und das Aktualisieren von Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="15ba9-110">Applications can use DDE for one time data transfers or for ongoing exchanges and updating data.</span></span> <span data-ttu-id="15ba9-111">Weitere Informationen zu DDE finden Sie unter [dynamischer Datenaustausch](../dataxchg/dynamic-data-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="15ba9-111">For more information on DDE, see [Dynamic Data Exchange](../dataxchg/dynamic-data-exchange.md).</span></span>

<span data-ttu-id="15ba9-112">Ddeml vereinfacht das Hinzufügen von DDE-Funktionen zu einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="15ba9-112">DDEML simplifies the task of adding DDE capability to an application.</span></span> <span data-ttu-id="15ba9-113">Anstatt DDE-Nachrichten direkt zu senden, zu veröffentlichen und zu verarbeiten, verwendet eine Anwendung die von der Ddeml bereitgestellten Funktionen zum Verwalten von DDE-Konversationen.</span><span class="sxs-lookup"><span data-stu-id="15ba9-113">Instead of sending, posting, and processing DDE messages directly, an application uses the functions provided by the DDEML to manage DDE conversations.</span></span> <span data-ttu-id="15ba9-114">Weitere Informationen zu DDEML finden Sie unter [dynamischer Datenaustausch-Verwaltungs Bibliothek](../dataxchg/dynamic-data-exchange-management-library.md).</span><span class="sxs-lookup"><span data-stu-id="15ba9-114">For more information on DDEML, see [Dynamic Data Exchange Management Library](../dataxchg/dynamic-data-exchange-management-library.md).</span></span>

## <a name="network-dde-files"></a><span data-ttu-id="15ba9-115">Netzwerk-DDE-Dateien</span><span class="sxs-lookup"><span data-stu-id="15ba9-115">Network DDE Files</span></span>

<span data-ttu-id="15ba9-116">Um die API-Elemente von Network DDE verwenden zu können, müssen Sie die Header Datei "nddeapi. h" in die Quelldateien einschließen und die Datei "nddeapi. lib" in die Linkzeile einschließen.</span><span class="sxs-lookup"><span data-stu-id="15ba9-116">To use the API elements of network DDE, you must include the NDDEApi.h header file in your source files and include NDDEApi.lib file on your link line.</span></span> <span data-ttu-id="15ba9-117">Außerdem müssen Sie sicherstellen, dass die NDDEApi.dll-Datei geladen ist.</span><span class="sxs-lookup"><span data-stu-id="15ba9-117">You must also make sure that the NDDEApi.dll file is loaded.</span></span>

<span data-ttu-id="15ba9-118">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="15ba9-118">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="15ba9-119">Netzwerk-DDE-Agent</span><span class="sxs-lookup"><span data-stu-id="15ba9-119">Network DDE Agent</span></span>](network-dde-agent.md)
-   [<span data-ttu-id="15ba9-120">DDE-Freigaben</span><span class="sxs-lookup"><span data-stu-id="15ba9-120">DDE Shares</span></span>](dde-shares.md)
-   [<span data-ttu-id="15ba9-121">Vertrauenswürdige Freigaben und Sicherheit</span><span class="sxs-lookup"><span data-stu-id="15ba9-121">Trusted Shares and Security</span></span>](trusted-shares-and-security.md)
-   [<span data-ttu-id="15ba9-122">Verwalten von DDE Shares</span><span class="sxs-lookup"><span data-stu-id="15ba9-122">Managing DDE Shares</span></span>](managing-dde-shares.md)

 

 
