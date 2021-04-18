---
description: Auflisten von Inhalten
ms.assetid: 86782a09-4fca-4ae0-beaf-296069e061dc
title: Auflisten von Inhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2e724b451d714516c4723edcd56936b71e4e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347150"
---
# <a name="enumerating-content"></a>Auflisten von Inhalten

Der Inhalt eines Geräts (unabhängig davon, ob es sich um einen Ordner, ein Telefonbuch, ein Video oder ein Image handelt) wird in der WPD-API als Objekt bezeichnet. Auf diese Objekte wird von Objekt bezeichmern verwiesen, die von-Eigenschaften beschrieben werden. Sie können die Objekte auf einem Gerät auflisten, indem Sie Methoden in der [**iportabledevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), der [**iportabledevicecontent-Schnitt**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)Stelle und der [**ienumportabledeviceobjectids**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)-Schnittstelle aufrufen.

Die Beispielanwendung veranschaulicht die inhaltsenumeration in der enumerateallcontent-Funktion, die im Modul "contentenumeration. cpp" zu finden ist. Diese Funktion ruft wiederum eine rekursiveenumerate-Funktion auf, die die Hierarchie von Objekten durchläuft, die auf dem ausgewählten Gerät gefunden wurden, und gibt für jedes Objekt einen Objekt Bezeichner zurück.

Wie bereits erwähnt, ruft die recursiveenumerate-Funktion einen Objekt Bezeichner für jedes Objekt ab, das auf dem Gerät gefunden wurde. Der Objekt Bezeichner ist ein Zeichen folgen Wert. Nachdem Ihre Anwendung diesen Bezeichner abgerufen hat, kann er weitere beschreibende Objektinformationen abrufen (z. b. den Namen des Objekts, den Bezeichner für das übergeordnete Objekt des Objekts usw.). Diese beschreibenden Informationen werden als Objekteigenschaften (oder Metadaten) bezeichnet. Die Anwendung kann diese Eigenschaften abrufen, indem Sie Member der [**iportabledeviceproperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)aufrufen.

Die enumerateallcontent-Funktion beginnt mit dem Abrufen eines Zeigers auf eine [**iportabledevicecontent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent). Dieser Zeiger wird durch Aufrufen der [**iportabledevice:: Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) -Methode abgerufen.


```C++
void EnumerateAllContent(
    IPortableDevice* pDevice)
{
    HRESULT                         hr = S_OK;
    CComPtr<IPortableDeviceContent> pContent;

    if (pDevice == NULL)
    {
        printf("! A NULL IPortableDevice interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent interface from the IPortableDevice interface to
    // access the content-specific methods.
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



Nachdem der Zeiger auf die iportabledevicecontent-Schnittstelle abgerufen wurde, ruft die enumerateallcontent-Funktion die recursiveenumerate-Funktion auf, die die Hierarchie von Objekten durchläuft, die auf dem angegebenen Gerät gefunden wurden, und gibt jeweils einen Objekt Bezeichner zurück.

Die recursiveenumerate-Funktion beginnt mit dem Abrufen eines Zeigers auf eine [**ienumportabledeviceobjectids-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids). Diese Schnittstelle macht die Methoden verfügbar, die eine Anwendung verwendet, um in der Liste der auf einem bestimmten Gerät gefundenen Objekte zu navigieren.

In diesem Beispiel ruft die recursiveenumerate-Funktion die [**ienumportabledeviceobjectids:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) -Methode auf, um die Liste der-Objekte zu durchlaufen.

Jeder Aufrufen der [**ienumportabledeviceobjects:: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) -Methode fordert einen Batch von 10 bezeichern an. (Dieser Wert wird durch den num \_ angegeben. Objekte \_ zum \_ Anfordern einer Konstante, die als erstes Argument bereitgestellt wird.)


```C++
#define NUM_OBJECTS_TO_REQUEST  10

// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                  pszObjectID,
    IPortableDeviceContent* pContent)
{
    CComPtr<IEnumPortableDeviceObjectIDs> pEnumObjectIDs;

    // Print the object identifier being used as the parent during enumeration.
    printf("%ws\n",pszObjectID);

    // Get an IEnumPortableDeviceObjectIDs interface by calling EnumObjects with the
    // specified parent object identifier.
    HRESULT hr = pContent->EnumObjects(0,               // Flags are unused
                                       pszObjectID,     // Starting from the passed in object
                                       NULL,            // Filter is unused
                                       &pEnumObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }

    // Loop calling Next() while S_OK is being returned.
    while(hr == S_OK)
    {
        DWORD  cFetched = 0;
        PWSTR  szObjectIDArray[NUM_OBJECTS_TO_REQUEST] = {0};
        hr = pEnumObjectIDs->Next(NUM_OBJECTS_TO_REQUEST,   // Number of objects to request on each NEXT call
                                  szObjectIDArray,          // Array of PWSTR array which will be populated on each NEXT call
                                  &cFetched);               // Number of objects written to the PWSTR array
        if (SUCCEEDED(hr))
        {
            // Traverse the results of the Next() operation and recursively enumerate
            // Remember to free all returned object identifiers using CoTaskMemFree()
            for (DWORD dwIndex = 0; dwIndex < cFetched; dwIndex++)
            {
                RecursiveEnumerate(szObjectIDArray[dwIndex],pContent);

                // Free allocated PWSTRs after the recursive enumeration call has completed.
                CoTaskMemFree(szObjectIDArray[dwIndex]);
                szObjectIDArray[dwIndex] = NULL;
            }
        }
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ienumportabledeviceobjectids-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[**Iportabledevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Iportabledevicecontent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Iportabledeviceproperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



