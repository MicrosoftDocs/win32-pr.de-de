---
description: Gibt an, ob eine Medien Senke den Hardware Datenfluss unterstützt.
ms.assetid: 15838467-D253-4ECE-B9E7-AFD3A21B3AF2
title: MF_STREAM_SINK_SUPPORTS_HW_CONNECTION-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a95bfecba4cf53b6ef7c8863ec0456e310d8bcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485206"
---
# <a name="mf_stream_sink_supports_hw_connection-attribute"></a><span data-ttu-id="be8c8-103">Daten \_ Strom- \_ Senke \_ unterstützt das \_ HW- \_ Verbindungs Attribut</span><span class="sxs-lookup"><span data-stu-id="be8c8-103">MF\_STREAM\_SINK\_SUPPORTS\_HW\_CONNECTION attribute</span></span>

<span data-ttu-id="be8c8-104">Gibt an, ob eine Medien Senke den Hardware Datenfluss unterstützt.</span><span class="sxs-lookup"><span data-stu-id="be8c8-104">Indicates whether a media sink supports hardware data flow.</span></span>

## <a name="data-type"></a><span data-ttu-id="be8c8-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="be8c8-105">Data type</span></span>

<span data-ttu-id="be8c8-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be8c8-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="be8c8-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be8c8-107">Remarks</span></span>

<span data-ttu-id="be8c8-108">Dieses Attribut wird verwendet, wenn eine Medien Senke ein Hardware Gerät als Proxy verwendet und Daten über einen Hardwarebus empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="be8c8-108">This attribute is used when a media sink proxies a hardware device and is able to receive data over a hardware bus.</span></span> <span data-ttu-id="be8c8-109">Beispielsweise kann ein Hardware-Audiodecoder Audiodaten direkt an die audiorenderinghardware senden.</span><span class="sxs-lookup"><span data-stu-id="be8c8-109">For example, a hardware audio decoder might send audio data directly to the audio rendering hardware.</span></span>

<span data-ttu-id="be8c8-110">In diesem Szenario werden der Decoder und die Senke weiterhin in der Microsoft Media Foundation durch eine [Media Foundation Transformation](media-foundation-transforms.md) (MFT) und eine Medien Senke dargestellt.</span><span class="sxs-lookup"><span data-stu-id="be8c8-110">In this scenario, the decoder and the sink are still represented in the Microsoft Media Foundation by a [Media Foundation transform](media-foundation-transforms.md) (MFT) and a media sink.</span></span> <span data-ttu-id="be8c8-111">Zwischen diesen beiden Objekten auf der Pipeline Ebene werden jedoch keine Daten übertragen, sondern nur auf der Hardwareebene, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="be8c8-111">However, no data flows between these two objects at the pipeline layer, only at the hardware layer, as shown in the following diagram.</span></span>

![ein Diagramm, das eine Hardware Proxy Quelle anzeigt.](images/proxy-mft4.png)

<span data-ttu-id="be8c8-113">Die Verbindung zwischen dem MFT und der Medien Senke wird wie folgt ausgehandelt.</span><span class="sxs-lookup"><span data-stu-id="be8c8-113">The connection between the MFT and the media sink is negotiated as follows.</span></span>

1.  <span data-ttu-id="be8c8-114">Die Pipeline prüft, ob es sich bei der MFT um einen Hardware Proxy handelt, indem auf der MFT das Attribut Attribut für die MFT-Aufzählung der [ \_ Hardware- \_ \_ URL \_ ](mft-enum-hardware-url-attribute.md) überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="be8c8-114">The pipeline checks if the MFT is a hardware proxy, by checking for the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="be8c8-115">Weitere Informationen finden Sie unter [Hardware-MFTs](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="be8c8-115">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>
2.  <span data-ttu-id="be8c8-116">Die Pipeline erhält einen Zeiger auf die [**imfstreamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Schnittstelle der Stream-Senke in der Medien Senke.</span><span class="sxs-lookup"><span data-stu-id="be8c8-116">The pipeline gets a pointer to the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface of the stream sink on the media sink.</span></span>
3.  <span data-ttu-id="be8c8-117">Die Pipeline verwendet den [**imfstreamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Zeiger zum Abfragen der MF-Daten \_ Strom- \_ Senke \_ unterstützt das \_ HW- \_ Verbindungs Attribut.</span><span class="sxs-lookup"><span data-stu-id="be8c8-117">The pipeline uses the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer to query for the MF\_STREAM\_SINK\_SUPPORTS\_HW\_CONNECTION attribute.</span></span> <span data-ttu-id="be8c8-118">Wenn dieses Attribut vorhanden und gleich **true** ist, unterstützt die Medienquelle Hardware Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="be8c8-118">If this attribute is present and equal to **TRUE**, the media source supports hardware connections.</span></span>
4.  <span data-ttu-id="be8c8-119">Die Pipeline legt das [Attribut Attribut des verbundenen MFT- \_ \_ Streams \_ ](mft-connected-stream-attribute.md) in der streamsenke fest.</span><span class="sxs-lookup"><span data-stu-id="be8c8-119">The pipeline sets the [MFT\_CONNECTED\_STREAM\_ATTRIBUTE](mft-connected-stream-attribute.md) attribute on the stream sink.</span></span> <span data-ttu-id="be8c8-120">Der Wert dieses Attributs ist der [**imfattribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger aus dem MFT.</span><span class="sxs-lookup"><span data-stu-id="be8c8-120">The value of this attribute is the [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer from the MFT.</span></span>
5.  <span data-ttu-id="be8c8-121">Die Pipeline legt die mit dem [ \_ HW- \_ \_ \_ streamattribut verbundene MFT](mft-connected-to-hw-stream.md) für die streamsenke und die MFT auf " **true** " fest.</span><span class="sxs-lookup"><span data-stu-id="be8c8-121">The pipeline sets the [MFT\_CONNECTED\_TO\_HW\_STREAM](mft-connected-to-hw-stream.md) attribute to **TRUE** on both the stream sink and the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="be8c8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be8c8-122">Requirements</span></span>



| <span data-ttu-id="be8c8-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be8c8-123">Requirement</span></span> | <span data-ttu-id="be8c8-124">Wert</span><span class="sxs-lookup"><span data-stu-id="be8c8-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be8c8-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be8c8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="be8c8-126">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="be8c8-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="be8c8-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be8c8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="be8c8-128">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="be8c8-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="be8c8-129">Header</span><span class="sxs-lookup"><span data-stu-id="be8c8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="be8c8-130"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="be8c8-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be8c8-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be8c8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be8c8-132">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="be8c8-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




