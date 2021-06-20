---
title: Abrufen von WPD-Objekteigenschaften
description: Die WpdServiceApiSample-Anwendung veranschaulicht, wie eine Anwendung die Inhaltsobjekteigenschaften abrufen kann, die von einem bestimmten Contacts-Dienst unterstützt werden.
ms.assetid: 7fbd6f65-366a-49ea-a680-be77ca0d64f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e57258993d0a81f68042195db2caf338c97c53
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404313"
---
# <a name="retrieving-wpd-object-properties"></a>Abrufen von WPD-Objekteigenschaften

Dienste enthalten häufig untergeordnete Objekte, die zu einem der Formate gehören, die von jedem Dienst unterstützt werden. Ein Contacts-Dienst kann beispielsweise mehrere Kontaktobjekte im Abstrakten Kontaktformat unterstützen. Jedes Kontaktobjekt wird durch verwandte Eigenschaften (Kontaktname, Telefonnummer, E-Mail-Adresse und ähnliches) beschrieben.

Die WpdServiceApiSample-Anwendung enthält Code, der veranschaulicht, wie eine Anwendung die Inhaltsobjekteigenschaften abrufen kann, die von einem bestimmten Contacts-Dienst unterstützt werden. In diesem Beispiel werden die folgenden Schnittstellen verwendet.



| Schnittstelle | Beschreibung    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)             | Ruft die **IPortableDeviceContent2-Schnittstelle ab, um** auf die unterstützten Dienstmethoden zu zugreifen. |
| [**IPortableDeviceContent2**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2)           | Ermöglicht den Zugriff auf die inhaltsspezifischen Methoden.                                             |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)       | Ruft die Objekteigenschaftswerte ab.                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)               | Enthält die Eigenschaftswerte, die für dieses Objekt gelesen wurden.                                    |
| [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) | Enthält die Parameter für eine bestimmte Methode.                                                  |



 

Wenn der Benutzer die Option "7" in der Befehlszeile auswählt, ruft die Anwendung die **ReadContentProperties-Methode** auf, die sich im ContentProperties.cpp-Modul befindet.

Diese Methode ruft die folgenden vier Eigenschaften für das angegebene Kontaktobjekt ab.



| Eigenschaft                     | Beschreibung                                                                                                                                                                                                      | Device Services PROPERTYKEY     | Entsprechende WPD \_ PROPERTYKEY-Eigenschaft         |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|-------------------------------------|
| Bezeichner des übergeordneten Objekts     | Eine Zeichenfolge, die den Bezeichner für das übergeordnete Element des angegebenen Objekts angibt.                                                                                                                                            | PKEY \_ GenericObj \_ ParentID      | ÜBERGEORDNETE ID \_ DES WPD-OBJEKTS \_ \_             |
| Objektname                  | Eine Zeichenfolge, die den Namen des angegebenen Objekts angibt.                                                                                                                                                             | PKEY \_ \_ GenericObj-Name          | \_WPD-OBJEKTNAME \_                   |
| Persistenter eindeutiger Bezeichner | Eine Zeichenfolge, die einen eindeutigen Bezeichner für das gegebene Objekt angibt. Dieser Bezeichner ist im Gegensatz zum Objektbezeichner sitzungsübergreifend persistent. Bei Diensten muss dies eine Zeichenfolgendarstellung einer GUID sein. | PKEY \_ GenericObj \_ PersistentUID | PERSISTENTE EINDEUTIGE ID \_ DES WPD-OBJEKTS \_ \_ \_ |
| Objektformat                | Ein GUID (Globally Unique Identifier), der das Format der Datei angibt, die einem bestimmten Objekt entspricht.                                                                                                        | PKEY \_ GenericObj \_ ObjectFormat  | \_WPD-OBJEKTFORMAT \_                 |



 

-   Übergeordnete ID
-   Name
-   PersistentUID
-   Format

Beachten Sie, dass die Beispielanwendung vor dem Abrufen der Inhaltseigenschaften einen Kontaktdienst auf einem verbundenen Gerät öffnet.

Der folgende Code für die **ReadContentProperties-Methode** veranschaulicht, wie die Anwendung die [**IPortableDeviceContent2-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledevicecontent2) verwendet, um eine [**IPortableDeviceProperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) abzurufen. Durch Übergeben der PROPERTYKEYS der angeforderten Eigenschaften an die [**IPortableDeviceProperties::GetValues-Methode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) ruft **ReadContentProperties** die angeforderten Werte ab und zeigt sie dann im Konsolenfenster an.


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

[**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



