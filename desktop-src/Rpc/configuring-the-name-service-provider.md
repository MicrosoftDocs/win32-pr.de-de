---
title: Konfigurieren des Name Service-Anbieters
description: Wenn Ihre verteilte Anwendung ihre Schnittstelle bei einem Namensdienst registriert, müssen sowohl der Client als auch der Server den gleichen Namensdienst verwenden.
ms.assetid: a3f201e1-1a01-4794-9026-05e51a96afc0
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Konfigurieren des Namensdienst Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7a44ec9a1c83eb7c37f10caae6ca3870679bde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036942"
---
# <a name="configuring-the-name-service-provider"></a><span data-ttu-id="c3331-104">Konfigurieren des Name Service-Anbieters</span><span class="sxs-lookup"><span data-stu-id="c3331-104">Configuring the Name Service Provider</span></span>

<span data-ttu-id="c3331-105">Wenn Ihre verteilte Anwendung ihre Schnittstelle bei einem Namensdienst registriert, müssen sowohl der Client als auch der Server den gleichen Namensdienst verwenden.</span><span class="sxs-lookup"><span data-stu-id="c3331-105">If your distributed application registers its interface with a name service, both the client and server must be using the same name service.</span></span> <span data-ttu-id="c3331-106">Microsoft RPC interagiert mit Microsoft Locator und einem beliebigen namens Dienstanbieter (NSP), der der Microsoft RPC Name Service Interface (NSI) entspricht – beispielsweise der DCE-Zell Verzeichnisdienst, auf den über den Namensdienst Daemon (nsid) der Digital Equipment Corporation zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="c3331-106">Microsoft RPC interoperates with Microsoft Locator and any name service provider (NSP) that adheres to the Microsoft RPC name service interface (NSI)—for example, the DCE Cell Directory Service accessed through Digital Equipment Corporation's name service daemon (NSID).</span></span> <span data-ttu-id="c3331-107">Der Microsoft-Locator, der für die Verwendung in Windows-Umgebungen entwickelt wurde, ist der Standardname Service-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="c3331-107">Microsoft Locator, which is designed for use in Windows environments, is the default name service provider.</span></span>

<span data-ttu-id="c3331-108">In diesem Abschnitt wird erläutert, wie Sie namens Dienstanbieter installieren und konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="c3331-108">This section presents a discussion of installing and configuring name service providers:</span></span>

-   [<span data-ttu-id="c3331-109">Konfigurieren des Namens Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="c3331-109">Configuring the Name Service</span></span>](configuring-the-name-service-for-windows-xp-windows-2000-or-windows-nt.md)
-   [<span data-ttu-id="c3331-110">Konfigurieren des Namens Dienstanbieter für Windows 95</span><span class="sxs-lookup"><span data-stu-id="c3331-110">Configuring the Name Service for Windows 95</span></span>](configuring-the-name-service-for-windows-95.md)
-   [<span data-ttu-id="c3331-111">Konfigurieren des Namens Dienstanbieter für Windows 3. x oder MS-DOS</span><span class="sxs-lookup"><span data-stu-id="c3331-111">Configuring the Name Service for Windows 3.x or MS-DOS</span></span>](configuring-the-name-service-for-windows-3-x-or-ms-dos.md)
-   [<span data-ttu-id="c3331-112">Starten und Beenden von Microsoft Locator</span><span class="sxs-lookup"><span data-stu-id="c3331-112">Starting and Stopping Microsoft Locator</span></span>](starting-and-stopping-microsoft-locator.md)

 

 




