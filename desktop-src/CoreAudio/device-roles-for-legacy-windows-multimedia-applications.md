---
description: Geräte Rollen für ältere Windows-Multimediaanwendungen
ms.assetid: 54dcaa0e-2652-406d-ba24-c8885924acc6
title: Geräte Rollen für ältere Windows-Multimediaanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a4ad6728659e4c865aed773575268844fe330e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354278"
---
# <a name="device-roles-for-legacy-windows-multimedia-applications"></a>Geräte Rollen für ältere Windows-Multimediaanwendungen

> [!Note]  
> Die mmdevice-API unterstützt Geräte Rollen. Die Benutzeroberfläche in Windows Vista implementiert jedoch keine Unterstützung für dieses Feature. Die Unterstützung von Benutzeroberflächen für Geräte Rollen kann in einer zukünftigen Version von Windows implementiert werden. Weitere Informationen finden Sie unter [Geräte Rollen in Windows Vista](device-roles-in-windows-vista.md).

 

Die Legacy Funktionen von Windows Multimedia **waveoutxxx** und **waveinixxx** bieten keine Möglichkeit für eine Anwendung, das [audioendpunktgerät](audio-endpoint-devices.md) auszuwählen, das dem Benutzer einer bestimmten [Geräte Rolle](device-roles.md)zugewiesen wurde. In Windows Vista können die Kerndatei-APIs jedoch in Verbindung mit einer Windows-Multimediaanwendung verwendet werden, um die Geräteauswahl basierend auf der Geräte Rolle zu aktivieren. Mithilfe der [mmdevice-API](mmdevice-api.md)kann eine **waveoutxxx** -Anwendung z. b. das audioendpunktgerät identifizieren, das einer Rolle zugewiesen ist, das entsprechende Wellenform-Ausgabegerät identifiziert und die **WaveOutOpen** -Funktion aufruft, um eine Instanz des Geräts zu öffnen. Weitere Informationen zu **waveoutxxx** und **waveinxxx** finden Sie in der Windows SDK-Dokumentation.

Im folgenden Codebeispiel wird veranschaulicht, wie Sie die Wellenform-Geräte-ID für das renderingendpunktgerät abrufen, das einer bestimmten Geräte Rolle zugewiesen ist:


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



Im vorangehenden Codebeispiel akzeptiert die getwaveoutid-Funktion eine Geräte Rolle (econsole, emultimedia oder eCommunications) als Eingabeparameter. Der zweite Parameter ist ein Zeiger, über den die-Funktion die Wellenform-Geräte-ID für das Wellenform-Ausgabegerät schreibt, das der angegebenen Rolle zugewiesen ist. Die Anwendung kann dann **WaveOutOpen** mit dieser ID anrufen, um das Gerät zu öffnen.

Die Hauptschleife im vorangehenden Codebeispiel enthält zwei Aufrufe der **waveoutmessage** -Funktion. Der erste-Befehl sendet eine drv- \_ queryfunctioninstanceidsize-Nachricht, um die Größe der Endpunkt- [ID-Zeichenfolge](endpoint-id-strings.md) des Wellenform-Geräts, die durch den *waveoutid* -Parameter identifiziert wird, in Bytes abzurufen. (Die Endpunkt-ID-Zeichenfolge identifiziert das audioendpunktgerät, das der Wellenform-Geräte Abstraktion zugrunde liegt.) Die von diesem-Befehl gemeldete Größe schließt den Platz für das abschließende Null-Zeichen am Ende der Zeichenfolge ein. Das Programm kann die Größen Informationen verwenden, um einen Puffer zuzuordnen, der groß genug ist, um die gesamte Endpunkt-ID-Zeichenfolge zu enthalten.

Der zweite aufrut von **waveoutmessage** sendet eine drv \_ -queryfunctioninstanceid-Meldung, um die Geräte-ID-Zeichenfolge des Wellenform-Ausgabegeräts abzurufen. Der Beispielcode vergleicht diese Zeichenfolge mit der Geräte-ID-Zeichenfolge des audioendpunktgeräts mit der angegebenen Geräte Rolle. Wenn die Zeichen folgen Stimmen, schreibt die Funktion die Wellenform-Geräte-ID in den Speicherort, auf den der Parameter *pwaveoutid* zeigt. Der Aufrufer kann diese ID verwenden, um das Wellenform-Ausgabegerät zu öffnen, das über die angegebene Geräte Rolle verfügt.

Windows Vista unterstützt die \_ Nachrichten drv queryfunctioninstanceidsize und drv \_ queryfunctioninstanceid. Sie werden in früheren Versionen von Windows, einschließlich Windows Server 2003, Windows XP und Windows 2000, nicht unterstützt.

Die Funktion im vorangehenden Codebeispiel erhält die Wellenform-Geräte-ID für ein renderinggerät, aber mit einigen Änderungen kann Sie angepasst werden, um die Wellenform-Geräte-ID für ein Erfassungsgerät zu erhalten. Die Anwendung kann dann **waveinopen** mit dieser ID anrufen, um das Gerät zu öffnen. Gehen Sie folgendermaßen vor, um das vorangehende Codebeispiel zu ändern, um die Wellenform-Geräte-ID für das Gerät für die audioerfassungs-Endpunkt zu erhalten, das einer bestimmten Rolle zugewiesen ist:

-   Ersetzen Sie alle **waveoutxxx** -Funktionsaufrufe im vorangehenden Beispiel durch die entsprechenden **Wavin xxx** -Funktionsaufrufe.
-   Ändern Sie den Handle-Typ hwaveout in hwaader.
-   Ersetzen Sie [**erole-Enumerationskonstante**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) Ausdrucks durch ecapture.

In Windows Vista weisen die Funktionen **WaveOutOpen** und **waveinopen** stets die von Ihnen erstellten Audiostreams der Standard Sitzung zu – die prozessspezifische Sitzung, die durch den Sitzungs-GUID-Wert GUID NULL identifiziert wird \_ .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Interoperabilität mit Legacy-audioapis](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



