---
description: Geräteeigenschaften
ms.assetid: ad8753ba-ad20-4122-b0f2-eb165f98db67
title: Geräteeigenschaften (Core-audioapis)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a868e4bb806bd49d934febed164bcd70fba39f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340100"
---
# <a name="device-properties-core-audio-apis"></a>Geräteeigenschaften (Core-audioapis)

Beim Auflisten von [audioendpunktgeräten](audio-endpoint-devices.md)kann eine Client Anwendung die Endpunkt Objekte für Ihre Geräteeigenschaften Abfragen. Die Geräteeigenschaften werden in der mmdevice-API-Implementierung der **IPropertyStore** -Schnittstelle verfügbar gemacht. Bei einem Verweis auf die [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle eines Endpunkt Objekts kann ein Client einen Verweis auf den Eigenschaften Speicher des Endpunkt Objekts abrufen, indem er die [**immdevice:: openpropertystore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) -Methode aufrufen.

Das Property-Store-Objekt macht eine **IPropertyStore** -Schnittstelle verfügbar. Die beiden primären Methoden in dieser Schnittstelle sind **IPropertyStore:: GetValue**, der einen Geräte Eigenschafts Wert abruft, und **IPropertyStore:: SetValue**, der einen Wert für die Geräte Eigenschaft festlegt. Weitere Informationen zu **IPropertyStore** finden Sie in der Windows SDK-Dokumentation.

Die Implementierung des Eigenschafts Speicher der mmdevice-API unterscheidet sich vom standardmäßigen shelleigenschafts-Speicher Objekt. Um einen Eigenschafts Wert zu ändern, muss die Client Anwendung die **IPropertyStore:: SetValue** -Methode aufrufen. Während dieses Aufrufes werden die neuen Werte festgelegt und in der Registrierung geschrieben. Daher muss die Anwendung die **IPropertyStore:: Commit** -Methode nach dem **SetValue** -Befehl nicht aufrufen. Das Handle für die Registrierung wird nur geschlossen, wenn der Client den Schnittstellen Zeiger freigibt.

In der Regel wird von Drittanbieter-Client Anwendungen die **GetValue** -Methode, jedoch nicht die **SetValue** -Methode aufgerufen. Der Endpunkt-Manager legt die grundlegenden Geräteeigenschaften für Endpunkte fest. Der Endpunkt-Manager ist die Komponente von Windows Vista, die für das Erkennen des Vorhandenseins von audioendpunktgeräten verantwortlich ist.

Jeder pkey \_ xxx-Eigenschaften Bezeichner in der folgenden Liste ist eine Konstante vom Typ **PropertyKey** , die in der Header Datei functiondiscoverykeys \_ devpkey. h definiert ist. Alle audioendpunktgeräte verfügen über diese drei Geräteeigenschaften.



| Eigenschaft                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Pkey-Geräte \_ Name (tviceinterface \_ FriendlyName)**](pkey-deviceinterface-friendlyname.md) | Der Anzeige Name des audioadapters, an den das Endpunkt Gerät angefügt wird (z. b. "XYZ-Audioadapter"). Das **PROPVARIANT** -Element **VT** ist auf VT \_ LPWSTR festgelegt, und der Member **pwszval** verweist auf eine NULL-terminierte Zeichenfolge mit breit Zeichen, die den anzeigen Amen enthält. |
| [**Pkey- \_ Gerät \_ devicedebug**](pkey-device-devicedesc.md)                       | Die Geräte Beschreibung des Endpunkt Geräts (z. b. "Sprecher"). Der **PROPVARIANT** -Member **VT** ist auf VT \_ LPWSTR festgelegt, und der Member **pwszval** verweist auf eine mit NULL endenden Zeichenfolge mit breit Zeichen, die die Geräte Beschreibung enthält.                                       |
| [**Pkey- \_ Gerät \_ FriendlyName**](pkey-device-friendlyname.md)                   | Der Anzeige Name des Endpunkt Geräts (z. b. "Sprecher (XYZ-Audioadapter)"). Das **PROPVARIANT** -Element **VT** ist auf VT \_ LPWSTR festgelegt, und der Member **pwszval** verweist auf eine NULL-terminierte Zeichenfolge mit breit Zeichen, die den anzeigen Amen enthält.                             |



 

Einige audioendpunktgeräte verfügen möglicherweise über zusätzliche Eigenschaften, die nicht in der vorangehenden Liste angezeigt werden. Weitere Informationen zu zusätzlichen Eigenschaften finden Sie unter [Eigenschaften für audioendpunkte](audio-endpoint-properties.md). Weitere Informationen zu **PropertyKey** finden Sie in der Windows SDK-Dokumentation.

Im folgenden Codebeispiel werden die anzeigen Amen aller audiorendering-Endpunkt Geräte im System ausgegeben:


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



Das fehlgeschlagene Makro im vorangehenden Codebeispiel ist in der Header Datei Winerror. h definiert.

Im vorangehenden Codebeispiel ruft der **for**-Loop-Text in der printendpointnames-Funktion die [**immdevice:: GetId**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getid) -Methode auf, um die [Endpunkt-ID-Zeichenfolge](endpoint-id-strings.md) für das audioendpunkt-Gerät abzurufen, das von der **immdevice** -Schnittstellen Instanz dargestellt wird. Durch die Zeichenfolge wird das Gerät in Bezug auf alle anderen audioendpunktgeräte im System eindeutig identifiziert. Ein Client kann die Zeichenfolge der Endpunkt-ID verwenden, um eine Instanz des audioendpunktgeräts zu einem späteren Zeitpunkt oder in einem anderen Prozess zu erstellen, indem die [**immdeviceenumerator:: getdevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) -Methode aufgerufen wird. Clients sollten den Inhalt der Endpunkt-ID-Zeichenfolge als nicht transparent behandeln. Das heißt, Clients sollten nicht versuchen, den Inhalt der Zeichenfolge zu analysieren, um Informationen über das Gerät zu erhalten. Der Grund hierfür ist, dass das Zeichen folgen Format nicht definiert ist und sich möglicherweise von einer Implementierung der mmdevice-API zum nächsten ändert.

Die benutzerfreundlichen Gerätenamen und Endpunkt-ID-Zeichen folgen, die von der printendpointnames-Funktion im vorangehenden Codebeispiel abgerufen werden, sind identisch mit den benutzerfreundlichen Gerätenamen und Endpunkt-ID-Zeichen folgen, die von DirectSound während der Geräte Enumeration bereitgestellt werden. Weitere Informationen finden Sie unter [Audioereignisse für Legacy-Audioanwendungen](audio-events-for-legacy-audio-applications.md).

Im vorangehenden Codebeispiel ruft die Funktion printendpointnames die **cokreateinstance** -Funktion auf, um einen Enumerator für die audioendpunktgeräte im System zu erstellen. Wenn das aufrufende Programm die **CoInitialize** -Funktion oder die **CoInitializeEx** -Funktion nicht zum Initialisieren der com-Bibliothek aufgerufen hat, tritt beim **CoCreateInstance** -Aufruf ein Fehler auf. Weitere Informationen zu **cokreateinstance**, **CoInitialize** und **CoInitializeEx** finden Sie in der Windows SDK-Dokumentation.

Weitere Informationen zu den Schnittstellen " **immdeviceenumerator**", " **immdevicecollection**" und " **immdevice** " finden Sie unter [mmdevice-API](mmdevice-api.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioendpunktgeräte](audio-endpoint-devices.md)
</dt> </dl>

 

 



