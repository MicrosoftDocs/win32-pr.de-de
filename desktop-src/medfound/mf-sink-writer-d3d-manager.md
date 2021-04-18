---
description: Enthält einen Zeiger auf den DXGI-Device Manager für den Senke-Writer.
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: MF_SINK_WRITER_D3D_MANAGER-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23dea964be1a0ff726a974deaf1949863331df1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352542"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a><span data-ttu-id="bfd92-103">MF \_ Sink \_ Writer \_ D3D \_ Manager-Attribut</span><span class="sxs-lookup"><span data-stu-id="bfd92-103">MF\_SINK\_WRITER\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="bfd92-104">Enthält einen Zeiger auf den DXGI-Device Manager für den [Senke-Writer](sink-writer.md).</span><span class="sxs-lookup"><span data-stu-id="bfd92-104">Contains a pointer to the DXGI Device Manager for the [Sink Writer](sink-writer.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="bfd92-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bfd92-105">Data type</span></span>

<span data-ttu-id="bfd92-106">**IMF dxgidebug Manager \** _ als " _*IUnknown \*\* " gespeichert_</span><span class="sxs-lookup"><span data-stu-id="bfd92-106">**IMFDXGIDeviceManager\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="remarks"></a><span data-ttu-id="bfd92-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfd92-107">Remarks</span></span>

<span data-ttu-id="bfd92-108">Der Wert dieses Attributs ist ein Zeiger auf die [_ *imfdxgidebug Manager* \*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bfd92-108">The value of this attribute is a pointer to the [_ *IMFDXGIDeviceManager*\*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span>

<span data-ttu-id="bfd92-109">Verwenden Sie dieses Attribut, um ein Direct3D-Gerät für alle Video Encoder oder Medien senken bereitzustellen, die vom senkenwriter geladen werden.</span><span class="sxs-lookup"><span data-stu-id="bfd92-109">Use this attribute to provide a Direct3D device for any video encoders or media sinks loaded by the Sink Writer.</span></span>

<span data-ttu-id="bfd92-110">Verwenden Sie dieses Attribut mit den folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="bfd92-110">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="bfd92-111">**Mfkreatesinkschreiterfrommediasink**</span><span class="sxs-lookup"><span data-stu-id="bfd92-111">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="bfd92-112">**MF | atesinkschreiterfromurl**</span><span class="sxs-lookup"><span data-stu-id="bfd92-112">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="bfd92-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfd92-113">Requirements</span></span>



| <span data-ttu-id="bfd92-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfd92-114">Requirement</span></span> | <span data-ttu-id="bfd92-115">Wert</span><span class="sxs-lookup"><span data-stu-id="bfd92-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfd92-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfd92-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bfd92-117">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bfd92-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="bfd92-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfd92-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bfd92-119">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bfd92-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="bfd92-120">Header</span><span class="sxs-lookup"><span data-stu-id="bfd92-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfd92-121"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="bfd92-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfd92-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfd92-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfd92-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="bfd92-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bfd92-124">Senke-Writer</span><span class="sxs-lookup"><span data-stu-id="bfd92-124">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 




