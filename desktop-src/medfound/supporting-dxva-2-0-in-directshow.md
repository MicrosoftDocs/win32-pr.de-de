---
description: In diesem Thema wird beschrieben, wie DirectX Video Acceleration (DXVA) 2,0 in einem DirectShow-Decoderfilter unterstützt wird.
ms.assetid: 40deaddb-bb17-4a34-8294-5c7dc8a8a457
title: Unterstützung von DXVA 2,0 in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda956b60d4905c2392e1a50bd62ee8421b944b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863407"
---
# <a name="supporting-dxva-20-in-directshow"></a><span data-ttu-id="0d6cd-103">Unterstützung von DXVA 2,0 in DirectShow</span><span class="sxs-lookup"><span data-stu-id="0d6cd-103">Supporting DXVA 2.0 in DirectShow</span></span>

<span data-ttu-id="0d6cd-104">In diesem Thema wird beschrieben, wie DirectX Video Acceleration (DXVA) 2,0 in einem DirectShow-Decoderfilter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-104">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a DirectShow decoder filter.</span></span> <span data-ttu-id="0d6cd-105">Insbesondere wird die Kommunikation zwischen dem Decoder und dem Videorenderer beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-105">Specifically, it describes the communication between the decoder and the video renderer.</span></span> <span data-ttu-id="0d6cd-106">In diesem Thema wird nicht beschrieben, wie DXVA-Decodierung implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-106">This topic does not describe how to implement DXVA decoding.</span></span>

-   [<span data-ttu-id="0d6cd-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="0d6cd-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="0d6cd-108">Hinweise zur Migration</span><span class="sxs-lookup"><span data-stu-id="0d6cd-108">Migration Notes</span></span>](#migration-notes)
-   [<span data-ttu-id="0d6cd-109">Suchen einer decoderkonfiguration</span><span class="sxs-lookup"><span data-stu-id="0d6cd-109">Finding a Decoder Configuration</span></span>](#finding-a-decoder-configuration)
-   [<span data-ttu-id="0d6cd-110">Benachrichtigen des Videorenderers</span><span class="sxs-lookup"><span data-stu-id="0d6cd-110">Notifying the Video Renderer</span></span>](#notifying-the-video-renderer)
-   [<span data-ttu-id="0d6cd-111">Zuordnen von nicht komprimierten Puffern</span><span class="sxs-lookup"><span data-stu-id="0d6cd-111">Allocating Uncompressed Buffers</span></span>](#allocating-uncompressed-buffers)
-   [<span data-ttu-id="0d6cd-112">Decodierung</span><span class="sxs-lookup"><span data-stu-id="0d6cd-112">Decoding</span></span>](#decoding)
-   [<span data-ttu-id="0d6cd-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d6cd-113">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="0d6cd-114">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="0d6cd-114">Prerequisites</span></span>

<span data-ttu-id="0d6cd-115">Dieses Thema setzt voraus, dass Sie mit dem Schreiben von DirectShow-Filtern vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-115">This topic assumes that you are familiar with writing DirectShow filters.</span></span> <span data-ttu-id="0d6cd-116">Weitere Informationen finden Sie im Thema [Schreiben von DirectShow-Filtern](../directshow/writing-directshow-filters.md) in der DirectShow-SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-116">For more information, see the topic [Writing DirectShow Filters](../directshow/writing-directshow-filters.md) in the DirectShow SDK documentation.</span></span> <span data-ttu-id="0d6cd-117">In den Codebeispielen in diesem Thema wird davon ausgegangen, dass der Decoderfilter von der [**ctransformfilter**](../directshow/ctransformfilter.md) -Klasse mit der folgenden Klassendefinition abgeleitet ist:</span><span class="sxs-lookup"><span data-stu-id="0d6cd-117">The code examples in this topic assume that the decoder filter is derived from the [**CTransformFilter**](../directshow/ctransformfilter.md) class, with the following class definition:</span></span>


```C++
class CDecoder : public CTransformFilter
{
public:
    static CUnknown* WINAPI CreateInstance(IUnknown *pUnk, HRESULT *pHr);

    HRESULT CompleteConnect(PIN_DIRECTION direction, IPin *pPin);

    HRESULT InitAllocator(IMemAllocator **ppAlloc);
    HRESULT DecideBufferSize(IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp);

    // TODO: The implementations of these methods depend on the specific decoder.
    HRESULT CheckInputType(const CMediaType *mtIn);
    HRESULT CheckTransform(const CMediaType *mtIn, const CMediaType *mtOut);
    HRESULT CTransformFilter::GetMediaType(int,CMediaType *);

private:
    CDecoder(HRESULT *pHr);
    ~CDecoder();

    CBasePin * GetPin(int n);

    HRESULT ConfigureDXVA2(IPin *pPin);
    HRESULT SetEVRForDXVA2(IPin *pPin);

    HRESULT FindDecoderConfiguration(
        /* [in] */  IDirectXVideoDecoderService *pDecoderService,
        /* [in] */  const GUID& guidDecoder, 
        /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
        /* [out] */ BOOL *pbFoundDXVA2Configuration
        );

private:
    IDirectXVideoDecoderService *m_pDecoderService;

    DXVA2_ConfigPictureDecode m_DecoderConfig;
    GUID                      m_DecoderGuid;
    HANDLE                    m_hDevice;

    FOURCC                    m_fccOutputFormat;
};
```



<span data-ttu-id="0d6cd-118">Im restlichen Teil dieses Themas verweist der Begriff " *Decoder* " auf den Decoder-Filter, der komprimierte Videos empfängt und unkomprimierte Videos ausgibt.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-118">In the remainder of this topic, the term *decoder* refers to the decoder filter, which receives compressed video and outputs uncompressed video.</span></span> <span data-ttu-id="0d6cd-119">Der Begriff " *Decoder-Gerät* " bezieht sich auf einen Hardware-Video Beschleuniger, der vom Grafiktreiber implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-119">The term *decoder device* refers to a hardware video accelerator implemented by the graphics driver.</span></span>

<span data-ttu-id="0d6cd-120">Dies sind die grundlegenden Schritte, die ein Decoder-Filter ausführen muss, um DXVA 2,0 zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="0d6cd-120">Here are the basic steps that a decoder filter must perform to support DXVA 2.0:</span></span>

1.  <span data-ttu-id="0d6cd-121">Aushandeln eines Medientyps.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-121">Negotiate a media type.</span></span>
2.  <span data-ttu-id="0d6cd-122">Suchen Sie die Konfiguration des DXVA-Decoders.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-122">Find a DXVA decoder configuration.</span></span>
3.  <span data-ttu-id="0d6cd-123">Benachrichtigen Sie den Videorenderer, dass der Decoder DXVA-Decodierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-123">Notify the video renderer that the decoder is using DXVA decoding.</span></span>
4.  <span data-ttu-id="0d6cd-124">Stellen Sie eine benutzerdefinierte Zuweisung bereit, die Direct3D-Oberflächen zuordnet.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-124">Provide a custom allocator that allocates Direct3D surfaces.</span></span>

<span data-ttu-id="0d6cd-125">Diese Schritte werden im weiteren Verlauf dieses Themas ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-125">These steps are described in more detail in the remainder of this topic.</span></span>

## <a name="migration-notes"></a><span data-ttu-id="0d6cd-126">Hinweise zur Migration</span><span class="sxs-lookup"><span data-stu-id="0d6cd-126">Migration Notes</span></span>

<span data-ttu-id="0d6cd-127">Wenn Sie von DXVA 1,0 migrieren, sollten Sie einige bedeutende Unterschiede zwischen den beiden Versionen beachten:</span><span class="sxs-lookup"><span data-stu-id="0d6cd-127">If you are migrating from DXVA 1.0, you should be aware of some significant differences between the two versions:</span></span>

-   <span data-ttu-id="0d6cd-128">DXVA 2,0 verwendet nicht die [**iamvideoaccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) -und [**iamvideoacceleratornotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) -Schnittstellen, da der Decoder direkt über die [**idirectxvideodecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) -Schnittstelle auf die DXVA 2,0-APIs zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-128">DXVA 2.0 does not use the [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) and [**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) interfaces, because the decoder can access the DXVA 2.0 APIs directly through the [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) interface.</span></span>
-   <span data-ttu-id="0d6cd-129">Während der Medientyp Aushandlung verwendet der Decoder keine Video-Acceleration-GUID als Untertyp.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-129">During media type negotiation, the decoder does not use a video acceleration GUID as the subtype.</span></span> <span data-ttu-id="0d6cd-130">Stattdessen ist der Untertyp nur das unkomprimierte Videoformat (z. b. NV12), wie bei der Software Decodierung.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-130">Instead, the subtype is just the uncompressed video format (such as NV12), as with software decoding.</span></span>
-   <span data-ttu-id="0d6cd-131">Das Verfahren zum Konfigurieren der Zugriffstaste hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-131">The procedure for configuring the accelerator has changed.</span></span> <span data-ttu-id="0d6cd-132">In DXVA 1,0 ruft der Decoder **Execute** mit einer **DXVA \_ configpicturedecode** -Struktur auf, um den accerlator zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-132">In DXVA 1.0, the decoder calls **Execute** with a **DXVA\_ConfigPictureDecode** structure to configure the accerlator.</span></span> <span data-ttu-id="0d6cd-133">In DXVA 2,0 verwendet der Decoder die [**idirectxvideodecoderservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) -Schnittstelle, wie im nächsten Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-133">In DXVA 2.0, the decoder uses the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface, as described in the next section.</span></span>
-   <span data-ttu-id="0d6cd-134">Der Decoder ordnet die nicht komprimierten Puffer zu.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-134">The decoder allocates the uncompressed buffers.</span></span> <span data-ttu-id="0d6cd-135">Der Videorenderer ordnet sie nicht mehr zu.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-135">The video renderer no longer allocates them.</span></span>
-   <span data-ttu-id="0d6cd-136">Anstelle des Aufrufs von [**iamvideoaccelerator::D isplayframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) , um den decodierten Frame anzuzeigen, übergibt der Decoder den Frame an den Renderer, indem er [**IMemInputPin:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive)anruft, wie beim Debuggen von Software.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-136">Instead of calling [**IAMVideoAccelerator::DisplayFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) to display the decoded frame, the decoder delivers the frame to the renderer by calling [**IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive), as with software decoding.</span></span>
-   <span data-ttu-id="0d6cd-137">Der Decoder ist nicht mehr dafür verantwortlich, zu überprüfen, wann Datenpuffer für Updates sicher sind.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-137">The decoder is no longer responsible for checking when data buffers are safe for updates.</span></span> <span data-ttu-id="0d6cd-138">Daher weist DXVA 2,0 keine Methode auf, die [**iamvideoaccelerator:: queryrenderstatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus)entspricht.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-138">Therefore DXVA 2.0 does not have any method equivalent to [**IAMVideoAccelerator::QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus).</span></span>
-   <span data-ttu-id="0d6cd-139">Die unter Bild Mischung erfolgt durch den Videorenderer mithilfe der DXVA 2.0-Videoprozessor-APIs.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-139">Subpicture blending is done by the video renderer, using the DXVA2.0 video processor APIs.</span></span> <span data-ttu-id="0d6cd-140">Decoderer, die Teilbilder bereitstellen (z. b. DVD-Decoders), sollten Teil Bilddaten an eine separate Ausgabe-PIN senden.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-140">Decoders that provide subpictures (for example, DVD decoders) should send subpicture data on a separate output pin.</span></span>

<span data-ttu-id="0d6cd-141">Für Decodierungs Vorgänge verwendet DXVA 2,0 die gleichen Datenstrukturen wie DXVA 1,0.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-141">For decoding operations, DXVA 2.0 uses the same data structures as DXVA 1.0.</span></span>

<span data-ttu-id="0d6cd-142">Der EVR-Filter (Enhanced Video Renderer) unterstützt DXVA 2,0.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-142">The enhanced video renderer (EVR) filter supports DXVA 2.0.</span></span> <span data-ttu-id="0d6cd-143">Die Filter für die Video Mischung Renderer (VMR-7 und VMR-9) unterstützen nur DXVA 1,0.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-143">The Video Mixing Renderer filters (VMR-7 and VMR-9) support DXVA 1.0 only.</span></span>

## <a name="finding-a-decoder-configuration"></a><span data-ttu-id="0d6cd-144">Suchen einer decoderkonfiguration</span><span class="sxs-lookup"><span data-stu-id="0d6cd-144">Finding a Decoder Configuration</span></span>

<span data-ttu-id="0d6cd-145">Nachdem der Decoder den Ausgabe Medientyp aushandiert hat, muss er eine kompatible Konfiguration für das DXVA-Decodergerät finden.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-145">After the decoder negotiates the output media type, it must find a compatible configuration for the DXVA decoder device.</span></span> <span data-ttu-id="0d6cd-146">Sie können diesen Schritt innerhalb der [**cbaseoutputpin:: completeconnect**](../directshow/cbaseoutputpin-completeconnect.md) -Methode der Ausgabe-PIN ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-146">You can perform this step inside the output pin's [**CBaseOutputPin::CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="0d6cd-147">Mit diesem Schritt wird sichergestellt, dass der Grafiktreiber die vom Decoder benötigten Funktionen unterstützt, bevor der Decoder die Verwendung von DXVA committet.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-147">This step ensures that the graphics driver supports the capabilities needed by the decoder, before the decoder commits to using DXVA.</span></span>

<span data-ttu-id="0d6cd-148">Gehen Sie folgendermaßen vor, um eine Konfiguration für das Decoder-Gerät zu finden:</span><span class="sxs-lookup"><span data-stu-id="0d6cd-148">To find a configuration for the decoder device, do the following:</span></span>

1.  <span data-ttu-id="0d6cd-149">Fragen Sie die Eingabe-PIN des Renderers für die [**IMF GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-149">Query the renderer's input pin for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="0d6cd-150">Aufrufen von [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , um einen Zeiger auf die [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-150">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span> <span data-ttu-id="0d6cd-151">Die Dienst-GUID ist der Mr- \_ Video \_ Acceleration \_ Service.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-151">The service GUID is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>
3.  <span data-ttu-id="0d6cd-152">Wenn Sie [**IDirect3DDeviceManager9:: opentovicehandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) aufzurufen, erhalten Sie ein Handle für das Direct3D-Gerät des Renderers.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-152">Call [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) to get a handle to the renderer's Direct3D device.</span></span>
4.  <span data-ttu-id="0d6cd-153">Aufrufen von [**IDirect3DDeviceManager9:: getvideoservice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) und übergeben des Geräte Handles.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-153">Call [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) and pass in the device handle.</span></span> <span data-ttu-id="0d6cd-154">Diese Methode gibt einen Zeiger auf die [**idirectxvideodecoderservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-154">This method returns a pointer to the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface.</span></span>
5.  <span data-ttu-id="0d6cd-155">Aufrufen von [**idirectxvideodecoderservice:: getdecoderdeviceguids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids).</span><span class="sxs-lookup"><span data-stu-id="0d6cd-155">Call [**IDirectXVideoDecoderService::GetDecoderDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids).</span></span> <span data-ttu-id="0d6cd-156">Diese Methode gibt ein Array von Decoder-Geräte-GUIDs zurück.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-156">This method returns an array of decoder device GUIDs.</span></span>
6.  <span data-ttu-id="0d6cd-157">Durchlaufen Sie das Array von decoderguids, um diejenigen zu finden, die der Decoder-Filter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-157">Loop through the array of decoder GUIDs to find the ones that the decoder filter supports.</span></span> <span data-ttu-id="0d6cd-158">Für einen MPEG-2-Decoder würden Sie z. b. nach **DXVA2 \_ ModeMPEG2 \_ mucomp**, **DXVA2 \_ ModeMPEG2 \_ IDCT** oder **DXVA2 \_ ModeMPEG2 \_ VLD** suchen.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-158">For example, for an MPEG-2 decoder, you would look for **DXVA2\_ModeMPEG2\_MOCOMP**, **DXVA2\_ModeMPEG2\_IDCT**, or **DXVA2\_ModeMPEG2\_VLD**.</span></span>

7.  <span data-ttu-id="0d6cd-159">Wenn Sie eine Geräte-GUID für den Kandidaten Decoder finden, übergeben Sie die GUID an die [**idirectxvideodecoderservice:: getdecoderrendertargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-159">When you find a candidate decoder device GUID, pass the GUID to the [**IDirectXVideoDecoderService::GetDecoderRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) method.</span></span> <span data-ttu-id="0d6cd-160">Diese Methode gibt ein Array von renderzielformaten zurück, die als **D3DFORMAT** -Werte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-160">This method returns an array of render target formats, specified as **D3DFORMAT** values.</span></span>
8.  <span data-ttu-id="0d6cd-161">Durchlaufen Sie die renderzielformate, und suchen Sie nach einem, das Ihrem Ausgabeformat entspricht.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-161">Loop through the render target formats and look for one that matches your output format.</span></span> <span data-ttu-id="0d6cd-162">In der Regel unterstützt ein Decoder-Gerät ein einzelnes renderzielformat.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-162">Typically, a decoder device supports a single render target format.</span></span> <span data-ttu-id="0d6cd-163">Der Decoderfilter sollte mithilfe dieses unter Typs eine Verbindung mit dem Renderer herstellen.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-163">The decoder filter should connect to the renderer using this subtype.</span></span> <span data-ttu-id="0d6cd-164">Beim ersten Aufrufe von [**completeconnect**](../directshow/cbaseoutputpin-completeconnect.md)kann der Decoder das renderzielformat determinimieren und dieses Format dann als bevorzugten Ausgabetyp zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-164">In the first call to [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md), the decoder can determing the render target format and then return this format as a preferred output type.</span></span>

9.  <span data-ttu-id="0d6cd-165">Aufrufen von [**idirectxvideodecoderservice:: getdecoderkonfigurationen**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations).</span><span class="sxs-lookup"><span data-stu-id="0d6cd-165">Call [**IDirectXVideoDecoderService::GetDecoderConfigurations**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations).</span></span> <span data-ttu-id="0d6cd-166">Übergeben Sie dieselbe Decoder-Geräte-GUID, zusammen mit einer [**DXVA2 \_ videodesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) -Struktur, die das vorgeschlagene Format beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-166">Pass in the same decoder device GUID, along with a [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure that describes the proposed format.</span></span> <span data-ttu-id="0d6cd-167">Die-Methode gibt ein Array von [**DXVA2 \_ configpicturedecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) -Strukturen zurück.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-167">The method returns an array of [**DXVA2\_ConfigPictureDecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) structures.</span></span> <span data-ttu-id="0d6cd-168">Jede Struktur beschreibt eine mögliche Konfiguration für das Decoder-Gerät.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-168">Each structure describes one possible configuration for the decoder device.</span></span>

10. <span data-ttu-id="0d6cd-169">Wenn Sie davon ausgehen, dass die vorherigen Schritte erfolgreich ausgeführt wurden, speichern Sie das Direct3D-Geräte handle, die Decoder-Geräte-GUID und die Konfigurations Struktur.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-169">Assuming that the previous steps are successful, store the Direct3D device handle, the decoder device GUID, and the configuration structure.</span></span> <span data-ttu-id="0d6cd-170">Der Filter verwendet diese Informationen zum Erstellen des Decoder-Geräts.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-170">The filter will use this information to create the decoder device.</span></span>

<span data-ttu-id="0d6cd-171">Der folgende Code zeigt, wie Sie eine decoderkonfiguration suchen.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-171">The following code shows how to find a decoder configuration.</span></span>


```C++
HRESULT CDecoder::ConfigureDXVA2(IPin *pPin)
{
    UINT    cDecoderGuids = 0;
    BOOL    bFoundDXVA2Configuration = FALSE;
    GUID    guidDecoder = GUID_NULL;

    DXVA2_ConfigPictureDecode config;
    ZeroMemory(&config, sizeof(config));

    // Variables that follow must be cleaned up at the end.

    IMFGetService               *pGetService = NULL;
    IDirect3DDeviceManager9     *pDeviceManager = NULL;
    IDirectXVideoDecoderService *pDecoderService = NULL;

    GUID   *pDecoderGuids = NULL; // size = cDecoderGuids
    HANDLE hDevice = INVALID_HANDLE_VALUE;

    // Query the pin for IMFGetService.
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pGetService));

    // Get the Direct3D device manager.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(

            MR_VIDEO_ACCELERATION_SERVICE,
            IID_PPV_ARGS(&pDeviceManager)
            );
    }

    // Open a new device handle.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    } 

    // Get the video decoder service.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->GetVideoService(
            hDevice, IID_PPV_ARGS(&pDecoderService));
    }

    // Get the decoder GUIDs.
    if (SUCCEEDED(hr))
    {
        hr = pDecoderService->GetDecoderDeviceGuids(
            &cDecoderGuids, &pDecoderGuids);
    }

    if (SUCCEEDED(hr))
    {
        // Look for the decoder GUIDs we want.
        for (UINT iGuid = 0; iGuid < cDecoderGuids; iGuid++)
        {
            // Do we support this mode?
            if (!IsSupportedDecoderMode(pDecoderGuids[iGuid]))
            {
                continue;
            }

            // Find a configuration that we support. 
            hr = FindDecoderConfiguration(pDecoderService, pDecoderGuids[iGuid],
                &config, &bFoundDXVA2Configuration);
            if (FAILED(hr))
            {
                break;
            }

            if (bFoundDXVA2Configuration)
            {
                // Found a good configuration. Save the GUID and exit the loop.
                guidDecoder = pDecoderGuids[iGuid];
                break;
            }
        }
    }

    if (!bFoundDXVA2Configuration)
    {
        hr = E_FAIL; // Unable to find a configuration.
    }

    if (SUCCEEDED(hr))
    {
        // Store the things we will need later.

        SafeRelease(&m_pDecoderService);
        m_pDecoderService = pDecoderService;
        m_pDecoderService->AddRef();

        m_DecoderConfig = config;
        m_DecoderGuid = guidDecoder;
        m_hDevice = hDevice;
    }

    if (FAILED(hr))
    {
        if (hDevice != INVALID_HANDLE_VALUE)
        {
            pDeviceManager->CloseDeviceHandle(hDevice);
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pDeviceManager);
    SafeRelease(&pDecoderService);
    return hr;
}
HRESULT CDecoder::FindDecoderConfiguration(
    /* [in] */  IDirectXVideoDecoderService *pDecoderService,
    /* [in] */  const GUID& guidDecoder, 
    /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
    /* [out] */ BOOL *pbFoundDXVA2Configuration
    )
{
    HRESULT hr = S_OK;
    UINT cFormats = 0;
    UINT cConfigurations = 0;

    D3DFORMAT                   *pFormats = NULL;     // size = cFormats
    DXVA2_ConfigPictureDecode   *pConfig = NULL;      // size = cConfigurations

    // Find the valid render target formats for this decoder GUID.
    hr = pDecoderService->GetDecoderRenderTargets(
        guidDecoder,
        &cFormats,
        &pFormats
        );

    if (SUCCEEDED(hr))
    {
        // Look for a format that matches our output format.
        for (UINT iFormat = 0; iFormat < cFormats;  iFormat++)
        {
            if (pFormats[iFormat] != (D3DFORMAT)m_fccOutputFormat)
            {
                continue;
            }

            // Fill in the video description. Set the width, height, format, 
            // and frame rate.
            DXVA2_VideoDesc videoDesc = {0};

            FillInVideoDescription(&videoDesc); // Private helper function.
            videoDesc.Format = pFormats[iFormat];

            // Get the available configurations.
            hr = pDecoderService->GetDecoderConfigurations(
                guidDecoder,
                &videoDesc,
                NULL, // Reserved.
                &cConfigurations,
                &pConfig
                );

            if (FAILED(hr))
            {
                break;
            }

            // Find a supported configuration.
            for (UINT iConfig = 0; iConfig < cConfigurations; iConfig++)
            {
                if (IsSupportedDecoderConfig(pConfig[iConfig]))
                {
                    // This configuration is good.
                    *pbFoundDXVA2Configuration = TRUE;
                    *pSelectedConfig = pConfig[iConfig];
                    break;
                }
            }

            CoTaskMemFree(pConfig);
            break;

        } // End of formats loop.
    }

    CoTaskMemFree(pFormats);

    // Note: It is possible to return S_OK without finding a configuration.
    return hr;
}
```



<span data-ttu-id="0d6cd-172">Da dieses Beispiel generisch ist, wurde ein Teil der Logik in Hilfsfunktionen eingefügt, die vom Decoder implementiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-172">Because this example is generic, some of the logic has been placed in helper functions that would need to be implemented by the decoder.</span></span> <span data-ttu-id="0d6cd-173">Der folgende Code zeigt die Deklarationen für diese Funktionen:</span><span class="sxs-lookup"><span data-stu-id="0d6cd-173">The following code shows the declarations for these functions:</span></span>


```C++
// Returns TRUE if the decoder supports a given decoding mode.
BOOL IsSupportedDecoderMode(const GUID& mode);

// Returns TRUE if the decoder supports a given decoding configuration.
BOOL IsSupportedDecoderConfig(const DXVA2_ConfigPictureDecode& config);

// Fills in a DXVA2_VideoDesc structure based on the input format.
void FillInVideoDescription(DXVA2_VideoDesc *pDesc);
```



## <a name="notifying-the-video-renderer"></a><span data-ttu-id="0d6cd-174">Benachrichtigen des Videorenderers</span><span class="sxs-lookup"><span data-stu-id="0d6cd-174">Notifying the Video Renderer</span></span>

<span data-ttu-id="0d6cd-175">Wenn der Decoder eine decoderkonfiguration findet, besteht der nächste Schritt darin, den Videorenderer zu benachrichtigen, dass der Decoder die Hardwarebeschleunigung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-175">If the decoder finds a decoder configuration, the next step is to notify the video renderer that the decoder will use hardware acceleration.</span></span> <span data-ttu-id="0d6cd-176">Sie können diesen Schritt innerhalb der [**completeconnect**](../directshow/cbaseoutputpin-completeconnect.md) -Methode ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-176">You can perform this step inside the [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="0d6cd-177">Dieser Schritt muss ausgeführt werden, bevor der Zuweiser ausgewählt wird, da er sich auf die Auswahl der Zuweisung auswirkt.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-177">This step must occur before the allocator is selected, because it affects how the allocator is selected.</span></span>

1.  <span data-ttu-id="0d6cd-178">Fragen Sie die Eingabe-PIN des Renderers für die [**IMF GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-178">Query the renderer's input pin for the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="0d6cd-179">Aufrufen von [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , um einen Zeiger auf die [**idirectxvideomemoryconfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-179">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) interface.</span></span> <span data-ttu-id="0d6cd-180">Die Dienst-GUID ist der **Mr- \_ Video \_ Acceleration \_ Service**.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-180">The service GUID is **MR\_VIDEO\_ACCELERATION\_SERVICE**.</span></span>
3.  <span data-ttu-id="0d6cd-181">Aufrufen von [**idirectxvideomemoryconfiguration:: getavailablesurfacetypeer byindex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) in einer Schleife, um die *dwtypeindex* -Variable von NULL zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-181">Call [**IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) in a loop, incrementing the *dwTypeIndex* variable from zero.</span></span> <span data-ttu-id="0d6cd-182">Beenden Sie, wenn die Methode den Wert **DXVA2 \_ surfacetype \_ decoderrendertarget** im *pdwtype* -Parameter zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-182">Stop when the method returns the value **DXVA2\_SurfaceType\_DecoderRenderTarget** in the *pdwType* parameter.</span></span> <span data-ttu-id="0d6cd-183">Mit diesem Schritt wird sichergestellt, dass der Videorenderer die hardwarebeschleunigte Decodierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-183">This step ensures that the video renderer supports hardware-accelerated decoding.</span></span> <span data-ttu-id="0d6cd-184">Dieser Schritt ist für den EVR-Filter immer erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-184">This step will always succeed for the EVR filter.</span></span>
4.  <span data-ttu-id="0d6cd-185">Wenn der vorherige Schritt erfolgreich war, nennen Sie [**idirectxvideomemoryconfiguration:: setsurfacetype**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) mit dem Wert DXVA2 \_ surfacetype \_ decoderrendertarget.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-185">If the previous step succeeded, call [**IDirectXVideoMemoryConfiguration::SetSurfaceType**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) with the value DXVA2\_SurfaceType\_DecoderRenderTarget.</span></span> <span data-ttu-id="0d6cd-186">Durch den Aufruf von **setsurfaketype** mit diesem Wert wird der Videorenderer in den DXVA-Modus versetzt.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-186">Calling **SetSurfaceType** with this value puts the video renderer into DXVA mode.</span></span> <span data-ttu-id="0d6cd-187">Wenn sich der Videorenderer in diesem Modus befindet, muss der Decoder seine eigene Zuweisung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-187">When the video renderer is in this mode, the decoder must provide its own allocator.</span></span>

<span data-ttu-id="0d6cd-188">Der folgende Code zeigt, wie Sie den Videorenderer benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-188">The following code shows how to notify the video renderer.</span></span>


```C++
HRESULT CDecoder::SetEVRForDXVA2(IPin *pPin)
{
    HRESULT hr = S_OK;

    IMFGetService                       *pGetService = NULL;
    IDirectXVideoMemoryConfiguration    *pVideoConfig = NULL;

    // Query the pin for IMFGetService.
    hr = pPin->QueryInterface(__uuidof(IMFGetService), (void**)&pGetService);

    // Get the IDirectXVideoMemoryConfiguration interface.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(
            MR_VIDEO_ACCELERATION_SERVICE, IID_PPV_ARGS(&pVideoConfig));
    }

    // Notify the EVR. 
    if (SUCCEEDED(hr))
    {
        DXVA2_SurfaceType surfaceType;

        for (DWORD iTypeIndex = 0; ; iTypeIndex++)
        {
            hr = pVideoConfig->GetAvailableSurfaceTypeByIndex(iTypeIndex, &surfaceType);
            
            if (FAILED(hr))
            {
                break;
            }

            if (surfaceType == DXVA2_SurfaceType_DecoderRenderTarget)
            {
                hr = pVideoConfig->SetSurfaceType(DXVA2_SurfaceType_DecoderRenderTarget);
                break;
            }
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pVideoConfig);

    return hr;
}
```



<span data-ttu-id="0d6cd-189">Wenn der Decoder eine gültige Konfiguration findet und den Videorenderer erfolgreich benachrichtigt, kann der Decoder DXVA für die Decodierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-189">If the decoder finds a valid configuration and successfully notifies the video renderer, the decoder can use DXVA for decoding.</span></span> <span data-ttu-id="0d6cd-190">Der Decoder muss eine benutzerdefinierte Zuweisung für seine Ausgabe-PIN implementieren, wie im nächsten Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-190">The decoder must implement a custom allocator for its output pin, as described in the next section.</span></span>

## <a name="allocating-uncompressed-buffers"></a><span data-ttu-id="0d6cd-191">Zuordnen von nicht komprimierten Puffern</span><span class="sxs-lookup"><span data-stu-id="0d6cd-191">Allocating Uncompressed Buffers</span></span>

<span data-ttu-id="0d6cd-192">In DXVA 2,0 ist der Decoder für das Zuordnen von Direct3D-Oberflächen zur Verwendung als nicht komprimierte Video Puffer verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-192">In DXVA 2.0, the decoder is responsible for allocating Direct3D surfaces to use as uncompressed video buffers.</span></span> <span data-ttu-id="0d6cd-193">Daher muss der Decoder einen benutzerdefinierten Zuweiser implementieren, der die Oberflächen erstellt.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-193">Therefore, the decoder must implement a custom allocator that will create the surfaces.</span></span> <span data-ttu-id="0d6cd-194">Die von dieser Zuweisung bereitgestellten Medien Beispiele enthalten Zeiger auf die Direct3D-Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-194">The media samples provided by this allocator will hold pointers to the Direct3D surfaces.</span></span> <span data-ttu-id="0d6cd-195">Der EVR Ruft einen Zeiger auf die-Oberfläche ab, indem er [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) im Medien Beispiel aufruft.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-195">The EVR retrieves a pointer to the surface by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the media sample.</span></span> <span data-ttu-id="0d6cd-196">Der Dienst Bezeichner ist der **Mr- \_ Puffer \_ Dienst**.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-196">The service identifier is **MR\_BUFFER\_SERVICE**.</span></span>

<span data-ttu-id="0d6cd-197">Führen Sie die folgenden Schritte aus, um die benutzerdefinierte Zuweisung bereitzustellen:</span><span class="sxs-lookup"><span data-stu-id="0d6cd-197">To provide the custom allocator, perform the following steps:</span></span>

1.  <span data-ttu-id="0d6cd-198">Definieren Sie eine Klasse für die Medien Beispiele.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-198">Define a class for the media samples.</span></span> <span data-ttu-id="0d6cd-199">Diese Klasse kann von der [**cmediasample**](../directshow/cmediasample.md) -Klasse abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-199">This class can derive from the [**CMediaSample**](../directshow/cmediasample.md) class.</span></span> <span data-ttu-id="0d6cd-200">Führen Sie in dieser Klasse die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="0d6cd-200">Inside this class, do the following:</span></span>
    -   <span data-ttu-id="0d6cd-201">Speichert einen Zeiger auf die Direct3D-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-201">Store a pointer to the Direct3D surface.</span></span>
    -   <span data-ttu-id="0d6cd-202">Implementieren Sie die [**IMF GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-202">Implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span> <span data-ttu-id="0d6cd-203">Fragen Sie in der [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) -Methode, wenn es sich bei der Dienst-GUID um den **\_ Puffer \_ Dienst** handelt, die Direct3D-Oberfläche nach der angeforderten Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0d6cd-203">In the [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) method, if the service GUID is **MR\_BUFFER\_SERVICE**, query the Direct3D surface for the requested interface.</span></span> <span data-ttu-id="0d6cd-204">Andernfalls kann **GetService** den **\_ \_ nicht unterstützten MF- \_ Dienst** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-204">Otherwise, **GetService** can return **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
    -   <span data-ttu-id="0d6cd-205">Überschreiben Sie die [**cmediasample:: getpointer**](../directshow/cmediasample-getpointer.md) -Methode, um E \_ notimpl zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-205">Override the [**CMediaSample::GetPointer**](../directshow/cmediasample-getpointer.md) method to return E\_NOTIMPL.</span></span>
2.  <span data-ttu-id="0d6cd-206">Definieren Sie eine Klasse für die Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-206">Define a class for the allocator.</span></span> <span data-ttu-id="0d6cd-207">Die Zuweisung kann von der [**cbasezucator**](../directshow/cbaseallocator.md) -Klasse abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-207">The allocator can derive from the [**CBaseAllocator**](../directshow/cbaseallocator.md) class.</span></span> <span data-ttu-id="0d6cd-208">Führen Sie in dieser Klasse die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="0d6cd-208">Inside this class, do the following.</span></span>
    -   <span data-ttu-id="0d6cd-209">Überschreiben Sie die [**cbasezucator:: zugsc**](../directshow/cbaseallocator-alloc.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-209">Override the [**CBaseAllocator::Alloc**](../directshow/cbaseallocator-alloc.md) method.</span></span> <span data-ttu-id="0d6cd-210">Rufen Sie in dieser Methode [**idirectxvideoaccelerationservice:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) auf, um die Oberflächen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-210">Inside this method, call [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) to create the surfaces.</span></span> <span data-ttu-id="0d6cd-211">(Die [**idirectxvideodecoderservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) -Schnittstelle erbt diese Methode von [**idirectxvideoaccelerationservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).)</span><span class="sxs-lookup"><span data-stu-id="0d6cd-211">(The [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) interface inherits this method from [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).)</span></span>
    -   <span data-ttu-id="0d6cd-212">Überschreiben Sie die [**cbasezucator:: Free**](../directshow/cbaseallocator-free.md) -Methode, um die Oberflächen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-212">Override the [**CBaseAllocator::Free**](../directshow/cbaseallocator-free.md) method to release the surfaces.</span></span>
3.  <span data-ttu-id="0d6cd-213">Überschreiben Sie in der Ausgabe-PIN Ihres Filters die [**cbaseoutputpin:: init-**](../directshow/cbaseoutputpin-initallocator.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-213">In your filter's output pin, override the [**CBaseOutputPin::InitAllocator**](../directshow/cbaseoutputpin-initallocator.md) method.</span></span> <span data-ttu-id="0d6cd-214">Erstellen Sie innerhalb dieser Methode eine Instanz Ihrer benutzerdefinierten Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-214">Inside this method, create an instance of your custom allocator.</span></span>
4.  <span data-ttu-id="0d6cd-215">Implementieren Sie in Ihrem Filter die [**ctransformfilter::D ecidebuffersize**](../directshow/ctransformfilter-decidebuffersize.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-215">In your filter, implement the [**CTransformFilter::DecideBufferSize**](../directshow/ctransformfilter-decidebuffersize.md) method.</span></span> <span data-ttu-id="0d6cd-216">Der *pproperties* -Parameter gibt die Anzahl der für das EVR erforderlichen Oberflächen an.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-216">The *pProperties* parameter indicates the number of surfaces that the EVR requires.</span></span> <span data-ttu-id="0d6cd-217">Fügen Sie diesem Wert die Anzahl der vom Decoder benötigten Oberflächen hinzu, und nennen Sie [**imemzuzucator:: SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) für die Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-217">Add to this value the number of surfaces that your decoder requires, and call [**IMemAllocator::SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) on the allocator.</span></span>

<span data-ttu-id="0d6cd-218">Der folgende Code zeigt, wie die Beispiel Klasse "Media" implementiert wird:</span><span class="sxs-lookup"><span data-stu-id="0d6cd-218">The following code shows how to implement the media sample class:</span></span>


```C++
class CDecoderSample : public CMediaSample, public IMFGetService
{
    friend class CDecoderAllocator;

public:

    CDecoderSample(CDecoderAllocator *pAlloc, HRESULT *phr)
        : CMediaSample(NAME("DecoderSample"), (CBaseAllocator*)pAlloc, phr, NULL, 0),
          m_pSurface(NULL),
          m_dwSurfaceId(0)
    { 
    }

    // Note: CMediaSample does not derive from CUnknown, so we cannot use the
    //       DECLARE_IUNKNOWN macro that is used by most of the filter classes.

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        CheckPointer(ppv, E_POINTER);

        if (riid == IID_IMFGetService)
        {
            *ppv = static_cast<IMFGetService*>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            return CMediaSample::QueryInterface(riid, ppv);
        }
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return CMediaSample::AddRef();
    }

    STDMETHODIMP_(ULONG) Release()
    {
        // Return a temporary variable for thread safety.
        ULONG cRef = CMediaSample::Release();
        return cRef;
    }

    // IMFGetService::GetService
    STDMETHODIMP GetService(REFGUID guidService, REFIID riid, LPVOID *ppv)
    {
        if (guidService != MR_BUFFER_SERVICE)
        {
            return MF_E_UNSUPPORTED_SERVICE;
        }
        else if (m_pSurface == NULL)
        {
            return E_NOINTERFACE;
        }
        else
        {
            return m_pSurface->QueryInterface(riid, ppv);
        }
    }

    // Override GetPointer because this class does not manage a system memory buffer.
    // The EVR uses the MR_BUFFER_SERVICE service to get the Direct3D surface.
    STDMETHODIMP GetPointer(BYTE ** ppBuffer)
    {
        return E_NOTIMPL;
    }

private:

    // Sets the pointer to the Direct3D surface. 
    void SetSurface(DWORD surfaceId, IDirect3DSurface9 *pSurf)
    {
        SafeRelease(&m_pSurface);

        m_pSurface = pSurf;
        if (m_pSurface)
        {
            m_pSurface->AddRef();
        }

        m_dwSurfaceId = surfaceId;
    }

    IDirect3DSurface9   *m_pSurface;
    DWORD               m_dwSurfaceId;
};
```



<span data-ttu-id="0d6cd-219">Der folgende Code zeigt, wie die [**Zuordnungsmethode**](../directshow/cbaseallocator-alloc.md) für die Zuweisung implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-219">The following code shows how to implement the [**Alloc**](../directshow/cbaseallocator-alloc.md) method on the allocator.</span></span>


```C++
HRESULT CDecoderAllocator::Alloc()
{
    CAutoLock lock(this);

    HRESULT hr = S_OK;

    if (m_pDXVA2Service == NULL)
    {
        return E_UNEXPECTED;
    }

    hr = CBaseAllocator::Alloc();

    // If the requirements have not changed, do not reallocate.
    if (hr == S_FALSE)
    {
        return S_OK;
    }

    if (SUCCEEDED(hr))
    {
        // Free the old resources.
        Free();

        // Allocate a new array of pointers.
        m_ppRTSurfaceArray = new (std::nothrow) IDirect3DSurface9*[m_lCount];
        if (m_ppRTSurfaceArray == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            ZeroMemory(m_ppRTSurfaceArray, sizeof(IDirect3DSurface9*) * m_lCount);
        }
    }

    // Allocate the surfaces.
    if (SUCCEEDED(hr))
    {
        hr = m_pDXVA2Service->CreateSurface(
            m_dwWidth,
            m_dwHeight,
            m_lCount - 1,
            (D3DFORMAT)m_dwFormat,
            D3DPOOL_DEFAULT,
            0,
            DXVA2_VideoDecoderRenderTarget,
            m_ppRTSurfaceArray,
            NULL
            );
    }

    if (SUCCEEDED(hr))
    {
        for (m_lAllocated = 0; m_lAllocated < m_lCount; m_lAllocated++)
        {
            CDecoderSample *pSample = new (std::nothrow) CDecoderSample(this, &hr);

            if (pSample == NULL)
            {
                hr = E_OUTOFMEMORY;
                break;
            }
            if (FAILED(hr))
            {
                break;
            }
            // Assign the Direct3D surface pointer and the index.
            pSample->SetSurface(m_lAllocated, m_ppRTSurfaceArray[m_lAllocated]);

            // Add to the sample list.
            m_lFree.Add(pSample);
        }
    }

    if (SUCCEEDED(hr))
    {
        m_bChanged = FALSE;
    }
    return hr;
}
```



<span data-ttu-id="0d6cd-220">Dies ist der Code für die [**Free**](../directshow/cbaseallocator-free.md) -Methode:</span><span class="sxs-lookup"><span data-stu-id="0d6cd-220">Here is the code for the [**Free**](../directshow/cbaseallocator-free.md) method:</span></span>


```C++
void CDecoderAllocator::Free()
{
    CMediaSample *pSample = NULL;

    do
    {
        pSample = m_lFree.RemoveHead();
        if (pSample)
        {
            delete pSample;
        }
    } while (pSample);

    if (m_ppRTSurfaceArray)
    {
        for (long i = 0; i < m_lAllocated; i++)
        {
            SafeRelease(&m_ppRTSurfaceArray[i]);
        }

        delete [] m_ppRTSurfaceArray;
    }
    m_lAllocated = 0;
}
```



<span data-ttu-id="0d6cd-221">Weitere Informationen zum Implementieren von benutzerdefinierten Zuweisungen finden Sie im Thema [Bereitstellen einer benutzerdefinierten Zuweisung](../directshow/providing-a-custom-allocator.md) in der DirectShow-SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-221">For more information about implementing custom allocators, see the topic [Providing a Custom Allocator](../directshow/providing-a-custom-allocator.md) in the DirectShow SDK documentation.</span></span>

## <a name="decoding"></a><span data-ttu-id="0d6cd-222">Decodierung</span><span class="sxs-lookup"><span data-stu-id="0d6cd-222">Decoding</span></span>

<span data-ttu-id="0d6cd-223">Um das Decoder-Gerät zu erstellen, rufen Sie [**idirectxvideodecoderservice:: createvideodecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder)auf.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-223">To create the decoder device, call [**IDirectXVideoDecoderService::CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder).</span></span> <span data-ttu-id="0d6cd-224">Die-Methode gibt einen Zeiger auf die [**idirectxvideodecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) -Schnittstelle des Decoder-Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-224">The method returns a pointer to the [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) interface of the decoder device.</span></span>

<span data-ttu-id="0d6cd-225">Bei jedem Frame wird [**IDirect3DDeviceManager9:: testdevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) aufgerufen, um das Geräte Handle zu testen.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-225">On each frame, call [**IDirect3DDeviceManager9::TestDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) to test the device handle.</span></span> <span data-ttu-id="0d6cd-226">Wenn sich das Gerät geändert hat, gibt die Methode DXVA2 \_ E \_ New \_ Video Device zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="0d6cd-226">If the device has changed, the method returns DXVA2\_E\_NEW\_VIDEO\_DEVICE.</span></span> <span data-ttu-id="0d6cd-227">Wenn dies der Fall ist, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="0d6cd-227">If this occurs, do the following:</span></span>

1.  <span data-ttu-id="0d6cd-228">Schließen Sie das Geräte Handle durch Aufrufen von [**IDirect3DDeviceManager9:: closedevicehandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).</span><span class="sxs-lookup"><span data-stu-id="0d6cd-228">Close the device handle by calling [**IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).</span></span>
2.  <span data-ttu-id="0d6cd-229">Geben Sie die Zeiger [**idirectxvideodecoderservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) und [**idirectxvideodecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) frei.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-229">Release the [**IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) and [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) pointers.</span></span>
3.  <span data-ttu-id="0d6cd-230">Öffnen Sie ein neues Geräte handle.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-230">Open a new device handle.</span></span>
4.  <span data-ttu-id="0d6cd-231">Aushandeln Sie eine neue decoderkonfiguration, wie im Abschnitt Suchen [einer decoderkonfiguration](#finding-a-decoder-configuration)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-231">Negotiate a new decoder configuration, as described in the section [Finding a Decoder Configuration](#finding-a-decoder-configuration).</span></span>
5.  <span data-ttu-id="0d6cd-232">Erstellen Sie ein neues Decoder-Gerät.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-232">Create a new decoder device.</span></span>

<span data-ttu-id="0d6cd-233">Wenn das Geräte Handle gültig ist, funktioniert der Decodierungs Prozess wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0d6cd-233">Assuming that the device handle is valid, the decoding process works as follows:</span></span>

1.  <span data-ttu-id="0d6cd-234">Aufrufen von [**idirectxvideodecoder:: beginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).</span><span class="sxs-lookup"><span data-stu-id="0d6cd-234">Call [**IDirectXVideoDecoder::BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).</span></span>
2.  <span data-ttu-id="0d6cd-235">Führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="0d6cd-235">Do the following one or more times:</span></span>
    1.  <span data-ttu-id="0d6cd-236">Aufrufen von [**idirectxvideodecoder:: GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) zum Abrufen eines DXVA-decoderpuffers.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-236">Call [**IDirectXVideoDecoder::GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) to get a DXVA decoder buffer.</span></span>
    2.  <span data-ttu-id="0d6cd-237">Füllen Sie den Puffer aus.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-237">Fill the buffer.</span></span>
    3.  <span data-ttu-id="0d6cd-238">Nennen Sie [**idirectxvideodecoder:: ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).</span><span class="sxs-lookup"><span data-stu-id="0d6cd-238">Call [**IDirectXVideoDecoder::ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).</span></span>
3.  <span data-ttu-id="0d6cd-239">Nennen Sie [**idirectxvideodecoder:: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) , um die Decodierungs Vorgänge für den Frame auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-239">Call [**IDirectXVideoDecoder::Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) to perform the decoding operations on the frame.</span></span>

<span data-ttu-id="0d6cd-240">DXVA 2,0 verwendet die gleichen Datenstrukturen wie DXVA 1,0 für Decodierungs Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-240">DXVA 2.0 uses the same data structures as DXVA 1.0 for decoding operations.</span></span> <span data-ttu-id="0d6cd-241">Für den ursprünglichen Satz von DXVA-Profilen (für h. 261, h. 263 und MPEG-2) werden diese Datenstrukturen in der [Spezifikation DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-241">For the original set of DXVA profiles (for H.261, H.263, and MPEG-2), these data structures are described in the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

<span data-ttu-id="0d6cd-242">In jedem Paar von [**beginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)- / [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) -aufrufen können Sie [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) mehrmals aufrufen, aber nur einmal für jeden DXVA-Puffer.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-242">Within each pair of [**BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)/[**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) calls, you may call [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) multiple times, but only once for each type of DXVA buffer.</span></span> <span data-ttu-id="0d6cd-243">Wenn Sie es zweimal mit dem gleichen Puffertyp aufzurufen, überschreiben Sie die Daten.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-243">If you call it twice with the same buffer type, you will overwrite the data.</span></span>

<span data-ttu-id="0d6cd-244">Rufen Sie nach dem Aufrufen von [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) [**IMemInputPin:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) auf, um den Frame an den Videorenderer zu übermitteln, wie bei der Software Decodierung.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-244">After calling [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute), call [**IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) to deliver the frame to the video renderer, as with software decoding.</span></span> <span data-ttu-id="0d6cd-245">Die **Receive** -Methode ist asynchron. nach dem zurückkehren kann der Decoder den nächsten Frame Decodierungs Vorgang fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-245">The **Receive** method is asynchronous; after it returns, the decoder can continue decoding the next frame.</span></span> <span data-ttu-id="0d6cd-246">Der Anzeigetreiber verhindert, dass Decodierungs Befehle den Puffer überschreiben, während der Puffer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-246">The display driver prevents any decoding commands from overwriting the buffer while the buffer is in use.</span></span> <span data-ttu-id="0d6cd-247">Der Decoder sollte keine Oberfläche wieder verwenden, um einen anderen Frame zu decodieren, bis der Renderer das Beispiel freigegeben hat.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-247">The decoder should not reuse a surface to decode another frame until the renderer has released the sample.</span></span> <span data-ttu-id="0d6cd-248">Wenn der Renderer das Beispiel freigibt, fügt die Zuweisung das Beispiel wieder in den Pool der verfügbaren Beispiele ein.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-248">When the renderer releases the sample, the allocator puts the sample back into its pool of available samples.</span></span> <span data-ttu-id="0d6cd-249">Rufen Sie zum Abrufen des nächsten verfügbaren Beispiels [**cbaseoutputpin:: getdeliverybuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md)auf, das wiederum [**imemzuzukator:: GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer)aufruft.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-249">To get the next available sample, call [**CBaseOutputPin::GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md), which in turn calls [**IMemAllocator::GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer).</span></span> <span data-ttu-id="0d6cd-250">Weitere Informationen finden Sie im Thema [Übersicht über den Datenfluss in DirectShow](../directshow/overview-of-data-flow-in-directshow.md) in der DirectShow-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="0d6cd-250">For more information, see the topic [Overview of Data Flow in DirectShow](../directshow/overview-of-data-flow-in-directshow.md) in the DirectShow documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d6cd-251">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d6cd-251">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d6cd-252">DirectX-Video Beschleunigung 2,0</span><span class="sxs-lookup"><span data-stu-id="0d6cd-252">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
