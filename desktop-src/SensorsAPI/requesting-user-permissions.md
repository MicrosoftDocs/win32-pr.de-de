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
# <a name="requesting-user-permissions"></a>Anfordern von Benutzerberechtigungen

In diesem Thema wird beschrieben, wie Berechtigungen vom Benutzer angefordert werden, um Sensoren zu verwenden. Hintergrundinformationen zu Berechtigungen in der Sensor-API finden Sie unter [Verwalten von Benutzerberechtigungen](managing-user-permissions.md).

In den folgenden Beispielen werden einige der gängigen Szenarios veranschaulicht, die Sie zum Anfordern von Benutzerberechtigungen auswählen können.

Der folgende Beispielcode fordert einfach Berechtigungen für alle Sensoren an, die vom Sensor-Manager mithilfe eines asynchronen Methoden Aufrufes abgerufen werden. Die Plattform öffnet ein Dialogfeld, in dem der Benutzer aufgefordert wird, nicht bereits aktivierte Sensoren zu aktivieren. Um zu ermitteln, ob der Benutzer in diesem Fall Sensoren aktiviert hat, müssen Sie das Ereignis " [**isensorevents:: OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) " behandeln.


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



Sie können den Status des Sensors synchron testen, bevor Sie versuchen, Daten abzurufen. Der folgende Beispielcode veranschaulicht dieses Verfahren.


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



Im folgenden Beispielcode wird der Benutzer zur Eingabe von Sensor Berechtigungen aufgefordert, wenn der Versuch, einen Datenbericht von einem bestimmten Sensor abzurufen, fehlschlägt.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Isenmanager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)
</dt> <dt>

[Verwalten von Benutzerberechtigungen](managing-user-permissions.md)
</dt> </dl>

 

 
