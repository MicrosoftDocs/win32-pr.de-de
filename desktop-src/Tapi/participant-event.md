---
description: Die Teilnehmer Ereignis-Aufzählung \_ beschreibt Teilnehmer Ereignisse.
ms.assetid: 678165f2-ad0b-415f-86bf-8c4e3bd8d793
title: PARTICIPANT_EVENT-Enumeration (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 225b1b9901efa5648dfaa326c53ed69cff2c4295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370666"
---
# <a name="participant_event-enumeration"></a>Teilnehmer \_ ereignisenumeration

\[ Diese Enumeration ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **Teilnehmer \_ Ereignis** -Aufzählung beschreibt Teilnehmer Ereignisse. Die [**itparticipvorgänger Vent:: get- \_ Ereignis**](itparticipantevent-get-event.md) Methode gibt einen Member dieser Enumeration zurück, um den Typ des aufgetretenen Konferenzteilnehmer Ereignisses anzugeben. Diese Enumeration wird von Anwendungen verwendet, die auf die [ipconf-MSP](ipconf-msp.md)zugreifen.

## <a name="syntax"></a>Syntax


```C++
} PARTICIPANT_EVENT;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="PE_NEW_PARTICIPANT"></span><span id="pe_new_participant"></span>**\_neuen \_ Teilnehmer PE**
</dt> <dd>

Der Konferenz wurde ein neuer Teilnehmer hinzugefügt.

</dd> <dt>

<span id="PE_INFO_CHANGE"></span><span id="pe_info_change"></span>**PE- \_ Informations \_ Änderung**
</dt> <dd>

Die Informationen zu einem Teilnehmer wurden geändert.

</dd> <dt>

<span id="PE_PARTICIPANT_LEAVE"></span><span id="pe_participant_leave"></span>**PE- \_ Teilnehmer \_ verlassen**
</dt> <dd>

Ein Teilnehmer hat die Konferenz verlassen.

</dd> <dt>

<span id="PE_NEW_SUBSTREAM"></span><span id="pe_new_substream"></span>**\_neuen \_ substream PE**
</dt> <dd>

Dem Teilnehmer wurde ein neuer untergeordneter Stream hinzugefügt.

</dd> <dt>

<span id="PE_SUBSTREAM_REMOVED"></span><span id="pe_substream_removed"></span>**PE- \_ substrom \_ entfernt**
</dt> <dd>

Ein neuer teilstream wurde aus dem Teilnehmer entfernt.

</dd> <dt>

<span id="PE_SUBSTREAM_MAPPED"></span><span id="pe_substream_mapped"></span>**zugeordneter PE- \_ substream \_**
</dt> <dd>

Ein Teilnehmer wurde einem substream zugeordnet.

</dd> <dt>

<span id="PE_SUBSTREAM_UNMAPPED"></span><span id="pe_substream_unmapped"></span>**PE- \_ substream \_ nicht zugeordnet**
</dt> <dd>

Die Zuordnung eines Teilnehmers zu einem substream wurde aufgehoben.

</dd> <dt>

<span id="PE_PARTICIPANT_TIMEOUT"></span><span id="pe_participant_timeout"></span>**Timeout für PE- \_ Teilnehmer \_**
</dt> <dd>

Ein Teilnehmer wurde aufgrund eines Timeouts aus der Konferenz entfernt.

</dd> <dt>

<span id="PE_PARTICIPANT_RECOVERED"></span><span id="pe_participant_recovered"></span>**PE- \_ Teilnehmer \_ wieder hergestellt**
</dt> <dd>

Ein entfernter Teilnehmer ist wieder sichtbar. Normalerweise ist dies ein Teilnehmer, der abgelaufen ist, aber Signale empfangen werden.

</dd> <dt>

<span id="PE_PARTICIPANT_ACTIVE"></span><span id="pe_participant_active"></span>**aktiver PE- \_ Teilnehmer \_**
</dt> <dd>

Der Teilnehmer ist in der Konferenz aktiv geworden.

</dd> <dt>

<span id="PE_PARTICIPANT_INACTIVE"></span><span id="pe_participant_inactive"></span>**PE- \_ Teilnehmer \_ inaktiv**
</dt> <dd>

Der Teilnehmer ist in der Konferenz inaktiv geworden.

</dd> <dt>

<span id="PE_LOCAL_TALKING"></span><span id="pe_local_talking"></span>**lokales PE- \_ \_ Gespräch**
</dt> <dd>

Der lokale Teilnehmer hat mit der Diskussion begonnen.

</dd> <dt>

<span id="PE_LOCAL_SILENT"></span><span id="pe_local_silent"></span>**lokale PE-unbeaufsichtigte \_ \_**
</dt> <dd>

Der lokale Teilnehmer ist in der Konferenz unbeaufsichtigt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                              |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itparticipvorgänger Vent:: get- \_ Ereignis**](itparticipantevent-get-event.md)
</dt> <dt>

[Ipconf-msp](ipconf-msp.md)
</dt> <dt>

[Ipconf-MSP-Schnittstellen](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




