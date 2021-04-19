---
description: Abrufen der von einem Gerät unterstützten Inhaltstypen
ms.assetid: 1cedb8d9-2476-420c-bab4-c8a032af781b
title: Abrufen der von einem Gerät unterstützten Inhaltstypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e1b37160065be3130fca687f5f3277d9108a6ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362838"
---
# <a name="retrieving-the-content-types-supported-by-a-device"></a>Abrufen der von einem Gerät unterstützten Inhaltstypen

Wie bereits im Thema [Abrufen der von einem Gerät unterstützten funktionalen Kategorien](retrieving-the-functional-categories-supported-by-a-device.md) beschrieben, unterstützen tragbare Windows-Geräte möglicherweise mindestens eine Funktions Kategorie. Eine bestimmte funktionale Kategorie unterstützt möglicherweise einen oder mehrere Inhaltstypen. Beispielsweise kann die Speicher Kategorie Inhaltstypen von Ordner, Audiodaten und Image unterstützen.

Eine Beschreibung der von WPD unterstützten Inhaltstypen finden Sie im Thema [**WPD \_ - \_ Inhaltstyp \_ alle**](wpd-content-type-all.md) .

Die listsupportedcontenttypes-Funktion im Modul devicecapabili. cpp veranschaulicht das Abrufen von Inhaltstypen für die funktionalen Kategorien, die von einem ausgewählten Gerät unterstützt werden.

Die Anwendung kann die von einem Gerät unterstützten funktionalen Kategorien mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen abrufen.



| Schnittstelle                                                                                      | BESCHREIBUNG                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**Iportabledebug-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Bietet Zugriff auf die Methoden zum Abrufen von funktionalen Kategorien. |
| [**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md) | Wird zum Auflisten und Speichern von funktionalen Kategorieinformationen verwendet.         |



 

Der in der listsupportedcontenttypes-Funktion gefundene Code ist nahezu identisch mit dem Code, der in der listfunctionalcategories-Funktion gefunden wurde. (Weitere Informationen finden Sie im Thema [Abrufen von funktionalen Kategorien, die von einem Gerät unterstützt werden](retrieving-the-functional-categories-supported-by-a-device.md) . Der einzige Unterschied besteht im Aufrufen der [**iportabledevicecapabili:: getsupportedcontenttypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) -Methode, die in der Schleife angezeigt wird, die die funktionalen Kategorien durchläuft.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories   = 0;

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
// We will use these categories to enumerate functional objects
// that fall within them.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}

// Get the number of functional categories found on the device.
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name and supported content types.
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

            if ((pv.puuid != NULL)      &&
                (pv.vt    == VT_CLSID))
            {
                // Display the functional category name
                printf("Functional Category: ");
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");

                // Display the content types supported for this category
                CComPtr<IPortableDevicePropVariantCollection> pContentTypes;
                hr = pCapabilities->GetSupportedContentTypes(*pv.puuid, &pContentTypes);
                if (SUCCEEDED(hr))
                {
                    printf("Supported Content Types: ");
                    DisplayContentTypes(pContentTypes);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get supported content types from the device, hr = 0x%lx\n",hr);
                }
            }
            else
            {
                printf("! Invalid functional category found\n");
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

 

 



