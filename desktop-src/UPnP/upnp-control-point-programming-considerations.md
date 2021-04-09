---
title: Überlegungen zur Steuerungspunkt Programmierung
description: Entwickler, die UPnP-basierte Anwendungen (oder Steuerungs Punkte) erstellen, müssen diese Anwendungen von einem coinit \_ Apartmentthreaded-Client verwenden. Es gibt bekannte Probleme bei der Verwendung der Kontrollpunkt-API von einem coinit- \_ Multithread-Client, der unter hoher Belastung ausgeführt wird.
ms.assetid: a5d79a29-4192-40af-b75d-a31f1f46149c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76955177f9fc0c3b164d84998547c1afdfbfb4bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856664"
---
# <a name="control-point-programming-considerations"></a><span data-ttu-id="415aa-104">Überlegungen zur Steuerungspunkt Programmierung</span><span class="sxs-lookup"><span data-stu-id="415aa-104">Control Point Programming Considerations</span></span>

<span data-ttu-id="415aa-105">Entwickler, die UPnP-basierte Anwendungen (oder Steuerungs Punkte) erstellen, müssen diese Anwendungen von einem coinit \_ Apartmentthreaded-Client verwenden.</span><span class="sxs-lookup"><span data-stu-id="415aa-105">Developers who create UPnP-based applications (or control points) must use these applications from a COINIT\_APARTMENTTHREADED client.</span></span> <span data-ttu-id="415aa-106">Es gibt bekannte Probleme bei der Verwendung der Kontrollpunkt-API von einem coinit- \_ Multithread-Client, der unter hoher Belastung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="415aa-106">There are known problems when using the Control Point API from a COINIT\_MULTITHREADED client running under stress.</span></span>

 

 




