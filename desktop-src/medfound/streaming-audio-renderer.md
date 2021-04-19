---
description: Der streamingaudiorenderer (SAR) ist eine Medien Senke, die Audiodaten rendert.
ms.assetid: 5884a128-597d-432b-a706-e10c894d7965
title: Streamingaudiorenderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59c5b55f197d5e9770c6f1be55f680c7f9136f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356843"
---
# <a name="streaming-audio-renderer"></a>Streamingaudiorenderer

Der streamingaudiorenderer (SAR) ist eine Medien Senke, die Audiodaten rendert. Jede Instanz der SAR rendert einen einzelnen Audiodatenstrom. Zum Rendering mehrerer Streams verwenden Sie mehrere Instanzen von SAR.

Um den SAR zu erstellen, rufen Sie eine der folgenden Funktionen auf:

-   [**Mskreateaudiorenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer). Gibt einen Zeiger auf den SAR zurück.
-   [**MF | ateaudiorendereraktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate). Gibt einen Zeiger auf ein Aktivierungs Objekt zurück, das zum Erstellen der SAR verwendet werden kann.

Die zweite Funktion, die ein Aktivierungs Objekt zurückgibt, ist erforderlich, wenn geschützter Inhalt wiedergegeben wird, da das Aktivierungs Objekt in den geschützten Prozess serialisiert werden muss. Wenn Sie den Inhalt löschen möchten, können Sie beide Funktionen verwenden.

Der SAR kann unkomprimierte Audiodaten im PCM-oder IEEE-Gleit Komma Format empfangen. Wenn die Wiedergabe Rate schneller oder langsamer als 1 × ist, passt der SAR automatisch die Tonhöhe an.

## <a name="configuring-the-audio-renderer"></a>Konfigurieren des audiorenderers

Der SAR unterstützt mehrere Konfigurations Attribute. Der Mechanismus zum Festlegen dieser Attribute hängt von der Funktion ab, die Sie zum Erstellen der SAR-Methode aufruft. Gehen Sie wie folgt vor, wenn Sie die [**msup**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) -Funktion verwenden:

1.  Erstellen Sie einen neuen Attribut Speicher, indem Sie [**mfcreateattribute**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)aufrufen.
2.  Fügen Sie dem Attribut Speicher die Attribute hinzu.
3.  Übergeben Sie den Attribut Speicher an die [**mfkreateaudiorenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) -Funktion im *paudioattributparameter* .

Wenn Sie die [**mfkreateaudiorendereraktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) -Funktion verwenden, gibt die Funktion einen Zeiger auf die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle im *ppaktivierungs* -Parameter zurück. Verwenden Sie diesen Zeiger, um die Attribute hinzuzufügen.

Eine Liste der Konfigurations Attribute finden Sie unter [Attribute für audiorenderer](audio-renderer-attributes.md).

## <a name="selecting-the-audio-endpoint-device"></a>Auswählen des audioendpunktgeräts

Ein *audioendpunktgerät* ist ein Hardware Gerät, das Audiodaten rendert oder aufzeichnet. Beispiele hierfür sind Sprecher, Kopfhörer, Mikrofon und CD-Player. Der SAR verwendet immer ein audiorenderinggerät. Es gibt zwei Möglichkeiten, das Gerät auszuwählen.

Der erste Ansatz besteht darin, die audiorenderinggeräte im System mithilfe der [**immdeviceenumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle aufzuzählen. Diese Schnittstelle ist in der Dokumentation zur kernton-API dokumentiert.

1.  Erstellen Sie das Geräte Enumeratorobjekt.
2.  Verwenden Sie den Geräte Enumerator, um audiorenderinggeräte aufzuzählen. Jedes Gerät wird durch einen Zeiger auf die [**immdevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle dargestellt.
3.  Wählen Sie ein Gerät basierend auf den Geräteeigenschaften oder der Auswahl des Benutzers aus.
4.  Bitten Sie [**immdevice:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) , um den Geräte Bezeichner abzurufen.
5.  Legen Sie den Geräte Bezeichner als Wert für das Attribut [**\_ Endpunkt-ID für das MF- \_ audiorenderer \_ \_ \_**](mf-audio-renderer-attribute-endpoint-id-attribute.md) fest.

Anstatt Geräte aufzuzählen, können Sie das Audiogerät anhand seiner *Rolle* angeben. Eine audiorolle identifiziert eine allgemeine Kategorie der Verwendung. Beispielsweise ist die *Konsolen* Rolle für Spiele und System Benachrichtigungen definiert, während die *Multimedia* -Rolle für Musik und Filme definiert ist. Jeder Rolle ist ein audiorenderinggerät zugewiesen, und der Benutzer kann diese Zuweisungen ändern. Wenn Sie eine Geräte Rolle angeben, verwendet SAR das beliebige Audiogerät, das für diese Rolle zugewiesen wurde. Um die Geräte Rolle anzugeben, legen Sie das Attribut für das [**MF \_ - \_ audiorendererattribut \_ \_ EndPoint \_ Role**](mf-audio-renderer-attribute-endpoint-role-attribute.md) fest.

Die beiden in diesem Abschnitt aufgeführten Attribute schließen sich gegenseitig aus. Wenn Sie keinen der beiden Optionen festlegen, verwendet der SAR das Audiogerät, das der Rolle " **econsole** " zugewiesen ist.

Der folgende Code listet die audiorenderinggeräte auf und weist dem SAR das erste Gerät in der Liste zu. In diesem Beispiel wird die [**mfkreateaudiorenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) -Funktion verwendet, um den SAR zu erstellen.


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



Um das Aktivierungs Objekt für den SAR zu erstellen, ändern Sie den Code, der nach dem Aufrufen von " [**immdevice:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) " angezeigt wird, in Folgendes:


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

Eine Audiositzung ist eine Gruppe verwandter Audiodatenströme, die von einer Anwendung gemeinsam verwaltet werden können. Die Anwendung kann die Volumeebene und den stumm Zustand jeder Sitzung steuern. Sitzungen werden durch die GUID identifiziert. Um die Audiositzung für den SAR anzugeben, verwenden Sie das-Attribut für das [MF \_ - \_ audiorendererattribut \_ \_ Session \_ ID](mf-audio-renderer-attribute-session-id-attribute.md) . Wenn Sie dieses Attribut nicht festlegen, fügt der SAR die Standard Sitzung für diesen Prozess an, der durch **GUID \_ null** identifiziert wird.

Standardmäßig ist eine Audiositzung Prozess spezifisch, d. h., Sie enthält nur Datenströme aus dem aufrufenden Prozess. Um einer prozessübergreifenden Sitzung beizutreten, legen Sie das Attribut Flags für das [MF \_ - \_ audiorenderer \_ Attribut \_](mf-audio-renderer-attribute-flags-attribute.md) mit dem Wert **MF \_ - \_ audiorendererattributflags \_ \_ \_ CrossProcess** fest.

Nachdem Sie den SAR erstellt haben, verwenden Sie die [**imfaudiopolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) -Schnittstelle, um die Sitzung mit einer Gruppe von Sitzungen zu verknüpfen, die in der Systemsteuerung von der gleichen volumesteuerung gesteuert werden. Sie können diese Schnittstelle auch verwenden, um den anzeigen Amen und das Symbol festzulegen, die im volumesteuerelement angezeigt werden.

## <a name="controlling-volume-levels"></a>Steuern der volumeebenen

Verwenden Sie die [**imfsimpleaudiovolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) -Schnittstelle, um die Master Volume-Ebene aller Streams in der-Audiositzung von SAR zu steuern. Um das Volume eines einzelnen Streams zu steuern oder die Menge einzelner Kanäle innerhalb eines Streams zu steuern, verwenden Sie die [**imfaudiostreamvolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) -Schnittstelle. Beide Schnittstellen werden abgerufen, indem [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)aufgerufen wird. Sie können **GetService** direkt auf dem SAR aufrufen oder es für die Medien Sitzung aufrufen. Volumeebenen werden als Dämpfungswerte ausgedrückt. Für jeden Kanal ist die Ebene der Dämpfung das Produkt des Master Volumes und des channelvolumes.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> </dl>

 

 
