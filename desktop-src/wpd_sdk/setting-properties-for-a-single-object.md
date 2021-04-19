---
description: Festlegen von Eigenschaften für ein einzelnes Objekt
ms.assetid: 1c003534-96b4-419b-94d1-73b5ffa2eba1
title: Festlegen von Eigenschaften für ein einzelnes Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5649d05ccadfeaef0dd8805abd7d556f7725f175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350139"
---
# <a name="setting-properties-for-a-single-object"></a>Festlegen von Eigenschaften für ein einzelnes Objekt

Nachdem die Anwendung einen Objekt Bezeichner abgerufen hat (siehe das Thema zum Auflisten von [Inhalten](enumerating-content.md) ), können Sie die Eigenschaften für dieses Objekt festlegen, indem Sie Methoden in den in der folgenden Tabelle beschriebenen Schnittstellen aufrufen.



| Schnittstelle                                                                | BESCHREIBUNG                                                                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iportabledeviceproperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | Wird verwendet, um zu bestimmen, ob eine bestimmte Eigenschaft geschrieben werden kann, und um den Schreibvorgang zu senden.                                                                  |
| [**Iportabledevicecontent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | Ermöglicht den Zugriff auf die Inhalts spezifischen Methoden.                                                                                                            |
| [**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)         | Dient zum Speichern der zu schreibenden Werte, zum Bestimmen der Ergebnisse des Schreibvorgangs und zum Abrufen von Attribut Attributen (beim Bestimmen der Schreibfunktion). |



 

Anwendungen legen Eigenschaften für ein Objekt fest, indem Sie zuerst einen Eigenschaften Behälter erstellen, der die neuen Werte mithilfe der [**iportabledebug-Schnittstelle**](iportabledevicevalues.md)angibt. Nachdem der Eigenschaften Behälter erstellt wurde, legt eine Anwendung diese Eigenschaften fest, indem Sie die [**iportabledeviceproperties:: SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-setvalues) -Methode aufruft.

Die `WriteContentProperties` Funktion im Modul contentproperties. cpp der Beispielanwendung veranschaulicht, wie eine Anwendung für ein ausgewähltes Objekt eine neue Eigenschaft für den Objektnamen festlegen könnte.

Die erste Aufgabe, die von der-Funktion durchgeführt `WriteContentProperties` wird, besteht darin, den Benutzer zur Eingabe eines Objekt Bezeichners für das Objekt aufzufordern, für das die Anwendung den neuen Namen schreiben soll.


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



Danach ruft die Anwendung das WPD- \_ Eigenschafts Attribut ab und \_ \_ kann \_ einen Wert für die Eigenschaft WPD- \_ Objekt \_ Name schreiben, um zu bestimmen, ob die Eigenschaft geschrieben werden kann. (Beachten Sie, dass Ihre Anwendung jede Eigenschaft festlegen kann, für die die WPD \_ Das Eigenschafts \_ Attribut \_ kann den Wert "true" \_ schreiben.)


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



Der nächste Schritt besteht darin, den Benutzer zur Eingabe der neuen Namens Zeichenfolge aufzufordern. (Beachten Sie, dass durch den Aufrufen der [**iportabledevicevalues:: SetStringValue**](iportabledevicevalues-setstringvalue.md) -Methode lediglich der Eigenschaften Behälter erstellt wird. die tatsächliche Eigenschaft wurde noch nicht geschrieben.)


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



Schließlich wird der neue Wert, der vom Benutzer angegeben wird, auf das Objekt angewendet.


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

[**Iportabledevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Iportabledevicecontent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Iportabledevicekeycollection-Schnittstelle**](iportabledevicekeycollection.md)
</dt> <dt>

[**Iportabledeviceproperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Iportabledevicepropertiesbulk-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



