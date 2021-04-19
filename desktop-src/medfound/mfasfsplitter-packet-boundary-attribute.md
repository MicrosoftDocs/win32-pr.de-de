---
description: Gibt an, ob ein Puffer den Anfang eines Pakets für das Advanced Systems Format (ASF) enthält.
ms.assetid: eca3f9b7-6051-4654-8016-a9c679519bc7
title: MFASFSPLITTER_PACKET_BOUNDARY-Attribut (wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044fd3ed635dc7cb45db1cb9e5c480481b06cd31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348828"
---
# <a name="mfasfsplitter_packet_boundary-attribute"></a><span data-ttu-id="5f905-103">Mfasarsplitter- \_ Paket \_ Begrenzungs Attribut</span><span class="sxs-lookup"><span data-stu-id="5f905-103">MFASFSPLITTER\_PACKET\_BOUNDARY attribute</span></span>

<span data-ttu-id="5f905-104">Gibt an, ob ein Puffer den Anfang eines Pakets für das Advanced Systems Format (ASF) enthält.</span><span class="sxs-lookup"><span data-stu-id="5f905-104">Specifies whether a buffer contains the start of an Advanced Systems Format (ASF) packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="5f905-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5f905-105">Data type</span></span>

<span data-ttu-id="5f905-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5f905-106">**UINT32**</span></span>

<span data-ttu-id="5f905-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="5f905-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f905-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f905-108">Remarks</span></span>

<span data-ttu-id="5f905-109">Wenn ein Medien Puffer die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle über **QueryInterface** verfügbar macht und der Wert dieses Attributs ungleich NULL ist, behandelt der ASF-Splitter den Puffer als Anfang eines neuen Pakets.</span><span class="sxs-lookup"><span data-stu-id="5f905-109">If a media buffer exposes the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface through **QueryInterface**, and the value of this attribute is nonzero, the ASF splitter treats the buffer as the start of a new packet.</span></span>

<span data-ttu-id="5f905-110">Dieses Attribut gilt, wenn Sie den ASF-Splitter zum Analysieren von ASF-Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="5f905-110">This attribute applies if you are using the ASF splitter to parse ASF data.</span></span> <span data-ttu-id="5f905-111">Wenn Ihre ASF-Daten über Variable Paket Längen verfügen, müssen Sie dieses Attribut für die Medien Puffer festlegen, die Sie an die [**imfasfsplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="5f905-111">If your ASF data has variable packet lengths, you must set this attribute on the media buffers that you pass to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="5f905-112">Legen Sie das-Attribut auf **true** fest, wenn der Puffer den Anfang eines neuen Pakets enthält.</span><span class="sxs-lookup"><span data-stu-id="5f905-112">Set the attribute to **TRUE** if the buffer contains the start of a new packet.</span></span> <span data-ttu-id="5f905-113">Wenn der Puffer eine Fortsetzung des vorherigen Pakets enthält, legen Sie das-Attribut auf " **false**" fest.</span><span class="sxs-lookup"><span data-stu-id="5f905-113">If the buffer contains a continuation of the previous packet, set the attribute to **FALSE**.</span></span> <span data-ttu-id="5f905-114">Die Puffer können nicht mehrere Pakete umfassen.</span><span class="sxs-lookup"><span data-stu-id="5f905-114">The buffers cannot span multiple packets.</span></span>

<span data-ttu-id="5f905-115">Bei ASF-Daten mit fester Paketgröße ist dieses Attribut nicht erforderlich, und ein Puffer kann mehrere Pakete umfassen.</span><span class="sxs-lookup"><span data-stu-id="5f905-115">For ASF data with fixed packet sizes, this attribute is not required, and a buffer can can span multiple packets.</span></span>

<span data-ttu-id="5f905-116">Beachten Sie, dass die Standard Implementierungen von [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) , die von Media Foundation bereitgestellt werden, keine [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="5f905-116">Note that the standard implementations of the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) provided by Media Foundation do not expose [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span> <span data-ttu-id="5f905-117">Um dieses Attribut zu verwenden, müssen Sie eine eigene Implementierung von **imfmediabuffer** bereitstellen. beispielsweise durch das umwickeln der von [**MF | atememorybuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer)zurückgegebenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="5f905-117">To use this attribute, you must provide your own implementation of **IMFMediaBuffer**; for example, by wrapping the buffers returned by [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f905-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f905-118">Requirements</span></span>



| <span data-ttu-id="5f905-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f905-119">Requirement</span></span> | <span data-ttu-id="5f905-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5f905-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f905-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f905-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5f905-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f905-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5f905-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f905-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5f905-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f905-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5f905-125">Header</span><span class="sxs-lookup"><span data-stu-id="5f905-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f905-126"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f905-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f905-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f905-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f905-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="5f905-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5f905-129">ASF-Attribute</span><span class="sxs-lookup"><span data-stu-id="5f905-129">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="5f905-130">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5f905-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="5f905-131">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="5f905-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="5f905-132">**Imfmediabuffer**</span><span class="sxs-lookup"><span data-stu-id="5f905-132">**IMFMediaBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
</dt> </dl>

 

 




