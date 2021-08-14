---
description: Festlegen von Eigenschaften für ein einzelnes Objekt
ms.assetid: 1c003534-96b4-419b-94d1-73b5ffa2eba1
title: Festlegen von Eigenschaften für ein einzelnes Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a38964282b4ff6a51ee104bafc596f40f6107a87ae8069eba84a25386e7842
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704280"
---
# <a name="setting-properties-for-a-single-object"></a>Festlegen von Eigenschaften für ein einzelnes Objekt

Nachdem Ihre Anwendung einen Objektbezeichner (siehe das Thema [Enumerating Content)](enumerating-content.md) für ein bestimmtes Objekt abgerufen hat, kann sie Eigenschaften für dieses Objekt festlegen, indem sie Methoden in den schnittstellen aufruft, die in der folgenden Tabelle beschrieben werden.



| Schnittstelle                                                                | BESCHREIBUNG                                                                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceProperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | Wird verwendet, um zu bestimmen, ob eine bestimmte Eigenschaft geschrieben werden kann, und um den Schreibvorgang zu senden.                                                                  |
| [**IPortableDeviceContent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | Ermöglicht den Zugriff auf die inhaltsspezifischen Methoden.                                                                                                            |
| [**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)         | Wird verwendet, um die zu schreibenden Werte zu speichern, die Ergebnisse des Schreibvorgangs zu bestimmen und Attribute von Eigenschaften abzurufen (beim Bestimmen der Schreibfunktion). |



 

Anwendungen legen Eigenschaften für ein Objekt fest, indem sie zuerst einen Eigenschaftenbehälter erstellen, der die neuen Werte mithilfe der [**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)angibt. Nachdem die Eigenschaftensammlung erstellt wurde, legt eine Anwendung diese Eigenschaften fest, indem sie die [**IPortableDeviceProperties::SetValues-Methode aufruft.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-setvalues)

Die `WriteContentProperties` Funktion im ContentProperties.cpp-Modul der Beispielanwendung veranschaulicht, wie eine Anwendung eine neue Objektnameneigenschaft für ein ausgewähltes Objekt festlegen kann.

Die erste Aufgabe der `WriteContentProperties` Funktion besteht darin, den Benutzer aufzufordern, einen Objektbezeichner für das Objekt einzugeben, für das die Anwendung den neuen Namen schreibt.


```C++
HRESULT                               hr                   = S_OK;
WCHAR                                 szSelection[81]      = {0};
WCHAR                                 szNewObjectName[81]  = {0};
CComPtr<IPortableDeviceProperties>    pProperties;
CComPtr<IPortableDeviceContent>       pContent;
CComPtr<IPortableDeviceValues>        pObjectPropertiesToWrite;
CComPtr<IPortableDeviceValues>        pPropertyWriteResults;
CComPtr<IPortableDeviceValues>        pAttributes;
BOOL                                  bCanWrite            = FALSE;

// Prompt user to enter an object identifier on the device to write properties on.
printf("Enter the identifer of the object you wish to write properties on.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting property reading\n");
}
```



Danach ruft die Anwendung den WPD \_ PROPERTY \_ ATTRIBUTE CAN \_ \_ WRITE-Wert für die WPD \_ OBJECT \_ NAME-Eigenschaft ab, um zu bestimmen, ob die Eigenschaft geschrieben werden kann. (Beachten Sie, dass Ihre Anwendung eine beliebige Eigenschaft festlegen kann, für die die WPD \_ PROPERTY \_ ATTRIBUTE CAN WRITE value is \_ \_ true.)


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent interface
// to access the property-specific methods.
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 3) Check the property attributes to see if we can write/change the WPD_OBJECT_NAME property.
if (SUCCEEDED(hr))
{
    hr = pProperties->GetPropertyAttributes(szSelection,
                                            WPD_OBJECT_NAME,
                                            &pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->GetBoolValue(WPD_PROPERTY_ATTRIBUTE_CAN_WRITE, &bCanWrite);
        if (SUCCEEDED(hr))
        {
            if (bCanWrite)
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports TRUE\nThis means that the property can be changed/updated\n\n");
            }
            else
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports FALSE\nThis means that the property cannot be changed/updated\n\n");
            }
        }
        else
        {
            printf("! Failed to get the WPD_PROPERTY_ATTRIBUTE_CAN_WRITE value from WPD_OBJECT_NAME on object '%ws', hr = 0x%lx\n",szSelection, hr);
        }
    }
}
```



Der nächste Schritt besteht darin, den Benutzer zur Eingabe der neuen Namenszeichenfolge aufzufordern. (Beachten Sie, dass der Aufruf der [**IPortableDeviceValues::SetStringValue-Methode**](iportabledevicevalues-setstringvalue.md) lediglich den Eigenschaftenbehälter erstellt. Die tatsächliche Eigenschaft wurde noch nicht geschrieben.)


```C++
if (bCanWrite)
{
    printf("Enter the new WPD_OBJECT_NAME for the object '%ws'.\n>",szSelection);
    hr = StringCbGetsW(szNewObjectName,sizeof(szNewObjectName));
    if (FAILED(hr))
    {
        printf("An invalid object name was specified, aborting property writing\n");
    }

    // 5) CoCreate an IPortableDeviceValues interface to hold the property values
    // we wish to write.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pObjectPropertiesToWrite));
        if (SUCCEEDED(hr))
        {
            if (pObjectPropertiesToWrite != NULL)
            {
                hr = pObjectPropertiesToWrite->SetStringValue(WPD_OBJECT_NAME, szNewObjectName);
                if (FAILED(hr))
                {
                    printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceValues, hr= 0x%lx\n", hr);
                }
            }
        }
    }
```



Schließlich wird der vom Benutzer angegebene neue Wert auf das -Objekt angewendet.


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->SetValues(szSelection,                // The object whose properties we are reading
                                pObjectPropertiesToWrite,   // The properties we want to read
                                &pPropertyWriteResults);    // Driver supplied property result values for the property read operation
    if (FAILED(hr))
    {
        printf("! Failed to set properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
    else
    {
        printf("The WPD_OBJECT_NAME property on object '%ws' was written successfully (Read the properties again to see the updated value)\n", szSelection);
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPortableDevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceKeyCollection-Schnittstelle**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceProperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**IPortableDevicePropertiesBulk-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



