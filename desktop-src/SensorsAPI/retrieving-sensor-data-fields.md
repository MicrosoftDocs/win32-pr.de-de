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
# <a name="retrieving-sensor-data-values"></a><span data-ttu-id="b69d9-103">Abrufen von Sensor Datenwerten</span><span class="sxs-lookup"><span data-stu-id="b69d9-103">Retrieving Sensor Data Values</span></span>

<span data-ttu-id="b69d9-104">In diesem Thema wird beschrieben, wie Daten synchron und asynchron von einem Sensor abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b69d9-104">This topic describes how to retrieve data from a sensor, synchronously and asynchronously.</span></span>

## <a name="retrieving-data-synchronously"></a><span data-ttu-id="b69d9-105">Synchrones Abrufen von Daten</span><span class="sxs-lookup"><span data-stu-id="b69d9-105">Retrieving Data Synchronously</span></span>

<span data-ttu-id="b69d9-106">Sie können Sensordaten synchron abrufen, indem Sie [**iSensor:: GetData**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b69d9-106">You can retrieve sensor data synchronously by calling [**ISensor::GetData**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getdata).</span></span>

<span data-ttu-id="b69d9-107">Der folgende Beispielcode ruft einen Sensordaten Bericht ab und ruft dann drei einzelne Daten Feldwerte ab.</span><span class="sxs-lookup"><span data-stu-id="b69d9-107">The following example code retrieves a sensor data report, and then retrieves three individual data field values.</span></span> <span data-ttu-id="b69d9-108">Der Beispiel Sensor stellt benutzerdefinierte Daten über die aktuelle lokale Zeit in Stunden-, Minuten-und zweiten Datenfeldern bereit.</span><span class="sxs-lookup"><span data-stu-id="b69d9-108">The sample sensor provides custom data about the current local time in hour, minute, and second data fields.</span></span> <span data-ttu-id="b69d9-109">Die Variable mit dem Namen psensor enthält einen Zeiger auf [**iSensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) , der den Sensor darstellt, der die Daten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="b69d9-109">The variable named pSensor contains a pointer to [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) that represents the sensor that supplies the data.</span></span>


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



## <a name="retrieving-data-asynchronously"></a><span data-ttu-id="b69d9-110">Asynchrones Abrufen von Daten</span><span class="sxs-lookup"><span data-stu-id="b69d9-110">Retrieving Data Asynchronously</span></span>

<span data-ttu-id="b69d9-111">Sie können Sensordaten asynchron empfangen, indem Sie registrieren, um das Ereignis " [**isensorevents:: ondataupdatiert**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) " zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="b69d9-111">You can receive sensor data asynchronously by registering to receive the [**ISensorEvents::OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) event.</span></span> <span data-ttu-id="b69d9-112">Informationen zum Empfangen von Sensor Ereignis Rückrufen finden Sie unter [Verwenden von Sensor-API-Ereignissen](using-sensor-api-events.md).</span><span class="sxs-lookup"><span data-stu-id="b69d9-112">To understand how to receive sensor event callbacks, see [Using Sensor API Events](using-sensor-api-events.md).</span></span>

<span data-ttu-id="b69d9-113">Der folgende Beispielcode zeigt eine Implementierung von [**isensorevents:: ondataupveraltet**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) , die Datenwerte aus dem Datenbericht abruft, der vom-Ereignis bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b69d9-113">The following example code shows an implementation of [**ISensorEvents::OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) that retrieves data values from the data report provided by the event.</span></span> <span data-ttu-id="b69d9-114">Der Beispiel Sensor stellt benutzerdefinierte Daten über die aktuelle lokale Zeit in Stunden-, Minuten-und zweiten Datenfeldern bereit.</span><span class="sxs-lookup"><span data-stu-id="b69d9-114">The sample sensor provides custom data about the current local time in hour, minute, and second data fields.</span></span>


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



 

 
