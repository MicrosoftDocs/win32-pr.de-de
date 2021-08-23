---
description: Beschreibt den Inhalt eines elementaren Streams in einem MPEG-2-Transportstream. Diese Enumeration wird in der IMPEG2PIDMap-Schnittstelle verwendet, die auf den Ausgabepins des MPEG-2-Demultiplexers implementiert ist.
ms.assetid: 989ad56b-b5af-4811-889e-c79fcd3f7f01
title: MEDIA_SAMPLE_CONTENT-Enumeration (Bdatypes.h)
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
ms.openlocfilehash: 1dead22b2c8ea3cf7da665e01a4b36554b8282922a1d2b2a12d59f429f2acac4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684990"
---
# <a name="media_sample_content-enumeration"></a>MEDIA \_ SAMPLE \_ CONTENT-Enumeration

Beschreibt den Inhalt eines elementaren Streams in einem MPEG-2-Transportstream. Diese Enumeration wird in der [**IMPEG2PIDMap-Schnittstelle**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) verwendet, die auf den Ausgabepins des [MPEG-2-Demultiplexers](mpeg-2-demultiplexer.md)implementiert ist.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  MEDIA_TRANSPORT_PACKET,
  MEDIA_ELEMENTARY_STREAM,
  MEDIA_MPEG2_PSI,
  MEDIA_TRANSPORT_PAYLOAD
} MEDIA_SAMPLE_CONTENT;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**\_ \_ MEDIENTRANSPORTPAKET**
</dt> <dd>

Gibt ein vollständiges Transportstreampaket an, das ohne Verarbeitung übergeben werden soll.

</dd> <dt>

<span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**MEDIA \_ ELEMENTARY \_ STREAM**
</dt> <dd>

Gibt eine AUDIO- oder Video-PES-Nutzlast an.

</dd> <dt>

<span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA \_ MPEG2 \_ PSI**
</dt> <dd>

Gibt einen PAT-, PMT-, CAT- oder privaten Datenstrom an. Dies sind vollständige PSI-Abschnitte, die nicht neu zusammengesetzt werden müssen.

</dd> <dt>

<span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**NUTZLAST \_ DES MEDIENTRANSPORTS \_**
</dt> <dd>

Gibt erfasste TS-Paketnutzlasten an, z. B. PES-Pakete.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Bdatypes.h (einschließlich Bdaiface.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Enumerationstypen](directshow-enumerated-types.md)
</dt> </dl>

 

 




