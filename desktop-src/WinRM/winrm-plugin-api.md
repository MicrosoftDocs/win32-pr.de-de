---
title: WinRM-Plug-in-API
description: Die Plug-in-API (Application Programming Interface) des WinRM-Plug-ins stellt Funktionen bereit, mit denen ein Benutzer Plug-ins schreiben kann, indem er bestimmte APIs für unterstützte Ressourcen-URIs und Vorgänge implementiert
ms.assetid: d3e103c1-221b-441b-8bcb-883e3f2a4c1a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccc8920f7df788b4df355b0cbc23478e97111d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947873"
---
# <a name="winrm-plug-in-api"></a><span data-ttu-id="c1601-103">WinRM-Plug-in-API</span><span class="sxs-lookup"><span data-stu-id="c1601-103">WinRM Plug-in API</span></span>

<span data-ttu-id="c1601-104">Windows-Remoteverwaltung-Plug-ins sind native Dynamic-Link-Bibliotheken (DLLs), die in die Funktionalität von WinRM einbinden und diese erweitern.</span><span class="sxs-lookup"><span data-stu-id="c1601-104">Windows Remote Management plug-ins are native dynamic-link libraries (DLLs) that plug into and extend the functionality of WinRM.</span></span> <span data-ttu-id="c1601-105">Die Plug-in-API (Application Programming Interface) des WinRM-Plug-ins stellt Funktionen bereit, mit denen ein Benutzer Plug-ins schreiben kann, indem er bestimmte APIs für unterstützte [*Ressourcen-URIs*](windows-remote-management-glossary.md) und Vorgänge implementiert</span><span class="sxs-lookup"><span data-stu-id="c1601-105">The WinRM Plug-in application programming interface (API) provides functionality that enables a user to write plug-ins by implementing certain APIs for supported [*resource URIs*](windows-remote-management-glossary.md) and operations.</span></span> <span data-ttu-id="c1601-106">Nachdem die Plug-ins entweder für den WinRM-Dienst oder für Internetinformationsdienste (IIS) konfiguriert wurden, werden Sie in den WinRM-Host bzw. den IIS-Host geladen.</span><span class="sxs-lookup"><span data-stu-id="c1601-106">After the plug-ins are configured for either the WinRM service or Internet Information Services (IIS), they are loaded into the WinRM host or IIS host, respectively.</span></span> <span data-ttu-id="c1601-107">Remote Anforderungen werden an diese Plug-in-Einstiegspunkte weitergeleitet, um Vorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c1601-107">Remote requests are routed to these plug-in entry points to carry out operations.</span></span>

<span data-ttu-id="c1601-108">Der Abschnitt "WinRM-Plug-in-API-Referenz" enthält ausführliche Informationen zu den folgenden API-Elementen:</span><span class="sxs-lookup"><span data-stu-id="c1601-108">The WinRM Plug-in API reference section contains detailed information about the following API elements:</span></span>

-   [<span data-ttu-id="c1601-109">Einstiegspunkte für Autorisierungs-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="c1601-109">Authorization Plug-in Entry Points</span></span>](authorization-plug-in-entry-points.md)
-   [<span data-ttu-id="c1601-110">Autorisierungs-Plug-in-Methoden</span><span class="sxs-lookup"><span data-stu-id="c1601-110">Authorization Plug-in Methods</span></span>](authorization-plug-in-methods.md)
-   [<span data-ttu-id="c1601-111">Einstiegspunkte des Vorgangs-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="c1601-111">Operations Plug-in Entry Points</span></span>](operations-plug-in-entry-points.md)
-   [<span data-ttu-id="c1601-112">Vorgangs-Plug-in-Methoden</span><span class="sxs-lookup"><span data-stu-id="c1601-112">Operations Plug-in Methods</span></span>](operations-plug-in-methods.md)
-   [<span data-ttu-id="c1601-113">Strukturen</span><span class="sxs-lookup"><span data-stu-id="c1601-113">Structures</span></span>](winrm-plug-in-api-structures.md)

 

 




