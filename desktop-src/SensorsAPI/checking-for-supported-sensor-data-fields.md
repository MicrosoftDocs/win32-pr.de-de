---
description: In diesem Thema wird beschrieben, wie Sie überprüfen, ob ein Sensor eine bestimmte Gruppe von Datenfeldern bereitstellen kann.
ms.assetid: 918ba4a3-d2ac-47ee-ba29-f7ddf67ffbc5
title: Überprüfen auf unterstützte Sensor Datenfelder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfd9cf42d1008ec1bb0e2785ec5113c5a817105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353885"
---
# <a name="checking-for-supported-sensor-data-fields"></a>Überprüfen auf unterstützte Sensor Datenfelder

In diesem Thema wird beschrieben, wie Sie überprüfen, ob ein Sensor eine bestimmte Gruppe von Datenfeldern bereitstellen kann.

Nachdem Sie ein Sensor Objekt abgerufen haben, können Sie [**iSensor:: getsupporteddatafields**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getsupporteddatafields) aufrufen, um zu bestimmen, ob der Sensor die benötigten Daten bereitstellen kann.

Der folgende Beispielcode erstellt eine Hilfsfunktion, die testet, ob der Sensor alle drei Beispiel Datenfelder bereitstellen kann. Die Funktion nimmt einen Zeiger auf einen Sensor als Eingabe und gibt einen booleschen Wert zurück, wobei **true** angibt, dass der Sensor alle benötigten Datenfelder bereitstellen kann.


```C++
BOOL CheckForSupportedDataFields(ISensor* pSensor)
{
    assert(pSensor);

    HRESULT hr = S_OK;
    DWORD cKeys = 0; // Key count.
    BOOL bRet = FALSE;

    IPortableDeviceKeyCollection* pKeys = NULL; // Output

    // CoCreate a key collection to store property keys.
    hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection, 
                                NULL, 
                                CLSCTX_INPROC_SERVER, 
                                IID_PPV_ARGS(&pKeys));

    if(SUCCEEDED(hr))
    {
        hr = pSensor->GetSupportedDataFields(&pKeys);
    }

    if(SUCCEEDED(hr))
    {
        hr = pKeys->GetCount(&cKeys);
    }

    if(SUCCEEDED(hr))
    {
        PROPERTYKEY pk;
        BOOL bHour, bMinute, bSecond = FALSE;

        for (DWORD i = 0; i < cKeys; i++)
        {
            hr = pKeys->GetAt(i, &pk);

            if(SUCCEEDED(hr))
            {
                // Test for the data fields.
                if(IsEqualPropertyKey(pk, SAMPLE_SENSOR_DATA_TYPE_HOUR))
                {
                    bHour = TRUE;
                }
                else if(IsEqualPropertyKey(pk, SAMPLE_SENSOR_DATA_TYPE_MINUTE))
                {
                    bMinute = TRUE;
                }
                else if(IsEqualPropertyKey(pk, SAMPLE_SENSOR_DATA_TYPE_SECOND))
                {
                    bSecond = TRUE;
                }
            }
        }

        // Compute the return value.
        // If all three properties were found,
        // bRet will resolve to TRUE.
        bRet = bHour && bMinute && bSecond;
    }

    SafeRelease(&pKeys);

    return bRet;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Isensordatareport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport)
</dt> </dl>

 

 
