---
description: Verwenden von Licht Sensor Daten
ms.assetid: 98272df5-08c0-4392-a74b-2919bbdcb022
title: Verwenden von Licht Sensor Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ccf1c032b4100174afd6073d8c43db27bce3892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353858"
---
# <a name="using-light-sensor-data"></a><span data-ttu-id="378a0-103">Verwenden von Licht Sensor Daten</span><span class="sxs-lookup"><span data-stu-id="378a0-103">Using Light Sensor Data</span></span>

<span data-ttu-id="378a0-104">Es gibt zwei empfohlene Methoden zum Interpretieren und Verwenden von Lux-Daten, die von Umgebungslichtsensoren stammen.</span><span class="sxs-lookup"><span data-stu-id="378a0-104">There are two recommended ways of interpreting and using lux data that comes from ambient light sensors.</span></span>

-   <span data-ttu-id="378a0-105">Wenden Sie eine Transformation auf die Daten an, sodass die normalisierte Lichtebene direkt im Verhältnis zu Programmverhalten oder Interaktionen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="378a0-105">Apply a transform to the data so that the normalized light level can be used in direct proportion to program behaviors or interactions.</span></span> <span data-ttu-id="378a0-106">Ein Beispiel wäre das Ändern der Größe einer Schaltfläche in Ihrem Programm in direktem Verhältnis zu den normalisierten Daten (oder einem Bereich der normalisierten Daten, z.b. für die Einstellung "Outdoor").</span><span class="sxs-lookup"><span data-stu-id="378a0-106">An example would be to vary the size of a button in your program in direct proportion to the normalized data (or a range of the normalized data, corresponding to outdoors, for example).</span></span> <span data-ttu-id="378a0-107">Dieser Ansatz bietet die optimale Implementierung.</span><span class="sxs-lookup"><span data-stu-id="378a0-107">This approach gives the optimal implementation.</span></span>
-   <span data-ttu-id="378a0-108">Behandeln Sie Bereiche von Lux-Daten, und ordnen Sie Programmverhalten und Reaktionen auf den oberen und unteren Schwellenwert dieser Bereiche von Lux-Daten zu.</span><span class="sxs-lookup"><span data-stu-id="378a0-108">Deal with ranges of lux data, and map program behaviors and reactions to the upper and lower thresholds of these ranges of lux data.</span></span> <span data-ttu-id="378a0-109">Dies ist eine einfache Möglichkeit, auf Beleuchtungsbedingungen zu reagieren, und bietet möglicherweise nicht die optimale Benutzer Leistung.</span><span class="sxs-lookup"><span data-stu-id="378a0-109">This is a simple way to respond to lighting conditions and may not yield the optimal user experience.</span></span> <span data-ttu-id="378a0-110">Diese Vorgehensweise funktioniert jedoch problemlos, wenn reibungslose Übergänge nicht möglich sind.</span><span class="sxs-lookup"><span data-stu-id="378a0-110">However, this approach works fine if smooth transitions are not feasible.</span></span>

## <a name="handling-data-from-multiple-light-sensors"></a><span data-ttu-id="378a0-111">Verarbeiten von Daten aus mehreren Lichtsensoren</span><span class="sxs-lookup"><span data-stu-id="378a0-111">Handling Data from Multiple Light Sensors</span></span>

<span data-ttu-id="378a0-112">Um die präzisere Näherung der aktuellen Beleuchtungsbedingungen zu erreichen, können Sie Daten aus mehreren Umgebungslichtsensoren verwenden.</span><span class="sxs-lookup"><span data-stu-id="378a0-112">To produce the most accurate approximation of the current lighting conditions, you can use data from multiple ambient light sensors.</span></span> <span data-ttu-id="378a0-113">Da Ambient-Light-Sensoren teilweise oder vollständig durch Schatten oder Objekte verdeckt werden können, die den Sensor abdecken, können mehrere Sensoren, die eine gewisse Entfernung aufweisen, eine viel bessere Näherung der aktuellen Beleuchtungsbedingungen darstellen als ein einzelner Sensor.</span><span class="sxs-lookup"><span data-stu-id="378a0-113">Because ambient light sensors can be partly or fully obscured by shadows or objects that cover the sensor, multiple sensors placed some distance apart can provide a much better approximation of the current lighting conditions than a single sensor.</span></span>

<span data-ttu-id="378a0-114">Um die Daten zu verfolgen, die von mehreren Sensoren stammen, können Sie die folgenden beiden Methoden verwenden:</span><span class="sxs-lookup"><span data-stu-id="378a0-114">To keep track of the data coming from multiple sensors, you can use the following two techniques:</span></span>

-   <span data-ttu-id="378a0-115">Der aktuellste Datenwert für jeden Umgebungslichtsensor kann zusammen mit dem Zeitstempel des Sensordaten Berichts für jede dieser Messwerte beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="378a0-115">The most recent data value for each ambient light sensor can be retained, along with the time stamp from the sensor data report for each of these readings.</span></span> <span data-ttu-id="378a0-116">Der letzte für jeden Sensor Lesevorgang empfangene " [**isensordatareport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) " konnte beibehalten werden und kann beide Werte für einen späteren Verweis enthalten.</span><span class="sxs-lookup"><span data-stu-id="378a0-116">The last [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) received for each sensor reading could be retained and could provide both values for later reference.</span></span> <span data-ttu-id="378a0-117">Durch den Verweis auf den Zeitstempel für die einzelnen Sensordaten Berichte können die Daten basierend auf dem Alter verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="378a0-117">By referring to the time stamp for each sensor data report, the data can be managed based on its age.</span></span> <span data-ttu-id="378a0-118">Wenn die Daten z. b. mehr als 2 Sekunden alt sind, können Sie ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="378a0-118">For example, if the data is more than 2 seconds old, it could be omitted.</span></span> <span data-ttu-id="378a0-119">Basierend auf den neueren Sensordaten Werten könnte die höchste Lese barkeit verwendet werden, da der entsprechende Sensor vermutlich nicht verdeckt wäre.</span><span class="sxs-lookup"><span data-stu-id="378a0-119">Based on the newer sensor data values, the highest reading could be used because the corresponding sensor would be presumed not to be obscured.</span></span>
-   <span data-ttu-id="378a0-120">Sie können den zuletzt gemeldeten Umgebungslichtsensor-Wert verwenden.</span><span class="sxs-lookup"><span data-stu-id="378a0-120">You can use the last ambient light sensor value reported.</span></span> <span data-ttu-id="378a0-121">Diese Implementierung wäre nicht optimal, da die Werte von mehreren Sensoren nicht miteinander verglichen werden, um das genaueste Ergebnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="378a0-121">This implementation would not be optimal because the values from multiple sensors are not compared to one another to obtain the most accurate result.</span></span> <span data-ttu-id="378a0-122">Diese Methode wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="378a0-122">We do not recommend this method.</span></span>

## <a name="example-code"></a><span data-ttu-id="378a0-123">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="378a0-123">Example Code</span></span>

<span data-ttu-id="378a0-124">Der folgende Beispielcode zeigt eine Implementierung für das [**ondataupdatiert**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="378a0-124">The following example code shows an implementation for the [**OnDataUpdated**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-ondataupdated) event.</span></span> <span data-ttu-id="378a0-125">Der Ereignishandler ruft eine Hilfsfunktion mit dem Namen **UpdateUI** auf, die die Benutzeroberfläche basierend auf dem Lux-Wert ändert.</span><span class="sxs-lookup"><span data-stu-id="378a0-125">The event handler calls a helper function, named **UpdateUI**, that changes the user interface based on the lux value.</span></span> <span data-ttu-id="378a0-126">Wenn Sie die Implementierung von UpdateUI schreiben, sind Sie auf dem neuesten Stand.</span><span class="sxs-lookup"><span data-stu-id="378a0-126">Writing the implementation of UpdateUI is up to you.</span></span>


```C++
// Override of ISensorEvents::OnDataUpdated
// Part of an event sink implementation for ISensorEvents
STDMETHODIMP CALSEventSink::OnDataUpdated(
    ISensor* pSensor, 
    ISensorDataReport* pNewData)
{
    HRESULT hr = S_OK;
   
    if(pSensor == NULL ||
       pNewData == NULL)
    {
         return E_POINTER;
    }

    // Declare and initialize the PROPVARIANT
    PROPVARIANT lightLevel;
    PropVariantInit(&lightLevel);

    // Get the sensor reading from the ISensorDataReport object
    hr = pNewData->GetSensorValue(
        SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX, 
        &lightLevel);

    if(SUCCEEDED(hr))
    {
        if(lightlevel.vt == VT_R4)
        {
            // Extract the float value from the PROPVARIANT object
            float luxValue = lightLevel.fltVal;

            // Normalize the light sensor data
            double lightNormalized = ::log10(luxValue) / 5.0;

            // Handle UI changes based on the normalized LUX data
            // which ranges from 0.0 - 1.0 for a lux range of 
            // 0 lux to 100,000 lux. 
            UpdateUI(lightNormalized);
        }
    }

    // Release the variant.     
    PropVariantClear(&lightLevel);

    return hr;
}
```



 

 
