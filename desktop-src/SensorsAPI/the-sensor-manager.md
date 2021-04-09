---
description: Das Sensor-Manager-Objekt ermöglicht den Zugriff auf die Sensoren, die für ihre Verwendung verfügbar sind.
ms.assetid: dd39d533-9983-41b4-a9a3-d94dcadebaac
title: Das Sensor-Manager-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 715448a62c058c5e6825368003939e5ae2066847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128740"
---
# <a name="the-sensor-manager-object"></a><span data-ttu-id="1ced2-103">Das Sensor-Manager-Objekt</span><span class="sxs-lookup"><span data-stu-id="1ced2-103">The Sensor Manager Object</span></span>

<span data-ttu-id="1ced2-104">Das Sensor-Manager-Objekt ermöglicht den Zugriff auf die Sensoren, die für ihre Verwendung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1ced2-104">The sensor manager object provides access to the sensors that are available for your use.</span></span>

<span data-ttu-id="1ced2-105">Um die Sensor-API zu verwenden, müssen Sie zuerst die com- **cokreateinstance** -Methode aufrufen, um eine Instanz des Sensor-Manager-Objekts zu erstellen und einen Zeiger auf die Schnittstelle mit dem Namen " [**isensormanager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)" abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1ced2-105">To use the Sensor API, you must first call the COM **CoCreateInstance** method to create an instance of the sensor manager object and retrieve a pointer to its interface, named [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager).</span></span> <span data-ttu-id="1ced2-106">Der Sensor-Manager verwaltet die Liste der verfügbaren Sensoren.</span><span class="sxs-lookup"><span data-stu-id="1ced2-106">The sensor manager maintains the list of available sensors.</span></span> <span data-ttu-id="1ced2-107">Sie können " **isensormanager** " zum Aufrufen von Methoden verwenden, die Gruppen von Sensoren nach Kategorie oder nach Typ abrufen, oder Sie können eine Methode aufrufen, um einen bestimmten Sensor mithilfe der eindeutigen ID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1ced2-107">You can use **ISensorManager** to call methods that retrieve groups of sensors by category or by type, or you can call a method to retrieve a particular sensor by using its unique ID.</span></span> <span data-ttu-id="1ced2-108">Der Sensor-Manager ermöglicht Ihnen außerdem die Registrierung, um ein Ereignis zu erhalten, mit dem Sie benachrichtigt werden, wenn ein neuer Sensor mit der Plattform verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="1ced2-108">The sensor manager also enables you to register to receive an event that notifies you when a new sensor has been connected to the platform.</span></span>

<span data-ttu-id="1ced2-109">Manchmal stellt der Sensor-Manager einen Zeiger auf einen Sensor bereit, der Benutzer hat den Sensor jedoch nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1ced2-109">Sometimes, the sensor manager provides a pointer to a sensor, but the user has not enabled the sensor.</span></span> <span data-ttu-id="1ced2-110">Beispielsweise können Sie häufig Werte für nicht private Sensoreigenschaften abrufen, z. b. den Sensorhersteller oder das Modell, bevor der Benutzer den Sensor aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1ced2-110">For example, you can often retrieve values for non-private sensor properties, such as the sensor manufacturer or model, before the user enables the sensor.</span></span> <span data-ttu-id="1ced2-111">Anhand dieser Informationen können Sie entscheiden, ob der Benutzer zur Verwendung des Sensors aufgefordert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1ced2-111">This information can help you to decide whether to ask the user for permission to use the sensor.</span></span> <span data-ttu-id="1ced2-112">Sie können " [**isensormanager:: requestberechtigungs Berechtigungen**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) " aufrufen, um den Benutzer aufzufordern, einen bestimmten Sensor oder eine Sammlung von Sensoren zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1ced2-112">You can call [**ISensorManager::RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) to prompt the user to enable a particular sensor or collection of sensors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ced2-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ced2-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ced2-114">Verwalten von Benutzerberechtigungen</span><span class="sxs-lookup"><span data-stu-id="1ced2-114">Managing User Permissions</span></span>](managing-user-permissions.md)
</dt> <dt>

[<span data-ttu-id="1ced2-115">Anfordern von Benutzerberechtigungen</span><span class="sxs-lookup"><span data-stu-id="1ced2-115">Requesting User Permissions</span></span>](requesting-user-permissions.md)
</dt> </dl>

 

 
