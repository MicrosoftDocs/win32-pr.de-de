---
description: Abrufen der von einem Gerät unterstützten Renderingfunktionen
ms.assetid: 2332e3cc-087c-49cf-bde9-7f86f65158e7
title: Abrufen der von einem Gerät unterstützten Renderingfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b5e4fd09417585954ae205fc28fc8cf0e78ab02fdd3add616859b35b4237ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546230"
---
# <a name="retrieving-the-rendering-capabilities-supported-by-a-device"></a>Abrufen der von einem Gerät unterstützten Renderingfunktionen

Windows Portable Geräte, die die Funktionale Kategorie für Renderinginformationen (WPD \_ FUNCTIONAL \_ CATEGORY RENDERING \_ INFORMATION) unterstützen, geben \_ Renderinginformationen zurück, wenn sie abgefragt werden. Die Renderinginformationen beschreiben Anforderungen und Einschränkungen, die für Anwendungen gelten, die versuchen, Inhalte auf ein Gerät zu schreiben.

Die ListRenderingCapabilityInformation-Funktion, die Hilfsfunktion SupportsFunctionalCategory und die Hilfsfunktion ReadProfileInformationProperties im Modul DeviceCapabilities.cpp veranschaulichen das Abrufen von Renderingfunktionen für ein ausgewähltes Gerät.

Ihre Anwendung kann die von einem Gerät unterstützten Renderingfunktionen mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen abrufen.



| Schnittstelle                                                                                      | BESCHREIBUNG                                                 |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [**IPortableDeviceContent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Ermöglicht den Zugriff auf die IPortableDeviceProperties-Schnittstelle. |
| [**IPortableDeviceProperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Ermöglicht den Zugriff auf die eigenschaftenspezifischen Methoden.           |
| [**IPortableDeviceKeyCollection-Schnittstelle**](iportabledevicekeycollection.md)                 | Wird zum Speichern der Eigenschaftsschlüssel für das gegebene Profil verwendet.      |
| [**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)                               | Wird verwendet, um die Eigenschaftswerte für das gegebene Profil zu speichern.       |
| [**IPortableDeviceCapabilities-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Wird verwendet, um die Eigenschaftswerte für das gegebene Profil zu speichern.       |
| [**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md) | Wird verwendet, um die Eigenschaftswerte für das gegebene Profil zu speichern.       |
| [**IPortableDeviceValuesCollection-Schnittstelle**](iportabledevicevaluescollection.md)           | Wird verwendet, um die Eigenschaftswerte für das gegebene Profil zu speichern.       |



 

Eine der ersten Aufgaben, die von der Beispielanwendung ausgeführt wird, besteht in der Ermittlung, ob das ausgewählte Gerät Renderingfunktionen auflisten kann. Die Hilfsfunktion SupportsFunctionalCategory bestimmt, ob dies der Fall ist, indem die ListRenderingCapabilityInformation-Hilfsfunktion aufruft und WPD FUNCTIONAL CATEGORY RENDERING INFORMATION als zweites Argument übergeben \_ \_ \_ \_ wird.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
if (SupportsFunctionalCategory(pDevice, WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION) == FALSE)
{
    printf("This device does not support device rendering information to display\n");
    return;
}
```



Wenn das Gerät Renderingfunktionen auflisten kann, umfasst der nächste Schritt das Abrufen eines [**IPortableDeviceCapabilities-Objekts**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) und das Aufrufen der [**GetFunctionalObjects-Methode,**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) um einen Objektbezeichner für das Renderinginformationsobjekt abzurufen.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}

// Get the functional object identifier for the rendering information object
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalObjects(WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION, &pRenderingInfoObjects);
    if (FAILED(hr))
    {
        printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
    }
}
```



Der nächste Schritt besteht im Speichern des Renderinginformationsobjektbezeichners, der gerade in einer Zeichenfolgenvariablen (strRenderingInfoObjectID) abgerufen wurde, und anschließend zum Aufrufen der Hilfsfunktion ReadProfileInformationProperties. (Die Variable strRenderingInfoObjectID wird als zweites Argument an die Hilfsfunktion übergeben.)


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>          pCapabilities;
CComPtr<IPortableDevicePropVariantCollection> pRenderingInfoObjects;
CComPtr<IPortableDeviceValuesCollection>      pRenderingInfoProfiles;
CAtlStringW                                   strRenderingInfoObjectID;
if (SUCCEEDED(hr))
{
    PROPVARIANT pv = {0};
    PropVariantInit(&pv);
    hr = pRenderingInfoObjects->GetAt(0, &pv);
    if ((SUCCEEDED(hr))    &&
        (pv.vt== VT_LPWSTR) )
    {
        strRenderingInfoObjectID = pv.pwszVal;
    }
    else
    {
        printf("! Failed to get first rendering object's identifier, hr = 0x%lx\n", hr);
    }

    PropVariantClear(&pv);
}

if (SUCCEEDED(hr))
{
    hr = ReadProfileInformationProperties(pDevice,
                                          strRenderingInfoObjectID,
                                          &pRenderingInfoProfiles);
    // Error output statements are performed by the helper function, so they
    // are omitted here.
}
```



Eine der ersten Aufgaben, die von der Hilfsfunktion ausgeführt wird, ist das Abrufen eines [**IPortableDeviceContent-Objekts,**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) das für den Zugriff auf die inhaltsspezifischen Methoden verwendet wird.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



Als Nächstes ruft die Hilfsfunktion ein [**IPortableDeviceProperties-Objekt**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) ab, das für den Zugriff auf die eigenschaftenspezifischen Methoden verwendet wird.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



Der nächste Schritt besteht im Erstellen eines [**IPortableDeviceKeyCollection-Objekts,**](iportabledevicekeycollection.md) in dem die Eigenschaftsschlüssel für die Renderinginformationen gespeichert werden. Nachdem das Objekt erstellt wurde, wird die [**IPortableDeviceKeyCollection::Add-Methode**](iportabledevicekeycollection-add.md) aufgerufen, um die erforderlichen Schlüssel hinzuzufügen. (Es ist erforderlich, diese Schlüssel hinzuzufügen, damit die entsprechenden Renderingprofile in den nachfolgenden Schritten abgerufen werden können.)


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IPortableDeviceKeyCollection,
                      (VOID**) &pPropertiesToRead);
if (SUCCEEDED(hr))
{
    // Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_RENDERING_INFORMATION_PROFILES);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_RENDERING_INFORMATION_PROFILES to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



Der nächste Schritt besteht im Abrufen der Eigenschaftswerte aus dem Gerätetreiber durch Aufrufen der [**IPortableDeviceProperties::GetValues-Methode.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues)


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(wszFunctionalObjectID, // The object whose properties we are reading
                                pPropertiesToRead,     // The properties we want to read
                                &pObjectProperties);   // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", wszFunctionalObjectID, hr);
    }
}
```



Im nächsten Schritt wird das Renderinginformationsprofil abgerufen und im Argument ppRenderingInfoProfiles gespeichert.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceValuesCollection> pRenderingInfoProfiles;
CComPtr<IPortableDeviceContent>          pContent;
CComPtr<IPortableDeviceProperties>       pProperties;
CComPtr<IPortableDeviceKeyCollection>    pPropertiesToRead;
CComPtr<IPortableDeviceValues>           pObjectProperties;
if (SUCCEEDED(hr))
{
    hr = pObjectProperties->GetIPortableDeviceValuesCollectionValue(WPD_RENDERING_INFORMATION_PROFILES,
                                                                    &pRenderingInfoProfiles);
    if (FAILED(hr))
    {
        printf("! Failed to get WPD_RENDERING_INFORMATION_PROFILES from rendering information, hr= 0x%lx\n",  hr);
    }
}

// QueryInterface the interface into the out-going parameters.
if (SUCCEEDED(hr))
{
    hr = pRenderingInfoProfiles->QueryInterface(IID_PPV_ARGS(ppRenderingInfoProfiles));
    if (FAILED(hr))
    {
        printf("! Failed to QueryInterface for IPortableDeviceValuesCollection (Rendering information profiles), hr= 0x%lx\n",  hr);
    }
}
```



Nachdem die Hilfsfunktion die WPD RENDERING INFORMATION PROFILES-Eigenschaften gelesen \_ \_ \_ hat, werden die Renderingprofile angezeigt. Diese Profile werden von der Hilfsfunktion DisplayRenderingProfile angezeigt.


```C++
void DisplayRenderingProfile(
    IPortableDeviceValues* pProfile)
{
    HRESULT hr = S_OK;
    if (pProfile == NULL)
    {
        return;
    }

    if (SUCCEEDED(hr))
    {
        DWORD dwTotalBitrate    = 0;
        DWORD dwChannelCount    = 0;
        DWORD dwAudioFormatCode = 0;
        GUID  guidFormat        = WPD_OBJECT_FORMAT_UNSPECIFIED;

        // Display WPD_MEDIA_TOTAL_BITRATE
        hr = pProfile->GetUnsignedIntegerValue(WPD_MEDIA_TOTAL_BITRATE, &dwTotalBitrate);
        if (SUCCEEDED(hr))
        {
            printf("Total Bitrate: %d\n", dwTotalBitrate);
        }

        // If we fail to read the total bitrate as a single value, then it must be
        // a valid value set.  (i.e. returning IPortableDeviceValues as the value which
        // contains properties describing the valid values for this property.)
        if (hr == DISP_E_TYPEMISMATCH)
        {
            CComPtr<IPortableDeviceValues> pExpectedValues;
            hr = pProfile->GetIPortableDeviceValuesValue(WPD_MEDIA_TOTAL_BITRATE, &pExpectedValues);
            if (SUCCEEDED(hr))
            {
                printf("Total Bitrate: ");
                DisplayExpectedValues(pExpectedValues);
            }
        }

        // If we are still a failure here, report the error
        if (FAILED(hr))
        {

            printf("! Failed to get WPD_MEDIA_TOTAL_BITRATE from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_AUDIO_CHANNEL_COUNT
        hr = pProfile->GetUnsignedIntegerValue(WPD_AUDIO_CHANNEL_COUNT, &dwChannelCount);
        if (SUCCEEDED(hr))
        {
            printf("Channel Count: %d\n", dwChannelCount);
        }
        else
        {
            printf("! Failed to get WPD_AUDIO_CHANNEL_COUNT from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_AUDIO_FORMAT_CODE
        hr = pProfile->GetUnsignedIntegerValue(WPD_AUDIO_FORMAT_CODE,   &dwAudioFormatCode);
        if (SUCCEEDED(hr))
        {
            printf("Audio Format Code: %d\n", dwAudioFormatCode);
        }
        else
        {
            printf("! Failed to get WPD_AUDIO_FORMAT_CODE from rendering profile, hr = 0x%lx\n",hr);
        }

        // Display WPD_OBJECT_FORMAT
        hr = pProfile->GetGuidValue(WPD_OBJECT_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("Object Format: %ws\n", (LPWSTR)CComBSTR(guidFormat));
        }
        else
        {
            printf("! Failed to get WPD_OBJECT_FORMAT from rendering profile, hr = 0x%lx\n",hr);
        }
    }
}
```



Da die Renderingprofile statisch sind, kann Ihre Anwendung die Profile lesen und lokal speichern (anstatt jedes Mal, wenn die Daten benötigt werden, auf das Gerät zu zugreifen).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPortableDevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceCapabilities-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**IPortableDeviceContent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceKeyCollection-Schnittstelle**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**IPortableDeviceValuesCollection-Schnittstelle**](iportabledevicevaluescollection.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



