---
description: Abrufen der von einem Gerät unterstützten Inhaltstypen
ms.assetid: 1cedb8d9-2476-420c-bab4-c8a032af781b
title: Abrufen der von einem Gerät unterstützten Inhaltstypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f85366374ec28ed44664a3b86edbee1e046e1a5ee4e331dbe041398bdc48a9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083464"
---
# <a name="retrieving-the-content-types-supported-by-a-device"></a>Abrufen der von einem Gerät unterstützten Inhaltstypen

Wie im Thema [Abrufen der von einem Gerät unterstützten Funktionskategorien](retrieving-the-functional-categories-supported-by-a-device.md) beschrieben, unterstützen Windows Portable Devices möglicherweise eine oder mehrere Funktionskategorien. Jede bestimmte Funktionskategorie unterstützt möglicherweise einen oder mehrere Inhaltstypen. Beispielsweise kann die Speicherkategorie Inhaltstypen von Ordnern, Audiodateien und Bildern unterstützen.

Eine Beschreibung der von WPD unterstützten Inhaltstypen finden Sie im Thema [**WPD \_ CONTENT TYPE \_ \_ ALL.**](wpd-content-type-all.md)

Die ListSupportedContentTypes-Funktion im Modul DeviceCapabilities.cpp veranschaulicht das Abrufen von Inhaltstypen für die Funktionskategorien, die von einem ausgewählten Gerät unterstützt werden.

Ihre Anwendung kann die von einem Gerät unterstützten Funktionskategorien mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen abrufen.



| Schnittstelle                                                                                      | BESCHREIBUNG                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**IPortableDeviceCapabilities-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Ermöglicht den Zugriff auf die Abrufmethoden der Funktionskategorie. |
| [**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md) | Wird zum Aufzählen und Speichern von Funktionskategoriedaten verwendet.         |



 

Der In der ListSupportedContentTypes-Funktion gefundene Code ist fast identisch mit dem Code in der ListFunctionalCategories-Funktion. (Weitere Informationen finden Sie im Thema [Abrufen von funktionalen Kategorien,](retrieving-the-functional-categories-supported-by-a-device.md) die von einem Gerät unterstützt werden.) Der einzige Unterschied ist der Aufruf der [**IPortableDeviceCapabilities::GetSupportedContentTypes-Methode,**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) die innerhalb der Schleife angezeigt wird, die die Funktionskategorien durchläuft.


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

[**IPortableDevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceCapabilities-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



