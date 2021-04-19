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
# <a name="audiovideo-capture-in-media-foundation"></a><span data-ttu-id="84c0a-103">Audio-/Videoerfassung in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="84c0a-103">Audio/Video Capture in Media Foundation</span></span>

<span data-ttu-id="84c0a-104">Microsoft Media Foundation unterstützt die Audio-und Video Erfassung.</span><span class="sxs-lookup"><span data-stu-id="84c0a-104">Microsoft Media Foundation supports audio and video capture.</span></span> <span data-ttu-id="84c0a-105">Video Erfassungsgeräte werden über den UVC-Klassen Treiber unterstützt und müssen mit UVC 1,1 kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="84c0a-105">Video capture devices are supported through the UVC class driver and must be compatible with UVC 1.1.</span></span> <span data-ttu-id="84c0a-106">Audioerfassungs Geräte werden über die Windows-audiositzungs-API (WASAPI) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="84c0a-106">Audio capture devices are supported through Windows Audio Session API (WASAPI).</span></span>

<span data-ttu-id="84c0a-107">Ein Erfassungsgerät wird in Media Foundation durch ein Medienquellen Objekt dargestellt, das die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="84c0a-107">A capture device is represented in Media Foundation by a media source object, which exposes the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="84c0a-108">In den meisten Fällen wird diese Schnittstelle nicht direkt von der Anwendung verwendet, sondern eine API auf höherer Ebene, wie z. b. der [Quell Reader](source-reader.md) , um das Erfassungsgerät zu steuern.</span><span class="sxs-lookup"><span data-stu-id="84c0a-108">In most cases, the application will not use this interface directly, but will use a higher-level API such as the [Source Reader](source-reader.md) to control the capture device.</span></span>

## <a name="enumerate-capture-devices"></a><span data-ttu-id="84c0a-109">Erfassungsgeräte aufzählen</span><span class="sxs-lookup"><span data-stu-id="84c0a-109">Enumerate Capture Devices</span></span>

<span data-ttu-id="84c0a-110">Führen Sie die folgenden Schritte aus, um die Erfassungsgeräte auf dem System aufzuzählen:</span><span class="sxs-lookup"><span data-stu-id="84c0a-110">To enumerate the capture devices on the system, perform the following steps:</span></span>

1.  <span data-ttu-id="84c0a-111">Rufen Sie die Funktion [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen Attribut Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84c0a-111">Call the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function to create an attribute store.</span></span>
2.  <span data-ttu-id="84c0a-112">Legen Sie das Attribut [ \_ \_ \_ \_ Quelltyp des MF-devsource-Attributs](mf-devsource-attribute-source-type.md) auf einen der folgenden Werte fest:</span><span class="sxs-lookup"><span data-stu-id="84c0a-112">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to one of the following values:</span></span>

    | <span data-ttu-id="84c0a-113">Wert</span><span class="sxs-lookup"><span data-stu-id="84c0a-113">Value</span></span>                                                    | <span data-ttu-id="84c0a-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84c0a-114">Description</span></span>                      |
    |----------------------------------------------------------|----------------------------------|
    | <span data-ttu-id="84c0a-115">**MF \_ devsource \_ - \_ Attribut \_ Quelltyp ( \_ audcap- \_ GUID)**</span><span class="sxs-lookup"><span data-stu-id="84c0a-115">**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**</span></span> | <span data-ttu-id="84c0a-116">Listet audioerfassungs Geräte auf.</span><span class="sxs-lookup"><span data-stu-id="84c0a-116">Enumerate audio capture devices.</span></span> |
    | <span data-ttu-id="84c0a-117">**MF \_ devsource \_ - \_ Attribut \_ Quelltyp \_ VidCap \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="84c0a-117">**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**</span></span> | <span data-ttu-id="84c0a-118">Aufzählen von Video Erfassungs Geräten.</span><span class="sxs-lookup"><span data-stu-id="84c0a-118">Enumerate video capture devices.</span></span> |

    

     

3.  <span data-ttu-id="84c0a-119">Nennen Sie die Funktion " [**mfenumschlag der vicesources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) ".</span><span class="sxs-lookup"><span data-stu-id="84c0a-119">Call the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span> <span data-ttu-id="84c0a-120">Diese Funktion weist ein Array von [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeigern zu.</span><span class="sxs-lookup"><span data-stu-id="84c0a-120">This function allocates an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers.</span></span> <span data-ttu-id="84c0a-121">Jeder Zeiger stellt ein Aktivierungs Objekt für ein Gerät im System dar.</span><span class="sxs-lookup"><span data-stu-id="84c0a-121">Each pointer represents an activation object for one device on the system.</span></span>
4.  <span data-ttu-id="84c0a-122">Rufen Sie die [**imfactivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) -Methode auf, um eine Instanz der Medienquelle von einem der Aktivierungs Objekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84c0a-122">Call the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method to create an instance of the media source from one of the activation objects.</span></span>

<span data-ttu-id="84c0a-123">Im folgenden Beispiel wird eine Medienquelle für das erste Video Erfassungsgerät in der-Enumerationsliste erstellt:</span><span class="sxs-lookup"><span data-stu-id="84c0a-123">The following example creates a media source for the first video capture device in the enumeration list:</span></span>


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



<span data-ttu-id="84c0a-124">Sie können die Aktivierungs Objekte für verschiedene Attribute Abfragen, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="84c0a-124">You can query the activation objects for various attributes, including the following:</span></span>

-   <span data-ttu-id="84c0a-125">Das Attribut für den [ \_ \_ \_ benutzerfreundlichen \_ Namen des MF-devsource-Attributs](mf-devsource-attribute-friendly-name.md) enthält den anzeigen amen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="84c0a-125">The [MF\_DEVSOURCE\_ATTRIBUTE\_FRIENDLY\_NAME](mf-devsource-attribute-friendly-name.md) attribute contains the display name of the device.</span></span> <span data-ttu-id="84c0a-126">Der Anzeige Name eignet sich für die Anzeige für den Benutzer, ist jedoch möglicherweise nicht eindeutig.</span><span class="sxs-lookup"><span data-stu-id="84c0a-126">The display name is suitable for showing to the user, but might not be unique.</span></span>
-   <span data-ttu-id="84c0a-127">Für Videogeräte enthält das Attribut " [MF \_ devsource \_ Attribute \_ Source \_ Type \_ VidCap \_ symbolischen \_ Link](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) " den symbolischen Link zum Gerät.</span><span class="sxs-lookup"><span data-stu-id="84c0a-127">For video devices, the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute contains the symbolic link to the device.</span></span> <span data-ttu-id="84c0a-128">Mit der symbolischen Verknüpfung wird das Gerät im System eindeutig identifiziert, es handelt sich jedoch nicht um eine lesbare Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="84c0a-128">The symbolic link uniquely identifies the device on the system, but is not a readable string.</span></span>
-   <span data-ttu-id="84c0a-129">Für Audiogeräte enthält das Attribut " [MF \_ devsource \_ Attribute \_ Source \_ Type \_ audcap \_ EndPoint \_ ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) " die audioendpunkt-ID des Geräts.</span><span class="sxs-lookup"><span data-stu-id="84c0a-129">For audio devices, the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) attribute contains the audio endpoint ID of the device.</span></span> <span data-ttu-id="84c0a-130">Die audioendpunkt-ID ähnelt einem symbolischen Link.</span><span class="sxs-lookup"><span data-stu-id="84c0a-130">The audio endpoint ID is similar to a symbolic link.</span></span> <span data-ttu-id="84c0a-131">Es identifiziert das Gerät im System eindeutig, ist aber keine lesbare Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="84c0a-131">It uniquely identifies the device on the system, but is not a readable string.</span></span>

<span data-ttu-id="84c0a-132">Im folgenden Beispiel wird ein Array von [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeigern angenommen und der Anzeige Name der einzelnen Geräte im Debugfenster ausgegeben:</span><span class="sxs-lookup"><span data-stu-id="84c0a-132">The following example takes an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers and prints the display name of each device to the debug window:</span></span>


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



<span data-ttu-id="84c0a-133">Wenn Sie den symbolischen Link für ein Videogerät bereits kennen, gibt es eine weitere Möglichkeit, die Medienquelle für das Gerät zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="84c0a-133">If you already know the symbolic link for a video device, there is another way to create the media source for the device:</span></span>

1.  <span data-ttu-id="84c0a-134">Rufen Sie [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen Attribut Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84c0a-134">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span>
2.  <span data-ttu-id="84c0a-135">Legen Sie das Attribut [ \_ \_ \_ \_ Quelltyp des MF-devsource-Attributs](mf-devsource-attribute-source-type.md) auf das **MF \_ devsource- \_ Attribut \_ \_ Quelltyp \_ VidCap \_ GUID** fest.</span><span class="sxs-lookup"><span data-stu-id="84c0a-135">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="84c0a-136">Legen Sie das Attribut " [MF \_ devsource \_ Attribute \_ Source \_ Type \_ VidCap \_ symbolischen \_ Link](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) " auf den symbolischen Link fest.</span><span class="sxs-lookup"><span data-stu-id="84c0a-136">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute to the symbolic link.</span></span>
4.  <span data-ttu-id="84c0a-137">Aufrufen der Funktion [**mfkreatedevicesource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) oder [**mfkreatedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="84c0a-137">Call either the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span> <span data-ttu-id="84c0a-138">Der erste gibt einen [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="84c0a-138">The former returns an [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) pointer.</span></span> <span data-ttu-id="84c0a-139">Letztere gibt einen [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger auf ein Aktivierungs Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="84c0a-139">The latter returns an [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer to an activation object.</span></span> <span data-ttu-id="84c0a-140">Sie können das Activation-Objekt verwenden, um die Quelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84c0a-140">You can use the activation object to create the source.</span></span> <span data-ttu-id="84c0a-141">(Ein Aktivierungs Objekt kann an einen anderen Prozess gemarshallt werden. Daher ist es nützlich, wenn Sie die Quelle in einem anderen Prozess erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="84c0a-141">(An activation object can be marshaled to another process, so it is useful if you want to create the source in another process.</span></span> <span data-ttu-id="84c0a-142">Weitere Informationen finden Sie unter [Activation Objects](activation-objects.md).)</span><span class="sxs-lookup"><span data-stu-id="84c0a-142">For more information, see [Activation Objects](activation-objects.md).)</span></span>

<span data-ttu-id="84c0a-143">Im folgenden Beispiel wird die symbolische Verknüpfung eines Videogeräts erstellt und eine Medienquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="84c0a-143">The following example takes the symbolic link of a video device and creates a media source.</span></span>


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



<span data-ttu-id="84c0a-144">Es gibt eine entsprechende Methode zum Erstellen eines Audiogeräts über die audioendpunkt-ID:</span><span class="sxs-lookup"><span data-stu-id="84c0a-144">There is an equivalent way to create an audio device from the audio endpoint ID:</span></span>

1.  <span data-ttu-id="84c0a-145">Rufen Sie [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen Attribut Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84c0a-145">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span>
2.  <span data-ttu-id="84c0a-146">Legen Sie das Attribut [ \_ \_ \_ \_ Quelltyp des MF-devsource-Attributs](mf-devsource-attribute-source-type.md) auf das **MF \_ devsource- \_ Attribut \_ \_ Quelltyp " \_ audcap \_ GUID**"</span><span class="sxs-lookup"><span data-stu-id="84c0a-146">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="84c0a-147">Legen Sie das Attribut für den [MF \_ devsource- \_ Attribut \_ \_ Quelltyp " \_ audcap \_ EndPoint \_ ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) " der Endpunkt-ID fest.</span><span class="sxs-lookup"><span data-stu-id="84c0a-147">Set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_ENDPOINT\_ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) attribute to the endpoint ID.</span></span>
4.  <span data-ttu-id="84c0a-148">Aufrufen der Funktion [**mfkreatedevicesource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) oder [**mfkreatedevicesourceaktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .</span><span class="sxs-lookup"><span data-stu-id="84c0a-148">Call either the [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) function.</span></span>

<span data-ttu-id="84c0a-149">Im folgenden Beispiel wird eine audioendpunkt-ID angenommen und eine Medienquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="84c0a-149">The following example takes an audio endpoint ID and creates a media source.</span></span>


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



## <a name="use-a-capture-device"></a><span data-ttu-id="84c0a-150">Verwenden eines Erfassungs Geräts</span><span class="sxs-lookup"><span data-stu-id="84c0a-150">Use a capture device</span></span>

<span data-ttu-id="84c0a-151">Nachdem Sie die Medienquelle für ein Erfassungsgerät erstellt haben, rufen Sie mithilfe des [Quell Readers](source-reader.md) Daten vom Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="84c0a-151">After you create the media source for a capture device, use the [Source Reader](source-reader.md) to get data from the device.</span></span> <span data-ttu-id="84c0a-152">Der Quell Leser liefert Medien Beispiele, die die Aufzeichnungs Audiodaten oder Video Frames enthalten.</span><span class="sxs-lookup"><span data-stu-id="84c0a-152">The Source Reader delivers media samples that contain the capture audio data or video frames.</span></span> <span data-ttu-id="84c0a-153">Der nächste Schritt hängt von Ihrem Anwendungsszenario ab:</span><span class="sxs-lookup"><span data-stu-id="84c0a-153">The next step depends on your application scenario:</span></span>

-   <span data-ttu-id="84c0a-154">Video Vorschau: Verwenden Sie Microsoft Direct3D oder Direct2D, um das Video anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="84c0a-154">Video preview: Use Microsoft Direct3D or Direct2D to display the video.</span></span>
-   <span data-ttu-id="84c0a-155">Datei Erfassung: Verwenden Sie den [sendenden Writer](sink-writer.md) , um die Datei zu codieren.</span><span class="sxs-lookup"><span data-stu-id="84c0a-155">File capture: Use the [Sink Writer](sink-writer.md) to encode the file.</span></span>
-   <span data-ttu-id="84c0a-156">Audiovorschau: Verwenden Sie [WASAPI](/windows/desktop/CoreAudio/wasapi).</span><span class="sxs-lookup"><span data-stu-id="84c0a-156">Audio preview: Use [WASAPI](/windows/desktop/CoreAudio/wasapi).</span></span>

<span data-ttu-id="84c0a-157">Wenn Sie die Audioerfassung mit Video Erfassung kombinieren möchten, verwenden Sie die *Aggregat Medienquelle*.</span><span class="sxs-lookup"><span data-stu-id="84c0a-157">If you want to combine audio capture with video capture, use the *aggregate media source*.</span></span> <span data-ttu-id="84c0a-158">Die Aggregat Medienquelle enthält eine Sammlung von Medienquellen und kombiniert all ihre Streams zu einem einzelnen Medienquellen Objekt.</span><span class="sxs-lookup"><span data-stu-id="84c0a-158">The aggregate media source contains a collection of media sources and combines all of their streams into a single media source object.</span></span> <span data-ttu-id="84c0a-159">Um eine Instanz der aggregierten Medienquelle zu erstellen, rufen Sie die [**mfkreateaggregatesource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="84c0a-159">To create an instance of the aggregate media source, call the [**MFCreateAggregateSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) function.</span></span>

## <a name="shut-down-the-capture-device"></a><span data-ttu-id="84c0a-160">Geräte Erfassungsgerät Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="84c0a-160">Shut down the capture device</span></span>

<span data-ttu-id="84c0a-161">Wenn das Erfassungsgerät nicht mehr benötigt wird, müssen Sie das Gerät Herunterfahren, indem Sie [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) für das [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Objekt aufrufen, das Sie durch Aufrufen von [**mfcreatedevicesource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) oder [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject)abgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="84c0a-161">When the capture device is no longer needed, you must shut down the device by calling [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) object you obtained by calling [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) or [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> <span data-ttu-id="84c0a-162">Wenn das **herunter** fahren nicht aufgerufen wird, kann es zu Arbeitsspeicher Verknüpfungen kommen, da das System bis zum **herunter** fahren einen Verweis auf **imfmediasource** -Ressourcen aufbewahren kann.</span><span class="sxs-lookup"><span data-stu-id="84c0a-162">Failure to call **Shutdown** can result in memory links because the system may keep a reference to **IMFMediaSource** resources until **Shutdown** is called.</span></span>


```C++
if (g_pSource)
{
    g_pSource->Shutdown();
    g_pSource->Release();
    g_pSource = NULL;
}
```



<span data-ttu-id="84c0a-163">Wenn Sie einem Erfassungsgerät eine Zeichenfolge mit dem symbolischen Link zugeordnet haben, sollten Sie dieses Objekt auch freigeben.</span><span class="sxs-lookup"><span data-stu-id="84c0a-163">If you allocated a string containing the symbolic link to a capture device, you should release this object as well.</span></span>


```C++
    CoTaskMemFree(g_pwszSymbolicLink);
    g_pwszSymbolicLink = NULL;

    g_cchSymbolicLink = 0;
```



## <a name="related-topics"></a><span data-ttu-id="84c0a-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="84c0a-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84c0a-165">Audio-/Videoaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="84c0a-165">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> </dl>

 

 
