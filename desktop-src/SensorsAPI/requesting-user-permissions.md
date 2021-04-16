---
description: In diesem Thema wird beschrieben, wie Berechtigungen vom Benutzer angefordert werden, um Sensoren zu verwenden. Hintergrundinformationen zu Berechtigungen in der Sensor-API finden Sie unter Verwalten von Benutzerberechtigungen.
ms.assetid: e43ad497-86f1-4804-a67a-0aeb56b80d7f
title: Anfordern von Benutzerberechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e103426388d2db49bb5a8fb01d3370207ec49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525655"
---
# <a name="requesting-user-permissions"></a><span data-ttu-id="0e089-104">Anfordern von Benutzerberechtigungen</span><span class="sxs-lookup"><span data-stu-id="0e089-104">Requesting User Permissions</span></span>

<span data-ttu-id="0e089-105">In diesem Thema wird beschrieben, wie Berechtigungen vom Benutzer angefordert werden, um Sensoren zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e089-105">This topic describes how to request permissions from the user to use sensors.</span></span> <span data-ttu-id="0e089-106">Hintergrundinformationen zu Berechtigungen in der Sensor-API finden Sie unter [Verwalten von Benutzerberechtigungen](managing-user-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="0e089-106">For background information about permissions in the Sensor API, see [Managing User Permissions](managing-user-permissions.md).</span></span>

<span data-ttu-id="0e089-107">In den folgenden Beispielen werden einige der gängigen Szenarios veranschaulicht, die Sie zum Anfordern von Benutzerberechtigungen auswählen können.</span><span class="sxs-lookup"><span data-stu-id="0e089-107">The following examples illustrate some of the common scenarious where you can choose to request user permissions.</span></span>

<span data-ttu-id="0e089-108">Der folgende Beispielcode fordert einfach Berechtigungen für alle Sensoren an, die vom Sensor-Manager mithilfe eines asynchronen Methoden Aufrufes abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0e089-108">The following example code simply requests permissions for all sensors retrieved from the sensor manager, by type, using an asynchronous method call.</span></span> <span data-ttu-id="0e089-109">Die Plattform öffnet ein Dialogfeld, in dem der Benutzer aufgefordert wird, nicht bereits aktivierte Sensoren zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0e089-109">The platform will open a dialog box to prompt the user only to enable sensors that are not already enabled.</span></span> <span data-ttu-id="0e089-110">Um zu ermitteln, ob der Benutzer in diesem Fall Sensoren aktiviert hat, müssen Sie das Ereignis " [**isensorevents:: OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) " behandeln.</span><span class="sxs-lookup"><span data-stu-id="0e089-110">To determine whether the user enabled any sensors in this case, you must handle the [**ISensorEvents::OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) event.</span></span>


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByType(SAMPLE_SENSOR_TYPE_TIME, &pSensorColl);

if(SUCCEEDED(hr))
{
    // Request permissions for all sensors
    // in the collection.
    hr = pSensorManager->RequestPermissions(0, pSensorColl, FALSE);
}

```



<span data-ttu-id="0e089-111">Sie können den Status des Sensors synchron testen, bevor Sie versuchen, Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0e089-111">You can choose to test the sensor state synchronously before attempting to retrieve data.</span></span> <span data-ttu-id="0e089-112">Der folgende Beispielcode veranschaulicht dieses Verfahren.</span><span class="sxs-lookup"><span data-stu-id="0e089-112">The following example code demonstrates this technique.</span></span>


```C++
if(SUCCEEDED(hr))
{
   // Check the current sensor state.
   SensorState state = SENSOR_STATE_NOT_AVAILABLE;

   hr = pSensor->GetState(&state);

   if(SUCCEEDED(hr))
   {
       if(state == SENSOR_STATE_ACCESS_DENIED)
       {
           wprintf_s(L"\nSensor not enabled, requesting permissions...\n");
           hr = pSensorManager->RequestPermissions(0, pSensorColl, TRUE);

           if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED) ||
              hr == HRESULT_FROM_WIN32(ERROR_CANCELLED)) 
           {
               wprintf_s(L"\nYou have previously denied access to this sensor.\n");
               wprintf_s(L"Please use the Location and Other Sensors control panel\n");
               wprintf_s(L"to enable the WDK Time Sensor and run this program again.\n");
           }
       }
   }
}

if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);
}
```



<span data-ttu-id="0e089-113">Im folgenden Beispielcode wird der Benutzer zur Eingabe von Sensor Berechtigungen aufgefordert, wenn der Versuch, einen Datenbericht von einem bestimmten Sensor abzurufen, fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="0e089-113">The following example code prompts the user for sensor permissions if an attempt to retrieve a data report from a particular sensor fails.</span></span>


```C++
if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);

    if(E_ACCESSDENIED == hr)
    {
       wprintf_s(L"\nSensor not enabled, requesting permissions...\n");
       hr = pSensorManager->RequestPermissions(0, pSensorColl, TRUE);

       if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED) ||
          hr == HRESULT_FROM_WIN32(ERROR_CANCELLED)) 
       {
           wprintf_s(L"\nYou have previously denied access to this sensor.\n");
           wprintf_s(L"Please use the Location and Other Sensors control panel\n");
           wprintf_s(L"to enable the WDK Time Sensor and run this program again.\n");
       }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="0e089-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0e089-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e089-115">**Isenmanager**</span><span class="sxs-lookup"><span data-stu-id="0e089-115">**ISensorManager**</span></span>](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)
</dt> <dt>

[<span data-ttu-id="0e089-116">Verwalten von Benutzerberechtigungen</span><span class="sxs-lookup"><span data-stu-id="0e089-116">Managing User Permissions</span></span>](managing-user-permissions.md)
</dt> </dl>

 

 
