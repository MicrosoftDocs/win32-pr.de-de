---
description: Die Sensor-API macht die folgenden COM-Schnittstellen verfügbar.
ms.assetid: 872de1e9-20f9-409b-9917-24b13a8cc08a
title: COM-Schnittstellen (Sensor-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a73e506f5b2a59a7ce8373b810aeba779f5e9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353032"
---
# <a name="com-interfaces-sensor-api"></a><span data-ttu-id="6b074-103">COM-Schnittstellen (Sensor-API)</span><span class="sxs-lookup"><span data-stu-id="6b074-103">COM Interfaces (Sensor API)</span></span>

<span data-ttu-id="6b074-104">Die Sensor-API macht die folgenden COM-Schnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6b074-104">The Sensor API exposes the following COM interfaces.</span></span>



| <span data-ttu-id="6b074-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6b074-105">Interface</span></span>                                              | <span data-ttu-id="6b074-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b074-106">Description</span></span>                                                                                                      |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b074-107">**Ilocationberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="6b074-107">**ILocationPermissions**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-ilocationpermissions)   | <span data-ttu-id="6b074-108">Gibt den Status der Systemeinstellung an, mit der Benutzer die Speicherort Einstellungen ändern können.</span><span class="sxs-lookup"><span data-stu-id="6b074-108">Provides the status of the system setting that allows users to change location settings.</span></span>                         |
| <span data-ttu-id="6b074-109">[**Ilogicalsensormanager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b074-109">[**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85))</span></span> | <span data-ttu-id="6b074-110">Stellt Methoden bereit, die von logischen Sensor Entwicklern zum Verwalten logischer Sensorverbindungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b074-110">Provides methods used by logical sensor authors to manage logical sensor connections.</span></span>                            |
| [<span data-ttu-id="6b074-111">**ISensor**</span><span class="sxs-lookup"><span data-stu-id="6b074-111">**ISensor**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor)                             | <span data-ttu-id="6b074-112">Stellt einen Sensor dar.</span><span class="sxs-lookup"><span data-stu-id="6b074-112">Represents a sensor.</span></span>                                                                                             |
| [<span data-ttu-id="6b074-113">**Isencollection**</span><span class="sxs-lookup"><span data-stu-id="6b074-113">**ISensorCollection**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection)         | <span data-ttu-id="6b074-114">Stellt eine Auflistung von Sensoren dar.</span><span class="sxs-lookup"><span data-stu-id="6b074-114">Represents a collection of sensors.</span></span>                                                                              |
| [<span data-ttu-id="6b074-115">**Isensordatareport**</span><span class="sxs-lookup"><span data-stu-id="6b074-115">**ISensorDataReport**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport)         | <span data-ttu-id="6b074-116">Stellt einen Sensordaten Bericht dar.</span><span class="sxs-lookup"><span data-stu-id="6b074-116">Represents a sensor data report.</span></span>                                                                                 |
| [<span data-ttu-id="6b074-117">**Isenevents**</span><span class="sxs-lookup"><span data-stu-id="6b074-117">**ISensorEvents**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents)                 | <span data-ttu-id="6b074-118">Die Rückruf Schnittstelle zum Empfangen von Sensor Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="6b074-118">The callback interface for receiving sensor events.</span></span>                                                              |
| [<span data-ttu-id="6b074-119">**Isenmanager**</span><span class="sxs-lookup"><span data-stu-id="6b074-119">**ISensorManager**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)               | <span data-ttu-id="6b074-120">Stellt Methoden zum Ermitteln und Abrufen verfügbarer Sensoren und eine Methode zum Anfordern von Sensor-Manager-Ereignissen bereit.</span><span class="sxs-lookup"><span data-stu-id="6b074-120">Provides methods for discovering and retrieving available sensors and a method to request sensor manager events.</span></span> |
| [<span data-ttu-id="6b074-121">**Isenmanagerevents**</span><span class="sxs-lookup"><span data-stu-id="6b074-121">**ISensorManagerEvents**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents)   | <span data-ttu-id="6b074-122">Die Rückruf Schnittstelle zum Empfangen von Sensor-Manager-Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="6b074-122">The callback interface for receiving sensor manager events.</span></span>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="6b074-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b074-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b074-124">Programmier Referenz zur Sensor-API</span><span class="sxs-lookup"><span data-stu-id="6b074-124">Sensor API Programming Reference</span></span>](sensor-api-programming-reference.md)
</dt> </dl>

 

 
