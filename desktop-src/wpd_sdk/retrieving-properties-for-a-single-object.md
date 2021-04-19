---
description: Abrufen von Eigenschaften für ein einzelnes Objekt
ms.assetid: e4e3b286-6330-4147-a367-57accf5beae6
title: Abrufen von Eigenschaften für ein einzelnes Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5851b31256659c2ca036bac504a53fa51a20ee14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353831"
---
# <a name="retrieving-properties-for-a-single-object"></a>Abrufen von Eigenschaften für ein einzelnes Objekt

Nachdem die Anwendung einen Objekt Bezeichner abgerufen hat (siehe das Thema zum Auflisten von Inhalten), kann er beschreibende Informationen zu diesem Objekt abrufen, indem er Methoden in der [**iportabledeviceproperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) und die [**iportabledevicekeycollection-Schnittstelle**](iportabledevicekeycollection.md) [aufruft](enumerating-content.md) .

Die [**iportabledeviceproperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) -Methode ruft eine Liste der angegebenen Eigenschaften für ein angegebenes Objekt ab. (Ihre Anwendung könnte auch die GetValues-Methode aufrufen und einen **null** -Wert für den pkeys-Parameter angeben, um alle Eigenschaften für ein bestimmtes Objekt abzurufen. die Leistung dieser Methode kann jedoch beim Abrufen aller Eigenschaften erheblich langsamer sein.)

Bevor die Anwendung GetValues aufruft, muss Sie jedoch die abzurufenden Eigenschaften ermitteln, indem die entsprechenden Schlüssel in einem [**iportabledevicekeycollection-Objekt**](iportabledevicekeycollection.md)festgelegt werden. Ihre Anwendung identifiziert die relevanten Eigenschaften, indem Sie die [**iportabledevicekeycollection:: Add**](iportabledevicekeycollection-add.md) -Methode aufrufen und einen PropertyKey-Wert bereitstellt, der jede abzurufende Eigenschaft identifiziert.

Die Funktion "lesecontentproperties" im Modul "contentproperties. cpp" der Beispielanwendung veranschaulicht, wie die fünf Eigenschaften für ein ausgewähltes Objekt abgerufen wurden. In der folgenden Tabelle werden die einzelnen Eigenschaften und deren zugehöriger refpropertykey-Wert beschrieben.



| Eigenschaft                     | BESCHREIBUNG                                                                                                                                      | PROPERTYKEY                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| Übergeordnete Objekt Kennung     | Eine Zeichenfolge, die den Bezeichner für das übergeordnete Objekt des angegebenen-Objekts angibt.                                                                            | übergeordnete WPD- \_ Objekt- \_ \_ ID             |
| Objektname                  | Eine Zeichenfolge, die den Namen des angegebenen-Objekts angibt.                                                                                            | WPD- \_ Objekt \_ Name                   |
| Persistente eindeutige Kennung | Eine Zeichenfolge, die einen eindeutigen Bezeichner für das angegebene Objekt angibt. (Dieser Bezeichner ist im Gegensatz zum Objekt Bezeichner Sitzungs übergreifend persistent.) | \_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt |
| Objekt Format                | Eine Globally Unique Identifier (GUID), die das Format der Datei angibt, die einem angegebenen Objekt entspricht.                                       | WPD- \_ Objekt \_ Format                 |
| Objekt Inhaltstyp          | Eine GUID, die den Typ des Inhalts angibt, der einem angegebenen Objekt zugeordnet ist.                                                                        | Inhaltstyp für WPD- \_ Objekt \_ \_          |



 

Der folgende Auszug aus der Funktion "Read contentproperties" veranschaulicht, wie die Beispielanwendung die [**iportabledevicekeycollection-Schnittstelle**](iportabledevicekeycollection.md) und die [**iportabledevicekeycollection:: Add**](iportabledevicekeycollection-add.md) -Methode verwendet, um die abzurufenden Eigenschaften zu identifizieren.


```C++
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPropertiesToRead));
if (SUCCEEDED(hr))
{
    // 4) Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PARENT_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PARENT_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_NAME);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PERSISTENT_UNIQUE_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PERSISTENT_UNIQUE_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_FORMAT);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_FORMAT to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_CONTENT_TYPE);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_CONTENT_TYPE to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



Nachdem die Beispielanwendung die entsprechenden Schlüssel festgelegt hat, wurde die [**iportabledeviceproperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) -Methode aufgerufen, um die angegebenen Werte für das angegebene Objekt abzurufen.


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(szSelection,         // The object whose properties we are reading
                                pPropertiesToRead,   // The properties we want to read
                                &pObjectProperties); // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iportabledevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Iportabledevicekeycollection-Schnittstelle**](iportabledevicekeycollection.md)
</dt> <dt>

[**Iportabledeviceproperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



