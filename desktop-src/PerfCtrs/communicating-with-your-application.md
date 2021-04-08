---
description: In der Regel stellt ein Anbieter Daten im Auftrag einer Anwendung bereit.
ms.assetid: 65ea6099-79df-4baa-9752-7df032ccc9a0
title: Kommunikation mit Ihrer Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6def58d3e03676f3b1b46ba3ebd756eb3adc6196
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865131"
---
# <a name="communicating-with-your-application"></a><span data-ttu-id="73421-103">Kommunikation mit Ihrer Anwendung</span><span class="sxs-lookup"><span data-stu-id="73421-103">Communicating With Your Application</span></span>

<span data-ttu-id="73421-104">In der Regel stellt ein Anbieter Daten im Auftrag einer Anwendung bereit.</span><span class="sxs-lookup"><span data-stu-id="73421-104">Typically, a provider provides data on behalf of an application.</span></span> <span data-ttu-id="73421-105">Beispielsweise kann ein Server eine Leistungs-DLL erstellen, um die Leistungsdaten des Zählers bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="73421-105">For example, a server might create a performance DLL to provide its counter data.</span></span> <span data-ttu-id="73421-106">Die Kommunikation zwischen einer Anwendung und Ihrem Anbieter unterscheidet sich für Anwendungen im Benutzermodus und im Kernel Modus.</span><span class="sxs-lookup"><span data-stu-id="73421-106">Communication between an application and its provider differs for user-mode and kernel-mode applications.</span></span> <span data-ttu-id="73421-107">Anbieter werden im Benutzermodus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73421-107">Providers execute in user mode.</span></span> <span data-ttu-id="73421-108">Aus diesem Grund können Benutzermodusanwendungen, wie z. b. Druck-und Anzeige Anwendungen, beliebige Verfahren für die prozessübergreifende Kommunikation verwenden, z. b. Named Pipes, Datei Zuordnung oder RPC.</span><span class="sxs-lookup"><span data-stu-id="73421-108">Because of this, user-mode applications, such as print and display applications, can use any technique for interprocess communication, such as named pipes, file mapping, or RPC.</span></span> <span data-ttu-id="73421-109">Kernelmodusanwendungen müssen jedoch eine ioctl-Schnittstelle bereitstellen, die die Leistungsdaten an den Anbieter zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="73421-109">However, kernel-mode applications must provide an IOCTL interface that returns the performance data to the provider.</span></span>

> [!WARNING]
> <span data-ttu-id="73421-110">Verwenden Sie com nicht als IPC-Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="73421-110">Do not use COM as the IPC mechanism.</span></span> <span data-ttu-id="73421-111">Das System kann den com-Initialisierungs Status des Threads nicht garantieren, der die-Schnittstelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="73421-111">The system cannot guarantee the COM initialization state of the thread calling the interface.</span></span> <span data-ttu-id="73421-112">Daher ist die dll möglicherweise nicht in der Lage, com erfolgreich zu initialisieren und die Daten zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="73421-112">Therefore, the DLL may not be able to successfully initialize COM and collect the data.</span></span>

 

 

 



