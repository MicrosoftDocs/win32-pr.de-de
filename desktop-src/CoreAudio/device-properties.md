---
description: Geräteeigenschaften
ms.assetid: ad8753ba-ad20-4122-b0f2-eb165f98db67
title: Geräteeigenschaften (Kernaudio-APIs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e1a5068329ea2da794b68b777aa989a2e8b4a665df082982916942aa15b56e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407018"
---
# <a name="device-properties-core-audio-apis"></a>Geräteeigenschaften (Kernaudio-APIs)

Während des Aufzählens von [Audioendpunktgeräten](audio-endpoint-devices.md)kann eine Clientanwendung die Endpunktobjekte für ihre Geräteeigenschaften abfragen. Die Geräteeigenschaften werden in der Implementierung der MMDevice-API der **IPropertyStore-Schnittstelle** verfügbar gemacht. Bei einem Verweis auf die [**IMMDevice-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) eines Endpunktobjekts kann ein Client einen Verweis auf den Eigenschaftenspeicher des Endpunktobjekts abrufen, indem er die [**IMMDevice::OpenPropertyStore-Methode aufruft.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore)

Das PropertyStore-Objekt macht eine **IPropertyStore-Schnittstelle** verfügbar. Die beiden primären Methoden in dieser Schnittstelle sind **IPropertyStore::GetValue**, die einen Geräteeigenschaftswert abrufen, und **IPropertyStore::SetValue**, mit dem ein Geräteeigenschaftswert festgelegt wird. Weitere Informationen zu **IPropertyStore** finden Sie in der Windows SDK-Dokumentation.

Die Implementierung des Eigenschaftenspeichers der MMDevice-API unterscheidet sich vom Standard-Shelleigenschaftenspeicherobjekt. Um einen Eigenschaftswert zu ändern, muss die Clientanwendung die **IPropertyStore::SetValue-Methode** aufrufen. Während dieses Aufrufs werden die neuen Werte festgelegt und in die Registrierung geschrieben. Daher muss die Anwendung die **IPropertyStore::Commit-Methode** nach dem **SetValue-Aufruf** nicht aufrufen. Das Handle für die Registrierung wird nur geschlossen, wenn der Client den Schnittstellenzeiger freigibt.

In der Regel rufen Clientanwendungen von Drittanbietern die **GetValue-Methode** auf, jedoch nicht die **SetValue-Methode.** Der Endpunkt-Manager legt die grundlegenden Geräteeigenschaften für Endpunkte fest. Der Endpunkt-Manager ist die Windows Vista-Komponente, die für die Erkennung des Vorhandenseins von Audioendpunktgeräten verantwortlich ist.

Jeder PKEY \_ Xxx-Eigenschaftenbezeichner in der folgenden Liste ist eine Konstante vom Typ **PROPERTYKEY,** die in der Headerdatei Functiondiscoverykeys \_ devpkey.h definiert ist. Alle Audioendpunktgeräte verfügen über diese drei Geräteeigenschaften.



| Eigenschaft                                                                         | Beschreibung                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ DeviceInterface \_ FriendlyName**](pkey-deviceinterface-friendlyname.md) | Der Anzeigename des Audioadapters, an den das Endpunktgerät angefügt ist (z. B. "XYZ-Audioadapter"). **PROPVARIANT** member **vt** ist auf VT \_ LPWSTR festgelegt, und der Member **pwszVal** zeigt auf eine auf NULL endende Zeichenfolge mit Breitzeichen, die den Anzeigenamen enthält. |
| [**PKEY \_ Device \_ DeviceDesc**](pkey-device-devicedesc.md)                       | Die Gerätebeschreibung des Endpunktgeräts (z. B. "Lautsprecher"). **Propvariant** member **vt** is set to VT \_ LPWSTR and **member pwszVal** points to a null-terminated, wide-character string that contains the device description.                                       |
| [**PKEY \_ Device \_ FriendlyName**](pkey-device-friendlyname.md)                   | Der Anzeigename des Endpunktgeräts (z. B. "Lautsprecher (XYZ-Audioadapter)"). **PROPVARIANT** member **vt** ist auf VT \_ LPWSTR festgelegt, und der Member **pwszVal** zeigt auf eine auf NULL endende Zeichenfolge mit Breitzeichen, die den Anzeigenamen enthält.                             |



 

Einige Audioendpunktgeräte verfügen möglicherweise über zusätzliche Eigenschaften, die nicht in der vorherigen Liste angezeigt werden. Weitere Informationen zu zusätzlichen Eigenschaften finden Sie unter [Audioendpunkteigenschaften.](audio-endpoint-properties.md) Weitere Informationen zu **PROPERTYKEY** finden Sie in der Windows SDK-Dokumentation.

Im folgenden Codebeispiel werden die Anzeigenamen aller Audiorendering-Endpunktgeräte im System gedruckt:


```C++
//-----------------------------------------------------------
// This function enumerates all active (plugged in) audio
// rendering endpoint devices. It prints the friendly name
// and endpoint ID string of each endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

void PrintEndpointNames()
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDeviceCollection *pCollection = NULL;
    IMMDevice *pEndpoint = NULL;
    IPropertyStore *pProps = NULL;
    LPWSTR pwszID = NULL;

    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->EnumAudioEndpoints(
                        eRender, DEVICE_STATE_ACTIVE,
                        &pCollection);
    EXIT_ON_ERROR(hr)

    UINT  count;
    hr = pCollection->GetCount(&count);
    EXIT_ON_ERROR(hr)

    if (count == 0)
    {
        printf("No endpoints found.\n");
    }

    // Each loop prints the name of an endpoint device.
    for (ULONG i = 0; i < count; i++)
    {
        // Get pointer to endpoint number i.
        hr = pCollection->Item(i, &pEndpoint);
        EXIT_ON_ERROR(hr)

        // Get the endpoint ID string.
        hr = pEndpoint->GetId(&pwszID);
        EXIT_ON_ERROR(hr)
        
        hr = pEndpoint->OpenPropertyStore(
                          STGM_READ, &pProps);
        EXIT_ON_ERROR(hr)

        PROPVARIANT varName;
        // Initialize container for property value.
        PropVariantInit(&varName);

        // Get the endpoint's friendly-name property.
        hr = pProps->GetValue(
                       PKEY_Device_FriendlyName, &varName);
        EXIT_ON_ERROR(hr)

        // Print endpoint friendly name and endpoint ID.
        printf("Endpoint %d: \"%S\" (%S)\n",
               i, varName.pwszVal, pwszID);

        CoTaskMemFree(pwszID);
        pwszID = NULL;
        PropVariantClear(&varName);
        SAFE_RELEASE(pProps)
        SAFE_RELEASE(pEndpoint)
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    return;

Exit:
    printf("Error!\n");
    CoTaskMemFree(pwszID);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pCollection)
    SAFE_RELEASE(pEndpoint)
    SAFE_RELEASE(pProps)
}
```



Das FAILED-Makro im vorherigen Codebeispiel ist in der Headerdatei Winerror.h definiert.

Im vorherigen Codebeispiel ruft der for-loop-Text in der PrintEndpointNames-Funktion die [**IMMDevice::GetId-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) auf, um die [Endpunkt-ID-Zeichenfolge](endpoint-id-strings.md) für das Audioendpunktgerät abzurufen, das von der **IMMDevice-Schnittstelleninstanz** dargestellt wird. Die Zeichenfolge identifiziert das Gerät eindeutig in Bezug auf alle anderen Audioendpunktgeräte im System. Ein Client kann die Endpunkt-ID-Zeichenfolge verwenden, um eine Instanz des Audioendpunktgeräts zu einem späteren Zeitpunkt oder in einem anderen Prozess zu erstellen, indem er die [**IMMDeviceEnumerator::GetDevice-Methode aufruft.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) Clients sollten den Inhalt der Endpunkt-ID-Zeichenfolge als nicht transparent behandeln. Das heißt, Clients sollten nicht versuchen, den Inhalt der Zeichenfolge zu analysieren, um Informationen zum Gerät abzurufen. Der Grund dafür ist, dass das Zeichenfolgenformat nicht definiert ist und sich von einer Implementierung der MMDevice-API zur nächsten ändern kann.

Die Anzeigegerätenamen und Endpunkt-ID-Zeichenfolgen, die von der PrintEndpointNames-Funktion im vorherigen Codebeispiel abgerufen werden, sind identisch mit den anzeigefreundlichen Gerätenamen und Endpunkt-ID-Zeichenfolgen, die von DirectSound während der Geräteenumeration bereitgestellt werden. Weitere Informationen finden Sie unter [Audioereignisse für Ältere Audioanwendungen.](audio-events-for-legacy-audio-applications.md)

Im vorherigen Codebeispiel ruft die PrintEndpointNames-Funktion die **CoCreateInstance-Funktion** auf, um einen Enumerator für die Audioendpunktgeräte im System zu erstellen. Der **CoCreateInstance-Aufruf** schlägt fehl, es sei denn, das aufrufende Programm hat zuvor entweder die **CoInitialize-** oder **CoInitializeEx-Funktion** aufgerufen, um die COM-Bibliothek zu initialisieren. Weitere Informationen zu **CoCreateInstance,** **CoInitialize** und **CoInitializeEx** finden Sie in der Windows SDK-Dokumentation.

Weitere Informationen zu den Schnittstellen **IMMDeviceEnumerator,** **IMMDeviceCollection** und **IMMDevice** finden Sie unter [MMDevice-API.](mmdevice-api.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioendpunktgeräte](audio-endpoint-devices.md)
</dt> </dl>

 

 



