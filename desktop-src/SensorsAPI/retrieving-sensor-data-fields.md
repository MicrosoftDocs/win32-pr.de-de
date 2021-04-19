---
description: In diesem Thema wird beschrieben, wie Daten synchron und asynchron von einem Sensor abgerufen werden.
ms.assetid: 4ae80816-5e53-4ed1-9300-4b38c22d65e2
title: Abrufen von Sensor Datenwerten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4642f120e549cd77b1b37610037092facf2ead1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346086"
---
# <a name="retrieving-sensor-data-values"></a>Abrufen von Sensor Datenwerten

In diesem Thema wird beschrieben, wie Daten synchron und asynchron von einem Sensor abgerufen werden.

## <a name="retrieving-data-synchronously"></a>Synchrones Abrufen von Daten

Sie können Sensordaten synchron abrufen, indem Sie [**iSensor:: GetData**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata)aufrufen.

Der folgende Beispielcode ruft einen Sensordaten Bericht ab und ruft dann drei einzelne Daten Feldwerte ab. Der Beispiel Sensor stellt benutzerdefinierte Daten über die aktuelle lokale Zeit in Stunden-, Minuten-und zweiten Datenfeldern bereit. Die Variable mit dem Namen psensor enthält einen Zeiger auf [**iSensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) , der den Sensor darstellt, der die Daten bereitstellt.


```C++
if(SUCCEEDED(hr))
{
    // Get the data report.
    hr = pSensor->GetData(&pReport);
}
  
if(SUCCEEDED(hr))
{
    PROPVARIANT var = {};

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_HOUR, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulHour = var.ulVal;                
        }
    }

    PropVariantClear(&var);

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_MINUTE, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulMinute = var.ulVal;
        }
    }

    PropVariantClear(&var);

    hr = pReport->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_SECOND, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulSecond = var.ulVal;
        }
    }

    PropVariantClear(&var);        

    if(SUCCEEDED(hr))
    {
        // Print the local time to the console window.
        wprintf_s(L"\nCurrent local time is: \n");
        wprintf_s(L"%02d:%02d:%02d (synchronous)\n\n", ulHour, ulMinute, ulSecond);
    }

```



## <a name="retrieving-data-asynchronously"></a>Asynchrones Abrufen von Daten

Sie können Sensordaten asynchron empfangen, indem Sie registrieren, um das Ereignis " [**isensorevents:: ondataupdatiert**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) " zu empfangen. Informationen zum Empfangen von Sensor Ereignis Rückrufen finden Sie unter [Verwenden von Sensor-API-Ereignissen](using-sensor-api-events.md).

Der folgende Beispielcode zeigt eine Implementierung von [**isensorevents:: ondataupveraltet**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) , die Datenwerte aus dem Datenbericht abruft, der vom-Ereignis bereitgestellt wird. Der Beispiel Sensor stellt benutzerdefinierte Daten über die aktuelle lokale Zeit in Stunden-, Minuten-und zweiten Datenfeldern bereit.


```C++
STDMETHODIMP OnDataUpdated(
        ISensor *pSensor,
        ISensorDataReport *pNewData)
{
    HRESULT hr = S_OK;

    if(NULL == pNewData ||
       NULL == pSensor)
    {
        return E_INVALIDARG;
    }

    ULONG ulHour = 0;
    ULONG ulMinute = 0;
    ULONG ulSecond = 0;

    PROPVARIANT var = {};

    hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_HOUR, &var);

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulHour = var.ulVal;                
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_MINUTE, &var);
    }

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulMinute = var.ulVal;
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        hr = pNewData->GetSensorValue(SAMPLE_SENSOR_DATA_TYPE_SECOND, &var);
    }

    if(SUCCEEDED(hr))
    {
        if(var.vt == VT_UI4)
        {
            // Get the hour value.
            ulSecond = var.ulVal;
        }
    }

    PropVariantClear(&var);

    if(SUCCEEDED(hr))
    {
        // Print
        wprintf_s(L"Current local time is: \n");
        wprintf_s(L"%02d:%02d:%02d (asynchronous)\n", ulHour, ulMinute, ulSecond);
    }

    return hr;
}
```



 

 
