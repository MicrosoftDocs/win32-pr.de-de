---
description: Die Medientyp Konstanten sind unten definiert.
ms.assetid: 3e418c9a-a008-4b94-b5d2-7c2eccb3bf87
title: TAPIMEDIATYPE_ Konstanten (Tapi3. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71a7d7ffb411d84e99863bb89274e43200b319d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371281"
---
# <a name="tapimediatype_-constants"></a><span data-ttu-id="27058-103">Tapimediatype- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="27058-103">TAPIMEDIATYPE\_ Constants</span></span>

<span data-ttu-id="27058-104">Die folgenden Medientypen sind definiert:</span><span class="sxs-lookup"><span data-stu-id="27058-104">The following media types are defined:</span></span>



| <span data-ttu-id="27058-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="27058-105">Constant/value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="27058-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27058-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TAPIMEDIATYPE_AUDIO"></span><span id="tapimediatype_audio"></span><dl> <span data-ttu-id="27058-107"><dt>**Tapimediatype \_ Audiodatei**</dt> <dt>0x8</dt></span><span class="sxs-lookup"><span data-stu-id="27058-107"><dt>**TAPIMEDIATYPE\_AUDIO**</dt> <dt>0x8</dt></span></span> </dl>                    | <span data-ttu-id="27058-108">Ein audiomedienstream, der den Computer eingibt oder verlässt.</span><span class="sxs-lookup"><span data-stu-id="27058-108">An audio media stream that is entering or leaving the computer.</span></span> <span data-ttu-id="27058-109">Ein Eingabestream wird in der Regel auf Referenten abgespielt oder an ein Mobilgerät gesendet, und ein verlässt Stream wird in der Regel über ein Mikrofon oder Mobilgerät erfasst.</span><span class="sxs-lookup"><span data-stu-id="27058-109">An entering media stream would typically be played on speakers, or sent to a handset device and a leaving stream would typically be captured through a microphone or handset device.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="TAPIMEDIATYPE_VIDEO"></span><span id="tapimediatype_video"></span><dl> <span data-ttu-id="27058-110"><dt>**Tapimediatype \_ Video**</dt> <dt>0X8000</dt></span><span class="sxs-lookup"><span data-stu-id="27058-110"><dt>**TAPIMEDIATYPE\_VIDEO**</dt> <dt>0x8000</dt></span></span> </dl>                 | <span data-ttu-id="27058-111">Ein Video Mediendaten Strom, der den Computer eingibt oder verlässt.</span><span class="sxs-lookup"><span data-stu-id="27058-111">A video media stream that is entering or leaving the computer.</span></span> <span data-ttu-id="27058-112">Ein Eingabestream wird in der Regel in einem Videofenster gerendert, und ein belassen von Mediendaten wird normalerweise mit einer Videokamera aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="27058-112">An entering media stream would typically be rendered in a video window and a leaving media stream would typically be captured with a video camera.</span></span><br/>                                                                                                                                                                                                                                                                         |
| <span id="TAPIMEDIATYPE_DATAMODEM"></span><span id="tapimediatype_datamodem"></span><dl> <span data-ttu-id="27058-113"><dt>**Tapimediatype \_ DataModem**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="27058-113"><dt>**TAPIMEDIATYPE\_DATAMODEM**</dt> <dt>0x10</dt></span></span> </dl>       | <span data-ttu-id="27058-114">Ein Daten Mediendaten Strom, der einem Datenmodem zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="27058-114">A data media stream that is associated with a data modem.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="TAPIMEDIATYPE_G3FAX"></span><span id="tapimediatype_g3fax"></span><dl> <span data-ttu-id="27058-115"><dt>**Tapimediatype \_ G3FAX**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="27058-115"><dt>**TAPIMEDIATYPE\_G3FAX**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="27058-116">Ein Daten Mediendaten Strom, der einem G3-Protokoll Fax zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="27058-116">A data media stream that is associated with a G3 protocol fax.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="TAPIMEDIATYPE_MULTITRACK"></span><span id="tapimediatype_multitrack"></span><dl> <span data-ttu-id="27058-117"><dt>**Tapimediatype \_ Multitrack**</dt> <dt>0x10000</dt></span><span class="sxs-lookup"><span data-stu-id="27058-117"><dt>**TAPIMEDIATYPE\_MULTITRACK**</dt> <dt>0x10000</dt></span></span> </dl> | <span data-ttu-id="27058-118">Ein Stream befindet sich in einem Multitrack-Terminal.</span><span class="sxs-lookup"><span data-stu-id="27058-118">A stream is on a multitrack terminal.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="MEDIATYPE_RTP_Single_Stream"></span><span id="mediatype_rtp_single_stream"></span><span id="MEDIATYPE_RTP_SINGLE_STREAM"></span><dl> <span data-ttu-id="27058-119"><dt>**\_Einzelner RTP- \_ Stream für MediaType \_**</dt></span><span class="sxs-lookup"><span data-stu-id="27058-119"><dt>**MEDIATYPE\_RTP\_Single\_Stream**</dt></span></span> </dl>     | <span data-ttu-id="27058-120">Diese GUID wird zwischen einem von der Anwendung bereitgestellten Terminal und dem MSP-Stream verwendet.</span><span class="sxs-lookup"><span data-stu-id="27058-120">This GUID is used between an application supplied terminal and the MSP's stream.</span></span> <span data-ttu-id="27058-121">Wenn die PIN des Terminals diesen Medientyp unterstützt, tauscht der Stream unformatierte RTP-Daten mit dem Terminal aus.</span><span class="sxs-lookup"><span data-stu-id="27058-121">If the pin of the terminal supports this media type, the stream will exchange raw RTP data with the terminal.</span></span> <span data-ttu-id="27058-122">Dieser Modus wird nur von den Videostreams in h323 MSP und ipconf MSP für Windows 2000 SP1 oder höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="27058-122">This mode is supported only by the video streams on the H323 MSP and IPConf MSP for Windows 2000 SP1 or above.</span></span><br/> <span data-ttu-id="27058-123">**Header:** In "ipmsp. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="27058-123">**Header:** Declared in ipmsp.h.</span></span> <span data-ttu-id="27058-124">Der Header "ipmsp. h" ist in unter Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="27058-124">The header ipmsp.h is not available in in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="27058-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27058-125">Requirements</span></span>



| <span data-ttu-id="27058-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27058-126">Requirement</span></span> | <span data-ttu-id="27058-127">Wert</span><span class="sxs-lookup"><span data-stu-id="27058-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="27058-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="27058-128">TAPI version</span></span><br/> | <span data-ttu-id="27058-129">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="27058-129">Requires TAPI 3.0 or later</span></span><br/>                                              |
| <span data-ttu-id="27058-130">Header</span><span class="sxs-lookup"><span data-stu-id="27058-130">Header</span></span><br/>       | <dl> <span data-ttu-id="27058-131"><dt>Tapi3. h</dt></span><span class="sxs-lookup"><span data-stu-id="27058-131"><dt>Tapi3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27058-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27058-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27058-133">**Itqoabvent:: get- \_ mediaType**</span><span class="sxs-lookup"><span data-stu-id="27058-133">**ITQOSEvent::get\_MediaType**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_mediatype)
</dt> <dt>

[<span data-ttu-id="27058-134">**Itammediaformat:: get \_ Mediaformat**</span><span class="sxs-lookup"><span data-stu-id="27058-134">**ITAMMediaFormat::get\_MediaFormat**</span></span>](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-get_mediaformat)
</dt> <dt>

[<span data-ttu-id="27058-135">**Itammediaformat::p UT \_ Mediaformat**</span><span class="sxs-lookup"><span data-stu-id="27058-135">**ITAMMediaFormat::put\_MediaFormat**</span></span>](/windows/win32/api/tapi3/nf-tapi3-itammediaformat-put_mediaformat)
</dt> <dt>

[<span data-ttu-id="27058-136">**Itcallinfo:: get \_ callinfolong**</span><span class="sxs-lookup"><span data-stu-id="27058-136">**ITCallInfo::get\_CallInfoLong**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)
</dt> <dt>

[<span data-ttu-id="27058-137">**Itmediasupport:: get- \_ mediatypes**</span><span class="sxs-lookup"><span data-stu-id="27058-137">**ITMediaSupport::get\_MediaTypes**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itmediasupport-get_mediatypes)
</dt> <dt>

[<span data-ttu-id="27058-138">**Itterminalsupport:: "kreateterminal"**</span><span class="sxs-lookup"><span data-stu-id="27058-138">**ITTerminalSupport::CreateTerminal**</span></span>](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> </dl>

 

