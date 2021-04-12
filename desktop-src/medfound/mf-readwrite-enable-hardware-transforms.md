---
description: Ermöglicht es dem Quell-oder senkenwriter, hardwarebasierte Media Foundation Transformationen (MFTs) zu verwenden.
ms.assetid: 03f2fa76-b828-40b1-929d-60e7d5ab49bb
title: MF_READWRITE_ENABLE_HARDWARE_TRANSFORMS-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 642be732a51f064d07e57609a886810f2a9c40b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347508"
---
# <a name="mf_readwrite_enable_hardware_transforms-attribute"></a><span data-ttu-id="cc4cc-103">MF- \_ Lesevorgang \_ enable \_ Hardware Transformationen- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="cc4cc-103">MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS attribute</span></span>

<span data-ttu-id="cc4cc-104">Ermöglicht es dem Quell-oder senkenwriter, hardwarebasierte Media Foundation Transformationen (MFTs) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cc4cc-104">Enables the source reader or sink writer to use hardware-based Media Foundation transforms (MFTs).</span></span>

## <a name="data-type"></a><span data-ttu-id="cc4cc-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="cc4cc-105">Data type</span></span>

<span data-ttu-id="cc4cc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cc4cc-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="cc4cc-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="cc4cc-107">Get/set</span></span>

<span data-ttu-id="cc4cc-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="cc4cc-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="cc4cc-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="cc4cc-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="cc4cc-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc4cc-110">Remarks</span></span>

<span data-ttu-id="cc4cc-111">Standardmäßig verwenden der Quell-und der sendende Writer keine Hardware-Decoder oder-Encoder.</span><span class="sxs-lookup"><span data-stu-id="cc4cc-111">By default, the source reader and sink writer do not use hardware decoders or encoders.</span></span> <span data-ttu-id="cc4cc-112">Um die Verwendung von Hardware-MFTs zu aktivieren, legen Sie dieses Attribut auf " **true** " fest, wenn Sie den Quell-oder sendenden Writer erstellen.</span><span class="sxs-lookup"><span data-stu-id="cc4cc-112">To enable the use of hardware MFTs, set this attribute to **TRUE** when you create the source reader or sink writer.</span></span>

<span data-ttu-id="cc4cc-113">Verwenden Sie dieses Attribut mit den folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="cc4cc-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="cc4cc-114">**MF | atesourcereaderfromb-testream**</span><span class="sxs-lookup"><span data-stu-id="cc4cc-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="cc4cc-115">**Mfkreatesourcereaderfrommediasource**</span><span class="sxs-lookup"><span data-stu-id="cc4cc-115">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="cc4cc-116">**MF | atesourcereaderfromurl**</span><span class="sxs-lookup"><span data-stu-id="cc4cc-116">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [<span data-ttu-id="cc4cc-117">**Mfkreatesinkschreiterfrommediasink**</span><span class="sxs-lookup"><span data-stu-id="cc4cc-117">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="cc4cc-118">**MF | atesinkschreiterfromurl**</span><span class="sxs-lookup"><span data-stu-id="cc4cc-118">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

<span data-ttu-id="cc4cc-119">Es gibt eine Ausnahme zum Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="cc4cc-119">There is one exception to the default behavior.</span></span> <span data-ttu-id="cc4cc-120">Der Quell-und sendende Writer verwendet automatisch MFTs, die lokal im Prozess des Aufrufers registriert sind.</span><span class="sxs-lookup"><span data-stu-id="cc4cc-120">The source reader and sink writer automatically use MFTs that are registered locally in the caller's process.</span></span> <span data-ttu-id="cc4cc-121">Um eine MFT lokal zu registrieren, müssen Sie [**mftregisterlocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) oder [**mftregisterlocalbyclsid**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cc4cc-121">To register an MFT locally, call [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid).</span></span> <span data-ttu-id="cc4cc-122">Lokal registrierte Hardware-MFTs werden auch dann verwendet, wenn das Paket "read- **\_ \_ \_ Hardware \_ Transformationen aktivieren** " nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cc4cc-122">Hardware MFTs that are registered locally are used even if the **MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS** attribute is not set.</span></span>

<span data-ttu-id="cc4cc-123">Dieses Attribut wirkt sich nicht auf die hardwarebeschleunigte Video Decodierung aus, die DirectX Video Acceleration (DXVA) verwendet.</span><span class="sxs-lookup"><span data-stu-id="cc4cc-123">This attribute does not affect hardware-accelerated video decoding that uses DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="cc4cc-124">Legen Sie zum Aktivieren der DXVA-Decodierung im Quell Leser das [ \_ \_ \_ D3D \_ Manager](mf-source-reader-d3d-manager.md) -Attribut des MF-Quell Readers fest.</span><span class="sxs-lookup"><span data-stu-id="cc4cc-124">To enable DXVA decoding in the source reader, set the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute.</span></span>

<span data-ttu-id="cc4cc-125">Wenn dieses Attribut auf **true** festgelegt ist, legen Sie das-Attribut für das [MF- \_ Lese schreiben \_ deaktiviert \_](mf-readwrite-disable-converters.md)</span><span class="sxs-lookup"><span data-stu-id="cc4cc-125">If this attribute is **TRUE**, do not set the [MF\_READWRITE\_DISABLE\_CONVERTERS](mf-readwrite-disable-converters.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc4cc-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc4cc-126">Requirements</span></span>



| <span data-ttu-id="cc4cc-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc4cc-127">Requirement</span></span> | <span data-ttu-id="cc4cc-128">Wert</span><span class="sxs-lookup"><span data-stu-id="cc4cc-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc4cc-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc4cc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cc4cc-130">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="cc4cc-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="cc4cc-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc4cc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cc4cc-132">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="cc4cc-132">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="cc4cc-133">Header</span><span class="sxs-lookup"><span data-stu-id="cc4cc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc4cc-134"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="cc4cc-134"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc4cc-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc4cc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc4cc-136">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="cc4cc-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cc4cc-137">Senkenwriter-Attribute</span><span class="sxs-lookup"><span data-stu-id="cc4cc-137">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="cc4cc-138">Attribute des Quell Readers</span><span class="sxs-lookup"><span data-stu-id="cc4cc-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




