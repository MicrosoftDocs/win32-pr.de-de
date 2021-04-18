---
title: RAS-Server Verwaltung
description: Windows NT Server 4,0 bietet eine Reihe von Funktionen für die Verwaltung von Benutzerberechtigungen und Ports auf Windows NT-/Windows 2000-RAS-Servern.
ms.assetid: 0b517c4d-dcae-477b-b274-c3773bd172ef
keywords:
- Server Verwaltung, RAS
- Verwaltung, RAS-Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e096610e1cfe986c504a017f4d2b0d1033a6e6d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207209"
---
# <a name="ras-server-administration"></a><span data-ttu-id="5a65f-105">RAS-Server Verwaltung</span><span class="sxs-lookup"><span data-stu-id="5a65f-105">RAS Server Administration</span></span>

<span data-ttu-id="5a65f-106">Windows NT Server 4,0 bietet eine Reihe von Funktionen für die Verwaltung von Benutzerberechtigungen und Ports auf Windows NT-/Windows 2000-RAS-Servern.</span><span class="sxs-lookup"><span data-stu-id="5a65f-106">Windows NT Server 4.0 provides a set of functions for administering user permissions and ports on Windows NT/Windows 2000 RAS servers.</span></span> <span data-ttu-id="5a65f-107">Windows 95 unterstützt diese Funktionen nicht.</span><span class="sxs-lookup"><span data-stu-id="5a65f-107">Windows 95 does not support these functions.</span></span> <span data-ttu-id="5a65f-108">Mithilfe dieser Funktionen können Sie eine RAS-Server-Verwaltungs Anwendung entwickeln, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="5a65f-108">Using these functions, you can develop a RAS server administration application to perform the following tasks:</span></span>

-   <span data-ttu-id="5a65f-109">Listet die Benutzer auf, die über einen angegebenen Satz von RAS-Berechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="5a65f-109">Enumerate those users who have a specified set of RAS permissions</span></span>
-   <span data-ttu-id="5a65f-110">Zuweisen oder widerrufen von RAS-Berechtigungen für einen angegebenen Benutzer</span><span class="sxs-lookup"><span data-stu-id="5a65f-110">Assign or revoke RAS permissions for a specified user</span></span>
-   <span data-ttu-id="5a65f-111">Auflisten der konfigurierten Ports auf einem RAS-Server</span><span class="sxs-lookup"><span data-stu-id="5a65f-111">Enumerate the configured ports on a RAS server</span></span>
-   <span data-ttu-id="5a65f-112">Informationen und Statistiken zu einem angegebenen Port auf einem RAS-Server</span><span class="sxs-lookup"><span data-stu-id="5a65f-112">Get information and statistics about a specified port on a RAS server</span></span>
-   <span data-ttu-id="5a65f-113">Zurücksetzen der Statistik Zähler für einen angegebenen Port</span><span class="sxs-lookup"><span data-stu-id="5a65f-113">Reset the statistics counters for a specified port</span></span>
-   <span data-ttu-id="5a65f-114">Trennen der Verbindung mit einem angegebenen Port</span><span class="sxs-lookup"><span data-stu-id="5a65f-114">Disconnect a specified port</span></span>

<span data-ttu-id="5a65f-115">Sie können auch eine RAS-Server-Verwaltungs-dll zum Überwachen von Benutzer Verbindungen und Zuweisen von IP-Adressen zu einwählbenutzern installieren.</span><span class="sxs-lookup"><span data-stu-id="5a65f-115">You can also install a RAS server administration DLL for auditing user connections and assigning IP addresses to dial-in users.</span></span> <span data-ttu-id="5a65f-116">Die dll exportiert eine Reihe von Funktionen, die der RAS-Server aufruft, wenn ein Benutzer versucht, eine Verbindung herzustellen oder die Verbindung zu trennen.</span><span class="sxs-lookup"><span data-stu-id="5a65f-116">The DLL exports a set of functions that the RAS server calls whenever a user tries to connect or disconnect.</span></span>

 

 




