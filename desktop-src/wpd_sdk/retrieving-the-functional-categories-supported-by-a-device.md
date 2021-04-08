---
description: Abrufen der von einem Gerät unterstützten funktionalen Kategorien
ms.assetid: 7748e111-9987-4685-8fc8-10c5d4631080
title: Abrufen der von einem Gerät unterstützten funktionalen Kategorien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6514c6255fa089dc235b5edd8a25b5ef581aee84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866743"
---
# <a name="retrieving-the-functional-categories-supported-by-a-device"></a>Abrufen der von einem Gerät unterstützten funktionalen Kategorien

Tragbare Windows-Geräte unterstützen möglicherweise mindestens eine Funktions Kategorie. Diese Kategorien werden in der folgenden Tabelle beschrieben.



| Category                    | BESCHREIBUNG                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------|
| Audioerfassung               | Das Gerät kann verwendet werden, um Audiodaten aufzuzeichnen.                                              |
| Renderinginformationen       | Das Gerät stellt Daten bereit, die die Mediendateien beschreiben, die Sie Rendern können. |
| SMS (Short Message Service) | Das Gerät unterstützt Textnachrichten.                                                  |
| Trotzdem Image Erfassung         | Das Gerät kann zum Erfassen von Images verwendet werden.                                      |
| Storage                     | Das Gerät kann zum Speichern von Dateien verwendet werden.                                               |



 

Die listfunctionalcategories-Funktion im Modul devicecapabili. cpp veranschaulicht das Abrufen von funktionalen Kategorien für ein ausgewähltes Gerät.

Die Anwendung kann die von einem Gerät unterstützten funktionalen Kategorien mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen abrufen.



| Schnittstelle                                                                                      | BESCHREIBUNG                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**Iportabledebug-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Bietet Zugriff auf die Methoden zum Abrufen von funktionalen Kategorien. |
| [**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md) | Wird zum Auflisten und Speichern von funktionalen Kategorieinformationen verwendet.         |



 

Die erste Aufgabe, die von der Beispielanwendung durchgeführt wird, ist das Abrufen eines [**iportabledevicecapabili-**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) Objekts, das verwendet wird, um die funktionalen Kategorien auf dem ausgewählten Gerät abzurufen.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories = 0;

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

// Get all functional categories supported by the device.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}
```



Die abgerufenen Kategorien werden in einem [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Objekt gespeichert.

Der nächste Schritt besteht aus der Enumeration und der Anzeige der unterstützten Kategorien. Der erste Schritt, den die Beispielanwendung erreicht, ist das Abrufen der Anzahl unterstützter Kategorien. Diese Anzahl wird dann verwendet, um das [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Objekt zu durchlaufen, das die unterstützten Kategorien enthält.


```C++
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumCategories; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pCategories->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have a functional category.  It is assumed that
            // functional categories are returned as VT_CLSID
            // VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the functional category name
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iportabledevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Iportabledebug-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



