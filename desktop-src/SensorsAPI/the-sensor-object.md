---
description: Das Sensor Objekt stellt einen bestimmten Sensor dar.
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: Das Sensor Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6034c008edf75b16a8156ab53ff66a418261d965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348727"
---
# <a name="the-sensor-object"></a><span data-ttu-id="f1309-103">Das Sensor Objekt</span><span class="sxs-lookup"><span data-stu-id="f1309-103">The Sensor Object</span></span>

<span data-ttu-id="f1309-104">Das Sensor Objekt stellt einen bestimmten Sensor dar.</span><span class="sxs-lookup"><span data-stu-id="f1309-104">The sensor object represents a particular sensor.</span></span>

<span data-ttu-id="f1309-105">Die Sensor-API stellt die einzelnen Sensoren als Sensor Objekt dar.</span><span class="sxs-lookup"><span data-stu-id="f1309-105">The Sensor API represents each sensor as a sensor object.</span></span> <span data-ttu-id="f1309-106">Sie können über die [**iSensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) -Schnittstelle mit einem bestimmten Sensor Objekt arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f1309-106">You can work with a particular sensor object through its [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface.</span></span> <span data-ttu-id="f1309-107">Diese Schnittstelle ermöglicht Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f1309-107">This interface enables you to:</span></span>

-   <span data-ttu-id="f1309-108">Abrufen von Metadaten über den Sensor, z. b. ID, Typ oder Anzeige Name.</span><span class="sxs-lookup"><span data-stu-id="f1309-108">Retrieve metadata about the sensor, such as its ID, type, or friendly name.</span></span>
-   <span data-ttu-id="f1309-109">Abrufen von Informationen über die spezifischen Daten, die der Sensor bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f1309-109">Retrieve information about the specific data the sensor can provide.</span></span>
-   <span data-ttu-id="f1309-110">Synchrones Abrufen der Daten.</span><span class="sxs-lookup"><span data-stu-id="f1309-110">Retrieve the data, synchronously.</span></span>
-   <span data-ttu-id="f1309-111">Abrufen von Zustandsinformationen, z. b. ob der Sensor bereit ist.</span><span class="sxs-lookup"><span data-stu-id="f1309-111">Retrieve state information, such as whether the sensor is ready.</span></span>
-   <span data-ttu-id="f1309-112">Geben Sie an, welche Ereignisse ihr Programm empfängt.</span><span class="sxs-lookup"><span data-stu-id="f1309-112">Specify which events your program will receive.</span></span>
-   <span data-ttu-id="f1309-113">Geben Sie die Rückruf Schnittstelle an, die die Sensor-API verwenden kann, um dem Programm Ereignis Benachrichtigungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f1309-113">Specify the callback interface that the Sensor API can use to provide your program with event notifications.</span></span>

 

 



