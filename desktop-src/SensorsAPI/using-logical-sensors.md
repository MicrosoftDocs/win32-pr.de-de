---
description: Verwenden logischer Sensoren
ms.assetid: 97f4c44e-27dd-4f2a-b987-060bb2d9bc00
title: Verwenden logischer Sensoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb0493cfe8ff3a489e926792f9a101eb5d9db6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128737"
---
# <a name="using-logical-sensors"></a><span data-ttu-id="61a8f-103">Verwenden logischer Sensoren</span><span class="sxs-lookup"><span data-stu-id="61a8f-103">Using Logical Sensors</span></span>

<span data-ttu-id="61a8f-104">Um einen Geräteknoten für einen logischen Sensor zu instanziieren oder eine erneute Verbindung mit einem vorhandenen logischen Sensorgeräte Knoten herzustellen, muss eine Anwendung oder ein Dienst [**ilogicalsensormanager:: Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))anrufen.</span><span class="sxs-lookup"><span data-stu-id="61a8f-104">To instantiate a device node for a logical sensor, or to reconnect to an existing logical sensor device node, an application or service must call [**ILogicalSensorManager::Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span> <span data-ttu-id="61a8f-105">Der *ppropertystore* -Parameter für diese Methode erfordert einen Zeiger auf eine [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle, die die IDs für die Sensor Treiber enthält, mit denen eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="61a8f-105">The *pPropertyStore* parameter for this method requires a pointer to an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface that contains the IDs for the sensor drivers to connect to.</span></span> <span data-ttu-id="61a8f-106">Dies bedeutet, dass Sie einen Eigenschaften Speicher erstellen und diese Daten zum Speicher hinzufügen müssen, bevor Sie diese Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="61a8f-106">This means that you must create a property store and add this data to the store before calling this method.</span></span>

### <a name="connecting-to-the-logical-sensor"></a><span data-ttu-id="61a8f-107">Herstellen einer Verbindung mit dem logischen Sensor</span><span class="sxs-lookup"><span data-stu-id="61a8f-107">Connecting to the Logical Sensor</span></span>

<span data-ttu-id="61a8f-108">Zum Herstellen einer Verbindung mit einem logischen Sensor müssen Sie mindestens eine Hardware-ID, die in der INF-Datei des Sensor Treibers definiert ist, und eine logische **GUID** , die den Sensor identifiziert, bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="61a8f-108">To connect to a logical sensor, you must provide, at a minimum, a hardware ID, as defined in the sensor driver's .inf file, and a logical **GUID** that identifies the sensor.</span></span> <span data-ttu-id="61a8f-109">Diese **GUID** wird von der Plattform zum Identifizieren des Sensors verwendet, wenn Sie den Sensorgeräte Knoten trennen oder deinstallieren möchten.</span><span class="sxs-lookup"><span data-stu-id="61a8f-109">The platform uses this **GUID** to identify the sensor when you choose to disconnect from, or uninstall, the sensor device node.</span></span>

<span data-ttu-id="61a8f-110">Der folgende Beispielcode erstellt eine Hilfsmethode, die eine Verbindung mit einem angegebenen logischen Sensor herstellt.</span><span class="sxs-lookup"><span data-stu-id="61a8f-110">The following example code creates a helper method that connects to a specified logical sensor.</span></span> <span data-ttu-id="61a8f-111">Die Methoden Parameter erhalten die Sensor Hardware-ID und eine eindeutige **GUID** zum Identifizieren des Sensors.</span><span class="sxs-lookup"><span data-stu-id="61a8f-111">The method parameters receive the sensor hardware ID and a unique **GUID** to identify the sensor.</span></span>


```C++
HRESULT ConnectToLogicalSensor(PCWSTR* wszHardwareID, GUID guidLogicalID)
{
    HRESULT hr = S_OK;
    
    ILogicalSensorManager* pLSM = NULL;
    IPropertyStore* pStore = NULL;
    PROPVARIANT pv = {};

    // Create the property store.
    hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pStore));

    if(SUCCEEDED(hr))
    {
        // Create the logical sensor manager.
        hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pLSM));
    }

    // Fill in the values.
    if(SUCCEEDED(hr))
    {
        hr = InitPropVariantFromStringVector(wszHardwareID, 1, &pv);
    }

    if(SUCCEEDED(hr))
    {
        hr = pStore->SetValue(PKEY_Device_HardwareIds, pv);
    }

    if(SUCCEEDED(hr))
    {
        hr = pStore->SetValue(PKEY_Device_CompatibleIds, pv);
    }

    if(SUCCEEDED(hr))
    {
        // Connect to the logical sensor.
        hr = pLSM->Connect(guidLogicalID, pStore);
    }

    SafeRelease(&pStore);
    SafeRelease(&pLSM);

    return hr;
}
```



### <a name="disconnecting-from-a-logical-sensor"></a><span data-ttu-id="61a8f-112">Trennen der Verbindung mit einem logischen Sensor</span><span class="sxs-lookup"><span data-stu-id="61a8f-112">Disconnecting from a Logical Sensor</span></span>

<span data-ttu-id="61a8f-113">Um die Verbindung mit einem logischen Sensor zu trennen, müssen Sie die gleiche logische ID angeben, die Sie beim Aufrufen von [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="61a8f-113">To disconnect from a logical sensor, you must provide the same logical ID that you used when you called [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span>

<span data-ttu-id="61a8f-114">Der folgende Beispielcode erstellt eine Hilfsfunktion, die die Verbindung mit einem logischen Sensor trennt.</span><span class="sxs-lookup"><span data-stu-id="61a8f-114">The following example code creates a helper function that disconnects from a logical sensor.</span></span>


```C++
HRESULT DisconnectFromLogicalSensor(GUID guidLogicalID)
{
    HRESULT hr = S_OK;

    ILogicalSensorManager* pLSM = NULL;
 
    if(SUCCEEDED(hr))
    {
        // Create the logical sensor manager.
        hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pLSM));
    }

    if(SUCCEEDED(hr))
    {
        hr = pLSM->Disconnect(guidLogicalID);
    }

    SafeRelease(&pLSM);

    return hr;
}
```



### <a name="uninstalling-a-logical-sensor"></a><span data-ttu-id="61a8f-115">Deinstallieren eines logischen Sensors</span><span class="sxs-lookup"><span data-stu-id="61a8f-115">Uninstalling a Logical Sensor</span></span>

<span data-ttu-id="61a8f-116">Zum Deinstallieren eines logischen Sensors müssen Sie dieselbe logische ID angeben, die Sie beim Aufrufen von [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="61a8f-116">To uninstall a logical sensor, you must provide the same logical ID that you used when you called [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)).</span></span>

<span data-ttu-id="61a8f-117">Der folgende Beispielcode erstellt eine Hilfsfunktion, die einen logischen Sensor deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="61a8f-117">The following example code creates a helper function that uninstalls a logical sensor.</span></span>


```C++
HRESULT UninstallLogicalSensor(REFGUID guidLogicalID)
{
    HRESULT hr = S_OK;

    ILogicalSensorManager* pLSM;
 
    // Create the logical sensor manager.
    hr = CoCreateInstance(CLSID_LogicalSensorManager, 
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_PPV_ARGS(&pLSM));
 
    if(SUCCEEDED(hr))
    {
        hr = pLSM->Uninstall(guidLogicalID);
    }

    SafeRelease(&pLSM);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="61a8f-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="61a8f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61a8f-119">Informationen zu logischen Sensoren</span><span class="sxs-lookup"><span data-stu-id="61a8f-119">About Logical Sensors</span></span>](about-logical-sensors.md)
</dt> </dl>

 

 
