---
title: Abrufen von WPD-Objekteigenschaften
description: Abrufen von Objekteigenschaften
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3c6eba4435b23ef5c637feaca7c2d4ab6b160e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042712"
---
# <a name="retrieving-wpd-object-properties"></a>Abrufen von WPD-Objekteigenschaften

Dienste enthalten häufig untergeordnete Objekte, die zu einem der Formate gehören, die von den einzelnen Diensten unterstützt werden. Beispielsweise kann ein Kontakt Dienst mehrere Kontakt Objekte des abstrakten Kontakt Formats unterstützen. Alle Kontakt Objekte werden durch verwandte Eigenschaften (Kontakt Name, Telefonnummer, e-Mail-Adresse usw.) beschrieben.

Die Anwendung wpdserviceapisample enthält Code, der veranschaulicht, wie eine Anwendung die Inhalts Objekteigenschaften abrufen kann, die von einem bestimmten Kontakt Dienst unterstützt werden. In diesem Beispiel werden die folgenden Schnittstellen verwendet.



|                                                                      |                                                                                              |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Schnittstelle                                                            | BESCHREIBUNG                                                                                  |
| [**Iportablede viceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | Ruft die **IPortableDeviceContent2** -Schnittstelle für den Zugriff auf die unterstützten Dienst Methoden ab. |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | Ermöglicht den Zugriff auf die Inhalts spezifischen Methoden.                                             |
| [**Iportabledeviceproperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | Ruft die Objekt Eigenschaftswerte ab.                                                        |
| [**Iportablede vicevalues**](iportabledevicevalues.md)               | Enthält die Eigenschaftswerte, die für dieses Objekt gelesen wurden.                                    |
| [**Iportabledevicekeycollection**](iportabledevicekeycollection.md) | Enthält die Parameter für eine bestimmte Methode.                                                  |



 

Wenn der Benutzer die Option "7" in der Befehlszeile auswählt, ruft die Anwendung die Methode "read **contentproperties** " auf, die im Modul "contentproperties. cpp" zu finden ist.

Diese Methode ruft die folgenden vier Eigenschaften für das angegebene Contact-Objekt ab.



|                              |                                                                                                                                                                                                                  |                                 |                                     |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| Eigenschaft                     | BESCHREIBUNG                                                                                                                                                                                                      | PropertyKey für Geräte Dienste     | Äquivalenter WPD \_ PropertyKey         |
| Übergeordnete Objekt Kennung     | Eine Zeichenfolge, die den Bezeichner für das übergeordnete Objekt des angegebenen-Objekts angibt.                                                                                                                                            | Pkey \_ genericobj \_ -Element-ID      | übergeordnete WPD- \_ Objekt- \_ \_ ID             |
| Objektname                  | Eine Zeichenfolge, die den Namen des angegebenen Objekts angibt.                                                                                                                                                             | Name des pkey- \_ genericobj \_          | WPD- \_ Objekt \_ Name                   |
| Persistente eindeutige Kennung | Eine Zeichenfolge, die einen eindeutigen Bezeichner für das angegebene Objekt angibt. Dieser Bezeichner ist im Gegensatz zum Objekt Bezeichner Sitzungs übergreifend persistent. Bei-Diensten muss dies eine Zeichen folgen Darstellung einer GUID sein. | Pkey- \_ genericobj \_ persistentuid | \_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt |
| Objekt Format                | Eine Globally Unique Identifier (GUID), die das Format der Datei angibt, die einem bestimmten Objekt entspricht.                                                                                                        | Pkey- \_ genericobj- \_ ObjectFormat  | WPD- \_ Objekt \_ Format                 |



 

-   Übergeordnete ID
-   Name
-   Persistentuid
-   Format

Beachten Sie, dass die Beispielanwendung vor dem Abrufen der Inhalts Eigenschaften einen Kontakt Dienst auf einem verbundenen Gerät öffnet.

Der folgende Code für die Methode "read **contentproperties** " veranschaulicht, wie die Anwendung mithilfe der [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) -Schnittstelle eine [**iportabledeviceproperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) -Schnittstelle abruft. Indem die PropertyKeys der angeforderten Eigenschaften an die [**iportabledeviceproperties:: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) -Methode übergeben werden, ruft "read **contentproperties** " die angeforderten Werte ab und zeigt Sie dann im Konsolenfenster an.


```C++
// Reads properties for the user specified object.
void ReadContentProperties(
    IPortableDeviceService*    pService)
{
    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    HRESULT                               hr              = S_OK;
    WCHAR                                 szSelection[81] = {0};
    CComPtr<IPortableDeviceProperties>    pProperties;
    CComPtr<IPortableDeviceValues>        pObjectProperties;
    CComPtr<IPortableDeviceContent2>      pContent;
    CComPtr<IPortableDeviceKeyCollection> pPropertiesToRead;

    // Prompt user to enter an object identifier on the device to read properties from.
    printf("Enter the identifer of the object you wish to read properties from.\n>");
    hr = StringCbGetsW(szSelection,sizeof(szSelection));
    if (FAILED(hr))
    {
        printf("An invalid object identifier was specified, aborting property reading\n");
    }

    // 1) Get an IPortableDeviceContent2 interface from the IPortableDeviceService interface to
    // access the content-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pService->Content(&pContent);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceContent2 from IPortableDeviceService, hr = 0x%lx\n",hr);
        }
    }

    // 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent2 interface
    // to access the property-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pContent->Properties(&pProperties);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent2, hr = 0x%lx\n",hr);
        }
    }

    // 3) CoCreate an IPortableDeviceKeyCollection interface to hold the property keys
    // we wish to read.
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
            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ParentID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ParentID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_Name);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_Name to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_PersistentUID);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_PersistentUID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

            hrTemp = pPropertiesToRead->Add(PKEY_GenericObj_ObjectFormat);
            if (FAILED(hrTemp))
            {
                printf("! Failed to add PKEY_GenericObj_ObjectFormat to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
            }

        }
    }

    // 5) Call GetValues() passing the collection of specified PROPERTYKEYs.
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

    // 6) Display the returned property values to the user
    if (SUCCEEDED(hr))
    {
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_ParentID,        NAME_GenericObj_ParentID);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_Name,            NAME_GenericObj_Name);
        DisplayStringProperty(pObjectProperties, PKEY_GenericObj_PersistentUID,   NAME_GenericObj_PersistentUID);
        DisplayGuidProperty  (pObjectProperties, PKEY_GenericObj_ObjectFormat,    NAME_GenericObj_ObjectFormat);
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)
</dt> <dt>

[**Iportabledeviceproperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[Wpdservicesapisample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



