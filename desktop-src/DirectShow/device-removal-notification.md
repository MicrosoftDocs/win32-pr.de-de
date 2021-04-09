---
description: Benachrichtigung zum Entfernen von Geräten
ms.assetid: 0b96231a-f990-4c1c-8d00-cafeb3985ab3
title: Benachrichtigung zum Entfernen von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c84fa280e0adbc1d0eec9043fbb2f1446487f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103958115"
---
# <a name="device-removal-notification"></a><span data-ttu-id="57281-103">Benachrichtigung zum Entfernen von Geräten</span><span class="sxs-lookup"><span data-stu-id="57281-103">Device Removal Notification</span></span>

<span data-ttu-id="57281-104">Wenn der Benutzer ein Plug & Play Gerät entfernt, das im Diagramm verwendet wurde, stellt der Filter Graph-Manager ein Ereignis für ein Ereignis mit dem Ereignis " [**EC- \_ Gerät \_**](ec-device-lost.md) "</span><span class="sxs-lookup"><span data-stu-id="57281-104">If the user removes a Plug and Play device that the graph was using, the filter graph manager posts an [**EC\_DEVICE\_LOST**](ec-device-lost.md) event.</span></span> <span data-ttu-id="57281-105">Wenn das Gerät wieder verfügbar wird, sendet der Filter Graph-Manager ein anderes Ereignis für das Ereignis " **EC- \_ Gerät \_** ".</span><span class="sxs-lookup"><span data-stu-id="57281-105">If the device becomes available again, the filter graph manager posts another **EC\_DEVICE\_LOST** event.</span></span> <span data-ttu-id="57281-106">Der vorherige Status des Erfassungs Filters ist jedoch nicht mehr gültig.</span><span class="sxs-lookup"><span data-stu-id="57281-106">However, the previous state of the capture filter is no longer valid.</span></span> <span data-ttu-id="57281-107">Die Anwendung muss das Diagramm neu erstellen, damit das Gerät verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="57281-107">The application must rebuild the graph to use the device.</span></span>

<span data-ttu-id="57281-108">DirectShow sendet kein Ereignis, wenn ein neues Gerät angeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="57281-108">DirectShow does not send any event when a new device is plugged in.</span></span> <span data-ttu-id="57281-109">Um zu erfahren, wann ein neues Gerät verfügbar ist, kann die Anwendung die Nachrichten des WM- \_ devicechange-Fensters überwachen.</span><span class="sxs-lookup"><span data-stu-id="57281-109">To learn when a new device is available, the application can monitor WM\_DEVICECHANGE window messages.</span></span> <span data-ttu-id="57281-110">Weitere Informationen finden Sie unter "Geräteverwaltung" in der Platform SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="57281-110">For more information, see "Device Management" in the Platform SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57281-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="57281-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57281-112">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="57281-112">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



