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
# <a name="setting-metadata-on-a-file"></a><span data-ttu-id="95a2d-110">Festlegen von Metadaten für eine Datei</span><span class="sxs-lookup"><span data-stu-id="95a2d-110">Setting Metadata on a File</span></span>

<span data-ttu-id="95a2d-111">Sie können Metadaten für eine Datei festlegen, bevor Sie Sie auf das Gerät schreiben (bei Verwendung von [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)) oder in einem vorhandenen Speicher (durch Aufrufen von [**IWMDMStorage3:: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)).</span><span class="sxs-lookup"><span data-stu-id="95a2d-111">You can set metadata on a file before writing it to the device (when using [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)) or on an existing storage (by calling [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)).</span></span> <span data-ttu-id="95a2d-112">Attribute können nur für einen vorhandenen Speicher festgelegt werden (durch Aufrufen von [**iwmdmstorage:: SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes) oder [**IWMDMStorage2:: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)).</span><span class="sxs-lookup"><span data-stu-id="95a2d-112">You can set attributes only on an existing storage (by calling [**IWMDMStorage::SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes) or [**IWMDMStorage2::SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)).</span></span>

<span data-ttu-id="95a2d-113">Das Festlegen von Metadaten erfolgt durch Erstellen und Auffüllen einer [**iwmdmmetadata**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) -Schnittstelle, die an [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="95a2d-113">Setting metadata is done by creating and filling an [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) interface that is passed into [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).</span></span> <span data-ttu-id="95a2d-114">Diese Methode kann jedoch alle vorhandenen Metadaten für die Datei löschen, außer hart codierte Metadaten, die im Dateisystem selbst gespeichert sind, wie z. b. Dateiname oder Größe.</span><span class="sxs-lookup"><span data-stu-id="95a2d-114">However, this method can clear all existing metadata on the file, other than hard-coded metadata stored in the file system itself, such as file name or size.</span></span> <span data-ttu-id="95a2d-115">Daher müssen Sie alle vorhandenen Metadaten, die Sie beibehalten möchten, in die von Ihnen gesendeten iwmdmmetadata-Schnittstelle kopieren.</span><span class="sxs-lookup"><span data-stu-id="95a2d-115">Therefore, you must copy all existing metadata that you wish to retain into the IWMDMMetaData interface you submit.</span></span> <span data-ttu-id="95a2d-116">Da Windows Media Device Manager nicht zum Abrufen von Metadaten aus lokalen Dateien verwendet werden kann, müssen Sie das Windows Media-Format-SDK (oder ein anderes Tool) verwenden, um diese Metadaten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="95a2d-116">Because Windows Media Device Manager cannot be used to retrieve metadata from local files, you must use the Windows Media Format SDK (or some other tool) to retrieve such metadata.</span></span>

<span data-ttu-id="95a2d-117">Führen Sie die folgenden Schritte aus, um die Eigenschaften von ASF-Dateien mit dem Windows Media-Format-SDK abzurufen:</span><span class="sxs-lookup"><span data-stu-id="95a2d-117">To use the Windows Media Format SDK to retrieve ASF file properties, follow these steps:</span></span>

1.  <span data-ttu-id="95a2d-118">Erstellen Sie ein Metadateneditor-Objekt, indem Sie **wmcreateeditor** aufrufen und eine **IWMMetadataEditor** -Schnittstelle anfordern.</span><span class="sxs-lookup"><span data-stu-id="95a2d-118">Create a metadata editor object by calling **WMCreateEditor** and requesting an **IWMMetadataEditor** interface.</span></span>
2.  <span data-ttu-id="95a2d-119">Öffnen Sie die Datei für das Lesen von Metadaten durch Aufrufen von **IWMMetadataEditor:: Open**.</span><span class="sxs-lookup"><span data-stu-id="95a2d-119">Open the file for metadata reading by calling **IWMMetadataEditor::Open**.</span></span>
3.  <span data-ttu-id="95a2d-120">Wenn die Datei eine gültige ASF-Datei ist und geöffnet werden kann, Fragen Sie den Editor nach der **iwmheaderinfo** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="95a2d-120">If the file is a valid ASF file and can be opened, query the editor for the **IWMHeaderInfo** interface.</span></span>
4.  <span data-ttu-id="95a2d-121">Rufen Sie die Dateieigenschaften durch Aufrufen von **iwmheaderinfo:: getattributebyname** ab, und übergeben Sie die gewünschte Eigenschafts Konstante für das Windows Media-Format.</span><span class="sxs-lookup"><span data-stu-id="95a2d-121">Retrieve file properties by calling **IWMHeaderInfo::GetAttributeByName**, passing in the desired Windows Media Format SDK property constant.</span></span> <span data-ttu-id="95a2d-122">In der folgenden Tabelle finden Sie eine Liste der Format-SDK-Konstanten mit äquivalenten Windows Media Device Manager SDK-Konstanten.</span><span class="sxs-lookup"><span data-stu-id="95a2d-122">A list of Format SDK constants with equivalent Windows Media Device Manager SDK constants is given in the following table.</span></span>



| <span data-ttu-id="95a2d-123">SDK-Konstante für Windows Media-Format</span><span class="sxs-lookup"><span data-stu-id="95a2d-123">Windows Media Format SDK Constant</span></span>    | <span data-ttu-id="95a2d-124">Windows Media Device Manager SDK-Konstante</span><span class="sxs-lookup"><span data-stu-id="95a2d-124">Windows Media Device Manager SDK Constant</span></span>      |
|--------------------------------------|------------------------------------------------|
| <span data-ttu-id="95a2d-125">g \_ wszwmtitle</span><span class="sxs-lookup"><span data-stu-id="95a2d-125">g\_wszWMTitle</span></span>                        | <span data-ttu-id="95a2d-126">g \_ wszwmdmtitle</span><span class="sxs-lookup"><span data-stu-id="95a2d-126">g\_wszWMDMTitle</span></span>                                |
| <span data-ttu-id="95a2d-127">g \_ wszwmauthor</span><span class="sxs-lookup"><span data-stu-id="95a2d-127">g\_wszWMAuthor</span></span>                       | <span data-ttu-id="95a2d-128">g \_ wszwmdmauthor</span><span class="sxs-lookup"><span data-stu-id="95a2d-128">g\_wszWMDMAuthor</span></span>                               |
| <span data-ttu-id="95a2d-129">g \_ wszwmalbumtitle</span><span class="sxs-lookup"><span data-stu-id="95a2d-129">g\_wszWMAlbumTitle</span></span>                   | <span data-ttu-id="95a2d-130">g \_ wszwmdmalbumtitle</span><span class="sxs-lookup"><span data-stu-id="95a2d-130">g\_wszWMDMAlbumTitle</span></span>                           |
| <span data-ttu-id="95a2d-131">g \_ wszwmgenre</span><span class="sxs-lookup"><span data-stu-id="95a2d-131">g\_wszWMGenre</span></span>                        | <span data-ttu-id="95a2d-132">g \_ wszwmdmgenre</span><span class="sxs-lookup"><span data-stu-id="95a2d-132">g\_wszWMDMGenre</span></span>                                |
| <span data-ttu-id="95a2d-133">g \_ wszwmyear</span><span class="sxs-lookup"><span data-stu-id="95a2d-133">g\_wszWMYear</span></span>                         | <span data-ttu-id="95a2d-134">g \_ wszwmdmyear</span><span class="sxs-lookup"><span data-stu-id="95a2d-134">g\_wszWMDMYear</span></span>                                 |
| <span data-ttu-id="95a2d-135">g \_ wszwmtracknumber oder g \_ wszwmtrack</span><span class="sxs-lookup"><span data-stu-id="95a2d-135">g\_wszWMTrackNumber or g\_wszWMTrack</span></span> | <span data-ttu-id="95a2d-136">g \_ wszwmdmtrack</span><span class="sxs-lookup"><span data-stu-id="95a2d-136">g\_wszWMDMTrack</span></span>                                |
| <span data-ttu-id="95a2d-137">g \_ wszwmcomposer</span><span class="sxs-lookup"><span data-stu-id="95a2d-137">g\_wszWMComposer</span></span>                     | <span data-ttu-id="95a2d-138">g \_ wszwmdmcomposer</span><span class="sxs-lookup"><span data-stu-id="95a2d-138">g\_wszWMDMComposer</span></span>                             |
| <span data-ttu-id="95a2d-139">g \_ wszwmduration</span><span class="sxs-lookup"><span data-stu-id="95a2d-139">g\_wszWMDuration</span></span>                     | <span data-ttu-id="95a2d-140">g \_ wszwmdmduration</span><span class="sxs-lookup"><span data-stu-id="95a2d-140">g\_wszWMDMDuration</span></span>                             |
| <span data-ttu-id="95a2d-141">g \_ wszwmcopyright</span><span class="sxs-lookup"><span data-stu-id="95a2d-141">g\_wszWMCopyright</span></span>                    | <span data-ttu-id="95a2d-142">g \_ wszwmdmprovidercopyright</span><span class="sxs-lookup"><span data-stu-id="95a2d-142">g\_wszWMDMProviderCopyright</span></span>                    |
| <span data-ttu-id="95a2d-143">g \_ wszwmdescription</span><span class="sxs-lookup"><span data-stu-id="95a2d-143">g\_wszWMDescription</span></span>                  | <span data-ttu-id="95a2d-144">g \_ wszwmdmdescription</span><span class="sxs-lookup"><span data-stu-id="95a2d-144">g\_wszWMDMDescription</span></span>                          |
| <span data-ttu-id="95a2d-145">g \_ wszwmbitrate</span><span class="sxs-lookup"><span data-stu-id="95a2d-145">g\_wszWMBitrate</span></span>                      | <span data-ttu-id="95a2d-146">g \_ wszwmdmbitrate</span><span class="sxs-lookup"><span data-stu-id="95a2d-146">g\_wszWMDMBitrate</span></span>                              |
| <span data-ttu-id="95a2d-147">g \_ wszwmrating</span><span class="sxs-lookup"><span data-stu-id="95a2d-147">g\_wszWMRating</span></span>                       | <span data-ttu-id="95a2d-148">g \_ wszwmdmuserrating</span><span class="sxs-lookup"><span data-stu-id="95a2d-148">g\_wszWMDMUserRating</span></span>                           |
| <span data-ttu-id="95a2d-149">g \_ wszwmalbumartist</span><span class="sxs-lookup"><span data-stu-id="95a2d-149">g\_wszWMAlbumArtist</span></span>                  | <span data-ttu-id="95a2d-150">g \_ wszwmdmalbumartist</span><span class="sxs-lookup"><span data-stu-id="95a2d-150">g\_wszWMDMAlbumArtist</span></span>                          |
| <span data-ttu-id="95a2d-151">g \_ wszwmparametrialrating</span><span class="sxs-lookup"><span data-stu-id="95a2d-151">g\_wszWMParentalRating</span></span>               | <span data-ttu-id="95a2d-152">"g \_ wszwmdmparameentalrating"</span><span class="sxs-lookup"><span data-stu-id="95a2d-152">g\_wszWMDMParentalRating</span></span>                       |
| <span data-ttu-id="95a2d-153">g \_ wszwmradiostationname</span><span class="sxs-lookup"><span data-stu-id="95a2d-153">g\_wszWMRadioStationName</span></span>             | <span data-ttu-id="95a2d-154">g \_ wszwmdmmediastationname</span><span class="sxs-lookup"><span data-stu-id="95a2d-154">g\_wszWMDMMediaStationName</span></span>                     |
| <span data-ttu-id="95a2d-155">g \_ wszwmuntertitel</span><span class="sxs-lookup"><span data-stu-id="95a2d-155">g\_wszWMSubTitle</span></span>                     | <span data-ttu-id="95a2d-156">g \_ wszwmdmuntertitel</span><span class="sxs-lookup"><span data-stu-id="95a2d-156">g\_wszWMDMSubTitle</span></span>                             |
| <span data-ttu-id="95a2d-157">g \_ wszwmvideowidth</span><span class="sxs-lookup"><span data-stu-id="95a2d-157">g\_wszWMVideoWidth</span></span>                   | <span data-ttu-id="95a2d-158">g \_ wszwmdmwidth</span><span class="sxs-lookup"><span data-stu-id="95a2d-158">g\_wszWMDMWidth</span></span>                                |
| <span data-ttu-id="95a2d-159">g \_ wszwmvideoheight</span><span class="sxs-lookup"><span data-stu-id="95a2d-159">g\_wszWMVideoHeight</span></span>                  | <span data-ttu-id="95a2d-160">g \_ wszwmdmheight</span><span class="sxs-lookup"><span data-stu-id="95a2d-160">g\_wszWMDMHeight</span></span>                               |
| <span data-ttu-id="95a2d-161">g \_ wszwmmood</span><span class="sxs-lookup"><span data-stu-id="95a2d-161">g\_wszWMMood</span></span>                         | <span data-ttu-id="95a2d-162">g \_ wszwmdmtrackmood</span><span class="sxs-lookup"><span data-stu-id="95a2d-162">g\_wszWMDMTrackMood</span></span>                            |
| <span data-ttu-id="95a2d-163">g \_ wszwmcodec</span><span class="sxs-lookup"><span data-stu-id="95a2d-163">g\_wszWMCodec</span></span>                        | <span data-ttu-id="95a2d-164">g \_ wszaudiowavecodec oder g \_ wszvideofourcccodec</span><span class="sxs-lookup"><span data-stu-id="95a2d-164">g\_wszAudioWAVECodec or g\_wszVideoFourCCCodec</span></span> |



 

<span data-ttu-id="95a2d-165">Der folgende C++-Beispielcode veranschaulicht das Abrufen einer Reihe von Metadateneigenschaften aus einer ASF-Datei mithilfe des SDK für den Windows Media-Format und deren Umrechnung in die entsprechenden Windows Media Device Manager-Werte.</span><span class="sxs-lookup"><span data-stu-id="95a2d-165">The following C++ example code demonstrates retrieving a number of metadata properties from an ASF file using the Windows Media Format SDK and converting them to the equivalent Windows Media Device Manager values.</span></span>


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



<span data-ttu-id="95a2d-166">Die folgende C++-Beispiel Funktion zeigt, wie Sie mit DirectShow einige Dateiinformationen erhalten und diese den Metadaten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="95a2d-166">The following C++ example function shows how to use DirectShow to get some file information and add it to the metadata.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="95a2d-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95a2d-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95a2d-168">**Schreiben von Dateien auf das Gerät**</span><span class="sxs-lookup"><span data-stu-id="95a2d-168">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




