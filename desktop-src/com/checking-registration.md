---
title: Registrierung wird überprüft
description: Registrierung wird überprüft
ms.assetid: 7df63955-d838-4518-8473-0c1a24e90f69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee215fd052ffc242900eead069a8b72fd25b31d5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947531"
---
# <a name="checking-registration"></a><span data-ttu-id="9895b-103">Registrierung wird überprüft</span><span class="sxs-lookup"><span data-stu-id="9895b-103">Checking Registration</span></span>

<span data-ttu-id="9895b-104">Jedes Mal, wenn eine Anwendung geladen wird, sollte die Registrierung überprüft werden, um Folgendes zu bestimmen:</span><span class="sxs-lookup"><span data-stu-id="9895b-104">Each time an application loads, it should check its registration to determine the following:</span></span>

-   <span data-ttu-id="9895b-105">Gibt an, ob die CLSIDs in der Registrierung vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="9895b-105">Whether the CLSIDs are present in the registry.</span></span> <span data-ttu-id="9895b-106">Wenn Sie nicht vorhanden sind, sollte die Anwendung als ursprüngliches Setup registriert werden.</span><span class="sxs-lookup"><span data-stu-id="9895b-106">If they are not present, the application should register as the original setup.</span></span>
-   <span data-ttu-id="9895b-107">Gibt an, ob die CLSIDs der Anwendung im Register vorhanden sind, aber keine OLE 2-bezogenen Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="9895b-107">Whether the application's CLSIDs are present in the register but have no OLE 2-related information in them.</span></span> <span data-ttu-id="9895b-108">Wenn dies der Fall ist, sollte die Anwendung als ursprüngliches Setup registriert werden.</span><span class="sxs-lookup"><span data-stu-id="9895b-108">If this is the case, the application should register as the original setup.</span></span>
-   <span data-ttu-id="9895b-109">Gibt an, ob der Pfad mit den Server Einträgen ([LocalServer](localserver.md) und [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) und [InProcServer32](inprocserver32.md)und [DefaultIcon](defaulticon.md)) auf den Speicherort verweist, an dem die Anwendung zurzeit installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9895b-109">Whether the path containing server entries ([LocalServer](localserver.md) and [LocalServer32](localserver32.md), [InprocServer](inprocserver.md) and [InprocServer32](inprocserver32.md), and [DefaultIcon](defaulticon.md)) points to the location at which the application is currently installed.</span></span> <span data-ttu-id="9895b-110">Wenn der Pfad nicht, schreiben Sie die Pfad Einträge so um, dass Sie auf den aktuellen Speicherort zeigen.</span><span class="sxs-lookup"><span data-stu-id="9895b-110">If the path does not, rewrite the path entries to point to the current location.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9895b-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9895b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9895b-112">Registrieren von com-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="9895b-112">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 




