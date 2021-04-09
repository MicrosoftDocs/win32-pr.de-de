---
description: Wenn eine Windows-Abbild Erfassungs Schnittstelle (WIA) in mehr als einem Thread innerhalb eines einzelnen Prozesses verwendet wird, muss eine Anwendung Marshalling für diese Schnittstelle bereitstellen.
ms.assetid: b125b36e-1428-4aa6-b367-eac78291c88e
title: Verwenden mehrerer Threads in einer WIA-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb1dbfa552e72dc068aff63a0a316d9af680ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129389"
---
# <a name="using-multiple-threads-in-a-wia-application"></a><span data-ttu-id="662b9-103">Verwenden mehrerer Threads in einer WIA-Anwendung</span><span class="sxs-lookup"><span data-stu-id="662b9-103">Using Multiple Threads in a WIA Application</span></span>

<span data-ttu-id="662b9-104">Wenn eine Windows-Abbild Erfassungs Schnittstelle (WIA) in mehr als einem Thread innerhalb eines einzelnen Prozesses verwendet wird, muss eine Anwendung Marshalling für diese Schnittstelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="662b9-104">When using a Windows Image Acquisition (WIA) interface in more than one thread within a single process, an application must provide marshalling for that interface.</span></span> <span data-ttu-id="662b9-105">Wenn ein Thread einen Schnittstellen Zeiger erstellt, können Sie diesen Zeiger nicht in einem anderen Thread verwenden, ohne Marshalling zu müssen.</span><span class="sxs-lookup"><span data-stu-id="662b9-105">If one thread creates an interface pointer, you cannot use that pointer in a different thread without marshalling.</span></span>

<span data-ttu-id="662b9-106">Wenn ein Thread in einer Anwendung z. b. einen Zeiger auf die [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -oder [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle erhält, kann ein separater Thread diesen Schnittstellen Zeiger nicht ohne Marshalling verwenden.</span><span class="sxs-lookup"><span data-stu-id="662b9-106">For example, if one thread in an application obtains a pointer to the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) interface, a separate thread cannot use that interface pointer without marshalling.</span></span>

<span data-ttu-id="662b9-107">Ein gängiges Verfahren, mit dem dieses Marshalling erreicht wird, ist die Verwendung der globalen Schnittstellen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="662b9-107">A common technique used to accomplish this marshalling is to use the global interface table.</span></span> <span data-ttu-id="662b9-108">Die globale Schnittstellen Tabelle ist eine Tabelle, die in einem einzelnen Prozess über alle Threads hinweg verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="662b9-108">The global interface table is a table maintained across all threads within a single process.</span></span> <span data-ttu-id="662b9-109">Alle Threads, die innerhalb des Prozesses ausgeführt werden, können Schnittstellen abrufen, die für die globale Schnittstellen Tabelle registriert sind.</span><span class="sxs-lookup"><span data-stu-id="662b9-109">All threads running within the process can retrieve interfaces that are registered to the global interface table.</span></span> <span data-ttu-id="662b9-110">Diese Methode vermeidet das Erstellen von Streams zum Übergeben von Schnittstellen zwischen Threads.</span><span class="sxs-lookup"><span data-stu-id="662b9-110">This technique avoids the need to create streams for passing interfaces between threads.</span></span>

<span data-ttu-id="662b9-111">Informationen zur Verwendung der globalen Schnittstellen Tabelle finden Sie unter [iglobalinterfaketable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span><span class="sxs-lookup"><span data-stu-id="662b9-111">For information on how to use the global interface table, see [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span></span>

<span data-ttu-id="662b9-112">Auch wenn Sie nicht beabsichtigen, mehrere Threads in einer WIA-Anwendung zu verwenden, müssen Sie davon ausgehen, dass alle Datenübertragungs-oder Geräte Ereignis Rückruf Funktionen in separaten Threads ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="662b9-112">Even if you do not intend to use multiple threads in a WIA application, you must assume that all data transfer or device event callback functions run in separate threads.</span></span>

 

 
