---
description: In diesem Thema wird beschrieben, wie Sie Werte für Sensoreigenschaften abrufen und festlegen. Die iSensor-Schnittstelle stellt die Methoden zum Festlegen und Abrufen von Werten für Sensoreigenschaften bereit.
ms.assetid: 7d10e5b4-bae7-4564-84eb-75c6a2eeef8f
title: Abrufen und Festlegen von Sensor Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f64bf0e253f47ae2d8cd1f4945f3b87aa3406b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368866"
---
# <a name="retrieving-and-setting-sensor-properties"></a>Abrufen und Festlegen von Sensor Eigenschaften

In diesem Thema wird beschrieben, wie Sie Werte für Sensoreigenschaften abrufen und festlegen. Die [**iSensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) -Schnittstelle stellt die Methoden zum Festlegen und Abrufen von Werten für Sensoreigenschaften bereit.

## <a name="retrieving-sensor-properties"></a>Abrufen von Sensor Eigenschaften

Sie können einige Eigenschaftswerte von einem Sensor abrufen, bevor Sie vom Benutzer aktiviert wurden. Informationen wie der Herstellername oder das Modell des Sensors können Ihnen dabei helfen zu entscheiden, ob das Programm den Sensor verwenden kann.

Sie können auswählen, ob Sie einen einzelnen Eigenschafts Wert abrufen oder eine Auflistung von Eigenschafts Werten abrufen möchten. Um einen einzelnen Wert abzurufen, rufen Sie [**iSensor:: GetProperty**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperty)auf. Rufen Sie zum Abrufen einer Auflistung von Werten [**iSensor:: GetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-getproperties)auf. Sie können alle Eigenschaften eines Sensors abrufen, indem Sie **null** über den ersten Parameter an **iSensor:: GetProperties** übergeben.

Der folgende Beispielcode erstellt eine Hilfsfunktion, die den Wert einer einzelnen Eigenschaft ausgibt. Die-Funktion empfängt einen Zeiger auf den Sensor, von dem der Wert abgerufen werden soll, und ein Eigenschafts Schlüssel, der die zu druckende Eigenschaft enthält. Die Funktion kann Werte für Zahlen, Zeichen folgen und **GUID**-Werte, aber nicht für andere komplexere Typen drucken.


```C++
HRESULT PrintSensorProperty(ISensor* pSensor, REFPROPERTYKEY pk)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    PROPVARIANT pv = {};

    hr = pSensor->GetProperty(pk, &pv);

    if(SUCCEEDED(hr))
    {
        if(pv.vt == VT_UI4)  // Number
        {
            wprintf_s(L"\nSensor integer value: %u\n", pv.ulVal);
        }
        else if(pv.vt == VT_LPWSTR)  // String
        {
            wprintf_s(L"\nSensor string value: %s\n", pv.pwszVal);
        }
        else if(pv.vt == VT_CLSID)  // GUID
        {
            int iRet = 0;

            // Convert the GUID to a string.
            OLECHAR wszGuid[39] = {}; // Buffer for string.
            iRet = ::StringFromGUID2(*(pv.puuid), wszGuid, 39);

            assert(39 == iRet); // Count of characters returned for GUID.

            wprintf_s(L"\nSensor GUID value: %s\n", wszGuid);
        }
        else  // Interface or vector
        {
            wprintf_s(L"\nSensor property is a compound type. Unable to print value.");
        }
    }

    PropVariantClear(&pv);

    return hr;    
}
```



Im folgenden Beispielcode wird eine Funktion erstellt, die eine Auflistung von Eigenschaften abruft und druckt. Der zu druckende Satz von Eigenschaften wird durch das Array namens sensorproperties definiert.


```C++
HRESULT PrintSensorProperties(ISensor* pSensor)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    DWORD cVals = 0; // Count of returned properties.
    IPortableDeviceKeyCollection* pKeys = NULL; // Input
    IPortableDeviceValues* pValues = NULL;  // Output

    // Properties to print.
    const PROPERTYKEY SensorProperties[] =
    {
        SENSOR_PROPERTY_MANUFACTURER,
        SENSOR_PROPERTY_SERIAL_NUMBER,
        SENSOR_PROPERTY_DESCRIPTION,
        SENSOR_PROPERTY_FRIENDLY_NAME
    };

    // CoCreate a key collection to store property keys.
    hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection, 
                                NULL, 
                                CLSCTX_INPROC_SERVER,                                 
                                IID_PPV_ARGS(&pKeys));

    if(SUCCEEDED(hr))
    {
        // Add the properties to the key collection.
        for (DWORD dwIndex = 0; dwIndex < ARRAYSIZE(SensorProperties); dwIndex++)
        {
            hr = pKeys->Add(SensorProperties[dwIndex]);

            if(FAILED(hr))
            {
                // Unexpected.
                // This example returns the failed HRESULT.
                // You may choose to ignore failures, here.
                break;
            }
        }
    }

    if(SUCCEEDED(hr))
    {
        // Retrieve the properties from the sensor.
        hr = pSensor->GetProperties(pKeys, &pValues);
    }

    if(SUCCEEDED(hr))
    {
        // Get the number of values returned.        
        hr = pValues->GetCount(&cVals);
    }

    if(SUCCEEDED(hr))
    {
        PROPERTYKEY pk; // Keys
        PROPVARIANT pv = {}; // Values

        // Loop through the values;
        for (DWORD i = 0; i < cVals; i++)
        {
            // Get the value at the current index.
            hr = pValues->GetAt(i, &pk, &pv);

            if(SUCCEEDED(hr))
            { 
                // Find and print the property.
                if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_MANUFACTURER))
                {
                    wprintf_s(L"\nManufacturer: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_SERIAL_NUMBER))
                {
                    wprintf_s(L"Serial number: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_FRIENDLY_NAME))
                {
                    wprintf_s(L"Friendly name: %s\n", pv.pwszVal);
                }
                else if(IsEqualPropertyKey(pk, SENSOR_PROPERTY_DESCRIPTION))
                {
                    wprintf_s(L"Description: %s\n", pv.pwszVal);
                }
            }

            PropVariantClear(&pv);
        } // end i loop        
    }

    SafeRelease(&pKeys);
    SafeRelease(&pValues);

    return hr;
};
```



## <a name="setting-sensor-properties"></a>Festlegen von Sensor Eigenschaften

Bevor Sie Eigenschaftswerte für einen Sensor festlegen können, muss der Benutzer den Sensor aktivieren. Außerdem können nicht alle Sensoreigenschaften festgelegt werden.

Um einen oder mehrere Werte für Eigenschaften festzulegen, wenden Sie [**iSensor:: SetProperties**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-setproperties)an. Sie stellen diese Methode mit einem [iportabledevicevalues](/previous-versions//ms740012(v=vs.85)) -Zeiger bereit, der die Auflistung der festzulegenden Eigenschaften und die zugehörigen Werte enthält. Die-Methode gibt eine entsprechende [iportabledevicevalues](/previous-versions//ms740012(v=vs.85)) -Schnittstelle zurück, die möglicherweise Fehlercodes für Eigenschaften enthält, die nicht festgelegt werden konnten.

Im folgenden Beispielcode wird eine Hilfsfunktion erstellt, mit der ein neuer Wert für \_ die \_ Eigenschaft "Aktuelles \_ Berichts Intervall" der Sensor Eigenschaft festgelegt wird \_ . Die-Funktion nimmt einen Zeiger auf den Sensor, für den die-Eigenschaft festgelegt werden soll, und einen **ulong** -Wert, der das neue Berichts Intervall angibt, das festgelegt werden soll. (Beachten Sie, dass das Festlegen eines Werts für diese bestimmte Eigenschaft nicht gewährleistet, dass der Sensor den angegebenen Wert annimmt. Informationen zur Funktionsweise dieser Eigenschaft finden Sie unter [**Sensor Eigenschaften**](sensor-properties.md) .)


```C++
HRESULT SetCurrentReportInterval(ISensor* pSensor, ULONG ulNewInterval)
{
    assert(pSensor);

    HRESULT hr = S_OK;

    IPortableDeviceValues* pPropsToSet = NULL; // Input
    IPortableDeviceValues* pPropsReturn = NULL; // Output

    // Create the input object.
    hr = CoCreateInstance(__uuidof(PortableDeviceValues),
                            NULL,
                            CLSCTX_INPROC_SERVER,                           
                            IID_PPV_ARGS(&pPropsToSet));

    if(SUCCEEDED(hr))
    {
        // Add the current report interval property.
        hr = pPropsToSet->SetUnsignedIntegerValue(SENSOR_PROPERTY_CURRENT_REPORT_INTERVAL, ulNewInterval);
    }

    if(SUCCEEDED(hr))
    {
        // Only setting a single property, here.
        hr = pSensor->SetProperties(pPropsToSet, &pPropsReturn);
    }

    // Test for failure.
    if(hr == S_FALSE)
    {
        HRESULT hrError = S_OK;
      
        // Check results for failure.
        hr = pPropsReturn->GetErrorValue(SENSOR_PROPERTY_CURRENT_REPORT_INTERVAL, &hrError);

        if(SUCCEEDED(hr))
        {
            // Print an error message.
            wprintf_s(L"\nSetting current report interval failed with error 0x%X\n", hrError);

            // Return the error code.
            hr = hrError;
        }
    }
    else if(hr == E_ACCESSDENIED)
    {
        // No permission. Take appropriate action.
    }

    SafeRelease(&pPropsToSet);
    SafeRelease(&pPropsReturn);
   
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Sensor Eigenschaften**](sensor-properties.md)
</dt> </dl>

 

 
