---
title: Festlegen von Metadaten für eine Datei
description: Festlegen von Metadaten für eine Datei
ms.assetid: 478a5412-e8b4-41c8-802f-9c2748dbaeae
keywords:
- Windows Media-Device Manager, Metadaten
- Device Manager, Metadaten
- Programmier Handbuch, Metadaten
- Desktop Anwendungen, Metadaten
- Erstellen von Windows Media Device Manager-Anwendungen, Metadaten
- Schreiben von Dateien auf Geräte, Metadaten
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a6fa7002d4fafffe0793ef91b00dd3f1f0e20c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341655"
---
# <a name="setting-metadata-on-a-file"></a>Festlegen von Metadaten für eine Datei

Sie können Metadaten für eine Datei festlegen, bevor Sie Sie auf das Gerät schreiben (bei Verwendung von [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)) oder in einem vorhandenen Speicher (durch Aufrufen von [**IWMDMStorage3:: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)). Attribute können nur für einen vorhandenen Speicher festgelegt werden (durch Aufrufen von [**iwmdmstorage:: SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes) oder [**IWMDMStorage2:: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)).

Das Festlegen von Metadaten erfolgt durch Erstellen und Auffüllen einer [**iwmdmmetadata**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) -Schnittstelle, die an [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)übergeben wird. Diese Methode kann jedoch alle vorhandenen Metadaten für die Datei löschen, außer hart codierte Metadaten, die im Dateisystem selbst gespeichert sind, wie z. b. Dateiname oder Größe. Daher müssen Sie alle vorhandenen Metadaten, die Sie beibehalten möchten, in die von Ihnen gesendeten iwmdmmetadata-Schnittstelle kopieren. Da Windows Media Device Manager nicht zum Abrufen von Metadaten aus lokalen Dateien verwendet werden kann, müssen Sie das Windows Media-Format-SDK (oder ein anderes Tool) verwenden, um diese Metadaten abzurufen.

Führen Sie die folgenden Schritte aus, um die Eigenschaften von ASF-Dateien mit dem Windows Media-Format-SDK abzurufen:

1.  Erstellen Sie ein Metadateneditor-Objekt, indem Sie **wmcreateeditor** aufrufen und eine **IWMMetadataEditor** -Schnittstelle anfordern.
2.  Öffnen Sie die Datei für das Lesen von Metadaten durch Aufrufen von **IWMMetadataEditor:: Open**.
3.  Wenn die Datei eine gültige ASF-Datei ist und geöffnet werden kann, Fragen Sie den Editor nach der **iwmheaderinfo** -Schnittstelle ab.
4.  Rufen Sie die Dateieigenschaften durch Aufrufen von **iwmheaderinfo:: getattributebyname** ab, und übergeben Sie die gewünschte Eigenschafts Konstante für das Windows Media-Format. In der folgenden Tabelle finden Sie eine Liste der Format-SDK-Konstanten mit äquivalenten Windows Media Device Manager SDK-Konstanten.



| SDK-Konstante für Windows Media-Format    | Windows Media Device Manager SDK-Konstante      |
|--------------------------------------|------------------------------------------------|
| g \_ wszwmtitle                        | g \_ wszwmdmtitle                                |
| g \_ wszwmauthor                       | g \_ wszwmdmauthor                               |
| g \_ wszwmalbumtitle                   | g \_ wszwmdmalbumtitle                           |
| g \_ wszwmgenre                        | g \_ wszwmdmgenre                                |
| g \_ wszwmyear                         | g \_ wszwmdmyear                                 |
| g \_ wszwmtracknumber oder g \_ wszwmtrack | g \_ wszwmdmtrack                                |
| g \_ wszwmcomposer                     | g \_ wszwmdmcomposer                             |
| g \_ wszwmduration                     | g \_ wszwmdmduration                             |
| g \_ wszwmcopyright                    | g \_ wszwmdmprovidercopyright                    |
| g \_ wszwmdescription                  | g \_ wszwmdmdescription                          |
| g \_ wszwmbitrate                      | g \_ wszwmdmbitrate                              |
| g \_ wszwmrating                       | g \_ wszwmdmuserrating                           |
| g \_ wszwmalbumartist                  | g \_ wszwmdmalbumartist                          |
| g \_ wszwmparametrialrating               | "g \_ wszwmdmparameentalrating"                       |
| g \_ wszwmradiostationname             | g \_ wszwmdmmediastationname                     |
| g \_ wszwmuntertitel                     | g \_ wszwmdmuntertitel                             |
| g \_ wszwmvideowidth                   | g \_ wszwmdmwidth                                |
| g \_ wszwmvideoheight                  | g \_ wszwmdmheight                               |
| g \_ wszwmmood                         | g \_ wszwmdmtrackmood                            |
| g \_ wszwmcodec                        | g \_ wszaudiowavecodec oder g \_ wszvideofourcccodec |



 

Der folgende C++-Beispielcode veranschaulicht das Abrufen einer Reihe von Metadateneigenschaften aus einer ASF-Datei mithilfe des SDK für den Windows Media-Format und deren Umrechnung in die entsprechenden Windows Media Device Manager-Werte.


```C++
// Structure and array to hold equivalent Windows Media Format SDK 
// and Windows Media Device Manager SDK metadata property names.
struct EquivalentProperty
{
    LPCWSTR FormatSDKConst;
    LPCWSTR WMDMSDKConst;
};
EquivalentProperty EquivalentProperties []= 
{
    {g_wszWMTitle,        g_wszWMDMTitle},
    {g_wszWMAuthor,      g_wszWMDMAuthor},
    {g_wszWMAlbumTitle,  g_wszWMDMAlbumTitle},
    {g_wszWMGenre,       g_wszWMDMGenre},
    {g_wszWMYear,        g_wszWMDMYear},
    {g_wszWMTrackNumber, g_wszWMDMTrack},
    {g_wszWMTrack,       g_wszWMDMTrack},
    {g_wszWMComposer,    g_wszWMDMComposer},
    {g_wszWMBitrate,     g_wszWMDMBitrate},
    {g_wszWMDuration,    g_wszWMDMDuration},
    {g_wszWMCopyright,   g_wszWMDMProviderCopyright},
    {g_wszWMDescription, g_wszWMDMDescription},
    {g_wszWMRating,      g_wszWMDMUserRating},
    {g_wszWMAlbumArtist, g_wszWMDMAlbumArtist},
    {g_wszWMParentalRating,    g_wszWMDMParentalRating},
    {g_wszWMRadioStationName,  g_wszWMDMMediaStationName},
    {g_wszWMSubTitle,    g_wszWMDMSubTitle},
    {g_wszWMVideoWidth,  g_wszWMDMWidth},
    {g_wszWMVideoHeight, g_wszWMDMHeight},
    {g_wszWMMood,        g_wszWMDMTrackMood},
    {g_wszWMCodec,       g_wszAudioWAVECodec},
    {g_wszWMCodec,       g_wszVideoFourCCCodec}
};
// Function that tries to get metadata by using the Format SDK. 
// If it cannot open the file, it returns E_FAIL.
HRESULT GetFileMetadataFromFormatSDK(IWMDMMetaData* pMetadata, LPCWSTR file)
{
    if ((pMetaData == NULL) || (file == NULL)) return E_INVALIDPARAM;
    HRESULT hr = S_OK;
    CComPtr<IWMMetadataEditor> pEditor;

    // Do loop to allow easy error trapping. Even if there are no errors, 
    // the loop executes only once.
    do {
        hr = WMCreateEditor(&pEditor);
        if (FAILED(hr)) 
            break;

        // Open the file.
        hr = pEditor->Open(file);
        if (FAILED(hr)) 
            break;

        CComPtr<IWMHeaderInfo>pHeaderInfo;
        hr = pEditor->QueryInterface(__uuidof(IWMHeaderInfo), (void**)&pHeaderInfo);
        if (FAILED(hr))
            break;

        // Copy values from Format SDK to equivalent WMDM SDK metadata values.

        // Loop through all known values
        WORD stream = 0;
        WMT_ATTR_DATATYPE wmfType;
        WORD len = 0;
        BYTE* value = NULL;
        WMDM_TAG_DATATYPE wmdmType;
        for (int i = 0; i < sizeof(EquivalentProperties) / sizeof(EquivalentProperties[0]); i++)
        {
            // Request each value from our equivalency list by name.
            // The function is called twice: once to get the buffer size,
            // and once to get the value in the allocated buffer.
            if (FAILED(pHeaderInfo->GetAttributeByName(
                &stream, EquivalentProperties[i].FormatSDKConst, &wmfType, NULL, &len)))
            {
                continue;
            }

            value = new BYTE[len];
            if (value == NULL) continue;

            if (FAILED(pHeaderInfo->GetAttributeByName(&stream, EquivalentProperties[i].FormatSDKConst, &wmfType, value, &len)))
            {
                delete[] value;
                continue;
            }

            // Send the data to the equivalent WMDM metadata value.
            // First, find the equivalent WMDM type for the WMF type.
            switch(wmfType)
            {
            case WMT_TYPE_BINARY:
                wmdmType = WMDM_TYPE_BINARY;
                break;
            case WMT_TYPE_DWORD:
                wmdmType = WMDM_TYPE_DWORD;
                break;
            case WMT_TYPE_STRING:
                wmdmType = WMDM_TYPE_STRING;
                break;
            case WMT_TYPE_BOOL:
                wmdmType = WMDM_TYPE_BOOL;
                break;
            case WMT_TYPE_QWORD:
                wmdmType = WMDM_TYPE_QWORD;
                break;
            case WMT_TYPE_WORD:
                wmdmType = WMDM_TYPE_WORD;
                break;
            case WMT_TYPE_GUID:
                wmdmType = WMDM_TYPE_GUID;
                break;
            default:
                wmdmType = WMDM_TYPE_BINARY;
                break;
            }

            // Don't worry about trapping errors, because there's nothing 
            // we can do about it.
            pMetadata->AddItem(wmdmType, 
                EquivalentProperties[i].WMDMSDKConst, value, len);
            delete[] value;
        } // Add next value.
    } while (FALSE); // End Do loop error trap.

    // Close the file opened with IWMMetadataEditor.
    pEditor->Close();
    return hr;
}
```



Die folgende C++-Beispiel Funktion zeigt, wie Sie mit DirectShow einige Dateiinformationen erhalten und diese den Metadaten hinzufügen.


```C++
// For IMediaDet, you must link to strmiids.lib. Also include the following:
//#include <Qedit.h>  // for IMediaDet declaration.
//#include <Dshow.h>  // for VIDEOINFOHEADER declaration.
HRESULT GetFileMetadataFromDShow(IWMDMMetaData* pMetadata, LPCWSTR file)
{
    HRESULT hr = S_OK;

    // Add file metadata properties from DirectShow. 
    // This is good for non-ASF files, or to add any information
    // that the Format SDK didn't get.

    // Do loop to allow easy error trapping. Even if there are no errors, 
    // the loop executes only once.
    do
    {
        // Create the Media Detector object.
        CComPtr<IMediaDet> pIMediaDet;
        hr = pIMediaDet.CoCreateInstance(CLSID_MediaDet, NULL);
        if (FAILED(hr)) 
            break;

        // Open the file.
        hr = pIMediaDet->put_Filename(BSTR(file));
        if (FAILED(hr))
            break;

        // Get the media type for the default stream.
        AM_MEDIA_TYPE mediaType;
        hr = pIMediaDet->get_StreamMediaType(&mediaType);
        if (FAILED(hr))
            break;

        // We have the file open, so start requesting information from the 
        // Media Detector and adding it to the metadata. When adding 
        // individual metadata values, ignore the HRESULT, because failure 
        // to add these metadata values is not a breaking issue.

        // Get major and minor types.
        WCHAR strMediaType[64];
        ZeroMemory(strMediaType, 64);

        //Change the major type to a string, then add to IWMDMMetaData.
        StringFromGUID2(reinterpret_cast<GUID&>(mediaType.majortype),
            (LPOLESTR)strMediaType, 64);
        hr = pMetadata->AddItem(WMDM_TYPE_STRING, 
             g_wszWMDMediaClassPrimaryID, 
            (BYTE*) strMediaType, 
             sizeof(strMediaType) / sizeof(strMediaType[0]));

        // Clear local string, then retrieve subtype the same way.
        ZeroMemory(strMediaType, 64);
        StringFromGUID2(reinterpret_cast<GUID&>(mediaType.subtype),
            (LPOLESTR)strMediaType, 64);
        hr = pMetadata->AddItem(WMDM_TYPE_STRING, 
            g_wszWMDMMediaClassSecondaryID, (BYTE*) strMediaType,
            sizeof(strMediaType) / sizeof(strMediaType[0]));

        // Get the duration. Duration is retrieved in seconds, but set 
        // in 100-nanosecond units.
        double duration = 0;
        hr = pIMediaDet->get_StreamLength(&duration);
        if (duration > 0)
        {
            duration *= 10E7;
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMDuration, (BYTE*) &duration, sizeof(duration));
        }

        // Get the frame rate.
        double frameRate = 0;
        hr = pIMediaDet->get_FrameRate(&frameRate);
        if (frameRate > 0)
        {
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMFrameRate, 
                (BYTE*) &frameRate,
                sizeof(frameRate));
        }

        // Get the structure for the default stream's major type and 
        // fill in additional information.

        if (IsEqualGUID(mediaType.formattype, FORMAT_VideoInfo))
        {
            VIDEOINFOHEADER* data = (VIDEOINFOHEADER*) mediaType.pbFormat;
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMVideoBitrate, 
               (BYTE*) &data->dwBitRate, sizeof(DWORD));
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMHeight, 
               (BYTE*) &data->bmiHeader.biHeight, sizeof(LONG));
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMWidth, 
               (BYTE*) &data->bmiHeader.biWidth, sizeof(LONG));
        }

        if (IsEqualGUID(mediaType.formattype, FORMAT_WaveFormatEx))
        {
            WAVEFORMATEX* data = (WAVEFORMATEX*) mediaType.pbFormat;
            hr = pMetadata->AddItem(WMDM_TYPE_WORD, g_wszWMDMBlockAlignment, 
                (BYTE*) &data->nBlockAlign, sizeof(WORD));
            hr = pMetadata->AddItem(WMDM_TYPE_WORD, g_wszWMDMNumChannels, 
               (BYTE*) &data->nChannels, sizeof(WORD));
        }
    } while (FALSE); // End of error loop.
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben von Dateien auf das Gerät**](writing-files-to-the-device.md)
</dt> </dl>

 

 




