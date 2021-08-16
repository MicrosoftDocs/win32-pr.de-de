---
description: Abrufen der von einem Gerät unterstützten Funktionalen Kategorien
ms.assetid: 7748e111-9987-4685-8fc8-10c5d4631080
title: Abrufen der von einem Gerät unterstützten Funktionalen Kategorien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d410788616cc20563b914a293afcd8e2bbbd87099f738ae21463d2092c620597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842692"
---
# <a name="retrieving-the-functional-categories-supported-by-a-device"></a>Abrufen der von einem Gerät unterstützten Funktionalen Kategorien

Windows Portable Geräte können eine oder mehrere Funktionskategorien unterstützen. Diese Kategorien werden in der folgenden Tabelle beschrieben.



| Kategorie                    | Beschreibung                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------|
| Audioaufnahme               | Das Gerät kann zum Aufzeichnen von Audiodaten verwendet werden.                                              |
| Renderinginformationen       | Das Gerät stellt Daten zur Beschreibung der Mediendateien zur Auswahl, die gerendert werden können. |
| Kurznachrichtendienst (SMS) | Das Gerät unterstützt SMS.                                                  |
| Still Image Capture         | Das Gerät kann verwendet werden, um Noch-Bilder zu erfassen.                                      |
| Storage                     | Das Gerät kann zum Speichern von Dateien verwendet werden.                                               |



 

Die Funktion ListFunctionalCategories im Modul DeviceCapabilities.cpp veranschaulicht das Abrufen von Funktionskategorien für ein ausgewähltes Gerät.

Ihre Anwendung kann die von einem Gerät unterstützten Funktionskategorien mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen abrufen.



| Schnittstelle                                                                                      | Beschreibung                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**IPortableDeviceCapabilities-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Ermöglicht den Zugriff auf die Funktionskategorieabrufmethoden. |
| [**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md) | Wird zum Aufzählen und Speichern von Daten der Funktionalen Kategorie verwendet.         |



 

Die erste Aufgabe, die von der Beispielanwendung ausgeführt wird, ist das Abrufen eines [**IPortableDeviceCapabilities-Objekts,**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) das zum Abrufen der Funktionskategorien auf dem ausgewählten Gerät verwendet wird.


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



Die abgerufenen Kategorien werden in einem [**IPortableDevicePropVariantCollection-Objekt**](iportabledevicepropvariantcollection.md) gespeichert.

Der nächste Schritt ist die Enumeration und Anzeige der unterstützten Kategorien. Der erste Schritt der Beispielanwendung besteht im Abrufen der Anzahl der unterstützten Kategorien. Anschließend wird diese Anzahl verwendet, um das [**IPortableDevicePropVariantCollection-Objekt**](iportabledevicepropvariantcollection.md) zu iterieren, das die unterstützten Kategorien enthält.


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

[**IPortableDevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceCapabilities-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



