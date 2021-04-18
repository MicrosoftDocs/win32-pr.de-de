---
title: Informationen zur Remote Zugriffs Dienst-Verwaltung
description: Windows 2000 und spätere Betriebssysteme stellen eine Reihe von Funktionen für die Verwaltung von Benutzerberechtigungen und Ports auf RAS-Servern bereit.
ms.assetid: 95c6dceb-e3a9-421e-b43f-88b18b9e64ff
keywords:
- RRAS für den Routing-und RAS-Dienst, RAS-Verwaltung
- RRAS für den Routing-und RAS-Dienst, RAS-Verwaltung, beschrieben
- RAS-Verwaltungs-RRAS
- RRAS für RAS-Verwaltung, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73bdb55049e99b6d3df9980fc35879341b488531
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337788"
---
# <a name="about-remote-access-service-administration"></a><span data-ttu-id="ee9c9-107">Informationen zur Remote Zugriffs Dienst-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="ee9c9-107">About Remote Access Service Administration</span></span>

<span data-ttu-id="ee9c9-108">Windows 2000 und spätere Betriebssysteme stellen eine Reihe von Funktionen für die Verwaltung von Benutzerberechtigungen und Ports auf RAS-Servern bereit.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-108">Windows 2000 and later operating systems provide a set of functions for administering user permissions and ports on RAS servers.</span></span> <span data-ttu-id="ee9c9-109">Mithilfe dieser Funktionen können Sie eine RAS-Server-Verwaltungs Anwendung entwickeln, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="ee9c9-109">Using these functions, you can develop a RAS server administration application to perform the following tasks:</span></span>

-   <span data-ttu-id="ee9c9-110">Listet die Benutzer auf, die über einen angegebenen Satz von RAS-Berechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-110">Enumerate those users who have a specified set of RAS permissions</span></span>
-   <span data-ttu-id="ee9c9-111">Zuweisen oder widerrufen von RAS-Berechtigungen für einen angegebenen Benutzer</span><span class="sxs-lookup"><span data-stu-id="ee9c9-111">Assign or revoke RAS permissions for a specified user</span></span>
-   <span data-ttu-id="ee9c9-112">Auflisten der konfigurierten Ports auf einem RAS-Server</span><span class="sxs-lookup"><span data-stu-id="ee9c9-112">Enumerate the configured ports on a RAS server</span></span>
-   <span data-ttu-id="ee9c9-113">Informationen und Statistiken zu einem angegebenen Port auf einem RAS-Server</span><span class="sxs-lookup"><span data-stu-id="ee9c9-113">Get information and statistics about a specified port on a RAS server</span></span>
-   <span data-ttu-id="ee9c9-114">Zurücksetzen der Statistik Zähler für einen angegebenen Port</span><span class="sxs-lookup"><span data-stu-id="ee9c9-114">Reset the statistics counters for a specified port</span></span>
-   <span data-ttu-id="ee9c9-115">Trennen der Verbindung mit einem angegebenen Port</span><span class="sxs-lookup"><span data-stu-id="ee9c9-115">Disconnect a specified port</span></span>

<span data-ttu-id="ee9c9-116">Sie können auch eine RAS-Server-Verwaltungs-dll zum Überwachen von Benutzer Verbindungen und Zuweisen von IP-Adressen zu einwählbenutzern installieren.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-116">You can also install a RAS server administration DLL to audit user connections and assign IP addresses to dial-in users.</span></span> <span data-ttu-id="ee9c9-117">Die dll exportiert eine Reihe von Funktionen, die der RAS-Server aufruft, wenn ein Benutzer versucht, eine Verbindung herzustellen oder die Verbindung zu trennen.</span><span class="sxs-lookup"><span data-stu-id="ee9c9-117">The DLL exports a set of functions that the RAS server calls whenever a user tries to connect or disconnect.</span></span>

<span data-ttu-id="ee9c9-118">In dieser Dokumentation werden die folgenden Themen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="ee9c9-118">This documentation describes the following topics:</span></span>

-   [<span data-ttu-id="ee9c9-119">Funktions Vergleich: Windows 2000 und RRAS Redistributable</span><span class="sxs-lookup"><span data-stu-id="ee9c9-119">Function Comparison: Windows 2000 vs. RRAS Redistributable</span></span>](function-comparison-windows-2000-versus-rras-redistributable.md)
-   [<span data-ttu-id="ee9c9-120">RAS-Benutzerverwaltung</span><span class="sxs-lookup"><span data-stu-id="ee9c9-120">RAS User Administration</span></span>](ras-user-administration.md)
-   [<span data-ttu-id="ee9c9-121">RAS-Server und-Port Verwaltung</span><span class="sxs-lookup"><span data-stu-id="ee9c9-121">RAS Server and Port Administration</span></span>](ras-server-and-port-administration.md)
-   [<span data-ttu-id="ee9c9-122">RAS-Verwaltungs-dll</span><span class="sxs-lookup"><span data-stu-id="ee9c9-122">RAS Administration DLL</span></span>](ras-administration-dll.md)
-   [<span data-ttu-id="ee9c9-123">Registrierungs Einrichtung der RAS-Verwaltungs-dll</span><span class="sxs-lookup"><span data-stu-id="ee9c9-123">RAS Administration DLL Registry Setup</span></span>](ras-administration-dll-registry-setup.md)

 

 




