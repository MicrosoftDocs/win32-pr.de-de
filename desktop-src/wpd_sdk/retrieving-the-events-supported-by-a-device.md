---
description: Abrufen der von einem Gerät unterstützten Ereignisse
ms.assetid: 951b300f-03de-4a3d-9356-e3a7b5b17fdb
title: Abrufen der von einem Gerät unterstützten Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a542a34d0938c7e2ff86118818714f18b1224f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530251"
---
# <a name="retrieving-the-events-supported-by-a-device"></a>Abrufen der von einem Gerät unterstützten Ereignisse

Einige WPD-Treiber unterstützen die Ereignis Benachrichtigung. Dies bedeutet, dass eine Anwendung beim Treiber registriert werden kann, um eine Benachrichtigung zu erhalten, wenn eine bestimmte Aktion erfolgt. Beispielsweise kann eine Anwendung registrieren, um eine Benachrichtigung zu erhalten, wenn ein Objekt hinzugefügt oder entfernt wird.

Es gibt zehn vordefinierte Ereignisse, die eine Anwendung überwachen kann. Diese werden in der folgenden Tabelle beschrieben.



| Ereignis                       | BESCHREIBUNG                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Gerätefunktionen aktualisiert | Tritt auf, wenn sich die Gerätefunktionen geändert haben.                                                                                      |
| Gerät entfernt              | Tritt auf, wenn das Gerät getrennt ist.                                                                                                   |
| Gerät zurücksetzen                | Tritt auf, wenn das Gerät zurückgesetzt wurde.                                                                                                 |
| Objekt hinzugefügt                | Tritt auf, nachdem ein neues-Objekt auf dem Gerät verfügbar ist.                                                                             |
| Objekt entfernt              | Tritt auf, nachdem ein Objekt vom Gerät entfernt wurde.                                                                               |
| Objekt Übertragung angefordert   | Gibt an, dass für die Übertragung eines Objekts eine Anforderung durchgeführt wurde.                                                                          |
| Objekt aktualisiert              | Tritt auf, nachdem entweder ein-Objekt oder seine untergeordneten Elemente aktualisiert wurden. (Verbundene Clients sollten dann Ihre Ansicht des angegebenen Objekts aktualisieren.) |
| Speicherformat wird ausgeführt  | Tritt auf, wenn der Gerätespeicher formatiert wird.                                                                                     |



 

Eine Liste der Konstanten, die diesen Ereignissen zugeordnet sind, finden Sie im Thema [Ereignis Konstanten](event-constants.md) .

Die "listsupportedevents"-Funktion im Modul "devicecapabili. cpp" veranschaulicht das Abrufen von Ereignissen, die von einem bestimmten Gerät unterstützt werden.

Die Anwendung kann die Bezeichner für Ereignisse abrufen, die von einem Gerät unterstützt werden, und zwar mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen.



| Schnittstelle                                                                                      | BESCHREIBUNG                                               |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [**Iportabledebug-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Bietet Zugriff auf die unterstützten Ereignis Abruf Methoden. |
| [**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md) | Wird zum Auflisten und Speichern von funktionalen Kategorieinformationen verwendet.     |



 

Die erste Aufgabe, die von der Beispielanwendung durchgeführt wird, ist das Abrufen eines [**iportabledevicecapabili-**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) Objekts, das verwendet wird, um die vom jeweiligen Gerät unterstützten Ereignisse abzurufen.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pEvents;
DWORD dwNumEvents = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}


// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}
```



Die unterstützten Ereignisse werden durch Aufrufen der [**iportabledevicecapabili:: getsupportedevents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) -Methode abgerufen. Diese Methode ruft eine Auflistung der Ereignis Bezeichner für das angegebene Gerät ab und speichert Sie in einem [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Objekt, auf das durch das Peer Vents-Argument verwiesen wird.


```C++
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetSupportedEvents(&pEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get supported events from the device, hr = 0x%lx\n",hr);
    }
}
```



Der nächste Schritt besteht darin, die Anzahl der unterstützten Ereignisse abzurufen, sodass die Anwendung das [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Objekt durchlaufen und den Bezeichner für jede abrufen kann.


```C++
if (SUCCEEDED(hr))
{
    hr = pEvents->GetCount(&dwNumEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Supported Events Found on the device\n\n", dwNumEvents);

// Loop through each event and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumEvents; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pEvents->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have an event.  It is assumed that
            // events are returned as VT_CLSID VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the event name
                DisplayEvent(*pv.puuid);
                printf("\n");
                // Display the event options
                DisplayEventOptions(pCapabilities, *pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ereignis Konstanten**](event-constants.md)
</dt> <dt>

[**Iportabledevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Iportabledebug-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



