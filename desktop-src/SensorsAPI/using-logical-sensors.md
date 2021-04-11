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
# <a name="using-logical-sensors"></a>Verwenden logischer Sensoren

Um einen Geräteknoten für einen logischen Sensor zu instanziieren oder eine erneute Verbindung mit einem vorhandenen logischen Sensorgeräte Knoten herzustellen, muss eine Anwendung oder ein Dienst [**ilogicalsensormanager:: Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))anrufen. Der *ppropertystore* -Parameter für diese Methode erfordert einen Zeiger auf eine [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle, die die IDs für die Sensor Treiber enthält, mit denen eine Verbindung hergestellt werden soll. Dies bedeutet, dass Sie einen Eigenschaften Speicher erstellen und diese Daten zum Speicher hinzufügen müssen, bevor Sie diese Methode aufrufen.

### <a name="connecting-to-the-logical-sensor"></a>Herstellen einer Verbindung mit dem logischen Sensor

Zum Herstellen einer Verbindung mit einem logischen Sensor müssen Sie mindestens eine Hardware-ID, die in der INF-Datei des Sensor Treibers definiert ist, und eine logische **GUID** , die den Sensor identifiziert, bereitstellen. Diese **GUID** wird von der Plattform zum Identifizieren des Sensors verwendet, wenn Sie den Sensorgeräte Knoten trennen oder deinstallieren möchten.

Der folgende Beispielcode erstellt eine Hilfsmethode, die eine Verbindung mit einem angegebenen logischen Sensor herstellt. Die Methoden Parameter erhalten die Sensor Hardware-ID und eine eindeutige **GUID** zum Identifizieren des Sensors.


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



### <a name="disconnecting-from-a-logical-sensor"></a>Trennen der Verbindung mit einem logischen Sensor

Um die Verbindung mit einem logischen Sensor zu trennen, müssen Sie die gleiche logische ID angeben, die Sie beim Aufrufen von [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))verwendet haben.

Der folgende Beispielcode erstellt eine Hilfsfunktion, die die Verbindung mit einem logischen Sensor trennt.


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



### <a name="uninstalling-a-logical-sensor"></a>Deinstallieren eines logischen Sensors

Zum Deinstallieren eines logischen Sensors müssen Sie dieselbe logische ID angeben, die Sie beim Aufrufen von [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))verwendet haben.

Der folgende Beispielcode erstellt eine Hilfsfunktion, die einen logischen Sensor deinstalliert.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu logischen Sensoren](about-logical-sensors.md)
</dt> </dl>

 

 
