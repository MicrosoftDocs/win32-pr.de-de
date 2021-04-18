---
description: Abrufen eines Objekt Bezeichners aus einem persistenten eindeutigen Bezeichner
ms.assetid: 146f8943-d4e1-4b87-a812-e534082a4f14
title: Abrufen einer Objekt-ID aus einer permanenten eindeutigen ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f997f0faf586a374e5a83c6f96b6508f02eb41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368924"
---
# <a name="retrieving-an-object-id-from-a-persistent-unique-id"></a>Abrufen einer Objekt-ID aus einer permanenten eindeutigen ID

Objekt Bezeichner sind nur für eine bestimmte Geräte Sitzung eindeutig. Wenn der Benutzer eine neue Verbindung herstellt, Stimmen Bezeichner aus einer vorherigen Sitzung möglicherweise nicht mit den Bezeichners für die aktuelle Sitzung ab. Um dieses Problem zu beheben, unterstützt die WPD-API persistente eindeutige Bezeichner (PUIDs), die über Geräte Sitzungen hinweg beibehalten werden.

Einige Geräte speichern Ihre PUIDs nativ mit einem bestimmten Objekt. Andere Benutzer können die PUID basierend auf einem Hash ausgewählter Objektdaten generieren. Andere können Objekt Bezeichner als PUIDs behandeln (da Sie sicherstellen können, dass diese Bezeichner niemals geändert werden).

Die getobjectidentifierfrompersistentuniqueidentifier-Funktion im Modul contentproperties. cpp veranschaulicht das Abrufen eines Objekt Bezeichners für eine bestimmte PUID.

Die Anwendung kann einen Objekt Bezeichner für eine entsprechende PUID mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen abrufen.



| Schnittstelle                                                                                      | BESCHREIBUNG                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**Iportabledevicecontent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Bietet Zugriff auf die Abruf Methode.                                                            |
| [**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md) | Wird verwendet, um den Objekt Bezeichner und den entsprechenden permanenten eindeutigen Bezeichner (PUID) zu speichern. |



 

Die erste Aufgabe, die von der Beispielanwendung erreicht wird, ist das Abrufen einer PUID vom Benutzer.


```C++
// Prompt user to enter an unique identifier to convert to an object idenifier.
printf("Enter the Persistant Unique Identifier of the object you wish to convert into an object identifier.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid persistent object identifier was specified, aborting the query operation\n");
}
```



Danach ruft die Beispielanwendung ein [**iportabledevicecontent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) -Objekt ab, das verwendet wird, um die [**getobjectidsfrompersistentuniqueids**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) -Methode aufzurufen.


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



Anschließend wird ein [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Objekt erstellt, das die vom Benutzer bereitgestellte PUID enthält.


```C++
hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPersistentUniqueIDs));
```



Nachdem die vorangegangenen drei Schritte ausgeführt wurden, ist das Beispiel bereit, um den Objekt Bezeichner abzurufen, der mit der vom Benutzer bereitgestellten PUID übereinstimmt. Dies wird erreicht, indem die [**iportabledevicecontent:: getobjectidsfrompersistentuniqueids**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) -Methode aufgerufen wird. Vor dem Aufrufen dieser Methode wird im Beispiel eine PROPVARIANT-Struktur initialisiert, die vom Benutzer bereitgestellte PUID in diese Struktur geschrieben und dem iportabledevicepropvariantcollection-Objekt hinzugefügt, bei dem ppersistentuniqueids zeigt. Dieser Zeiger wird als erstes Argument an die getobjectidsfrompersistentuniqueids-Methode übermittelt. Das zweite Argument von getobjectidsfrompersistentuniqueids ist ein iportabledevicepropvariantcollection-Objekt, das den übereinstimmenden Objekt Bezeichner empfängt.


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

[**Iportabledevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Iportabledevicecontent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



