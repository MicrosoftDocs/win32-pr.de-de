---
description: Die Sensor-API kann Ereignis Benachrichtigungen bereitstellen.
ms.assetid: 2400619c-ee9c-4662-ae57-6d4bc317e730
title: Informationen zu Sensor-API-Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e941dca86d5b7ec3aa9922220c1232b10429f60a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867620"
---
# <a name="about-sensor-api-events"></a><span data-ttu-id="0fee5-103">Informationen zu Sensor-API-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="0fee5-103">About Sensor API Events</span></span>

<span data-ttu-id="0fee5-104">Die Sensor-API kann Ereignis Benachrichtigungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0fee5-104">The Sensor API can provide event notifications.</span></span>

<span data-ttu-id="0fee5-105">Wenn Sie sich beim Empfangen von Ereignissen über [**iSensor:: seteventsink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) oder [**isensormanager:: seteventsink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink)registrieren, müssen Sie einen Zeiger auf eine Rückruf Schnittstelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0fee5-105">When you register to receive events, through either [**ISensor::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) or [**ISensorManager::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink), you must provide a pointer to a callback interface.</span></span> <span data-ttu-id="0fee5-106">Sie müssen die Methoden der Rückruf Schnittstelle in Ihrem Code implementieren.</span><span class="sxs-lookup"><span data-stu-id="0fee5-106">You must implement the methods of the callback interface in your code.</span></span> <span data-ttu-id="0fee5-107">Die Sensor-API definiert die folgenden Rückruf Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="0fee5-107">The Sensor API defines the following callback interfaces:</span></span>

-   <span data-ttu-id="0fee5-108">[**Isenevents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span><span class="sxs-lookup"><span data-stu-id="0fee5-108">[**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents).</span></span> <span data-ttu-id="0fee5-109">Implementieren Sie diese Schnittstelle, um Ereignisse von Sensoren zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="0fee5-109">Implement this interface to receive events from sensors.</span></span> <span data-ttu-id="0fee5-110">Sensoren können Ihre Anwendung über neue Daten, Änderungen am Sensor Zustand, Sensor Trennung und benutzerdefinierte Ereignisse benachrichtigen, die vom Sensorhersteller definiert werden.</span><span class="sxs-lookup"><span data-stu-id="0fee5-110">Sensors can notify your application about new data, changes in sensor state, sensor disconnection, and custom events defined by the sensor manufacturer.</span></span>
-   <span data-ttu-id="0fee5-111">[**Isensormanagerevents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span><span class="sxs-lookup"><span data-stu-id="0fee5-111">[**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents).</span></span> <span data-ttu-id="0fee5-112">Implementieren Sie diese Schnittstelle, um Ereignisse vom Sensor-Manager zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="0fee5-112">Implement this interface to receive events from the sensor manager.</span></span> <span data-ttu-id="0fee5-113">Der Sensor-Manager kann die Anwendung Benachrichtigen, wenn ein Sensor eine Verbindung herstellt und daher möglicherweise zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0fee5-113">The sensor manager can notify your application when a sensor connects, and therefore may be available for use.</span></span>

<span data-ttu-id="0fee5-114">Sie können Ereignis Benachrichtigungen abbrechen, indem Sie " [**lteventsink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) " erneut aufrufen. dieses Mal wird ein **null** -Wert über den-Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="0fee5-114">You can cancel event notifications by calling [**SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) again, this time passing a **NULL** value through the parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0fee5-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0fee5-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fee5-116">Verwenden von Sensor-API-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="0fee5-116">Using Sensor API Events</span></span>](using-sensor-api-events.md)
</dt> </dl>

 

 
