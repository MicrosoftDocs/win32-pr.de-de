---
description: Zum Umstellen von Mediendateien in das ASF-Format können Sie Windows Media Encoder verwenden. Um diese Encoder verwenden zu können, müssen Sie beim System registriert werden.
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: Erstellen eines Encoders mithilfe von cokreateingestance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a19a3ec13f60e7f602fa4f16854efa060dd96d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358811"
---
# <a name="creating-an-encoder-by-using-cocreateinstance"></a><span data-ttu-id="4e798-104">Erstellen eines Encoders mithilfe von cokreateingestance</span><span class="sxs-lookup"><span data-stu-id="4e798-104">Creating an Encoder by Using CoCreateInstance</span></span>

<span data-ttu-id="4e798-105">Zum Umstellen von Mediendateien in das ASF-Format können Sie Windows Media Encoder verwenden.</span><span class="sxs-lookup"><span data-stu-id="4e798-105">For converting media files into ASF format, you can use Windows Media encoders.</span></span> <span data-ttu-id="4e798-106">Um diese Encoder verwenden zu können, müssen Sie beim System registriert werden.</span><span class="sxs-lookup"><span data-stu-id="4e798-106">To use these encoders, they must be registered with the system.</span></span> <span data-ttu-id="4e798-107">Encoder werden als [Media Foundation Transformationen](media-foundation-transforms.md) (MFTs) implementiert und müssen die IMF Transform-Schnittstelle verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="4e798-107">Encoders are implemented as [Media Foundation transforms](media-foundation-transforms.md) (MFTs) and must expose the IMFTransform interface.</span></span> <span data-ttu-id="4e798-108">In diesem Thema wird beschrieben, wie eine Anwendung einen Zeiger auf die imftransform-Schnittstelle des erforderlichen MFT-Encoders erhält und diese für die Verwendung instanziieren kann.</span><span class="sxs-lookup"><span data-stu-id="4e798-108">This topic describes how an application can get a pointer to the required MFT encoder's IMFTransform interface and instantiate it for use.</span></span>

<span data-ttu-id="4e798-109">Weitere Informationen zur encoderregistrierung finden Sie unter [Instanziieren eines Encoders MFT](instantiating-the-encoder-mft.md).</span><span class="sxs-lookup"><span data-stu-id="4e798-109">For information about encoder registration, see [Instantiating an Encoder MFT](instantiating-the-encoder-mft.md).</span></span>

-   [<span data-ttu-id="4e798-110">Verwenden der IMF Transform-Schnittstelle eines Encoders</span><span class="sxs-lookup"><span data-stu-id="4e798-110">Using an Encoder's IMFTransform Interface</span></span>](#creating-an-encoder-by-using-cocreateinstance)
    -   [<span data-ttu-id="4e798-111">Beispiel für Codierungs Erstellung</span><span class="sxs-lookup"><span data-stu-id="4e798-111">Encoder Creation Example</span></span>](#encoder-creation-example)
-   [<span data-ttu-id="4e798-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4e798-112">Related topics</span></span>](#related-topics)

## <a name="using-an-encoders-imftransform-interface"></a><span data-ttu-id="4e798-113">Verwenden der IMF Transform-Schnittstelle eines Encoders</span><span class="sxs-lookup"><span data-stu-id="4e798-113">Using an Encoder's IMFTransform Interface</span></span>

<span data-ttu-id="4e798-114">Nach erfolgreicher Registrierung von Windows Media Encoder beim System kann eine Anwendung die Encoder durch Aufrufen von [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)auflisten.</span><span class="sxs-lookup"><span data-stu-id="4e798-114">Upon successful registration of Windows Media encoders with the system, an application can enumerate the encoders by calling [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum).</span></span> <span data-ttu-id="4e798-115">Um nach dem richtigen Encoder zu suchen, müssen Sie Folgendes angeben:</span><span class="sxs-lookup"><span data-stu-id="4e798-115">To search for the right encoder, you must specify the following:</span></span>

-   <span data-ttu-id="4e798-116">Die GUID, die die Kategorie darstellt, bei der es sich entweder um einen **\_ \_ \_ Audioencoder der MFT-Kategorie** oder um einen **\_ \_ Video \_ Encoder für die MFT**</span><span class="sxs-lookup"><span data-stu-id="4e798-116">The GUID that represents the category, which is either **MFT\_CATEGORY\_AUDIO\_ENCODER** or **MFT\_CATEGORY\_VIDEO\_ENCODER**.</span></span>

-   <span data-ttu-id="4e798-117">Das Format, das verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4e798-117">The format to match.</span></span> <span data-ttu-id="4e798-118">Dies wird in der [**MFT- \_ Register \_ Type \_ Info**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) -Struktur festgelegt, die den Haupttyp und den Untertyp des Medientyps angibt, in dem der Encoder Beispiele generiert.</span><span class="sxs-lookup"><span data-stu-id="4e798-118">This is set in the [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structure that specifies the major type and subtype of the media type that the encoder will generate samples in.</span></span> <span data-ttu-id="4e798-119">Diese Struktur wird im *poutputtype* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="4e798-119">This structure is passed in the *pOutputType* parameter.</span></span> <span data-ttu-id="4e798-120">Informationen zu den unterstützten Typen finden Sie unter [Medientyp-GUIDs](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="4e798-120">For information about the supported types, see [Media Type GUIDs](media-type-guids.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="4e798-121">Die Eingabetyp Informationen im *pinputtype* -Parameter sind nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4e798-121">The input type information in the *pInputType* parameter is not required.</span></span> <span data-ttu-id="4e798-122">Dies liegt daran, dass der Eingabetyp der Anwendung bekannt ist und der Encoder erwartet, dass der Eingabedaten Strom ein unkomprimiertes Format hat.</span><span class="sxs-lookup"><span data-stu-id="4e798-122">This is because the input type is known to the application and the encoder expects the input stream to be in an uncompressed format.</span></span>

     

<span data-ttu-id="4e798-123">[**Mfitenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) gibt ein Array von [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Zeigern für die Encoder-MFTs zurück, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4e798-123">[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) returns an array of [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointers for the encoder MFTs that match the search criteria.</span></span> <span data-ttu-id="4e798-124">Sie können einen Encoder instanziieren, indem Sie die com-Funktion **CoCreateInstance** aufrufen und die CLSID des Encoders übergeben, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="4e798-124">You can instantiate an encoder by calling the COM function **CoCreateInstance** and passing the CLSID of the encoder you want to use.</span></span> <span data-ttu-id="4e798-125">Diese Funktion gibt einen Zeiger auf die **imftransform** -Schnittstelle zurück, die den Encoder darstellt.</span><span class="sxs-lookup"><span data-stu-id="4e798-125">This function returns a pointer to the **IMFTransform** interface that represents the encoder.</span></span> <span data-ttu-id="4e798-126">Weitere Informationen zu diesem Funktions aufzurufen finden Sie in der Windows SDK-Dokumentation für die Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="4e798-126">For more information about this function call, see the Windows SDK documentation for the Component Object Model (COM).</span></span>

### <a name="encoder-creation-example"></a><span data-ttu-id="4e798-127">Beispiel für Codierungs Erstellung</span><span class="sxs-lookup"><span data-stu-id="4e798-127">Encoder Creation Example</span></span>

<span data-ttu-id="4e798-128">Im folgenden Codebeispiel wird gezeigt, wie ein Audio-oder Video Encoder erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4e798-128">The following code example shows how to create an audio or video encoder.</span></span>


```C++
HRESULT FindEncoder(
    const GUID& subtype, 
    BOOL bAudio, 
    IMFTransform **ppEncoder
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    CLSID *ppCLSIDs = NULL;

    MFT_REGISTER_TYPE_INFO info = { 0 };

    info.guidMajorType = bAudio ? MFMediaType_Audio : MFMediaType_Video;
    info.guidSubtype = subtype;

    hr = MFTEnum(   
        bAudio ? MFT_CATEGORY_AUDIO_ENCODER : MFT_CATEGORY_VIDEO_ENCODER,
        0,          // Reserved
        NULL,       // Input type
        &info,      // Output type
        NULL,       // Reserved
        &ppCLSIDs,
        &count
        );

    if (SUCCEEDED(hr) && count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first encoder in the list.

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(ppCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(ppEncoder));
    }

    CoTaskMemFree(ppCLSIDs);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="4e798-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4e798-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e798-130">Instanziieren eines MFT-Encoders</span><span class="sxs-lookup"><span data-stu-id="4e798-130">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="4e798-131">Windows Media Encoder</span><span class="sxs-lookup"><span data-stu-id="4e798-131">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



