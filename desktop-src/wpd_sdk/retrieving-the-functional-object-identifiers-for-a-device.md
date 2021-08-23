---
description: Abrufen der funktionalen Objektbezeichner für ein Gerät
ms.assetid: 9a13071a-95a1-4330-92d5-11fa72a8f211
title: Abrufen der funktionalen Objektbezeichner für ein Gerät
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d0cc686a6997c10e26e3d83190503bba09fe15afc7f4e0cf75e297f0d905f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119263000"
---
# <a name="retrieving-the-functional-object-identifiers-for-a-device"></a>Abrufen der funktionalen Objektbezeichner für ein Gerät

Wie im Thema [Abrufen](retrieving-the-functional-categories-supported-by-a-device.md) der von einem Gerät unterstützten funktionalen Kategorien erwähnt, unterstützt Windows portable Geräte möglicherweise mindestens eine Funktionale Kategorie. Jede funktionstüchtige Kategorie kann ein oder mehrere funktionale Objekte unterstützen. Beispielsweise kann die Speicherkategorie drei funktionale Speicherobjekte unterstützen, von denen jedes durch eine eindeutige Bezeichnerzeichenfolge identifiziert wird. Das erste Speicherobjekt kann dann durch die Zeichenfolge "Storage1", das zweite durch die Zeichenfolge "Storage2" und das dritte durch die Zeichenfolge "Storage3" identifiziert werden.

Die ListFunctionalObjects-Funktion im DeviceCapabilities.cpp-Modul veranschaulicht das Abrufen von Inhaltstypen für die funktionskategorien, die von einem ausgewählten Gerät unterstützt werden.

Ihre Anwendung kann die von einem Gerät unterstützten Funktionalen Kategorien mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen abrufen.



| Schnittstelle                                                                                      | BESCHREIBUNG                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**IPortableDeviceCapabilities-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Ermöglicht den Zugriff auf die Funktionskategorieabrufmethoden. |
| [**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md) | Wird zum Aufzählen und Speichern von Daten der Funktionalen Kategorie verwendet.         |



 

Der code in der ListFunctionalObjects-Funktion ist fast identisch mit dem Code in der ListFunctionalCategories-Funktion. (Weitere Informationen finden Sie im Thema Abrufen von [funktionstüchtigen Kategorien, die von einem Gerät unterstützt](retrieving-the-functional-categories-supported-by-a-device.md) werden.) Der einzige Unterschied besteht im Aufruf der [**IPortableDeviceCapabilities::GetFunctionalObjects-Methode,**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) die innerhalb der Schleife angezeigt wird, die die funktionalen Kategorien durch iteriert.


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

[**IPortableDevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceCapabilities-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



