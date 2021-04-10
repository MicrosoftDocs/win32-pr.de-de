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
# <a name="retrieving-a-sensor-object"></a><span data-ttu-id="9695e-105">Abrufen eines Sensor Objekts</span><span class="sxs-lookup"><span data-stu-id="9695e-105">Retrieving a Sensor Object</span></span>

<span data-ttu-id="9695e-106">Zum Abrufen eines Sensor Objekts verwenden Sie die Schnittstelle " [**isensormanager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) ".</span><span class="sxs-lookup"><span data-stu-id="9695e-106">To retrieve a sensor object, you use the [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager) interface.</span></span> <span data-ttu-id="9695e-107">Sie können sich diese Schnittstelle als Stamm Schnittstelle für die Sensor-API vorstellen.</span><span class="sxs-lookup"><span data-stu-id="9695e-107">You can think of this interface as the root interface for the Sensor API.</span></span> <span data-ttu-id="9695e-108">Um den " **isenmanager**" verwenden zu können, müssen Sie zuerst die com- **cokreateinstance** -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9695e-108">To use **ISensorManager**, you must first call the COM **CoCreateInstance** method.</span></span>

<span data-ttu-id="9695e-109">Im folgenden Beispielcode wird eine Instanz des Sensor-Managers erstellt.</span><span class="sxs-lookup"><span data-stu-id="9695e-109">The following example code creates an instance of the sensor manager.</span></span>


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



<span data-ttu-id="9695e-110">Nachdem Sie erfolgreich einen Zeiger auf " [**isensormanager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager)" abgerufen haben, können Sie Sensoren nach Kategorie, Typ oder ID abrufen.</span><span class="sxs-lookup"><span data-stu-id="9695e-110">After successfully retrieving a pointer to [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager), you can retrieve sensors by category, type, or ID.</span></span> <span data-ttu-id="9695e-111">Wenn Sie Sensoren nach Typ oder Kategorie abrufen, erhalten Sie einen Zeiger auf eine Schnittstelle " [**isensorcollection**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) ", die alle verfügbaren Sensoren enthält, die zur angeforderten Kategorie oder zum angeforderten Typ gehören.</span><span class="sxs-lookup"><span data-stu-id="9695e-111">If you retrieve sensors by type or category, you receive a pointer to an [**ISensorCollection**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection) interface that contains all the available sensors that belong to the requested category or type.</span></span> <span data-ttu-id="9695e-112">Wenn Sie einen Sensor anhand seiner ID abrufen, erhalten Sie einen Zeiger auf eine [**iSensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) -Schnittstelle, die den von Ihnen angeforderten eindeutigen Sensor darstellt.</span><span class="sxs-lookup"><span data-stu-id="9695e-112">If you retrieve a sensor by its ID, you receive a pointer to an [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface that represents the unique sensor you requested.</span></span>

<span data-ttu-id="9695e-113">Der folgende Beispielcode ruft eine Auflistung von Sensoren ab, die zur Kategorie namens "Sample \_ Sensor \_ Category \_ Date \_ time" gehören.</span><span class="sxs-lookup"><span data-stu-id="9695e-113">The following example code retrieves a collection of sensors that belong to the category named SAMPLE\_SENSOR\_CATEGORY\_DATE\_TIME.</span></span> <span data-ttu-id="9695e-114">Der Code ruft dann den ersten Sensor in der Auflistung nach dem Index ab.</span><span class="sxs-lookup"><span data-stu-id="9695e-114">The code then retrieves the first sensor in the collection by its index.</span></span>


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



<span data-ttu-id="9695e-115">Beachten Sie, dass Sie alle verfügbaren Sensoren abrufen können, indem Sie die Sensor \_ Kategorie \_ alle verwenden.</span><span class="sxs-lookup"><span data-stu-id="9695e-115">Note that you can retrieve all of the available sensors by using SENSOR\_CATEGORY\_ALL.</span></span>

<span data-ttu-id="9695e-116">Auf ähnliche Weise können Sie Sensoren eines bestimmten Typs abrufen.</span><span class="sxs-lookup"><span data-stu-id="9695e-116">In a similar way, you can retrieve sensors of a particular type.</span></span>

<span data-ttu-id="9695e-117">Der folgende Beispielcode ruft eine Auflistung von Sensoren des Typs mit dem Namen Sample \_ \_ SensorType \_ time ab.</span><span class="sxs-lookup"><span data-stu-id="9695e-117">The following example code retrieves a collection of sensors of the type named SAMPLE\_SENSOR\_TYPE\_TIME.</span></span> <span data-ttu-id="9695e-118">Der Code ruft dann den ersten Sensor in der Auflistung nach dem Index ab.</span><span class="sxs-lookup"><span data-stu-id="9695e-118">The code then retrieves the first sensor in the collection by its index.</span></span>


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



<span data-ttu-id="9695e-119">Zum Abrufen eines Sensors anhand seiner ID müssen Sie die eindeutige ID für den Sensor kennen.</span><span class="sxs-lookup"><span data-stu-id="9695e-119">To retrieve a sensor by its ID, you must know the unique ID for the sensor.</span></span> <span data-ttu-id="9695e-120">Sensoren generieren diese ID normalerweise bei der ersten Verbindung, damit Sie mehrere Sensoren desselben Make-und Model-Modells identifizieren können.</span><span class="sxs-lookup"><span data-stu-id="9695e-120">Sensors usually generate this ID when first connected to enable you to identify multiple sensors of the same make and model.</span></span> <span data-ttu-id="9695e-121">Dies bedeutet, dass Sie die Sensor-ID wahrscheinlich nicht im Voraus kennen.</span><span class="sxs-lookup"><span data-stu-id="9695e-121">This means that you probably will not know the sensor ID in advance.</span></span> <span data-ttu-id="9695e-122">Wenn Sie jedoch eine Kopie einer bestimmten Sensor-ID gespeichert haben, die Sie zuvor abgerufen haben (z. b. durch Aufrufen von [**iSensor:: GetId**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid)), können Sie denselben Sensor erneut abrufen.</span><span class="sxs-lookup"><span data-stu-id="9695e-122">However, if you have stored a copy of a particular sensor ID that you previously retrieved, for example by calling [**ISensor::GetID**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getid), you may want to retrieve the same sensor again.</span></span>

<span data-ttu-id="9695e-123">Der folgende Beispielcode zeigt, wie ein Sensor mithilfe seiner ID abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9695e-123">The following example code shows how to retrieve a sensor by using its ID.</span></span>


```C++
ISensor* pSensor = NULL;

// Get the sensor collection.
hr = pSensorManager->GetSensorByID(SAMPLE_SENSOR_TIME_ID, &pSensor);

```



<span data-ttu-id="9695e-124">Sie können auch Sensoren abrufen, wenn Sie verfügbar werden, indem Sie ein Ereignis vom Sensor-Manager empfangen.</span><span class="sxs-lookup"><span data-stu-id="9695e-124">You can also retrieve sensors when they become available by receiving an event from the sensor manager.</span></span> <span data-ttu-id="9695e-125">Weitere Informationen finden Sie unter [**isensormanager::**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink)Einstellungs Element.</span><span class="sxs-lookup"><span data-stu-id="9695e-125">For more information, see [**ISensorManager::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9695e-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9695e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9695e-127">**Isensormanagerevents:: onsensorenter**</span><span class="sxs-lookup"><span data-stu-id="9695e-127">**ISensorManagerEvents::OnSensorEnter**</span></span>](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanagerevents-onsensorenter)
</dt> </dl>

 

 
