---
description: In diesem Thema wird beschrieben, wie Sie überprüfen, ob ein Sensor einen bestimmten Satz von Datenfeldern bereitstellen kann.
ms.assetid: 918ba4a3-d2ac-47ee-ba29-f7ddf67ffbc5
title: Überprüfen auf unterstützte Sensordatenfelder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa75c474dc4cd38d34074872765abc77a7dae00d18e8cc37d74cde70b6f22a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890265"
---
# <a name="checking-for-supported-sensor-data-fields"></a>Überprüfen auf unterstützte Sensordatenfelder

In diesem Thema wird beschrieben, wie Sie überprüfen, ob ein Sensor einen bestimmten Satz von Datenfeldern bereitstellen kann.

Nachdem Sie ein Sensorobjekt abgerufen haben, können Sie [**ISensor::GetSupportedDataFields**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getsupporteddatafields) aufrufen, um zu bestimmen, ob der Sensor die benötigten Daten bereitstellen kann.

Der folgende Beispielcode erstellt eine Hilfsfunktion, die testet, ob der Sensor alle drei Beispieldatenfelder bereitstellen kann. Die Funktion nimmt einen Zeiger auf einen Sensor als Eingabe und gibt einen booleschen Wert zurück, wobei **TRUE** angibt, dass der Sensor alle erforderlichen Datenfelder bereitstellen kann.


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

[**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport)
</dt> </dl>

 

 
