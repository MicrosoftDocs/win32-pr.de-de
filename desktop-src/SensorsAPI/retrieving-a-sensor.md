---
description: Zum Abrufen eines Sensor Objekts verwenden Sie die Schnittstelle "isensormanager". Sie können sich diese Schnittstelle als Stamm Schnittstelle für die Sensor-API vorstellen. Um den "isenmanager" verwenden zu können, müssen Sie zuerst die com-cokreateinstance-Methode aufrufen.
ms.assetid: 36631bae-f237-4951-9959-6ab6286bd1f7
title: Abrufen eines Sensor Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cda6ea04d1a0580c38aef5a0b9c4186b908300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958822"
---
# <a name="retrieving-a-sensor-object"></a>Abrufen eines Sensor Objekts

Zum Abrufen eines Sensor Objekts verwenden Sie die Schnittstelle " [**isensormanager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) ". Sie können sich diese Schnittstelle als Stamm Schnittstelle für die Sensor-API vorstellen. Um den " **isenmanager**" verwenden zu können, müssen Sie zuerst die com- **cokreateinstance** -Methode aufrufen.

Im folgenden Beispielcode wird eine Instanz des Sensor-Managers erstellt.


```C++
// Create the sensor manager.
hr = CoCreateInstance(CLSID_SensorManager, 
                        NULL, CLSCTX_INPROC_SERVER,
                        IID_PPV_ARGS(&pSensorManager));

if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DISABLED_BY_POLICY))
{
    // Unable to retrieve sensor manager due to 
    // group policy settings. Alert the user.
}
```



Nachdem Sie erfolgreich einen Zeiger auf " [**isensormanager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)" abgerufen haben, können Sie Sensoren nach Kategorie, Typ oder ID abrufen. Wenn Sie Sensoren nach Typ oder Kategorie abrufen, erhalten Sie einen Zeiger auf eine Schnittstelle " [**isensorcollection**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) ", die alle verfügbaren Sensoren enthält, die zur angeforderten Kategorie oder zum angeforderten Typ gehören. Wenn Sie einen Sensor anhand seiner ID abrufen, erhalten Sie einen Zeiger auf eine [**iSensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) -Schnittstelle, die den von Ihnen angeforderten eindeutigen Sensor darstellt.

Der folgende Beispielcode ruft eine Auflistung von Sensoren ab, die zur Kategorie namens "Sample \_ Sensor \_ Category \_ Date \_ time" gehören. Der Code ruft dann den ersten Sensor in der Auflistung nach dem Index ab.


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByCategory(SAMPLE_SENSOR_CATEGORY_DATE_TIME, &pSensorColl);
  
if(SUCCEEDED(hr))
{
    ULONG ulCount = 0;

    // Verify that the collection contains
    // at least one sensor.
    hr = pSensorColl->GetCount(&ulCount);

    if(SUCCEEDED(hr))
    {
        if(ulCount < 1)
        {
            wprintf_s(L"\nNo sensors of the requested category.\n");
            hr = E_UNEXPECTED;
        }
    }
}

if(SUCCEEDED(hr))
{
    // Get the first available sensor.
    hr = pSensorColl->GetAt(0, &pSensor);
}
```



Beachten Sie, dass Sie alle verfügbaren Sensoren abrufen können, indem Sie die Sensor \_ Kategorie \_ alle verwenden.

Auf ähnliche Weise können Sie Sensoren eines bestimmten Typs abrufen.

Der folgende Beispielcode ruft eine Auflistung von Sensoren des Typs mit dem Namen Sample \_ \_ SensorType \_ time ab. Der Code ruft dann den ersten Sensor in der Auflistung nach dem Index ab.


```C++
// Get the sensor collection.
hr = pSensorManager->GetSensorsByType(SAMPLE_SENSOR_TYPE_TIME, &pSensorColl);
  
if(SUCCEEDED(hr))
{
    ULONG ulCount = 0;

    // Verify that the collection contains
    // at least one sensor.
    hr = pSensorColl->GetCount(&ulCount);

    if(SUCCEEDED(hr))
    {
        if(ulCount < 1)
        {
            wprintf_s(L"\nNo sensors of the requested type.\n");
            hr = E_UNEXPECTED;
        }
    }
}

if(SUCCEEDED(hr))
{
    // Get the first available sensor.
    hr = pSensorColl->GetAt(0, &pSensor);
}
```



Zum Abrufen eines Sensors anhand seiner ID müssen Sie die eindeutige ID für den Sensor kennen. Sensoren generieren diese ID normalerweise bei der ersten Verbindung, damit Sie mehrere Sensoren desselben Make-und Model-Modells identifizieren können. Dies bedeutet, dass Sie die Sensor-ID wahrscheinlich nicht im Voraus kennen. Wenn Sie jedoch eine Kopie einer bestimmten Sensor-ID gespeichert haben, die Sie zuvor abgerufen haben (z. b. durch Aufrufen von [**iSensor:: GetId**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid)), können Sie denselben Sensor erneut abrufen.

Der folgende Beispielcode zeigt, wie ein Sensor mithilfe seiner ID abgerufen wird.


```C++
ISensor* pSensor = NULL;

// Get the sensor collection.
hr = pSensorManager->GetSensorByID(SAMPLE_SENSOR_TIME_ID, &pSensor);

```



Sie können auch Sensoren abrufen, wenn Sie verfügbar werden, indem Sie ein Ereignis vom Sensor-Manager empfangen. Weitere Informationen finden Sie unter [**isensormanager::**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink)Einstellungs Element.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Isensormanagerevents:: onsensorenter**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanagerevents-onsensorenter)
</dt> </dl>

 

 
