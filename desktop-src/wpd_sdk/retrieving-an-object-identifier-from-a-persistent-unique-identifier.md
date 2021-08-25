---
description: Abrufen eines Objektbezeichners aus einem persistenten eindeutigen Bezeichner
ms.assetid: 146f8943-d4e1-4b87-a812-e534082a4f14
title: Abrufen einer Objekt-ID aus einer persistenten eindeutigen ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d4f08d496c7c03101602c945e6c27e7a2624fe84957eda932ead806f964d3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054770"
---
# <a name="retrieving-an-object-id-from-a-persistent-unique-id"></a>Abrufen einer Objekt-ID aus einer persistenten eindeutigen ID

Objektbezeichner sind nur für eine bestimmte Gerätesitzung eindeutig. Wenn der Benutzer eine neue Verbindung ein richtet, können Bezeichner aus einer vorherigen Sitzung möglicherweise nicht mit Bezeichnern für die aktuelle Sitzung übereinstimmen. Um dieses Problem zu beheben, unterstützt die WPD-API persistente eindeutige Bezeichner (PERSISTENT UNIQUE Identifier, PUIDs), die über Gerätesitzungen hinweg beibehalten werden.

Einige Geräte speichern ihre PUIDs nativ mit einem bestimmten Objekt. Andere können die PUID basierend auf einem Hash der ausgewählten Objektdaten generieren. Andere können Objektbezeichner als PUIDs behandeln (da sie garantieren können, dass sich diese Bezeichner nie ändern).

Die GetObjectIdentifierFromPersistentUniqueIdentifier-Funktion im ContentProperties.cpp-Modul veranschaulicht das Abrufen eines Objektbezeichners für eine bestimmte PUID.

Ihre Anwendung kann einen Objektbezeichner für eine entsprechende PUID mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen abrufen.



| Schnittstelle                                                                                      | BESCHREIBUNG                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**IPortableDeviceContent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Ermöglicht den Zugriff auf die Abrufmethode.                                                            |
| [**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md) | Wird verwendet, um sowohl den Objektbezeichner als auch den entsprechenden persistenten eindeutigen Bezeichner (PUID) zu speichern. |



 

Die erste Aufgabe, die die Beispielanwendung erfüllt, besteht darin, eine PUID vom Benutzer zu erhalten.


```C++
// Prompt user to enter an unique identifier to convert to an object idenifier.
printf("Enter the Persistant Unique Identifier of the object you wish to convert into an object identifier.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid persistent object identifier was specified, aborting the query operation\n");
}
```



Anschließend ruft die Beispielanwendung ein [**IPortableDeviceContent-Objekt**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) ab, mit dem die [**GetObjectIDsFromPersistentUniqueIDs-Methode aufgerufen**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) wird.


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



Als Nächstes wird ein [**IPortableDevicePropVariantCollection-Objekt**](iportabledevicepropvariantcollection.md) erstellt, das die vom Benutzer bereitgestellte PUID enthält.


```C++
hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPersistentUniqueIDs));
```



Sobald die vorherigen drei Schritte erfolgt sind, kann das Beispiel den Objektbezeichner abrufen, der der vom Benutzer bereitgestellten PUID entspricht. Dies wird durch Aufrufen der [**IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs-Methode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) erreicht. Vor dem Aufrufen dieser Methode initialisiert das Beispiel eine PROPVARIANT-Struktur, schreibt die vom Benutzer bereitgestellte PUID in diese Struktur und fügt sie dem IPortableDevicePropVariantCollection-Objekt hinzu, auf das pPersistentUniqueIDs zeigt. Dieser Zeiger wird als erstes Argument an die GetObjectIDsFromPersistentUniqueIDs-Methode übergeben. Das zweite Argument von GetObjectIDsFromPersistentUniqueIDs ist ein IPortableDevicePropVariantCollection-Objekt, das den übereinstimmenden Objektbezeichner empfängt.


```C++
if (SUCCEEDED(hr))
{
    if (pPersistentUniqueIDs != NULL)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);

        // Initialize a PROPVARIANT structure with the object identifier string
        // that the user selected above. Notice we are allocating memory for the
        // PWSTR value.  This memory will be freed when PropVariantClear() is
        // called below.
        pv.vt      = VT_LPWSTR;
        pv.pwszVal = AtlAllocTaskWideString(szSelection);
        if (pv.pwszVal != NULL)
        {
            // Add the object identifier to the objects-to-delete list
            // (We are only deleting 1 in this example)
            hr = pPersistentUniqueIDs->Add(&pv);
            if (SUCCEEDED(hr))
            {
                // 3) Attempt to get the unique idenifier for the object from the device
                hr = pContent->GetObjectIDsFromPersistentUniqueIDs(pPersistentUniqueIDs,
                                                                   &pObjectIDs);
                if (SUCCEEDED(hr))
                {
                    PROPVARIANT pvId = {0};
                    hr = pObjectIDs->GetAt(0, &pvId);
                    if (SUCCEEDED(hr))
                    {
                        printf("The persistent unique identifier '%ws' relates to object identifier '%ws' on the device.\n", szSelection, pvId.pwszVal);
                    }
                    else
                    {
                        printf("! Failed to get the object identifier for '%ws' from the IPortableDevicePropVariantCollection, hr = 0x%lx\n",szSelection, hr);
                    }

                    // Free the returned allocated string from the GetAt() call
                    PropVariantClear(&pvId);
                }
                else
                {
                    printf("! Failed to get the object identifier from persistent object idenifier '%ws', hr = 0x%lx\n",szSelection, hr);
                }
            }
            else
            {
                printf("! Failed to get the object identifier from persistent object idenifier because we could no add the persistent object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
            printf("! Failed to get the object identifier because we could no allocate memory for the persistent object identifier string, hr = 0x%lx\n",hr);
        }

        // Free any allocated values in the PROPVARIANT before exiting
        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPortableDevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



