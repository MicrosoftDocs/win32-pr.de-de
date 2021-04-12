---
description: Gibt an, ob der Quell Leser eine DirectX-Videobeschleunigung (DXVA) im Video Decoder ermöglicht.
ms.assetid: ec539038-3fd3-41b7-a0e6-e75e3f2828a7
title: MF_SOURCE_READER_DISABLE_DXVA-Attribut (mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9362f067d1d6ceae426e9ee6530e08b95837595f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348738"
---
# <a name="mf_source_reader_disable_dxva-attribute"></a><span data-ttu-id="b1d07-103">MF- \_ Quell \_ Leser \_ deaktivierte \_ DXVA-Attribute</span><span class="sxs-lookup"><span data-stu-id="b1d07-103">MF\_SOURCE\_READER\_DISABLE\_DXVA attribute</span></span>

<span data-ttu-id="b1d07-104">Gibt an, ob der [Quell Leser](source-reader.md) eine DirectX-Videobeschleunigung (DXVA) im Video Decoder ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="b1d07-104">Specifies whether the [Source Reader](source-reader.md) enables DirectX Video Acceleration (DXVA) on the video decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="b1d07-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b1d07-105">Data type</span></span>

<span data-ttu-id="b1d07-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b1d07-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b1d07-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="b1d07-107">Get/set</span></span>

<span data-ttu-id="b1d07-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b1d07-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b1d07-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b1d07-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b1d07-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1d07-110">Remarks</span></span>

<span data-ttu-id="b1d07-111">Dieses Attribut gilt, wenn die folgenden Bedingungen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="b1d07-111">This attribute applies if the following conditions are true:</span></span>

-   <span data-ttu-id="b1d07-112">Der Quell Leser decodiert einen Videostream.</span><span class="sxs-lookup"><span data-stu-id="b1d07-112">The source reader decodes a video stream.</span></span>
-   <span data-ttu-id="b1d07-113">Der Video Decoder unterstützt die DXVA-Decodierung.</span><span class="sxs-lookup"><span data-stu-id="b1d07-113">The video decoder supports DXVA decoding.</span></span>
-   <span data-ttu-id="b1d07-114">Die Anwendung verwendet das [ \_ \_ \_ D3D \_ Manager](mf-source-reader-d3d-manager.md) -Attribut des MF-Quell Readers, um die [Direct3D-Device Manager](direct3d-device-manager.md) für den Quell Leser festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b1d07-114">The application uses the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute to set the [Direct3D Device Manager](direct3d-device-manager.md) on the source reader.</span></span>

<span data-ttu-id="b1d07-115">Dieses Attribut ermöglicht es der Anwendung, DXVA zu deaktivieren, während die Decodierung an Direct3D-Oberflächen noch nicht</span><span class="sxs-lookup"><span data-stu-id="b1d07-115">This attribute enables the application to disable DXVA while still decoding to Direct3D surfaces.</span></span>

<span data-ttu-id="b1d07-116">Standardmäßig verwendet der Quell Reader den [Direct3D-Device Manager](direct3d-device-manager.md) aus zwei Gründen:</span><span class="sxs-lookup"><span data-stu-id="b1d07-116">By default, the source reader uses the [Direct3D Device Manager](direct3d-device-manager.md) for two purposes:</span></span>

-   <span data-ttu-id="b1d07-117">, Um die DXVA-Decodierung im Video Decoder zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b1d07-117">To enable DXVA decoding in the video decoder.</span></span>
-   <span data-ttu-id="b1d07-118">, Um Direct3D-Oberflächen für die Videobeispiele zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="b1d07-118">To allocate Direct3D surfaces for the video samples.</span></span>

<span data-ttu-id="b1d07-119">Wenn der Wert des MF- \_ Quell \_ Readers \_ \_ DXVA-Attributs deaktiviert ist, deaktiviert der Quell Leser die DXVA-Decodierung, obwohl er weiterhin den Direct3D- [Device Manager](direct3d-device-manager.md) verwendet, um Direct3D-Oberflächen zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="b1d07-119">If the value of the MF\_SOURCE\_READER\_DISABLE\_DXVA attribute is **TRUE**, the source reader does disables DXVA decoding, although it still uses the [Direct3D Device Manager](direct3d-device-manager.md) to allocate Direct3D surfaces.</span></span>

<span data-ttu-id="b1d07-120">Wenn das [ \_ \_ \_ D3D \_ Manager](mf-source-reader-d3d-manager.md) -Attribut des MF-Quell Readers nicht festgelegt ist, \_ wird das \_ \_ DXVA-Attribut des MF-Quell Readers deaktiviert \_ .</span><span class="sxs-lookup"><span data-stu-id="b1d07-120">If the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute is not set, the MF\_SOURCE\_READER\_DISABLE\_DXVA attribute is ignored.</span></span>

<span data-ttu-id="b1d07-121">Der Standardwert dieses Attributs ist **false**. Dies bedeutet, dass die DXVA-Decodierung aktiviert ist, wenn verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b1d07-121">The default value of this attribute is **FALSE**, meaning that DXVA decoding is enabled when available.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1d07-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1d07-122">Requirements</span></span>



| <span data-ttu-id="b1d07-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1d07-123">Requirement</span></span> | <span data-ttu-id="b1d07-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b1d07-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1d07-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1d07-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b1d07-126">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b1d07-126">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b1d07-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1d07-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b1d07-128">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b1d07-128">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b1d07-129">Header</span><span class="sxs-lookup"><span data-stu-id="b1d07-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1d07-130"><dt>"Mfreadwrite. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b1d07-130"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1d07-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1d07-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1d07-132">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="b1d07-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b1d07-133">Quell Leser</span><span class="sxs-lookup"><span data-stu-id="b1d07-133">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="b1d07-134">Attribute des Quell Readers</span><span class="sxs-lookup"><span data-stu-id="b1d07-134">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




