---
description: Gibt an, ob eine Medienquelle den Hardware Datenfluss unterstützt.
ms.assetid: 32FEBC99-0AE0-4FE9-90AB-5FB204BD4C83
title: MF_SOURCE_STREAM_SUPPORTS_HW_CONNECTION-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751d672e664ab1849376d839285393075ddf6af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362875"
---
# <a name="mf_source_stream_supports_hw_connection-attribute"></a><span data-ttu-id="653e0-103">Der MF- \_ \_ Quellstream \_ unterstützt das \_ HW- \_ Verbindungs Attribut</span><span class="sxs-lookup"><span data-stu-id="653e0-103">MF\_SOURCE\_STREAM\_SUPPORTS\_HW\_CONNECTION attribute</span></span>

<span data-ttu-id="653e0-104">Gibt an, ob eine Medienquelle den Hardware Datenfluss unterstützt.</span><span class="sxs-lookup"><span data-stu-id="653e0-104">Indicates whether a media source supports hardware data flow.</span></span>

## <a name="data-type"></a><span data-ttu-id="653e0-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="653e0-105">Data type</span></span>

<span data-ttu-id="653e0-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="653e0-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="653e0-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="653e0-107">Remarks</span></span>

<span data-ttu-id="653e0-108">Dieses Attribut wird verwendet, wenn eine Medienquelle einen Proxy für ein Hardware Gerät verwendet und Daten nach unten über einen Hardwarebus übertragen kann, ohne dass Daten an die CPU gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="653e0-108">This attribute is used when a media source proxies a hardware device and is able to transfer data downstream over a hardware bus, without sending data up to the CPU.</span></span> <span data-ttu-id="653e0-109">Beispielsweise kann eine Webcam H. 264-codiertes Video direkt an einen integrierten Hardware Decoder übermitteln.</span><span class="sxs-lookup"><span data-stu-id="653e0-109">For example, a webcam might deliver H.264-encoded video directly to an integrated hardware decoder.</span></span>

<span data-ttu-id="653e0-110">In diesem Szenario werden Quelle und Decoder weiterhin in der Microsoft Media Foundation durch ein [Medienquellen](media-sources.md) Objekt und eine [Media Foundation Transformation](media-foundation-transforms.md) (MFT) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="653e0-110">In this scenario, the source and decoder are still represented in the Microsoft Media Foundation by a [media source](media-sources.md) object and a [Media Foundation transform](media-foundation-transforms.md) (MFT).</span></span> <span data-ttu-id="653e0-111">Zwischen diesen beiden Objekten auf der Pipeline Ebene werden jedoch keine Daten übertragen, sondern nur auf der Hardwareebene, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="653e0-111">However, no data flows between these two objects at the pipeline layer, only at the hardware layer, as shown in the following diagram.</span></span>

![ein Diagramm, das eine Hardware Proxy Quelle anzeigt.](images/proxy-mft3.png)

<span data-ttu-id="653e0-113">Die Verbindung zwischen der Medienquelle und der MFT wird wie folgt ausgehandelt.</span><span class="sxs-lookup"><span data-stu-id="653e0-113">The connection between the media source and the MFT is negotiated as follows.</span></span>

1.  <span data-ttu-id="653e0-114">Die Pipeline fragt die Medienquelle für die [**imfmediasourceex**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="653e0-114">The pipeline queries the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span> <span data-ttu-id="653e0-115">(Diese Schnittstelle ist für Medienquellen optional, die unterstützt.)</span><span class="sxs-lookup"><span data-stu-id="653e0-115">(This interface is optional for media sources to support.)</span></span>
2.  <span data-ttu-id="653e0-116">Die Pipeline ruft [**imfmediasourceex:: getstreamattributs**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) auf, um einen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="653e0-116">The pipeline calls [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
3.  <span data-ttu-id="653e0-117">Die Pipeline Abfragen für den MF- \_ Quelldaten \_ Strom \_ unterstützen das HW- \_ \_ Verbindungs Attribut.</span><span class="sxs-lookup"><span data-stu-id="653e0-117">The pipeline queries for the MF\_SOURCE\_STREAM\_SUPPORTS\_HW\_CONNECTION attribute.</span></span> <span data-ttu-id="653e0-118">Wenn das Attribut vorhanden und gleich **true** ist, unterstützt die Medienquelle Hardware Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="653e0-118">If the attribute is present and equal to **TRUE**, the media source supports hardware connections.</span></span>
4.  <span data-ttu-id="653e0-119">Die Pipeline prüft, ob es sich bei der MFT auch um einen Hardware Proxy handelt, indem auf der MFT das Attribut Attribut für die MFT-Aufzählung der [ \_ Hardware- \_ \_ URL \_ ](mft-enum-hardware-url-attribute.md) überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="653e0-119">The pipeline checks if the MFT is also a hardware proxy, by checking for the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="653e0-120">Weitere Informationen finden Sie unter [Hardware-MFTs](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="653e0-120">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>
5.  <span data-ttu-id="653e0-121">Die Pipeline legt das [Attribut Attribut des verbundenen MFT- \_ \_ Streams \_ ](mft-connected-stream-attribute.md) auf dem MFT fest.</span><span class="sxs-lookup"><span data-stu-id="653e0-121">The pipeline sets the [MFT\_CONNECTED\_STREAM\_ATTRIBUTE](mft-connected-stream-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="653e0-122">Der Wert dieses Attributs ist der [**imfattribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger, der aus der Medienquelle in Schritt 2 abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="653e0-122">The value of this attribute is the [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer obtained from the media source in step 2.</span></span>
6.  <span data-ttu-id="653e0-123">Die Pipeline legt die mit dem [ \_ HW- \_ \_ \_ streamattribut verbundene MFT](mft-connected-to-hw-stream.md) für die Medienquelle und die MFT auf " **true** " fest.</span><span class="sxs-lookup"><span data-stu-id="653e0-123">The pipeline sets the [MFT\_CONNECTED\_TO\_HW\_STREAM](mft-connected-to-hw-stream.md) attribute to **TRUE** on both the media source and the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="653e0-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="653e0-124">Requirements</span></span>



| <span data-ttu-id="653e0-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="653e0-125">Requirement</span></span> | <span data-ttu-id="653e0-126">Wert</span><span class="sxs-lookup"><span data-stu-id="653e0-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="653e0-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="653e0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="653e0-128">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="653e0-128">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="653e0-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="653e0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="653e0-130">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="653e0-130">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="653e0-131">Header</span><span class="sxs-lookup"><span data-stu-id="653e0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="653e0-132"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="653e0-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="653e0-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="653e0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="653e0-134">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="653e0-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="653e0-135">Hardware-MFTs</span><span class="sxs-lookup"><span data-stu-id="653e0-135">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> </dl>

 

 




