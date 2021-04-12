---
description: In diesem Thema wird beschrieben, wie die Video Erfassungsgeräte im Benutzersystem aufgelistet werden und wie eine Instanz eines Geräts erstellt wird.
ms.assetid: b1267478-329b-4e46-a2ed-1ec11d2e2e6d
title: Auflisten von Video Erfassungs Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ccdbcf9df284cdccda09939d2d8a27174a2299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393270"
---
# <a name="enumerating-video-capture-devices"></a><span data-ttu-id="25639-103">Auflisten von Video Erfassungs Geräten</span><span class="sxs-lookup"><span data-stu-id="25639-103">Enumerating Video Capture Devices</span></span>

<span data-ttu-id="25639-104">In diesem Thema wird beschrieben, wie die Video Erfassungsgeräte im System des Benutzers aufgelistet werden und wie eine Instanz eines Geräts erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="25639-104">This topic describes how to enumerate the video capture devices on the user's system, and how create an instance of a device.</span></span>

<span data-ttu-id="25639-105">Gehen Sie folgendermaßen vor, um die Video Erfassungsgeräte auf dem System aufzulisten:</span><span class="sxs-lookup"><span data-stu-id="25639-105">To enumerate the video capture devices on the system, do the following:</span></span>

1.  <span data-ttu-id="25639-106">Rufen Sie [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen Attribut Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="25639-106">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span> <span data-ttu-id="25639-107">Diese Funktion empfängt einen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="25639-107">This function receives an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="25639-108">Aufrufen Sie [**imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) , um das Attribut [ \_ \_ \_ \_ Quelltyp des MF-devsource-Attributs](mf-devsource-attribute-source-type.md) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="25639-108">Call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) to set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute.</span></span> <span data-ttu-id="25639-109">Legen Sie den Attribut Wert auf das **MF \_ devsource- \_ Attribut \_ \_ Quelltyp \_ VidCap \_ GUID** fest.</span><span class="sxs-lookup"><span data-stu-id="25639-109">Set the attribute value to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="25639-110">[**Mfenumschlag mvicesources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)aufruft.</span><span class="sxs-lookup"><span data-stu-id="25639-110">Call [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources).</span></span> <span data-ttu-id="25639-111">Diese Funktion empfängt ein Array von [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeigern und der Array Größe.</span><span class="sxs-lookup"><span data-stu-id="25639-111">This function receives an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers and the array size.</span></span> <span data-ttu-id="25639-112">Jeder Zeiger stellt ein bestimmtes Video Erfassungsgerät dar.</span><span class="sxs-lookup"><span data-stu-id="25639-112">Each pointer represents a distinct video capture device.</span></span>

<span data-ttu-id="25639-113">So erstellen Sie eine Instanz eines Aufzeichnungs Geräts:</span><span class="sxs-lookup"><span data-stu-id="25639-113">To create an instance of a capture device:</span></span>

-   <span data-ttu-id="25639-114">Aufrufen von [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) zum Abrufen eines Zeigers auf die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="25639-114">Call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span>

<span data-ttu-id="25639-115">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="25639-115">The following code shows these steps:</span></span>


```C++
HRESULT CreateVideoDeviceSource(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    IMFMediaSource *pSource = NULL;
    IMFAttributes *pAttributes = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to specify the enumeration parameters.
    HRESULT hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Source type: video capture devices
    hr = pAttributes->SetGUID(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate devices.
    UINT32 count;
    hr = MFEnumDeviceSources(pAttributes, &ppDevices, &count);
    if (FAILED(hr))
    {
        goto done;
    }

    if (count == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Create the media source object.
    hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(&pSource));
    if (FAILED(hr))
    {
        goto done;
    }

    *ppSource = pSource;
    (*ppSource)->AddRef();

done:
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
    SafeRelease(&pSource);
    return hr;
}
```



<span data-ttu-id="25639-116">Nachdem Sie die Medienquelle erstellt haben, geben Sie die Schnittstellen Zeiger frei, und geben Sie den Speicher für das Array frei:</span><span class="sxs-lookup"><span data-stu-id="25639-116">After you create media source, release the interface pointers and free the memory for the array:</span></span>


```C++
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
```



## <a name="related-topics"></a><span data-ttu-id="25639-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="25639-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25639-118">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="25639-118">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



