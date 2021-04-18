---
description: Bei Windows Sockets-Ereignis Objekten handelt es sich um einfache Konstrukte, die erstellt, geschlossen, festgelegt, gelöscht, gewartet und abgerufen werden können.
ms.assetid: 65a7627e-150e-4ca3-bc17-d2b380ee02d1
title: Verwenden von Ereignis Objekten (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26a9b70ff49bf7d46f2907c04fd8911d55dd623
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343675"
---
# <a name="using-event-objects-windows-sockets-2"></a><span data-ttu-id="b7500-103">Verwenden von Ereignis Objekten (Windows Sockets 2)</span><span class="sxs-lookup"><span data-stu-id="b7500-103">Using Event Objects (Windows Sockets 2)</span></span>

<span data-ttu-id="b7500-104">Bei Windows Sockets-Ereignis Objekten handelt es sich um einfache Konstrukte, die erstellt, geschlossen, festgelegt, gelöscht, gewartet und abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="b7500-104">Windows Sockets event objects are simple constructs that can be created and closed, set and cleared, waited upon and polled.</span></span> <span data-ttu-id="b7500-105">Das akzeptierte Modell besteht darin, dass Clients ein Ereignis Objekt erstellen und das Handle als Parameter (oder als Komponente einer Parameter Struktur) in Funktionen wie [**wspsend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) und [**wspeventselect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b7500-105">The accepted model is for clients to create an event object and supply the handle as a parameter (or as a component of a parameter structure) in functions such as [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="b7500-106">Wenn die nominierte Bedingung aufgetreten ist, verwendet der Dienstanbieter das Handle, um das Ereignis Objekt durch Aufrufen von [**wpusetevent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent)festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b7500-106">When the nominated condition has occurred, the service provider uses the handle to set the event object by calling [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent).</span></span> <span data-ttu-id="b7500-107">In der Zwischenzeit kann der Winsock-SPI-Client entweder blockieren und warten oder Abfragen, bis das Ereignis Objekt festgelegt wird (signalisiert).</span><span class="sxs-lookup"><span data-stu-id="b7500-107">Meanwhile, the Winsock SPI client may either block and wait or poll until the event object becomes set (signaled).</span></span> <span data-ttu-id="b7500-108">Der Client kann das Ereignis Objekt anschließend löschen oder zurücksetzen und wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="b7500-108">The client may subsequently clear or reset the event object and use it again.</span></span>

 

 
