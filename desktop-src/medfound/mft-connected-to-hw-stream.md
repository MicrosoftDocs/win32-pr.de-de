---
description: Gibt an, ob eine hardwarebasierte Media Foundation Transformation (MFT) mit einer anderen hardwarebasierten MFT verbunden ist.
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: MFT_CONNECTED_TO_HW_STREAM-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a3e8e4da74b3d581dd5ae4a53a03dc2b0fd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360133"
---
# <a name="mft_connected_to_hw_stream-attribute"></a><span data-ttu-id="28833-103">MFT- \_ Verbindung \_ mit dem \_ HW- \_ streamattribut</span><span class="sxs-lookup"><span data-stu-id="28833-103">MFT\_CONNECTED\_TO\_HW\_STREAM attribute</span></span>

<span data-ttu-id="28833-104">Gibt an, ob eine hardwarebasierte Media Foundation Transformation (MFT) mit einer anderen hardwarebasierten MFT verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="28833-104">Specifies whether a hardware-based Media Foundation transform (MFT) is connected to another hardware-based MFT.</span></span>

## <a name="data-type"></a><span data-ttu-id="28833-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="28833-105">Data type</span></span>

<span data-ttu-id="28833-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="28833-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="28833-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="28833-107">Get/set</span></span>

<span data-ttu-id="28833-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="28833-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="28833-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="28833-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="28833-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28833-110">Remarks</span></span>

<span data-ttu-id="28833-111">Anwendungen verwenden dieses Attribut in der Regel nicht.</span><span class="sxs-lookup"><span data-stu-id="28833-111">Applications typically do not use this attribute.</span></span>

<span data-ttu-id="28833-112">Dieses Attribut wird mit hardwarebasierten MFTs verwendet.</span><span class="sxs-lookup"><span data-stu-id="28833-112">This attribute is used with hardware-based MFTs.</span></span> <span data-ttu-id="28833-113">Wenn zwei Hardware-MFTs innerhalb einer Topologie verbunden sind, legt das topologielader dieses Attribut für die folgenden Objekte auf **true** fest:</span><span class="sxs-lookup"><span data-stu-id="28833-113">When two hardware MFTs are connected within a topology, the topology loader sets this attribute to **TRUE** on the following objects:</span></span>

-   <span data-ttu-id="28833-114">Der Ausgabestream der upstreammft</span><span class="sxs-lookup"><span data-stu-id="28833-114">The output stream of the upstream MFT</span></span>
-   <span data-ttu-id="28833-115">Der Eingabestream der Downstream-MFT</span><span class="sxs-lookup"><span data-stu-id="28833-115">The input stream of the downstream MFT</span></span>

<span data-ttu-id="28833-116">Um den Attribut Speicher für den Ausgabestream zu erhalten, ruft das topologielader [**imftransform:: getoutputstreamattributs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) auf der upstreammft auf.</span><span class="sxs-lookup"><span data-stu-id="28833-116">To get the attribute store for the output stream, the topology loader calls [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) on the upstream MFT.</span></span> <span data-ttu-id="28833-117">Um den Attribut Speicher für den Eingabestream zu erhalten, ruft das topologielader [**imftransform:: getinputstreamattribute auf dem downstreammft**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) auf.</span><span class="sxs-lookup"><span data-stu-id="28833-117">To get the attribute store for the input stream, the topology loader calls [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) on the downstream MFT.</span></span>

<span data-ttu-id="28833-118">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="28833-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="28833-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28833-119">Requirements</span></span>



| <span data-ttu-id="28833-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28833-120">Requirement</span></span> | <span data-ttu-id="28833-121">Wert</span><span class="sxs-lookup"><span data-stu-id="28833-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="28833-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28833-122">Minimum supported client</span></span><br/> | <span data-ttu-id="28833-123">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="28833-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="28833-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28833-124">Minimum supported server</span></span><br/> | <span data-ttu-id="28833-125">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="28833-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="28833-126">Header</span><span class="sxs-lookup"><span data-stu-id="28833-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="28833-127"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="28833-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28833-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28833-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28833-129">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="28833-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="28833-130">Hardware-MFTs</span><span class="sxs-lookup"><span data-stu-id="28833-130">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="28833-131">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="28833-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




