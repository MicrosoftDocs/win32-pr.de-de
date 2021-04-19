---
description: Microsoft Media Foundation unterstützt die Audio-und Video Erfassung.
ms.assetid: 8a9d96f8-1096-4b66-a2ec-8a95d754ea72
title: Audio-/Videoerfassung in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506c14ee4ab94a27cfafbe18a97ffa8f05676f1f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106373422"
---
# <a name="audiovideo-capture-in-media-foundation"></a>Audio-/Videoerfassung in Media Foundation

Microsoft Media Foundation unterstützt die Audio-und Video Erfassung. Video Erfassungsgeräte werden über den UVC-Klassen Treiber unterstützt und müssen mit UVC 1,1 kompatibel sein. Audioerfassungs Geräte werden über die Windows-audiositzungs-API (WASAPI) unterstützt.

Ein Erfassungsgerät wird in Media Foundation durch ein Medienquellen Objekt dargestellt, das die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle verfügbar macht. In den meisten Fällen wird diese Schnittstelle nicht direkt von der Anwendung verwendet, sondern eine API auf höherer Ebene, wie z. b. der [Quell Reader](source-reader.md) , um das Erfassungsgerät zu steuern.

## <a name="enumerate-capture-devices"></a>Erfassungsgeräte aufzählen

Führen Sie die folgenden Schritte aus, um die Erfassungsgeräte auf dem System aufzuzählen:

1.  Rufen Sie die Funktion [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen Attribut Speicher zu erstellen.
2.  Legen Sie das Attribut [ \_ \_ \_ \_ Quelltyp des MF-devsource-Attributs](mf-devsource-attribute-source-type.md) auf einen der folgenden Werte fest:

    | Wert                                                    | BESCHREIBUNG                      |
    |----------------------------------------------------------|----------------------------------|
    | **MF \_ devsource \_ - \_ Attribut \_ Quelltyp ( \_ audcap- \_ GUID)** | Listet audioerfassungs Geräte auf. |
    | **MF \_ devsource \_ - \_ Attribut \_ Quelltyp \_ VidCap \_ GUID** | Aufzählen von Video Erfassungs Geräten. |

    

     

3.  Nennen Sie die Funktion " [**mfenumschlag der vicesources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) ". Diese Funktion weist ein Array von [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeigern zu. Jeder Zeiger stellt ein Aktivierungs Objekt für ein Gerät im System dar.
4.  Rufen Sie die [**imfactivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) -Methode auf, um eine Instanz der Medienquelle von einem der Aktivierungs Objekte zu erstellen.

Im folgenden Beispiel wird eine Medienquelle für das erste Video Erfassungsgerät in der-Enumerationsliste erstellt:


```C++
HRESULT CreateVideoCaptureDevice(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    UINT32 count = 0;

    IMFAttributes *pConfig = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to hold the search criteria.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Request video capture devices.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }

    // Enumerate the devices,
    if (SUCCEEDED(hr))
    {
        hr = MFEnumDeviceSources(pConfig, &ppDevices, &count);
    }

    // Create a media source for the first device in the list.
    if (SUCCEEDED(hr))
    {
        if (count > 0)
        {
            hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(ppSource));
        }
        else
        {
            hr = MF_E_NOT_FOUND;
        }
    }

    for (DWORD i = 0; i < count; i++)
    {
        ppDevices[i]->Release();
    }
    CoTaskMemFree(ppDevices);
    return hr;
}
```



Sie können die Aktivierungs Objekte für verschiedene Attribute Abfragen, einschließlich der folgenden:

-   Das Attribut für den [ \_ \_ \_ benutzerfreundlichen \_ Namen des MF-devsource-Attributs](mf-devsource-attribute-friendly-name.md) enthält den anzeigen amen des Geräts. Der Anzeige Name eignet sich für die Anzeige für den Benutzer, ist jedoch möglicherweise nicht eindeutig.
-   Für Videogeräte enthält das Attribut " [MF \_ devsource \_ Attribute \_ Source \_ Type \_ VidCap \_ symbolischen \_ Link](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) " den symbolischen Link zum Gerät. Mit der symbolischen Verknüpfung wird das Gerät im System eindeutig identifiziert, es handelt sich jedoch nicht um eine lesbare Zeichenfolge.
-   Für Audiogeräte enthält das Attribut " [MF \_ devsource \_ Attribute \_ Source \_ Type \_ audcap \_ EndPoint \_ ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) " die audioendpunkt-ID des Geräts. Die audioendpunkt-ID ähnelt einem symbolischen Link. Es identifiziert das Gerät im System eindeutig, ist aber keine lesbare Zeichenfolge.

Im folgenden Beispiel wird ein Array von [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeigern angenommen und der Anzeige Name der einzelnen Geräte im Debugfenster ausgegeben:


```C++
void DebugShowDeviceNames(IMFActivate **ppDevices, UINT count)
{
    for (DWORD i = 0; i < count; i++)
    {
        HRESULT hr = S_OK;
        WCHAR *szFriendlyName = NULL;
    
        // Try to get the display name.
        UINT32 cchName;
        hr = ppDevices[i]->GetAllocatedString(
            MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME,
            &szFriendlyName, &cchName);

        if (SUCCEEDED(hr))
        {
            OutputDebugString(szFriendlyName);
            OutputDebugString(L"\n");
        }
        CoTaskMemFree(szFriendlyName);
    }
}
```



Wenn Sie den symbolischen Link für ein Videogerät bereits kennen, gibt es eine weitere Möglichkeit, die Medienquelle für das Gerät zu erstellen:

1.  Rufen Sie [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen Attribut Speicher zu erstellen.
2.  Legen Sie das Attribut [ \_ \_ \_ \_ Quelltyp des MF-devsource-Attributs](mf-devsource-attribute-source-type.md) auf das **MF \_ devsource- \_ Attribut \_ \_ Quelltyp \_ VidCap \_ GUID** fest.
3.  Legen Sie das Attribut " [MF \_ devsource \_ Attribute \_ Source \_ Type \_ VidCap \_ symbolischen \_ Link](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) " auf den symbolischen Link fest.
4.  Aufrufen der Funktion [**mfkreatedevicesource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) oder [**mfkreatedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) . Der erste gibt einen [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Zeiger zurück. Letztere gibt einen [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger auf ein Aktivierungs Objekt zurück. Sie können das Activation-Objekt verwenden, um die Quelle zu erstellen. (Ein Aktivierungs Objekt kann an einen anderen Prozess gemarshallt werden. Daher ist es nützlich, wenn Sie die Quelle in einem anderen Prozess erstellen möchten. Weitere Informationen finden Sie unter [Activation Objects](activation-objects.md).)

Im folgenden Beispiel wird die symbolische Verknüpfung eines Videogeräts erstellt und eine Medienquelle erstellt.


```C++
HRESULT CreateVideoCaptureDevice(PCWSTR *pszSymbolicLink, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to video.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }


    // Set the symbolic link.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
            (LPCWSTR)pszSymbolicLink
            );            
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



Es gibt eine entsprechende Methode zum Erstellen eines Audiogeräts über die audioendpunkt-ID:

1.  Rufen Sie [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen Attribut Speicher zu erstellen.
2.  Legen Sie das Attribut [ \_ \_ \_ \_ Quelltyp des MF-devsource-Attributs](mf-devsource-attribute-source-type.md) auf das **MF \_ devsource- \_ Attribut \_ \_ Quelltyp " \_ audcap \_ GUID**"
3.  Legen Sie das Attribut für den [MF \_ devsource- \_ Attribut \_ \_ Quelltyp " \_ audcap \_ EndPoint \_ ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) " der Endpunkt-ID fest.
4.  Aufrufen der Funktion [**mfkreatedevicesource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) oder [**mfkreatedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .

Im folgenden Beispiel wird eine audioendpunkt-ID angenommen und eine Medienquelle erstellt.


```C++
HRESULT CreateAudioCaptureDevice(PCWSTR *pszEndPointID, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to audio.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID
            );
    }

    // Set the endpoint ID.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID,
            (LPCWSTR)pszEndPointID
            ); 
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



## <a name="use-a-capture-device"></a>Verwenden eines Erfassungs Geräts

Nachdem Sie die Medienquelle für ein Erfassungsgerät erstellt haben, rufen Sie mithilfe des [Quell Readers](source-reader.md) Daten vom Gerät ab. Der Quell Leser liefert Medien Beispiele, die die Aufzeichnungs Audiodaten oder Video Frames enthalten. Der nächste Schritt hängt von Ihrem Anwendungsszenario ab:

-   Video Vorschau: Verwenden Sie Microsoft Direct3D oder Direct2D, um das Video anzuzeigen.
-   Datei Erfassung: Verwenden Sie den [sendenden Writer](sink-writer.md) , um die Datei zu codieren.
-   Audiovorschau: Verwenden Sie [WASAPI](/windows/desktop/CoreAudio/wasapi).

Wenn Sie die Audioerfassung mit Video Erfassung kombinieren möchten, verwenden Sie die *Aggregat Medienquelle*. Die Aggregat Medienquelle enthält eine Sammlung von Medienquellen und kombiniert all ihre Streams zu einem einzelnen Medienquellen Objekt. Um eine Instanz der aggregierten Medienquelle zu erstellen, rufen Sie die [**mfkreateaggregatesource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) -Funktion auf.

## <a name="shut-down-the-capture-device"></a>Geräte Erfassungsgerät Herunterfahren

Wenn das Erfassungsgerät nicht mehr benötigt wird, müssen Sie das Gerät Herunterfahren, indem Sie [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) für das [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Objekt aufrufen, das Sie durch Aufrufen von [**mfcreatedevicesource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) oder [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)abgerufen haben. Wenn das **herunter** fahren nicht aufgerufen wird, kann es zu Arbeitsspeicher Verknüpfungen kommen, da das System bis zum **herunter** fahren einen Verweis auf **imfmediasource** -Ressourcen aufbewahren kann.


```C++
if (g_pSource)
{
    g_pSource->Shutdown();
    g_pSource->Release();
    g_pSource = NULL;
}
```



Wenn Sie einem Erfassungsgerät eine Zeichenfolge mit dem symbolischen Link zugeordnet haben, sollten Sie dieses Objekt auch freigeben.


```C++
    CoTaskMemFree(g_pwszSymbolicLink);
    g_pwszSymbolicLink = NULL;

    g_cchSymbolicLink = 0;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videoaufzeichnung](audio-video-capture.md)
</dt> </dl>

 

 
