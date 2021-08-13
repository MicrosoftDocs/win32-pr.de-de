---
description: Der Streamingaudiorenderer (SAR) ist eine Mediensenke, die Audio rendert.
ms.assetid: 5884a128-597d-432b-a706-e10c894d7965
title: StreamingAudiorenderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01752cbec7d801177b39d939baeca93f720e12aafeaf9845c1aa0ded033c3fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238265"
---
# <a name="streaming-audio-renderer"></a>StreamingAudiorenderer

Der Streamingaudiorenderer (SAR) ist eine Mediensenke, die Audio rendert. Jede Instanz des SAR rendert einen einzelnen Audiostream. Um mehrere Datenströme zu rendern, verwenden Sie mehrere Instanzen der SAR.

Rufen Sie zum Erstellen der SAR eine der folgenden Funktionen auf:

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer). Gibt einen Zeiger auf die SAR zurück.
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate). Gibt einen Zeiger auf ein Aktivierungsobjekt zurück, das zum Erstellen der SAR verwendet werden kann.

Die zweite Funktion, die ein Aktivierungsobjekt zurückgibt, ist erforderlich, wenn Sie geschützte Inhalte wiedergeben, da das Aktivierungsobjekt in den geschützten Prozess serialisiert werden muss. Für klare Inhalte können Sie eine der beiden Funktionen verwenden.

Die SAR kann unkomprimierte Audiodaten im PCM- oder IEEE-Gleitkommaformat empfangen. Wenn die Wiedergaberate schneller oder langsamer als 1× ist, passt die SAR die Tonhöhe automatisch an.

## <a name="configuring-the-audio-renderer"></a>Konfigurieren des Audiorenderers

Die SAR unterstützt mehrere Konfigurationsattribute. Der Mechanismus zum Festlegen dieser Attribute hängt davon ab, welche Funktion Sie aufrufen, um die SAR zu erstellen. Wenn Sie die [**MFCreateAudioRenderer-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) verwenden, gehen Sie folgendermaßen vor:

1.  Erstellen Sie einen neuen Attributspeicher, indem Sie [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)aufrufen.
2.  Fügen Sie die Attribute dem Attributspeicher hinzu.
3.  Übergeben Sie den Attributspeicher an die [**MFCreateAudioRenderer-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) im *pAudioAttributes-Parameter.*

Wenn Sie die [**MFCreateAudioRendererActivate-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) verwenden, gibt die Funktion einen Zeiger auf die [**INTERFACESAttributes-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) im *ppActivate-Parameter* zurück. Verwenden Sie diesen Zeiger, um die Attribute hinzuzufügen.

Eine Liste der Konfigurationsattribute finden Sie unter [Audiorendererattribute.](audio-renderer-attributes.md)

## <a name="selecting-the-audio-endpoint-device"></a>Auswählen des Audioendpunktgeräts

Ein *Audioendpunktgerät* ist ein Hardwaregerät, das Audio entweder rendert oder erfasst. Beispiele hierfür sind Lautsprecher, Lautsprecher, Mikrofone und CD-Player. Die SAR verwendet immer ein Audiorenderinggerät. Es gibt zwei Möglichkeiten, das Gerät auszuwählen.

Der erste Ansatz besteht darin, die Audiorenderinggeräte im System mithilfe der [**IMMDeviceEnumerator-Schnittstelle aufzulisten.**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) Diese Schnittstelle ist in der Kerndokumentation der Audio-API dokumentiert.

1.  Erstellen Sie das Geräteenumeratorobjekt.
2.  Verwenden Sie den Geräteenumerator, um Audiorenderinggeräte aufzuzählen. Jedes Gerät wird durch einen Zeiger auf die [**IMMDevice-Schnittstelle**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) dargestellt.
3.  Wählen Sie ein Gerät basierend auf den Geräteeigenschaften oder der Auswahl des Benutzers aus.
4.  Rufen Sie [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) auf, um den Gerätebezeichner abzurufen.
5.  Legen Sie den Gerätebezeichner als Wert des [**Attributs MF \_ AUDIO \_ RENDERER \_ ATTRIBUTE ENDPOINT \_ \_ ID**](mf-audio-renderer-attribute-endpoint-id-attribute.md) fest.

Anstatt Geräte aufzählen zu müssen, können Sie das Audiogerät anhand seiner *Rolle* angeben. Eine Audiorolle identifiziert eine allgemeine Kategorie der Verwendung. Beispielsweise ist die *Konsolenrolle* für Spiele und Systembenachrichtigungen definiert, während die *Multimediarolle* für Musik und Filme definiert ist. Jeder Rolle ist ein Audiorenderinggerät zugewiesen, und der Benutzer kann diese Zuweisungen ändern. Wenn Sie eine Geräterolle angeben, verwendet die SAR das Audiogerät, das für diese Rolle zugewiesen wurde. Um die Geräterolle anzugeben, legen Sie das [**ATTRIBUT MF \_ AUDIO \_ RENDERER ATTRIBUTE ENDPOINT \_ \_ \_ ROLE**](mf-audio-renderer-attribute-endpoint-role-attribute.md) fest.

Die beiden in diesem Abschnitt aufgeführten Attribute schließen sich gegenseitig aus. Wenn Sie keines von ihnen festlegen, verwendet die SAR das Audiogerät, das der **eConsole-Rolle** zugewiesen ist.

Der folgende Code listet die Audiorenderinggeräte auf und weist das erste Gerät in der Liste dem SAR zu. In diesem Beispiel wird die [**MFCreateAudioRenderer-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) verwendet, um die SAR zu erstellen.


```C++
#include <mmdeviceapi.h>

HRESULT hr = S_OK;

IMMDeviceEnumerator *pEnum = NULL;      // Audio device enumerator.
IMMDeviceCollection *pDevices = NULL;   // Audio device collection.
IMMDevice *pDevice = NULL;              // An audio device.
IMFAttributes *pAttributes = NULL;      // Attribute store.
IMFMediaSink *pSink = NULL;             // Streaming audio renderer (SAR)

LPWSTR wstrID = NULL;                   // Device ID.

// Create the device enumerator.
hr = CoCreateInstance(
    __uuidof(MMDeviceEnumerator), 
    NULL,
    CLSCTX_ALL, 
    __uuidof(IMMDeviceEnumerator), 
    (void**)&pEnum
    );

// Enumerate the rendering devices.
if (SUCCEEDED(hr))
{
    hr = pEnum->EnumAudioEndpoints(eRender, DEVICE_STATE_ACTIVE, &pDevices);
}

// Get ID of the first device in the list.
if (SUCCEEDED(hr))
{
    hr = pDevices->Item(0, &pDevice);
}

if (SUCCEEDED(hr))
{
    hr = pDevice->GetId(&wstrID);
}

// Create an attribute store and set the device ID attribute.
if (SUCCEEDED(hr))
{
    hr = MFCreateAttributes(&pAttributes, 2);
}

if (SUCCEEDED(hr))
{
    hr = pAttributes->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

// Create the audio renderer.
if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRenderer(pAttributes, &pSink);    
}

SAFE_RELEASE(pEnum);
SAFE_RELEASE(pDevices);
SAFE_RELEASE(pDevice); 
SAFE_RELEASE(pAttributes);
CoTaskMemFree(wstrID);
```



Um das Aktivierungsobjekt für die SAR zu erstellen, ändern Sie den Code, der nach dem Aufruf von [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) angezeigt wird, wie folgt:


```C++
IMFActivate *pActivate = NULL;          // Activation object.

if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRendererActivate(&pActivate);    
}

if (SUCCEEDED(hr))
{
    hr = pActivate->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

SAFE_RELEASE(pActivate);
```



## <a name="selecting-the-audio-session"></a>Auswählen der Audiositzung

Eine Audiositzung ist eine Gruppe verwandter Audiostreams, die eine Anwendung zusammen verwalten kann. Die Anwendung kann die Volumeebene steuern und den Zustand der einzelnen Sitzungen stummschalten. Sitzungen werden anhand der GUID identifiziert. Um die Audiositzung für die SAR anzugeben, verwenden Sie das [MF \_ AUDIO \_ RENDERER ATTRIBUTE SESSION \_ \_ \_ ID-Attribut.](mf-audio-renderer-attribute-session-id-attribute.md) Wenn Sie dieses Attribut nicht festlegen, verbindet die SAR die Standardsitzung für diesen Prozess, die durch **GUID \_ NULL** identifiziert wird.

Standardmäßig ist eine Audiositzung prozessspezifisch, d. h., sie enthält nur Streams aus dem aufrufenden Prozess. Um einer prozessübergreifenden Sitzung beizutreten, legen Sie das [ATTRIBUT \_ MF AUDIO \_ RENDERER ATTRIBUTE \_ \_ FLAGS](mf-audio-renderer-attribute-flags-attribute.md) mit dem Wert **MF AUDIO \_ \_ RENDERER ATTRIBUTE \_ \_ FLAGS \_ CROSSPROCESS fest.**

Nachdem Sie die SAR erstellt haben, verwenden Sie die [**SCHNITTSTELLE ZUSCHALTAUDIOPOLICY,**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) um die Sitzung mit einer Gruppe von Sitzungen zu verbinden, die alle von demselben Volumesteuerelement in der Systemsteuerung gesteuert werden. Sie können diese Schnittstelle auch verwenden, um den Anzeigenamen und das Symbol festzulegen, die im Volumesteuerelement angezeigt werden.

## <a name="controlling-volume-levels"></a>Steuern von Volumeebenen

Um die Mastervolumeebene aller Streams in der Audiositzung der SAR zu steuern, verwenden Sie die [**INTERFACESSimpleAudioVolume-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) Verwenden Sie zum Steuern des Volumens eines einzelnen Streams oder zum Steuern des Volumens einzelner Kanäle innerhalb eines Streams die [**INTERFACESAudioStreamVolume-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) Beide Schnittstellen werden abgerufen, indem [**SIE DENGETService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)aufrufen. Sie können **GetService** direkt in der SAR oder in der Mediensitzung aufrufen. Volumeebenen werden als Dämpfungswerte ausgedrückt. Für jeden Kanal ist die Dämpfungsebene das Produkt des Mastervolumes und des Kanalvolumes.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> </dl>

 

 
