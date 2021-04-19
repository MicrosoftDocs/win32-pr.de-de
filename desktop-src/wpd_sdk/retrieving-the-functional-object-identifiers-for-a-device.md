---
description: Abrufen der funktionalen Objekt Bezeichner für ein Gerät
ms.assetid: 9a13071a-95a1-4330-92d5-11fa72a8f211
title: Abrufen der funktionalen Objekt Bezeichner für ein Gerät
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a753324e24a6b78625a78b4128380288b6672f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350322"
---
# <a name="retrieving-the-functional-object-identifiers-for-a-device"></a>Abrufen der funktionalen Objekt Bezeichner für ein Gerät

Wie bereits im Thema [Abrufen der von einem Gerät unterstützten funktionalen Kategorien](retrieving-the-functional-categories-supported-by-a-device.md) beschrieben, unterstützen tragbare Windows-Geräte möglicherweise mindestens eine Funktions Kategorie. Eine bestimmte funktionale Kategorie unterstützt möglicherweise ein oder mehrere funktionale Objekte. Beispielsweise kann die Speicher Kategorie drei funktionale Speicher Objekte unterstützen, die jeweils durch eine eindeutige Bezeichnerzeichenfolge identifiziert werden. Das erste Speicher Objekt kann dann durch die Zeichenfolge "Storage1", die zweite durch die Zeichenfolge "Storage2" und das dritte durch die Zeichenfolge "Storage3" identifiziert werden.

Die listfunctionalobjects-Funktion im Modul devicecapabili. cpp veranschaulicht das Abrufen von Inhaltstypen für die Funktions Kategorien, die von einem ausgewählten Gerät unterstützt werden.

Die Anwendung kann die von einem Gerät unterstützten funktionalen Kategorien mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen abrufen.



| Schnittstelle                                                                                      | BESCHREIBUNG                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**Iportabledebug-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Bietet Zugriff auf die Methoden zum Abrufen von funktionalen Kategorien. |
| [**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md) | Wird zum Auflisten und Speichern von funktionalen Kategorieinformationen verwendet.         |



 

Der in der listfunctionalobjects-Funktion gefundene Code ist nahezu identisch mit dem Code in der listfunctionalcategories-Funktion. (Weitere Informationen finden Sie im Thema [Abrufen von funktionalen Kategorien, die von einem Gerät unterstützt werden](retrieving-the-functional-categories-supported-by-a-device.md) . Der einzige Unterschied besteht im Aufrufen der [**iportabledevicecapabili:: getfunctionalobjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) -Methode, die in der Schleife angezeigt wird, die die funktionalen Kategorien durchläuft.


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

// Loop through each functional category and get the list of
// functional object identifiers associated with a particular
// category.
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

                // Display the object identifiers for all
                // functional objects within this category
                CComPtr<IPortableDevicePropVariantCollection> pFunctionalObjectIds;
                hr = pCapabilities->GetFunctionalObjects(*pv.puuid, &pFunctionalObjectIds);
                if (SUCCEEDED(hr))
                {
                    printf("Functional Objects: ");
                    DisplayFunctionalObjectIDs(pFunctionalObjectIds);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
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

 

 



