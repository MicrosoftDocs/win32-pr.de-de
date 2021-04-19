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
# <a name="media_sample_content-enumeration"></a>\_Aufzählung von Medien Sample- \_ Inhalten

Beschreibt den Inhalt eines elementaren Datenstroms innerhalb eines MPEG-2-Transportdaten Stroms. Diese Enumeration wird in der [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) -Schnittstelle verwendet, die auf den Ausgabe Pins des [MPEG-2-demultiplexers](mpeg-2-demultiplexer.md)implementiert ist.

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

<span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**Medien \_ Transport \_ Paket**
</dt> <dd>

Gibt ein umfassendes transportstreampaket an, das ohne Verarbeitung durchlaufen werden soll.

</dd> <dt>

<span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**Daten \_ Strom für Medien \_**
</dt> <dd>

Gibt eine Nutzlast für Audiodaten oder Videos an.

</dd> <dt>

<span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**Medien- \_ MPEG2 \_ PSI**
</dt> <dd>

Gibt einen Pat-, PMT-, Cat-oder privaten Datenstrom an. Hierbei handelt es sich um umfassende PSI-Abschnitte, die nicht erneut zusammengefügt werden müssen.

</dd> <dt>

<span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**Nutzlast für Medien \_ Transport \_**
</dt> <dd>

Gibt gesammelte TS-Paket Nutzlasten an, z. b. PE-Pakete.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Bdatypes. h (Include bmolface. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Enumerationstypen](directshow-enumerated-types.md)
</dt> </dl>

 

 




