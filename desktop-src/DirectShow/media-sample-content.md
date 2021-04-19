---
description: Beschreibt den Inhalt eines elementaren Datenstroms innerhalb eines MPEG-2-Transportdaten Stroms. Diese Enumeration wird in der IMPEG2PIDMap-Schnittstelle verwendet, die auf den Ausgabe Pins des MPEG-2-demultiplexers implementiert ist.
ms.assetid: 989ad56b-b5af-4811-889e-c79fcd3f7f01
title: MEDIA_SAMPLE_CONTENT Enumeration (bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SAMPLE_CONTENT
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 9065f2af948ff28d181b24842673b086882837bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370602"
---
# <a name="media_sample_content-enumeration"></a><span data-ttu-id="71aaf-104">\_Aufzählung von Medien Sample- \_ Inhalten</span><span class="sxs-lookup"><span data-stu-id="71aaf-104">MEDIA\_SAMPLE\_CONTENT enumeration</span></span>

<span data-ttu-id="71aaf-105">Beschreibt den Inhalt eines elementaren Datenstroms innerhalb eines MPEG-2-Transportdaten Stroms.</span><span class="sxs-lookup"><span data-stu-id="71aaf-105">Describes the contents of an elementary stream within an MPEG-2 transport stream.</span></span> <span data-ttu-id="71aaf-106">Diese Enumeration wird in der [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) -Schnittstelle verwendet, die auf den Ausgabe Pins des [MPEG-2-demultiplexers](mpeg-2-demultiplexer.md)implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="71aaf-106">This enumeration is used in the [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) interface, which is implemented on the output pins of the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="71aaf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="71aaf-107">Syntax</span></span>


```C++
typedef enum  { 
  MEDIA_TRANSPORT_PACKET,
  MEDIA_ELEMENTARY_STREAM,
  MEDIA_MPEG2_PSI,
  MEDIA_TRANSPORT_PAYLOAD
} MEDIA_SAMPLE_CONTENT;
```



## <a name="constants"></a><span data-ttu-id="71aaf-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="71aaf-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="71aaf-109"><span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**Medien \_ Transport \_ Paket**</span><span class="sxs-lookup"><span data-stu-id="71aaf-109"><span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**MEDIA\_TRANSPORT\_PACKET**</span></span>
</dt> <dd>

<span data-ttu-id="71aaf-110">Gibt ein umfassendes transportstreampaket an, das ohne Verarbeitung durchlaufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="71aaf-110">Specifies a complete transport stream packet to be passed through without processing.</span></span>

</dd> <dt>

<span data-ttu-id="71aaf-111"><span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**Daten \_ Strom für Medien \_**</span><span class="sxs-lookup"><span data-stu-id="71aaf-111"><span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**MEDIA\_ELEMENTARY\_STREAM**</span></span>
</dt> <dd>

<span data-ttu-id="71aaf-112">Gibt eine Nutzlast für Audiodaten oder Videos an.</span><span class="sxs-lookup"><span data-stu-id="71aaf-112">Specifies an audio or video PES payload.</span></span>

</dd> <dt>

<span data-ttu-id="71aaf-113"><span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**Medien- \_ MPEG2 \_ PSI**</span><span class="sxs-lookup"><span data-stu-id="71aaf-113"><span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA\_MPEG2\_PSI**</span></span>
</dt> <dd>

<span data-ttu-id="71aaf-114">Gibt einen Pat-, PMT-, Cat-oder privaten Datenstrom an.</span><span class="sxs-lookup"><span data-stu-id="71aaf-114">Specifies a PAT, PMT, CAT, or Private data stream.</span></span> <span data-ttu-id="71aaf-115">Hierbei handelt es sich um umfassende PSI-Abschnitte, die nicht erneut zusammengefügt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="71aaf-115">These are complete PSI sections which do not need to be reassembled.</span></span>

</dd> <dt>

<span data-ttu-id="71aaf-116"><span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**Nutzlast für Medien \_ Transport \_**</span><span class="sxs-lookup"><span data-stu-id="71aaf-116"><span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**MEDIA\_TRANSPORT\_PAYLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="71aaf-117">Gibt gesammelte TS-Paket Nutzlasten an, z. b. PE-Pakete.</span><span class="sxs-lookup"><span data-stu-id="71aaf-117">Specifies gathered TS packet payloads, such as PES packets.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71aaf-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71aaf-118">Requirements</span></span>



| <span data-ttu-id="71aaf-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71aaf-119">Requirement</span></span> | <span data-ttu-id="71aaf-120">Wert</span><span class="sxs-lookup"><span data-stu-id="71aaf-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71aaf-121">Header</span><span class="sxs-lookup"><span data-stu-id="71aaf-121">Header</span></span><br/> | <dl> <span data-ttu-id="71aaf-122"><dt>Bdatypes. h (Include bmolface. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71aaf-122"><dt>Bdatypes.h (include Bdaiface.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71aaf-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71aaf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71aaf-124">DirectShow-Enumerationstypen</span><span class="sxs-lookup"><span data-stu-id="71aaf-124">DirectShow Enumerated Types</span></span>](directshow-enumerated-types.md)
</dt> </dl>

 

 




