---
description: Abrufen unterstützter Dienst Methoden
ms.assetid: 783a6552-9b22-4af4-9252-b443e2624687
title: Abrufen unterstützter Dienst Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6029af655a8835a4eee887d919c534856062ff13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866503"
---
# <a name="retrieving-supported-service-methods"></a>Abrufen unterstützter Dienst Methoden

Dienst Methoden Kapseln Funktionen, die von den einzelnen Diensten definiert und implementiert werden. Sie sind spezifisch für jeden Diensttyp und werden durch eine eindeutige GUID dargestellt.

Der Kontakt Dienst definiert z. b. eine **BeginSync** -Methode, die Anwendungen aufrufen, um das Gerät für die Synchronisierung von Kontakt Objekten vorzubereiten, und eine **EndSync** -Methode, um das Gerät zu benachrichtigen, dass die Synchronisierung abgeschlossen ist.

Anwendungen können die unterstützten Methoden Programm gesteuert Abfragen und mithilfe der [**iportabledeviceservicecapabili-**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Schnittstelle auf diese Methoden und deren Attribute zugreifen.

Dienst Methoden sollten nicht mit WPD-Befehlen verwechselt werden. WPD-Befehle sind Teil der standardmäßigen WPD-Gerätetreiber Schnittstelle (DDI) und stellen den Mechanismus für die Kommunikation zwischen einer WPD-Anwendung und dem Treiber dar. Befehle sind vordefiniert, gruppiert nach Kategorien, z. b. \_ die WPD \_ -Kategorie Common, und werden durch eine PropertyKey-Struktur dargestellt. Weitere Informationen finden Sie im Thema " [**Befehle**](commands.md) ".

Die Anwendung wpdservicesapisample enthält Code, der veranschaulicht, wie eine Anwendung die von einem bestimmten Kontakt Dienst unterstützten Methoden mithilfe der Schnittstellen in der folgenden Tabelle abrufen kann.



|                                                                                      |                                                                                                                |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Schnittstelle                                                                            | BESCHREIBUNG                                                                                                    |
| [**Iportablede viceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Dient zum Abrufen der **iportabledeviceservicecapabili-** Schnittstelle für den Zugriff auf die unterstützten Dienst Methoden. |
| [**Iportablede viceservicecapabili**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Bietet Zugriff auf die unterstützten Methoden, Methoden Attribute und Methoden Parameter.                             |
| [**Iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) | Enthält die Liste der unterstützten Methoden.                                                                        |
| [**Iportablede vicevalues**](iportabledevicevalues.md)                               | Enthält die Attribute für eine Methode und für die Parameter einer bestimmten Methode.                                      |
| [**Iportabledevicekeycollection**](iportabledevicekeycollection.md)                 | Enthält die Parameter für eine bestimmte Methode.                                                                    |



 

Wenn der Benutzer die Option "5" in der Befehlszeile auswählt, ruft die Anwendung die **listsupportedmethods** -Methode auf, die im Modul "servicemethods. cpp" zu finden ist.

Beachten Sie, dass die Beispielanwendung vor dem Abrufen der Ereignisliste einen Kontakt Dienst auf einem verbundenen Gerät öffnet.

In WPD wird eine Methode anhand ihres Namens, ihrer Zugriffsrechte, der Parameter und der zugehörigen Daten beschrieben. Die Beispielanwendung zeigt einen benutzerfreundlichen Namen an, z. b. "custommethod" oder eine GUID. Auf den Methodennamen oder die GUID folgt der Zugriff auf Daten ("Lesen/Schreiben"), den Namen eines beliebigen zugeordneten Formats und die Parameterdaten. Diese Daten umfassen den Parameternamen, die Verwendung, den VarType und das Formular.

Fünf Methoden im servicemethods. cpp-Modul unterstützen das Abrufen von Methoden (und verknüpften Daten) für den jeweiligen Kontakt Dienst: **listsupportedmethods**, **Display Method**, **displaymethodaccess**, **Display Format** und **Display MethodParameters**. Die **listsupportedmethods** -Methode ruft die Anzahl unterstützter Methoden und den GUID-Bezeichner für jeden ab. Anschließend wird die **displaymethod** -Methode aufgerufen. Die **displaymethod** -Methode ruft die [**iportabledeviceservicecapebilitäts:: getmethodattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) -Methode auf, um die Optionen, Parameter usw. der angegebenen Methode abzurufen. Nachdem die Methoden Daten von **displaymethod** abgerufen wurden, werden der Name (oder die GUID), die Zugriffsbeschränkungen, das zugeordnete Format (sofern vorhanden) und die Parameter Beschreibungen gerendert. **Display methodaccess**, **Display Format** und **displaymethodparameters** sind Hilfsfunktionen, die ihre jeweiligen Datenfelder Rendering.

Die **listsupportedmethods** -Methode ruft die [**iportabledeviceservice:: Funktionen**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) -Methode auf, um eine [**iportabledeviceservicecapabili-**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Schnittstelle abzurufen. Mithilfe dieser Schnittstelle werden die unterstützten Methoden durch Aufrufen der [**iportabledeviceservicecapabili:: getsupportedmethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) -Methode abgerufen. Die **getsupportedmethods** -Methode ruft die GUIDs für jede Methode ab, die vom Dienst unterstützt wird, und kopiert diese GUID in ein [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Objekt.

Im folgenden Code wird die **listsupportedmethods** -Methode verwendet.


```C++
// List all supported methods on the service
void ListSupportedMethods(IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumMethods    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all methods supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedMethods(&pMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get supported methods from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported methods found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pMethods->GetCount(&dwNumMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported methods, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Methods Found on the service\n\n", dwNumMethods);

    // Loop through each method and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumMethods; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pMethods->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a method.  It is assumed that
                // methods are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayMethod(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }    
}
```



Nachdem die **listsupportedmethods** -Methode die GUID für jedes Ereignis abgerufen hat, das vom angegebenen Dienst unterstützt wird, ruft Sie die **displaymethod** -Methode auf, um die Methoden spezifischen Attribute abzurufen. Zu diesen Attributen gehören: der Skript Anzeige Name der Methode, die erforderlichen Zugriffsbeschränkungen, das zugehörige Format und die Liste der Parameter.

Die **displaymethod** -Methode ruft die [**iportabledeviceservicecapabili:: getmethodattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) -Methode auf, um eine Auflistung von Attributen für die angegebene Methode abzurufen. Anschließend wird die [**iportabledevicevalues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) -Methode aufgerufen, um den Namen der Methode abzurufen. Die **displaymethod** ruft [**iportabledevicevalues:: getunsignedintegervalue**](iportabledevicevalues-getunsignedintegervalue.md) auf, um die Zugriffs Umleitungen abzurufen. Anschließend wird [**iportabledevicevalues:: getguidvalue**](iportabledevicevalues-getguidvalue.md) aufgerufen, um ein zugeordnetes Format abzurufen. Und schließlich Ruft die **displaymethod** den [**iportabledevicevalues:: getiportabledevicekeycollectionvalue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) auf, um die Parameterdaten abzurufen. Sie übergibt die von diesen Methoden zurückgegebenen Daten an die Hilfsfunktionen " **displaymethodaccess**", " **Display Format**" und " **displaymethodparameters** ", die die Informationen für die angegebene Methode Rendering.

Im folgenden Code wird die **displaymethod** -Methode verwendet.


```C++
// Display basic information about a method
void DisplayMethod(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the method attributes which describe the method
    HRESULT hr = pCapabilities->GetMethodAttributes(Method, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the method attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR   pszMethodName  = NULL;
        DWORD   dwMethodAccess = WPD_COMMAND_ACCESS_READ;
        GUID    guidFormat     = GUID_NULL;

        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the method if available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_METHOD_ATTRIBUTE_NAME, &pszMethodName);
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszMethodName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Method));
        }       

        // Display the method access if available, otherwise default to WPD_COMMAND_ACCESS_READ access
        hr = pAttributes->GetUnsignedIntegerValue(WPD_METHOD_ATTRIBUTE_ACCESS, &dwMethodAccess);
        if (FAILED(hr))
        {
            dwMethodAccess = WPD_COMMAND_ACCESS_READ;
            hr = S_OK;
        }
        printf("\n\tAccess: ");
        DisplayMethodAccess(dwMethodAccess);

        // Display the associated format if specified.
        // Methods that have an associated format may only be supported for that format.
        // Methods that don't have associated formats generally apply to the entire service.
        hr = pAttributes->GetGuidValue(WPD_METHOD_ATTRIBUTE_ASSOCIATED_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("\n\tAssociated Format: ");
            DisplayFormat(pCapabilities, guidFormat);
        }

        // Display the method parameters, if available
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_METHOD_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayMethodParameters(pCapabilities, Method, pParameters);
        }
        
        CoTaskMemFree(pszMethodName);
        pszMethodName = NULL;

    }
}
```



Die Hilfsfunktion **displaymethodaccess** empfängt einen DWORD-Wert, der die Zugriffs Optionen der Methode enthält. Dieser Wert wird mit dem WPD \_ \_ -Befehls Zugriffs \_ Lese-und dem WPD \_ -Befehls Zugriffs-Lesevorgang verglichen \_ \_ , um die Zugriffsberechtigung der Methode zu bestimmen. Wenn das Ergebnis verwendet wird, rendert es eine Zeichenfolge, die die Zugriffsbeschränkung für die angegebene Methode angibt.

Im folgenden Code wird die-Hilfsfunktion **displaymethodaccess** verwendet.


```C++
void DisplayMethodAccess(
    DWORD   dwAccess)
{
    switch(static_cast<WPD_COMMAND_ACCESS_TYPES>(dwAccess))
    {
        case WPD_COMMAND_ACCESS_READ:
            printf("Read");
            break;
            
        case WPD_COMMAND_ACCESS_READWRITE:
            printf("Read/Write");
            break;

        default:
            printf("Unknown Access");
            break;
    }
}
```



Die Hilfsfunktion **displaymethod** empfängt ein [**iportabledeviceservicecapabili-**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Objekt und die GUID der Methode als Parameter. Mithilfe des **iportabledeviceservicecapabili-** Objekts wird die [**iportabledeviceservicecapabili:: getmethodattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) -Methode aufgerufen, um die Methoden Attribute abzurufen und Sie im Konsolenfenster der Anwendung zu erzeugen.

Die Hilfsfunktion **displaymethodparameters** empfängt ein [**iportabledeviceservicecapabili-**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) Objekt, die GUID der Methode und ein iportabledevicekeycollection-Objekt, das die Methoden Parameter enthält. Mithilfe des [**iportabledevicekeycollection**](iportabledevicekeycollection.md) -Objekts wird die [**iportabledeviceservicecapabili:: getmethodparameterattribute**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) -Methode aufgerufen, um den Namen, die Verwendung, den VarType und das Formular des Parameters abzurufen. Diese Informationen werden im Konsolenfenster der Anwendung gerendert.

Im folgenden Code wird die-Hilfsfunktion **displaymethodparameters** verwendet.


```C++
// Display the method parameters.
void DisplayMethodParameters(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method,
    IPortableDeviceKeyCollection*       pParameters)
{
    DWORD   dwNumParameters = 0;

    // Get the number of parameters for this event.
    HRESULT hr = pParameters->GetCount(&dwNumParameters);
    if (FAILED(hr))
    {
        printf("! Failed to get number of parameters, hr = 0x%lx\n",hr);
    }

    printf("\n\t%d Method Parameters:\n", dwNumParameters);

    // Loop through each parameter and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumParameters; dwIndex++)
        {
            PROPERTYKEY parameter;
            hr = pParameters->GetAt(dwIndex, &parameter);

            if (SUCCEEDED(hr))
            {
                CComPtr<IPortableDeviceValues> pAttributes;

                // Display the parameter's Name, Usage, Vartype, and Form
                hr = pCapabilities->GetMethodParameterAttributes(Method, parameter, &pAttributes);
                if (FAILED(hr))
                {
                    printf("! Failed to get the method parameter attributes, hr = 0x%lx\n",hr);
                }

                if (SUCCEEDED(hr))
                {
                    PWSTR   pszParameterName    = NULL;
                    DWORD   dwAttributeVarType  = 0;
                    DWORD   dwAttributeForm     = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                    DWORD   dwAttributeUsage    = (DWORD)-1;

                    hr = pAttributes->GetStringValue(WPD_PARAMETER_ATTRIBUTE_NAME, &pszParameterName);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tName: %ws\n", pszParameterName);
                    }
                    else
                    {
                        printf("! Failed to get the method parameter name, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_USAGE value, if specified. 
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_USAGE, &dwAttributeUsage);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tUsage: ");
                        DisplayParameterUsage(dwAttributeUsage);
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter usage, hr = 0x%lx\n",hr);
                    }

                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_VARTYPE, &dwAttributeVarType);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tVARTYPE: ");
                        DisplayVarType(static_cast<VARTYPE>(dwAttributeVarType));
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter VARTYPE, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_FORM value.
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_FORM, &dwAttributeForm);
                    if (FAILED(hr))
                    {
                        // If the read fails, assume WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED
                        dwAttributeForm = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                        hr = S_OK;
                    }

                    printf("\t\tForm: ");
                    DisplayParameterForm(dwAttributeForm);
                    printf("\n");

                    CoTaskMemFree(pszParameterName);
                    pszParameterName = NULL;
                }
                
                printf("\n");
            }
        }
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iportabledevicekeycollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**Iportablede viceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**Iportablede viceservicecapabili**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**Iportablede vicevalues**](iportabledevicevalues.md)
</dt> <dt>

[Wpdservicesapisample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



