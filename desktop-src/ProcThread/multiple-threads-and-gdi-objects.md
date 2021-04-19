---
description: Um die Leistung zu verbessern, wird der Zugriff auf Grafikgeräte Schnittstellen-Objekte (z. b. Paletten, Geräte Kontexte, Regionen und ähnliches) nicht serialisiert.
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: Mehrere Threads und GDI-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5822539248be5189f7a8e7fb15f4ef8a42ff1b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360533"
---
# <a name="multiple-threads-and-gdi-objects"></a><span data-ttu-id="52e3a-103">Mehrere Threads und GDI-Objekte</span><span class="sxs-lookup"><span data-stu-id="52e3a-103">Multiple Threads and GDI Objects</span></span>

<span data-ttu-id="52e3a-104">Um die Leistung zu verbessern, wird der Zugriff auf Grafikgeräte Schnittstellen-Objekte (z. b. Paletten, Geräte Kontexte, Regionen und ähnliches) nicht serialisiert.</span><span class="sxs-lookup"><span data-stu-id="52e3a-104">To enhance performance, access to graphics device interface (GDI) objects (such as palettes, device contexts, regions, and the like) is not serialized.</span></span> <span data-ttu-id="52e3a-105">Dadurch entsteht eine potenzielle Gefahr für Prozesse, die über mehrere Threads verfügen, die diese Objekte gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="52e3a-105">This creates a potential danger for processes that have multiple threads sharing these objects.</span></span> <span data-ttu-id="52e3a-106">Wenn ein Thread z. b. ein GDI-Objekt löscht, während er von einem anderen Thread verwendet wird, sind die Ergebnisse unvorhersehbar.</span><span class="sxs-lookup"><span data-stu-id="52e3a-106">For example, if one thread deletes a GDI object while another thread is using it, the results are unpredictable.</span></span> <span data-ttu-id="52e3a-107">Diese Gefahr kann vermieden werden, indem GDI-Objekte nicht gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="52e3a-107">This danger can be avoided simply by not sharing GDI objects.</span></span> <span data-ttu-id="52e3a-108">Wenn die Freigabe unvermeidlich (oder wünschenswert) ist, muss die Anwendung eigene Mechanismen für die Synchronisierung des Zugriffs bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="52e3a-108">If sharing is unavoidable (or desirable), the application must provide its own mechanisms for synchronizing access.</span></span> <span data-ttu-id="52e3a-109">Weitere Informationen zur Synchronisierung des Zugriffs finden Sie unter [Synchronisieren der Ausführung mehrerer Threads](synchronizing-execution-of-multiple-threads.md).</span><span class="sxs-lookup"><span data-stu-id="52e3a-109">For more information about synchronizing access, see [Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md).</span></span>

 

 



