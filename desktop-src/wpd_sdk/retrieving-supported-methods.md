---
description: Abrufen unterstützter Dienstmethoden
ms.assetid: 783a6552-9b22-4af4-9252-b443e2624687
title: Abrufen unterstützter Dienstmethoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce058fcab000a90459dcce5310645088b40a2432d1de8c9852c84770db058300
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839047"
---
# <a name="retrieving-supported-service-methods"></a>Abrufen unterstützter Dienstmethoden

Dienstmethoden kapseln Funktionen, die von jedem Dienst definiert und implementiert werden. Sie sind spezifisch für jeden Diensttyptyp und werden durch eine eindeutige GUID dargestellt.

Der Contacts-Dienst definiert beispielsweise eine **BeginSync-Methode,** die Anwendungen aufrufen, um das Gerät für die Synchronisierung von Contact-Objekten vorzubereiten, und eine **EndSync-Methode,** um das Gerät zu benachrichtigen, dass die Synchronisierung abgeschlossen wurde.

Anwendungen können die unterstützten Methoden programmgesteuert abfragen und mithilfe der [**IPortableDeviceServiceCapabilities-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) auf diese Methoden und ihre Attribute zugreifen.

Dienstmethoden sollten nicht mit WPD-Befehlen verwechselt werden. WPD-Befehle sind Teil der standardmäßigen WPD Device Driver Interface (DDI) und stellen den Mechanismus für die Kommunikation zwischen einer WPD-Anwendung und dem Treiber dar. Befehle sind vordefiniert, nach Kategorien,z. B. WPD CATEGORY COMMON, und \_ werden durch eine \_ PROPERTYKEY-Struktur dargestellt. Weitere Informationen finden Sie im Thema [**Befehle.**](commands.md)

Die WpdServicesApiSample-Anwendung enthält Code, der veranschaulicht, wie eine Anwendung die von einem bestimmten Contacts-Dienst unterstützten Methoden mithilfe der Schnittstellen in der folgenden Tabelle abrufen kann.



| Schnittstelle      | BESCHREIBUNG         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Wird zum Abrufen der **IPortableDeviceServiceCapabilities-Schnittstelle** für den Zugriff auf die unterstützten Dienstmethoden verwendet. |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Ermöglicht den Zugriff auf die unterstützten Methoden, Methodenattribute und Methodenparameter.                             |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Enthält die Liste der unterstützten Methoden.                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | Enthält die Attribute für eine Methode und für die Parameter einer bestimmten Methode.                                      |
| [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)                 | Enthält die Parameter für eine bestimmte Methode.                                                                    |



 

Wenn der Benutzer die Option "5" in der Befehlszeile auswählt, ruft die Anwendung die **ListSupportedMethods-Methode** auf, die sich im Modul ServiceMethods.cpp befindet.

Beachten Sie, dass die Beispielanwendung vor dem Abrufen der Ereignisliste einen Kontaktdienst auf einem verbundenen Gerät öffnet.

In WPD wird eine Methode durch ihren Namen, Zugriffsrechte, Parameter und zugehörige Daten beschrieben. Die Beispielanwendung zeigt einen benutzerfreundlichen Namen an, z. B. "CustomMethod" oder eine GUID. Auf den Methodennamen oder die GUID folgen Zugriffsdaten ("Lesen/Schreiben"), der Name jedes zugeordneten Formats und die Parameterdaten. Diese Daten umfassen den Parameternamen, die Verwendung, VARTYPE und das Formular.

Fünf Methoden im Modul ServiceMethods.cpp unterstützen das Abrufen von Methoden (und zugehörigen Daten) für den angegebenen Contacts-Dienst: **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **DisplayFormat** und **DisplayMethodParameters**. Die **ListSupportedMethods-Methode** ruft jeweils die Anzahl der unterstützten Methoden und den GUID-Bezeichner ab. anschließend wird die **DisplayMethod-Methode** aufruft. Die **DisplayMethod-Methode** ruft die [**IPortableDeviceServiceCapapbilities::GetMethodAttributes-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) auf, um die Optionen, Parameter und so weiter der angegebenen Methode abzurufen. Nachdem **die DisplayMethod** die Methodendaten abgerufen hat, rendert sie den Namen (oder die GUID), die Zugriffseinschränkungen, das zugeordnete Format (falls verfügbar) und die Parameterbeschreibungen. Die **DisplayMethodAccess-,** **DisplayFormat-** und **DisplayMethodParameters** sind Hilfsfunktionen, die ihre jeweiligen Datenfelder rendern.

Die **ListSupportedMethods-Methode** ruft die [**IPortableDeviceService::Capabilities-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) auf, um eine [**IPortableDeviceServiceCapabilities-Schnittstelle**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) abzurufen. Über diese Schnittstelle werden die unterstützten Methoden abgerufen, indem die [**IPortableDeviceServiceCapabilities::GetSupportedMethods-Methode aufgerufen**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) wird. Die **GetSupportedMethods-Methode** ruft die GUIDs für jede vom Dienst unterstützte Methode ab und kopiert diese GUID in ein [**IPortableDevicePropVariantCollection-Objekt.**](iportabledevicepropvariantcollection.md)

Im folgenden Code wird die **ListSupportedMethods-Methode** verwendet.


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



Nachdem die **ListSupportedMethods-Methode** die GUID für jedes Ereignis abgerufen hat, das vom angegebenen Dienst unterstützt wird, ruft sie die **DisplayMethod-Methode** auf, um die methodenspezifischen Attribute abzurufen. Zu diesen Attributen gehören: der skriptfreundliche Name der Methode, erforderliche Zugriffseinschränkungen, jedes zugeordnete Format und eine Liste von Parametern.

Die **DisplayMethod-Methode** ruft die [**IPortableDeviceServiceCapabilities::GetMethodAttributes-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) auf, um eine Auflistung von Attributen für die gegebene Methode abzurufen. Anschließend wird die [**IPortableDeviceValues::GetStringValue-Methode**](iportabledevicevalues-getstringvalue.md) aufgerufen, um den Namen der Methode abzurufen. **DisplayMethod ruft** den [**IPortableDeviceValues::GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) auf, um die Zugriffs restrctions abzurufen. Anschließend wird [**IPortableDeviceValues::GetGuidValue**](iportabledevicevalues-getguidvalue.md) aufgerufen, um ein beliebiges zugeordnetes Format abzurufen. Und schließlich ruft **displayMethod** den [**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) auf, um die Parameterdaten abzurufen. Sie übergibt die von diesen Methoden zurückgegebenen Daten an die **Hilfsfunktionen DisplayMethodAccess,** **DisplayFormat** und **DisplayMethodParameters,** die die Informationen für die gegebene Methode rendern.

Im folgenden Code wird die **DisplayMethod-Methode** verwendet.


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



Die **DisplayMethodAccess-Hilfsfunktion** empfängt einen DWORD-Wert, der die Zugriffsoptionen der Methode enthält. Dieser Wert wird mit WPD COMMAND ACCESS READ und WPD COMMAND ACCESS READWRITE verglichen, um die \_ \_ \_ \_ \_ \_ Zugriffsberechtigung der Methode zu bestimmen. Mithilfe des Ergebnisses wird eine Zeichenfolge gerendert, die die Zugriffseinschränkung für die gegebene Methode angibt.

Im folgenden Code wird die **Hilfsfunktion DisplayMethodAccess** verwendet.


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



Die **DisplayMethod-Hilfsfunktion** empfängt ein [**IPortableDeviceServiceCapabilities-Objekt**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) und die GUID der Methode als Parameter. Mithilfe des **IPortableDeviceServiceCapabilities-Objekts** wird die [**IPortableDeviceServiceCapabilities::GetMethodAttributes-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) aufgerufen, um die Methodenattribute abzurufen und im Konsolenfenster der Anwendung zu rendern.

Die **Hilfsfunktion DisplayMethodParameters** empfängt ein [**IPortableDeviceServiceCapabilities-Objekt,**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) die GUID der Methode und ein IPortableDeviceKeyCollection-Objekt, das die Methodenparameter enthält. Mithilfe des [**IPortableDeviceKeyCollection-Objekts**](iportabledevicekeycollection.md) wird die [**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes-Methode**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) aufgerufen, um den Namen, die Verwendung, den VARTYPE und das Formular des Parameters abzurufen. Diese Informationen werden im Konsolenfenster der Anwendung gerendert.

Im folgenden Code wird die **DisplayMethodParameters-Hilfsfunktion** verwendet.


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

[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



