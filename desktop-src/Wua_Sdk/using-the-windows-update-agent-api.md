---
description: Wenn Sie die Windows Update-Agent-API (WUA) verwenden möchten, erstellen Sie zunächst eine Instanz einer der Schnittstellen, indem Sie das-Objekt aus der entsprechenden Co-Klasse erstellen.
ms.assetid: b304971d-584a-4d0f-be5b-26f0ab315ec9
title: Verwenden der Windows Update-Agent-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b5d155a2354b68135d0742f765dffb01e7235f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752065"
---
# <a name="using-the-windows-update-agent-api"></a><span data-ttu-id="5cec2-103">Verwenden der Windows Update-Agent-API</span><span class="sxs-lookup"><span data-stu-id="5cec2-103">Using the Windows Update Agent API</span></span>

<span data-ttu-id="5cec2-104">Wenn Sie die Windows Update-Agent-API (WUA) verwenden möchten, erstellen Sie zunächst eine Instanz einer der Schnittstellen, indem Sie das-Objekt aus der entsprechenden Co-Klasse erstellen.</span><span class="sxs-lookup"><span data-stu-id="5cec2-104">To use the Windows Update Agent (WUA) API, first create an instance of one of the interfaces by creating the object from the appropriate coclass.</span></span>

<span data-ttu-id="5cec2-105">In den folgenden Themen wird beschrieben, wie Sie die WUA-API verwenden können:</span><span class="sxs-lookup"><span data-stu-id="5cec2-105">The following topics describe how you can use the WUA API:</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="5cec2-106">Diese Skripts dienen dazu, die Verwendung der Windows Update-Agent-APIs zu veranschaulichen und Beispiele dafür zu liefern, wie Entwickler diese APIs zum Lösen von Problemen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="5cec2-106">These scripts are intended to demonstrate the use of the Windows Update Agent APIs, and provide examples of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="5cec2-107">Diese Skripts sind nicht als Produktionscode gedacht, und die Skripts selbst werden von Microsoft nicht unterstützt (obwohl die zugrunde liegenden Windows Update-Agent-APIs unterstützt werden).</span><span class="sxs-lookup"><span data-stu-id="5cec2-107">These scripts are not intended as production code, and the scripts themselves are not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 

-   [<span data-ttu-id="5cec2-108">Windows Update-Agent-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="5cec2-108">Windows Update Agent Object Model</span></span>](windows-update-agent-object-model.md)
-   [<span data-ttu-id="5cec2-109">Ermitteln der aktuellen WUA-Version</span><span class="sxs-lookup"><span data-stu-id="5cec2-109">Determining the Current Version of WUA</span></span>](determining-the-current-version-of-wua.md)
-   [<span data-ttu-id="5cec2-110">Aktualisieren des Windows Update-Agents</span><span class="sxs-lookup"><span data-stu-id="5cec2-110">Updating the Windows Update Agent</span></span>](updating-the-windows-update-agent.md)
-   [<span data-ttu-id="5cec2-111">Aktualisieren von Windows Update-Agent-Header Dateien</span><span class="sxs-lookup"><span data-stu-id="5cec2-111">Updating Windows Update Agent Header Files</span></span>](updating-windows-update-agent-header-files.md)
-   [<span data-ttu-id="5cec2-112">Verwenden von WUA, um Offline nach Updates zu suchen</span><span class="sxs-lookup"><span data-stu-id="5cec2-112">Using WUA to Scan for Updates Offline</span></span>](using-wua-to-scan-for-updates-offline.md)
-   [<span data-ttu-id="5cec2-113">Gesicherte Methoden und Eigenschaften in der WUA-API</span><span class="sxs-lookup"><span data-stu-id="5cec2-113">Secured Methods and Properties in the WUA API</span></span>](secured-methods-and-properties-in-the-wua-api.md)
-   [<span data-ttu-id="5cec2-114">Suchen, herunterladen und Installieren von Updates</span><span class="sxs-lookup"><span data-stu-id="5cec2-114">Searching, Downloading, and Installing Updates</span></span>](searching--downloading--and-installing-updates.md)
-   [<span data-ttu-id="5cec2-115">Suchen, herunterladen und installieren spezifischer Updates</span><span class="sxs-lookup"><span data-stu-id="5cec2-115">Searching, Downloading, and Installing Specific Updates</span></span>](searching--downloading--and-installing-specific-updates.md)
-   [<span data-ttu-id="5cec2-116">Verwenden von WUA auf einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="5cec2-116">Using WUA From a Remote Computer</span></span>](using-wua-from-a-remote-computer.md)
-   [<span data-ttu-id="5cec2-117">Richtlinien für asynchrone WUA-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="5cec2-117">Guidelines for Asynchronous WUA Operations</span></span>](guidelines-for-asynchronous-wua-operations.md)
-   [<span data-ttu-id="5cec2-118">Verwenden von WUA über einen sekundären Anmeldungs Prozess (Ausführen als)</span><span class="sxs-lookup"><span data-stu-id="5cec2-118">Using WUA from a Secondary Logon (Run As) Process</span></span>](using-wua-from-a-secondary-logon--run-as--process.md)
-   [<span data-ttu-id="5cec2-119">Erfolgs-und Fehler Codes von WUA</span><span class="sxs-lookup"><span data-stu-id="5cec2-119">WUA Success and Error Codes</span></span>](wua-success-and-error-codes-.md)
-   [<span data-ttu-id="5cec2-120">WUA-Netzwerkfehler Codes</span><span class="sxs-lookup"><span data-stu-id="5cec2-120">WUA Networking Error Codes</span></span>](wua-networking-error-codes-.md)

 

 



