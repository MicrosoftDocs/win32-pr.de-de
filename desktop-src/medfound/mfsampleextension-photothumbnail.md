---
description: Enthält die Foto Miniaturansicht eines IMF Sample.
ms.assetid: 510706A3-92FB-4188-97B9-6E8E0B4B175F
title: MFSampleExtension_PhotoThumbnail-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cbdb6f79b1b1ee187677a7f1a7a7792acb10fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131116"
---
# <a name="mfsampleextension_photothumbnail-attribute"></a><span data-ttu-id="1ac48-103">MF SampleExtension- \_ photominiatur-Attribut</span><span class="sxs-lookup"><span data-stu-id="1ac48-103">MFSampleExtension\_PhotoThumbnail attribute</span></span>

<span data-ttu-id="1ac48-104">Enthält die Foto Miniaturansicht eines [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span><span class="sxs-lookup"><span data-stu-id="1ac48-104">Contains the photo thumbnail of a [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span>

## <a name="data-type"></a><span data-ttu-id="1ac48-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1ac48-105">Data type</span></span>

<span data-ttu-id="1ac48-106">**IUnknown** als **imfmediabuffer** gespeichert</span><span class="sxs-lookup"><span data-stu-id="1ac48-106">**IUnknown** stored as **IMFMediaBuffer**</span></span>

<span data-ttu-id="1ac48-107">Die Miniaturansicht wird mithilfe von " **ksproperty\tid \_ extendedcameracontrol**" konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="1ac48-107">The thumbnail is configured using the **KSPROPERTYSETID\_ExtendedCameraControl**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ac48-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ac48-108">Remarks</span></span>

<span data-ttu-id="1ac48-109">Dieses Attribut wird für das [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) festgelegt, das von MFT0 bereitgestellt wird, und ist die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle des [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) , der der Foto Miniaturansicht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1ac48-109">This attribute is set on the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) provided by the MFT0 and is the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) associated with the photo thumbnail.</span></span>

<span data-ttu-id="1ac48-110">Das Format der Foto Miniaturansicht kann JPEG (Major Type Image), NV12 oder ARGB32 sein.</span><span class="sxs-lookup"><span data-stu-id="1ac48-110">The format of the photo thumbnail can be JPEG (major type image), NV12 or ARGB32.</span></span>

<span data-ttu-id="1ac48-111">[Mfsampleextension \_ photothumbnailmediatype](mfsampleextension-photothumbnailmediatype.md) ist für Miniaturansichten erforderlich, um den Medientyp zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1ac48-111">The [MFSampleExtension\_PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md) is required for thumbnails to describe the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ac48-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ac48-112">Requirements</span></span>



| <span data-ttu-id="1ac48-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ac48-113">Requirement</span></span> | <span data-ttu-id="1ac48-114">Wert</span><span class="sxs-lookup"><span data-stu-id="1ac48-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ac48-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ac48-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1ac48-116">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1ac48-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="1ac48-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ac48-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1ac48-118">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1ac48-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="1ac48-119">Header</span><span class="sxs-lookup"><span data-stu-id="1ac48-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ac48-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ac48-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ac48-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ac48-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ac48-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="1ac48-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1ac48-123">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="1ac48-123">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> </dl>

 

 
