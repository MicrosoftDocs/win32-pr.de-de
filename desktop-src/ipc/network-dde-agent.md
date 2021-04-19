---
description: Der Netzwerk-DDE-Agent startet Network DDE, wenn er die DDE-Aktivität des lokalen Netzwerks erkennt.
ms.assetid: bc1e6a06-be07-4ae8-94da-9603a885b3a5
title: Netzwerk-DDE-Agent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a6259b512782102936f54f65646454509c6b37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345651"
---
# <a name="network-dde-agent"></a><span data-ttu-id="a9d61-103">Netzwerk-DDE-Agent</span><span class="sxs-lookup"><span data-stu-id="a9d61-103">Network DDE Agent</span></span>

<span data-ttu-id="a9d61-104">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a9d61-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="a9d61-105">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="a9d61-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="a9d61-106">Der Netzwerk-DDE-Agent startet Network DDE, wenn er die DDE-Aktivität des lokalen Netzwerks erkennt.</span><span class="sxs-lookup"><span data-stu-id="a9d61-106">The network DDE agent starts network DDE if it detects local network DDE activity.</span></span> <span data-ttu-id="a9d61-107">Ein Remote Client, der versucht, eine Verbindung herzustellen, wird nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="a9d61-107">It does not detect a remote client trying to connect.</span></span> <span data-ttu-id="a9d61-108">Daher muss Netzwerk DDE auf dem Server Computer gestartet werden, bevor der Client erfolgreich eine Verbindung herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="a9d61-108">Therefore, before any client can successfully connect, network DDE must be started on the server computer.</span></span> <span data-ttu-id="a9d61-109">Beachten Sie, dass Network DDE nicht standardmäßig gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a9d61-109">Note that network DDE is not started by default.</span></span> <span data-ttu-id="a9d61-110">Führen Sie NETDDE.EXE aus, um Network DDE zu starten.</span><span class="sxs-lookup"><span data-stu-id="a9d61-110">To start network DDE, run NETDDE.EXE.</span></span> <span data-ttu-id="a9d61-111">Diese Datei befindet sich in Ihrem Windows-Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="a9d61-111">This file is located in your Windows directory.</span></span>

<span data-ttu-id="a9d61-112">Der Netzwerk-DDE-Agent startet außerdem die Anwendungen, die für Netzwerk DDE erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a9d61-112">The network DDE agent also starts the applications necessary for network DDE.</span></span> <span data-ttu-id="a9d61-113">Nachdem Network DDE gestartet wurde, werden DDE-Konversationen über ein Netzwerk-DDE-Fenster gesteuert, das einer der Netzwerk-DDE-Anwendungen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a9d61-113">After network DDE is started, DDE conversations are controlled through a network DDE window associated with one of the network DDE applications.</span></span> <span data-ttu-id="a9d61-114">Diese Anwendung fungiert als Proxy.</span><span class="sxs-lookup"><span data-stu-id="a9d61-114">This application acts as a proxy.</span></span> <span data-ttu-id="a9d61-115">Er kommuniziert mit allen lokalen und Remote-DDE-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="a9d61-115">It communicates with all local and remote DDE applications.</span></span>

 

 



