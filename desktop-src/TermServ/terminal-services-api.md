---
title: Remotedesktopdienste-API
description: Die Remotedesktopdienste-API ist in erster Linie für Client/Server-Anwendungen und-Anwendungen zur Remotedesktopdienste Verwaltung nützlich.
ms.assetid: 4bd10a15-78d6-4754-9e17-f2576ee8b9d0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5aa187378625242463ea91151a6961b08d2a77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855900"
---
# <a name="remote-desktop-services-api"></a><span data-ttu-id="4e1db-103">Remotedesktopdienste-API</span><span class="sxs-lookup"><span data-stu-id="4e1db-103">Remote Desktop Services API</span></span>

<span data-ttu-id="4e1db-104">Die meisten Anwendungen werden unverändert in einer Remotedesktopdienste (ehemals Terminaldiensteumgebung) ausgeführt und müssen nicht die Remotedesktopdienste-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="4e1db-104">Most applications run without modification in a Remote Desktop Services (formerly known as Terminal Services) environment and do not need to use the Remote Desktop Services API.</span></span> <span data-ttu-id="4e1db-105">Die Remotedesktopdienste-API ist in erster Linie für Client/Server-Anwendungen und-Anwendungen zur Remotedesktopdienste Verwaltung nützlich.</span><span class="sxs-lookup"><span data-stu-id="4e1db-105">The Remote Desktop Services API is primarily useful to client/server applications and applications for Remote Desktop Services administration.</span></span>

<span data-ttu-id="4e1db-106">Die Remotedesktopdienste-API ist ein Satz von Funktionsaufrufen in Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="4e1db-106">The Remote Desktop Services API is a set of function calls into Wtsapi32.dll.</span></span> <span data-ttu-id="4e1db-107">Wenn Sie Ihre Anwendung so entwerfen möchten, dass Sie sowohl in Remotedesktopdienste-als auch in einer nicht-Remotedesktopdienste-Umgebung ausgeführt wird, verwenden Sie die dynamische Verknüpfung zur Laufzeit, um das vorhanden sein Wtsapi32.dll</span><span class="sxs-lookup"><span data-stu-id="4e1db-107">To design your application to run in both Remote Desktop Services and non-Remote Desktop Services environments, use run-time dynamic linking to check for the presence of Wtsapi32.dll.</span></span> <span data-ttu-id="4e1db-108">Weitere Informationen finden Sie unter [Lauf Zeit Verknüpfung mit Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span><span class="sxs-lookup"><span data-stu-id="4e1db-108">For more information, see [Run-Time Linking to Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span></span>

<span data-ttu-id="4e1db-109">Die Remotedesktopdienste-API ermöglicht es Anwendungen, die folgenden Aufgaben in einer Remotedesktopdienste Umgebung auszuführen:</span><span class="sxs-lookup"><span data-stu-id="4e1db-109">The Remote Desktop Services API enables applications to perform the following tasks in a Remote Desktop Services environment:</span></span>

-   <span data-ttu-id="4e1db-110">[Remotedesktopdienste Verwaltung](terminal-services-administration.md), z. b. das Auflisten und Verwalten von Remotedesktop-Sitzungshost (RD-Sitzungshost)-Servern (früher als Terminal Server bezeichnet) in einer Domäne oder das Auflisten und Verwalten von Sitzungen und Prozessen auf einem RD-Sitzungshost Server.</span><span class="sxs-lookup"><span data-stu-id="4e1db-110">[Remote Desktop Services Administration](terminal-services-administration.md), such as enumerating and managing Remote Desktop Session Host (RD Session Host) servers (formerly known as terminal servers) in a domain or enumerating and managing sessions and processes on an RD Session Host server.</span></span>
-   <span data-ttu-id="4e1db-111">Verbessern von Client/Server-Anwendungen in einer Remotedesktopdienste Umgebung.</span><span class="sxs-lookup"><span data-stu-id="4e1db-111">Enhancing client/server applications in a Remote Desktop Services environment.</span></span>
-   <span data-ttu-id="4e1db-112">Verwenden von [Remotedesktopdienste virtuellen Kanälen](terminal-services-virtual-channels.md) für die Kommunikation zwischen Client-und Server Modulen einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4e1db-112">Using [Remote Desktop Services Virtual Channels](terminal-services-virtual-channels.md) to communicate between client and server modules of an application.</span></span>
-   <span data-ttu-id="4e1db-113">[Festlegen und Abrufen Remotedesktopdienste spezifischer Benutzer Konfigurationsinformationen](terminal-services-user-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="4e1db-113">[Setting and retrieving Remote Desktop Services specific user configuration information](terminal-services-user-configuration.md).</span></span>

 

 




