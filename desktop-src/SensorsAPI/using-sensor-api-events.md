---
description: Die Sensor-API stellt Ereignis Benachrichtigungen über Rückruf Schnittstellen bereit.
ms.assetid: 0c396d54-cb2e-4b07-999f-3f4001db2a02
title: Verwenden von Sensor-API-Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54fcb14138c1b20470a2b716e5cce86235c3102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960118"
---
# <a name="using-sensor-api-events"></a>Verwenden von Sensor-API-Ereignissen

Die Sensor-API stellt Ereignis Benachrichtigungen über Rückruf Schnittstellen bereit.

Um Ereignis Benachrichtigungen zu empfangen, muss das Programm die erforderlichen com-Rückruf Schnittstellen implementieren. Zum Empfangen von Ereignissen von Sensoren müssen Sie " [**isensorevents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents)" implementieren. Um Ereignisse vom Sensor-Manager zu empfangen, müssen Sie " [**isensormanagerevents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents)" implementieren.

Im folgenden Beispielcode wird eine Klasse erstellt, die " [**isenevents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents)" implementiert.


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



Nachdem Sie die Rückruf Schnittstelle implementiert haben, können Sie einen bestimmten Sensor mit einem Zeiger auf eine Instanz der Rückruf Klasse bereitstellen, um mit dem Empfang von Ereignis Benachrichtigungen vom Sensor zu beginnen.

Im folgenden Beispielcode wird eine Instanz der Rückruf Klasse erstellt und anschließend Ereignis Notierungen von einem Sensor angefordert.


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

Der folgende Beispielcode zeigt, wie der Empfang von Ereignis Benachrichtigungen beendet wird.


```C++
if(SUCCEEDED(hr))
{
    hr = pSensor->SetEventSink(NULL);
}
```



## <a name="requesting-a-report-interval"></a>Anfordern eines Berichts Intervalls

Sie können einen Wert vorschlagen, um zu erfahren, wie oft Ihre Anwendung Daten aktualisierte Ereignisse empfängt. Es ist jedoch nicht erforderlich, dass Sensoren in einem bestimmten Intervall Ereignisse bereitstellen. Sie sollten sich bewusst sein, dass der vorgeschlagene Wert möglicherweise nicht mit dem tatsächlichen Berichts Intervall identisch ist, das vom Sensor verwendet wird, um Ereignisse zu Um das tatsächliche Berichts Intervall zu ermitteln, rufen Sie den Wert für \_ die \_ Eigenschaft des aktuellen \_ Berichts Intervalls der Sensor Eigenschaft \_ ab, wie unter [Abrufen und Festlegen von Sensor Eigenschaften](setting-and-retrieving-sensor-properties.md)beschrieben.

Der folgende Beispielcode erstellt eine Hilfsfunktion, die einen neuen Wert für die \_ \_ aktuelle \_ Berichts \_ Intervall Eigenschaft der Sensor Eigenschaft anfordert. Die-Funktion nimmt einen Zeiger auf den Sensor, für den die-Eigenschaft festgelegt werden soll, und einen **ulong** -Wert, der das neue Berichts Intervall angibt, das festgelegt werden soll.


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

 

 



