---
description: Die Sensor-API stellt Ereignisbenachrichtigungen über Rückrufschnittstellen bereit.
ms.assetid: 0c396d54-cb2e-4b07-999f-3f4001db2a02
title: Verwenden von Sensor-API-Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba26e99ef039808ea8c3d6bee9ac8a5b0d6b1a231fb2a4b62c2bb05a2489099
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126500"
---
# <a name="using-sensor-api-events"></a>Verwenden von Sensor-API-Ereignissen

Die Sensor-API stellt Ereignisbenachrichtigungen über Rückrufschnittstellen bereit.

Um Ereignisbenachrichtigungen zu empfangen, muss Ihr Programm die erforderlichen COM-Rückrufschnittstellen implementieren. Um Ereignisse von Sensoren zu empfangen, müssen Sie [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents)implementieren. Um Ereignisse vom Sensor-Manager zu empfangen, müssen Sie [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents)implementieren.

Im folgenden Beispielcode wird eine Klasse erstellt, die [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents)implementiert.


```C++
class CMyEvents : public ISensorEvents
{
public:

    STDMETHODIMP QueryInterface(REFIID iid, void** ppv)
    {
        if (ppv == NULL)
        {
            return E_POINTER;
        }
        if (iid == __uuidof(IUnknown))
        {
            *ppv = static_cast<IUnknown*>(this);
        }
        else if (iid == __uuidof(ISensorEvents))
        {
            *ppv = static_cast<ISensorEvents*>(this);
        }
        else
        {
            *ppv = NULL;
            return E_NOINTERFACE;
        }
        AddRef();
        return S_OK;
    }

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef); 
    }

    STDMETHODIMP_(ULONG) Release()
    {
        ULONG count = InterlockedDecrement(&m_cRef);
        if (count == 0)
        {
            delete this;
            return 0;
        }
        return count;
    }

    //
    // ISensorEvents methods.
    //

    STDMETHODIMP OnEvent(
            ISensor *pSensor,
            REFGUID eventID,
            IPortableDeviceValues *pEventData)
    {
        HRESULT hr = S_OK;

        // Handle custom events here.

        return hr;
    }

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

    STDMETHODIMP OnLeave(
            REFSENSOR_ID sensorID)
    {
        HRESULT hr = S_OK;

        // Peform any housekeeping tasks for the sensor that is leaving.
        // For example, if you have maintained a reference to the sensor,
        // release it now and set the pointer to NULL.

        return hr;
    }

    STDMETHODIMP OnStateChanged(
            ISensor* pSensor,
            SensorState state)
    {
        HRESULT hr = S_OK;

        if(NULL == pSensor)
        {
            return E_INVALIDARG;
        }


        if(state == SENSOR_STATE_READY)
        {
            wprintf_s(L"\nTime sensor is now ready.");
        }
        else if(state == SENSOR_STATE_ACCESS_DENIED)
        {
            wprintf_s(L"\nNo permission for the time sensor.\n");
            wprintf_s(L"Enable the sensor in the control panel.\n");
        }
  

        return hr;
    }

    private:
        long m_cRef;

};

```



Nach der Implementierung der Rückrufschnittstelle können Sie einen bestimmten Sensor mit einem Zeiger auf eine Instanz Ihrer Rückrufklasse bereitstellen, um mit dem Empfangen von Ereignisbenachrichtigungen vom Sensor zu beginnen.

Der folgende Beispielcode erstellt eine Instanz der Rückrufklasse und fordert dann Ereignisinformationen von einem Sensor an.


```C++
CMyEvents* pEventClass = NULL;
ISensorEvents* pMyEvents = NULL;

if(SUCCEEDED(hr))
{
    // Create an instance of the event class.
    pEventClass = new(std::nothrow) CMyEvents();        
}

if(SUCCEEDED(hr))
{
    // Retrieve the pointer to the callback interface.
    hr = pEventClass->QueryInterface(IID_PPV_ARGS(&pMyEvents));
}

if(SUCCEEDED(hr))
{
    // Start receiving events.
    hr = pSensor->SetEventSink(pMyEvents);
} 

```



Sie können ähnlichen Code schreiben, um Ereignisse vom Sensor-Manager zu empfangen.

Der folgende Beispielcode zeigt, wie Ereignisbenachrichtigungen nicht mehr empfangen werden.


```C++
if(SUCCEEDED(hr))
{
    hr = pSensor->SetEventSink(NULL);
}
```



## <a name="requesting-a-report-interval"></a>Anfordern eines Berichtsintervalls

Sie können einen Wert dafür vorschlagen, wie oft Ihre Anwendung datenaktuelle Ereignisse empfängt. Sensoren sind jedoch nicht erforderlich, um Ereignisse in einem bestimmten Intervall bereitzustellen. Beachten Sie, dass Ihr vorgeschlagener Wert möglicherweise nicht mit dem tatsächlichen Berichtsintervall übereinstimmt, das der Sensor zum Auslösen von Ereignissen verwendet. Um das tatsächliche Berichtsintervall zu ermitteln, rufen Sie den Wert für die EIGENSCHAFT SENSOR \_ PROPERTY CURRENT REPORT INTERVAL \_ \_ \_ ab, wie unter Abrufen und Festlegen von [Sensoreigenschaften](setting-and-retrieving-sensor-properties.md)beschrieben.

Der folgende Beispielcode erstellt eine Hilfsfunktion, die einen neuen Wert für die EIGENSCHAFT SENSOR PROPERTY CURRENT REPORT INTERVAL anfordert. \_ \_ \_ \_ Die Funktion verwendet einen Zeiger auf den Sensor, für den die Eigenschaft festgelegt werden soll, und einen **ULONG-Wert,** der das neue Berichtsintervall angibt, das festgelegt werden soll.


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

[Informationen zu Sensor-API-Ereignissen](about-sensor-events.md)
</dt> </dl>

 

 



