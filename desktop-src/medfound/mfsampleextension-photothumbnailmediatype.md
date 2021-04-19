---
description: Enthält den imemediatype, der den Bild Formattyp beschreibt, der im "MF SampleExtension photominiatur"-Attribut enthalten ist \_ .
ms.assetid: BA727189-385D-4BA1-9F17-AC6ECDD20ABF
title: MFSampleExtension_PhotoThumbnailMediaType-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0e415fb0d3b062b4a5064006d3873cd42ea593
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106366552"
---
# <a name="mfsampleextension_photothumbnailmediatype-attribute"></a><span data-ttu-id="39cb1-103">MF SampleExtension- \_ photothumbnailmediatype-Attribut</span><span class="sxs-lookup"><span data-stu-id="39cb1-103">MFSampleExtension\_PhotoThumbnailMediaType attribute</span></span>

<span data-ttu-id="39cb1-104">Enthält den [**imemediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , der den Bild Formattyp beschreibt, der im " [MF SampleExtension \_ photominiatur](mfsampleextension-photothumbnail.md) "-Attribut enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="39cb1-104">Contains the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) which describes the image format type contained in the [MFSampleExtension\_PhotoThumbnail](mfsampleextension-photothumbnail.md) attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="39cb1-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="39cb1-105">Data type</span></span>

<span data-ttu-id="39cb1-106">" **IUnknown** " wurde als " **IMF MediaType** " gespeichert</span><span class="sxs-lookup"><span data-stu-id="39cb1-106">**IUnknown** stored as **IMFMediaType**</span></span>

## <a name="remarks"></a><span data-ttu-id="39cb1-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39cb1-107">Remarks</span></span>

<span data-ttu-id="39cb1-108">Wenn das Attribut " [mfsampleextension \_ photominiatur](mfsampleextension-photothumbnail.md) " im Photo Sample vorhanden ist, ist mfsampleextension " \_ photothumbnailmediatype" erforderlich und muss mindestens einen MF [MT- \_ \_ \_ Haupttyp](mf-mt-major-type-attribute.md), den [MF \_ MT- \_ Untertyp](mf-mt-subtype-attribute.md) und die [MF-MT- \_ \_ Frame \_ Größe](mf-mt-frame-size-attribute.md) enthalten, die die Miniaturansicht beschreiben.</span><span class="sxs-lookup"><span data-stu-id="39cb1-108">If the [MFSampleExtension\_PhotoThumbnail](mfsampleextension-photothumbnail.md) attribute is present on the photo sample, the MFSampleExtension\_PhotoThumbnailMediaType is required and must contain, at a minimum, [MF\_MT\_MAJOR\_TYPE](mf-mt-major-type-attribute.md), [MF\_MT\_SUBTYPE](mf-mt-subtype-attribute.md) and [MF\_MT\_FRAME\_SIZE](mf-mt-frame-size-attribute.md) which describe the thumbnail.</span></span>

## <a name="requirements"></a><span data-ttu-id="39cb1-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39cb1-109">Requirements</span></span>



| <span data-ttu-id="39cb1-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39cb1-110">Requirement</span></span> | <span data-ttu-id="39cb1-111">Wert</span><span class="sxs-lookup"><span data-stu-id="39cb1-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39cb1-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39cb1-112">Minimum supported client</span></span><br/> | <span data-ttu-id="39cb1-113">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="39cb1-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="39cb1-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39cb1-114">Minimum supported server</span></span><br/> | <span data-ttu-id="39cb1-115">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="39cb1-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="39cb1-116">Header</span><span class="sxs-lookup"><span data-stu-id="39cb1-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="39cb1-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="39cb1-117"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39cb1-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39cb1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39cb1-119">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="39cb1-119">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="39cb1-120">MF SampleExtension- \_ Fotoansicht</span><span class="sxs-lookup"><span data-stu-id="39cb1-120">MFSampleExtension\_PhotoThumbnail</span></span>](mfsampleextension-photothumbnail.md)
</dt> </dl>

 

 




