---
description: Geräterollen für Legacy-Windows Multimediaanwendungen
ms.assetid: 54dcaa0e-2652-406d-ba24-c8885924acc6
title: Geräterollen für Legacy-Windows Multimediaanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6b0c1c8b61da896ca8877a913ba14d5013de71ac6fd7c14bcdebfe21c4ffcb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406920"
---
# <a name="device-roles-for-legacy-windows-multimedia-applications"></a>Geräterollen für Legacy-Windows Multimediaanwendungen

> [!Note]  
> Die MMDevice-API unterstützt Geräterollen. Die Benutzeroberfläche in Windows Vista implementiert jedoch keine Unterstützung für dieses Feature. Die Unterstützung der Benutzeroberfläche für Geräterollen kann in einer zukünftigen Version von Windows implementiert werden. Weitere Informationen finden Sie unter [Geräterollen in Windows Vista](device-roles-in-windows-vista.md).

 

Die älteren Windows Multimediafunktionen **waveOutXxx** und **waveInXxx** bieten keine Möglichkeit für eine Anwendung, das [Audioendpunktgerät](audio-endpoint-devices.md) auszuwählen, das der Benutzer einer bestimmten [Geräterolle](device-roles.md)zugewiesen hat. In Windows Vista können die Kernaudio-APIs jedoch in Verbindung mit einer Windows Multimediaanwendung verwendet werden, um die Geräteauswahl basierend auf der Geräterolle zu aktivieren. Beispielsweise kann eine **waveOutXxx-Anwendung** mithilfe der [MMDevice-API](mmdevice-api.md)das Audioendpunktgerät identifizieren, das einer Rolle zugewiesen ist, das entsprechende Waveformausgabegerät identifizieren und die **waveOutOpen-Funktion** aufrufen, um eine Instanz des Geräts zu öffnen. Weitere Informationen zu **waveOutXxx** und **waveInXxx** finden Sie in der Windows SDK-Dokumentation.

Das folgende Codebeispiel zeigt, wie Sie die Waveform-Geräte-ID für das Renderingendpunktgerät abrufen, das einer bestimmten Geräterolle zugewiesen ist:


```C++
//-----------------------------------------------------------
// This function gets the waveOut ID of the audio endpoint
// device that is currently assigned to the specified device
// role. The caller can use the waveOut ID to open the
// waveOut device that corresponds to the endpoint device.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

HRESULT GetWaveOutId(ERole role, int *pWaveOutId)
{
    HRESULT hr;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    WCHAR *pstrEndpointIdKey = NULL;
    WCHAR *pstrEndpointId = NULL;

    if (pWaveOutId == NULL)
    {
        return E_POINTER;
    }

    // Create an audio endpoint device enumerator.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get the audio endpoint device that the user has
    // assigned to the specified device role.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, role,
                                              &pDevice);
    EXIT_ON_ERROR(hr)

    // Get the endpoint ID string of the audio endpoint device.
    hr = pDevice->GetId(&pstrEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Get the size of the endpoint ID string.
    size_t  cbEndpointIdKey;

    hr = StringCbLength(pstrEndpointIdKey,
                        STRSAFE_MAX_CCH * sizeof(WCHAR),
                        &cbEndpointIdKey);
    EXIT_ON_ERROR(hr)

    // Include terminating null in string size.
    cbEndpointIdKey += sizeof(WCHAR);

    // Allocate a buffer for a second string of the same size.
    pstrEndpointId = (WCHAR*)CoTaskMemAlloc(cbEndpointIdKey);
    if (pstrEndpointId == NULL)
    {
        EXIT_ON_ERROR(hr = E_OUTOFMEMORY)
    }

    // Each for-loop iteration below compares the endpoint ID
    // string of the audio endpoint device to the endpoint ID
    // string of an enumerated waveOut device. If the strings
    // match, then we've found the waveOut device that is
    // assigned to the specified device role.
    int waveOutId;
    int cWaveOutDevices = waveOutGetNumDevs();

    for (waveOutId = 0; waveOutId < cWaveOutDevices; waveOutId++)
    {
        MMRESULT mmr;
        size_t cbEndpointId;

        // Get the size (including the terminating null) of
        // the endpoint ID string of the waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEIDSIZE,
                             (DWORD_PTR)&cbEndpointId, NULL);
        if (mmr != MMSYSERR_NOERROR ||
            cbEndpointIdKey != cbEndpointId)  // do sizes match?
        {
            continue;  // not a matching device
        }

        // Get the endpoint ID string for this waveOut device.
        mmr = waveOutMessage((HWAVEOUT)IntToPtr(waveOutId),
                             DRV_QUERYFUNCTIONINSTANCEID,
                             (DWORD_PTR)pstrEndpointId,
                             cbEndpointId);
        if (mmr != MMSYSERR_NOERROR)
        {
            continue;
        }

        // Check whether the endpoint ID string of this waveOut
        // device matches that of the audio endpoint device.
        if (lstrcmpi(pstrEndpointId, pstrEndpointIdKey) == 0)
        {
            *pWaveOutId = waveOutId;  // found match
            hr = S_OK;
            break;
        }
    }

    if (waveOutId == cWaveOutDevices)
    {
        // We reached the end of the for-loop above without
        // finding a waveOut device with a matching endpoint
        // ID string. This behavior is quite unexpected.
        hr = E_UNEXPECTED;
    }

Exit:
    SAFE_RELEASE(pEnumerator);
    SAFE_RELEASE(pDevice);
    CoTaskMemFree(pstrEndpointIdKey);  // NULL pointer okay
    CoTaskMemFree(pstrEndpointId);
    return hr;
}
```



Im vorherigen Codebeispiel akzeptiert die GetWaveOutId-Funktion eine Geräterolle (eConsole, eMultimedia oder eCommunications) als Eingabeparameter. Der zweite Parameter ist ein Zeiger, über den die Funktion die Waveform-Geräte-ID für das Waveform-Ausgabegerät schreibt, das der angegebenen Rolle zugewiesen ist. Die Anwendung kann dann **waveOutOpen** mit dieser ID aufrufen, um das Gerät zu öffnen.

Die Main-Schleife im vorherigen Codebeispiel enthält zwei Aufrufe der **waveOutMessage-Funktion.** Der erste Aufruf sendet eine DRV \_ QUERYFUNCTIONINSTANCEIDSIZE-Nachricht, um die Größe der [Endpunkt-ID-Zeichenfolge](endpoint-id-strings.md) des Wellenformgeräts in Bytes abzurufen, die durch den *waveOutId-Parameter* identifiziert wird. (Die Endpunkt-ID-Zeichenfolge identifiziert das Audioendpunktgerät, das der Waveform-Geräteabstraktion zugrundeliegt.) Die von diesem Aufruf gemeldete Größe enthält das Leerzeichen für das abschließende NULL-Zeichen am Ende der Zeichenfolge. Das Programm kann die Größeninformationen verwenden, um einen Puffer zuzuordnen, der groß genug ist, um die gesamte Endpunkt-ID-Zeichenfolge zu enthalten.

Der zweite Aufruf von **waveOutMessage** sendet eine DRV \_ QUERYFUNCTIONINSTANCEID-Nachricht, um die Geräte-ID-Zeichenfolge des Waveform-Ausgabegeräts abzurufen. Im Beispielcode wird diese Zeichenfolge mit der Geräte-ID-Zeichenfolge des Audioendpunktgeräts mit der angegebenen Geräterolle verglichen. Wenn die Zeichenfolgen übereinstimmen, schreibt die Funktion die Waveform-Geräte-ID an den Speicherort, auf den der Parameter *pWaveOutId* zeigt. Der Aufrufer kann diese ID verwenden, um das Wellenformausgabegerät zu öffnen, das über die angegebene Geräterolle verfügt.

Windows Vista unterstützt die Meldungen DRV \_ QUERYFUNCTIONINSTANCEIDSIZE und DRV \_ QUERYFUNCTIONINSTANCEID. Sie werden in früheren Versionen von Windows nicht unterstützt, einschließlich Windows Server 2003, Windows XP und Windows 2000.

Die Funktion im vorherigen Codebeispiel ruft die Waveform-Geräte-ID für ein Renderinggerät ab, kann aber mit einigen Änderungen angepasst werden, um die Waveform-Geräte-ID für ein Erfassungsgerät abzurufen. Die Anwendung kann dann **waveInOpen** mit dieser ID aufrufen, um das Gerät zu öffnen. Gehen Sie wie folgt vor, um das obige Codebeispiel zu ändern, um die Waveform-Geräte-ID für das Audioerfassungsendpunktgerät abzurufen, das einer bestimmten Rolle zugewiesen ist:

-   Ersetzen Sie alle **waveOutXxx-Funktionsaufrufe** im vorherigen Beispiel durch die entsprechenden **waveInXxx-Funktionsaufrufe.**
-   Ändern Sie den Handletyp HWAVEOUT in HWAVEIN.
-   Ersetzen Sie die ERole-Enumerationskonstante eRender durch eCapture. [](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)

In Windows Vista weisen die **WaveOutOpen-** und **waveInOpen-Funktionen** der Standardsitzung immer die audiostreams zu, die sie erstellen – die prozessspezifische Sitzung, die durch den GUID-Wert DER Sitzung ALS NULL identifiziert \_ wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Interoperabilität mit Legacy-Audio-APIs](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



