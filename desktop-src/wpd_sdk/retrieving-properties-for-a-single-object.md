---
description: Abrufen von Eigenschaften für ein einzelnes Objekt
ms.assetid: e4e3b286-6330-4147-a367-57accf5beae6
title: Abrufen von Eigenschaften für ein einzelnes Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0806de3da9cd3f0674057d413a071996f86f5d74a364c0f5db707965fc2220
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054720"
---
# <a name="retrieving-properties-for-a-single-object"></a>Abrufen von Eigenschaften für ein einzelnes Objekt

Nachdem Ihre Anwendung einen Objektbezeichner (siehe das Thema [Enumerating Content)](enumerating-content.md) für ein bestimmtes Objekt abgerufen hat, kann sie beschreibende Informationen zu diesem Objekt abrufen, indem methoden in der [**IPortableDeviceProperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) und der [**IPortableDeviceKeyCollection-Schnittstelle**](iportabledevicekeycollection.md)aufgerufen werden.

Die [**IPortableDeviceProperties::GetValues-Methode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) ruft eine Liste der angegebenen Eigenschaften für ein bestimmtes Objekt ab. (Ihre Anwendung könnte auch die GetValues-Methode aufrufen und einen **NULL-Wert** für den pKeys-Parameter angeben, um alle Eigenschaften für ein bestimmtes Objekt abzurufen. Die Leistung dieser Methode kann jedoch erheblich langsamer sein, wenn alle Eigenschaften abgerufen werden.)

Bevor Ihre Anwendung GetValues aufruft, muss sie jedoch die abzurufenden Eigenschaften identifizieren, indem entsprechende Schlüssel in einem [**IPortableDeviceKeyCollection-Objekt**](iportabledevicekeycollection.md)festgelegt werden. Ihre Anwendung identifiziert die interessanten Eigenschaften, indem sie die [**IPortableDeviceKeyCollection::Add-Methode**](iportabledevicekeycollection-add.md) aufruft und einen PROPERTYKEY-Wert angibt, der jede abzurufende Eigenschaft identifiziert.

Die ReadContentProperties-Funktion im ContentProperties.cpp-Modul der Beispielanwendung veranschaulicht, wie die fünf Eigenschaften für ein ausgewähltes Objekt abgerufen wurden. In der folgenden Tabelle werden jede dieser Eigenschaften und der entsprechende REFPROPERTYKEY-Wert beschrieben.



| Eigenschaft                     | BESCHREIBUNG                                                                                                                                      | PROPERTYKEY                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| Bezeichner des übergeordneten Objekts     | Eine Zeichenfolge, die den Bezeichner für das übergeordnete Element des angegebenen Objekts angibt.                                                                            | ÜBERGEORDNETE \_ \_ \_ WPD-OBJEKT-ID             |
| Objektname                  | Eine Zeichenfolge, die den Namen des angegebenen Objekts angibt.                                                                                            | \_WPD-OBJEKTNAME \_                   |
| Persistenter eindeutiger Bezeichner | Eine Zeichenfolge, die einen eindeutigen Bezeichner für das angegebene Objekt angibt. (Dieser Bezeichner ist sitzungsübergreifend persistent, im Gegensatz zum Objektbezeichner.) | \_PERSISTENTE EINDEUTIGE ID DES \_ \_ \_ WPD-OBJEKTS |
| Objektformat                | Ein GUID (Globally Unique Identifier), der das Format der Datei angibt, die einem bestimmten -Objekt entspricht.                                       | \_WPD-OBJEKTFORMAT \_                 |
| Objektinhaltstyp          | Eine GUID, die den Inhaltstyp angibt, der einem bestimmten -Objekt zugeordnet ist.                                                                        | \_ \_ WPD-OBJEKTINHALTSTYP \_          |



 

Der folgende Auszug aus der ReadContentProperties-Funktion veranschaulicht, wie die Beispielanwendung die [**IPortableDeviceKeyCollection-Schnittstelle**](iportabledevicekeycollection.md) und die [**IPortableDeviceKeyCollection::Add-Methode**](iportabledevicekeycollection-add.md) verwendet hat, um die Eigenschaften zu identifizieren, die sie abrufen würde.


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



Nachdem die Beispielanwendung die entsprechenden Schlüssel festgelegt hat, hat sie die [**IPortableDeviceProperties::GetValues-Methode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) aufgerufen, um die angegebenen Werte für das angegebene Objekt abzurufen.


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

[**IPortableDevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceKeyCollection-Schnittstelle**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceProperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



