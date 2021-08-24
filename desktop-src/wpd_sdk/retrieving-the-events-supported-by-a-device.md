---
description: Abrufen der von einem Gerät unterstützten Ereignisse
ms.assetid: 951b300f-03de-4a3d-9356-e3a7b5b17fdb
title: Abrufen der von einem Gerät unterstützten Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e0e24b5a4424d03c916ca73fd0192f9b6de0a80b6a2e2e67a129deb832f7bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119263120"
---
# <a name="retrieving-the-events-supported-by-a-device"></a>Abrufen der von einem Gerät unterstützten Ereignisse

Einige WPD-Treiber unterstützen Ereignisbenachrichtigungen. Dies bedeutet, dass sich eine Anwendung beim Treiber registrieren kann, um eine Benachrichtigung zu erhalten, wenn eine bestimmte Aktion auftritt. Beispielsweise kann sich eine Anwendung registrieren, um eine Benachrichtigung zu erhalten, wenn ein Objekt hinzugefügt oder entfernt wird.

Es gibt zehn vordefinierte Ereignisse, die eine Anwendung überwachen kann. Diese werden in der folgenden Tabelle beschrieben.



| Ereignis                       | BESCHREIBUNG                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Gerätefunktionen aktualisiert | Tritt ein, wenn sich die Gerätefunktionen geändert haben.                                                                                      |
| Gerät entfernt              | Tritt ein, wenn das Gerät nicht angeschlossen ist.                                                                                                   |
| Gerät zurücksetzen                | Tritt ein, wenn das Gerät zurückgesetzt wurde.                                                                                                 |
| Objekt hinzugefügt                | Tritt ein, nachdem ein neues -Objekt auf dem Gerät verfügbar wird.                                                                             |
| Objekt entfernt              | Tritt ein, nachdem ein Objekt vom Gerät entfernt wurde.                                                                               |
| Objektübertragung angefordert   | Gibt an, dass eine Anforderung zum Übertragen eines Objekts gestellt wurde.                                                                          |
| Objekt aktualisiert              | Tritt ein, nachdem entweder ein Objekt oder dessen untere Objekte aktualisiert wurden. (Verbundene Clients sollten dann ihre Ansicht des angegebenen Objekts aktualisieren.) |
| Storage in Bearbeitung  | Tritt auf, wenn der Gerätespeicher formatiert wird.                                                                                     |



 

Eine Liste der Konstanten, die diesen Ereignissen zugeordnet sind, finden Sie im [Thema Ereigniskonst](event-constants.md) konstanten.

Die ListSupportedEvents-Funktion im DeviceCapabilities.cpp-Modul veranschaulicht das Abrufen von Ereignissen, die von einem bestimmten Gerät unterstützt werden.

Ihre Anwendung kann die Bezeichner für Ereignisse abrufen, die von einem Gerät mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen unterstützt werden.



| Schnittstelle                                                                                      | BESCHREIBUNG                                               |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [**IPortableDeviceCapabilities-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Bietet Zugriff auf die unterstützten Ereignisabrufmethoden. |
| [**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md) | Wird zum Aufzählen und Speichern von Daten der Funktionalen Kategorie verwendet.     |



 

Die erste Aufgabe, die von der Beispielanwendung ausgeführt wird, ist das Abrufen eines [**IPortableDeviceCapabilities-Objekts,**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) das zum Abrufen der vom angegebenen Gerät unterstützten Ereignisse verwendet wird.


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



Die unterstützten Ereignisse werden durch Aufrufen der [**IPortableDeviceCapabilities::GetSupportedEvents-Methode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) abgerufen. Diese Methode ruft eine Auflistung von Ereignisbezeichnern für das gegebene Gerät ab und speichert sie in einem [**IPortableDevicePropVariantCollection-Objekt,**](iportabledevicepropvariantcollection.md) auf das das pEvents-Argument verweist.


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



Der nächste Schritt besteht im Abrufen der Anzahl der unterstützten Ereignisse, damit die Anwendung das [**IPortableDevicePropVariantCollection-Objekt**](iportabledevicepropvariantcollection.md) durch iterieren und den Bezeichner für die einzelnen Ereignisse abrufen kann.


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

[**Ereigniskonst constants**](event-constants.md)
</dt> <dt>

[**IPortableDevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceCapabilities-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



