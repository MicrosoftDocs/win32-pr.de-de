---
title: BITS_COST_STATE (Bits5 \_ 0. h)
description: Die Bits \_ Cost \_ State-Enumeration definiert die Konstanten Werte, die den Bits-Kosten Zustand angeben.
ms.assetid: A8C36D4E-98B3-45C4-9ECD-9B5280133176
topic_type:
- apiref
api_name:
- BITS_COST_STATE_UNRESTRICTED
- BITS_COST_STATE_CAPPED_USAGE_UNKNOWN
- BITS_COST_STATE_BELOW_CAP
- BITS_COST_STATE_NEAR_CAP
- BITS_COST_STATE_OVERCAP_CHARGED
- BITS_COST_STATE_OVERCAP_THROTTLED
- BITS_COST_STATE_USAGE_BASED
- BITS_COST_OPTION_IGNORE_CONGESTION
- BITS_COST_STATE_RESERVED
- BITS_COST_STATE_TRANSFER_NOT_ROAMING
- BITS_COST_STATE_TRANSFER_NO_SURCHARGE
- BITS_COST_STATE_TRANSFER_STANDARD
- BITS_COST_STATE_TRANSFER_UNRESTRICTED
- BITS_COST_STATE_TRANSFER_ALWAYS
api_location:
- Bits5_0.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/20/2019
ms.openlocfilehash: 88fb0b949fb06a6e1eb6e14cdf55c8d54d9ab33c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956586"
---
# <a name="bits_cost_state"></a>Bits- \_ Kosten \_ Status

Definiert Konstanten, die den Bits-Kosten Zustand angeben.

<dl> <dt>

<span id="BITS_COST_STATE_UNRESTRICTED"></span><span id="bits_cost_state_unrestricted"></span>**Bits- \_ Kosten \_ Status \_ uneingeschränkt**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_CAPPED_USAGE_UNKNOWN"></span><span id="bits_cost_state_capped_usage_unknown"></span>**die Verwendung des Bits- \_ Kosten \_ Zustands ist \_ \_ \_ unbekannt.**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_BELOW_CAP"></span><span id="bits_cost_state_below_cap"></span>**Bits- \_ Kosten \_ Status \_ unter \_ Grenze**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_NEAR_CAP"></span><span id="bits_cost_state_near_cap"></span>**Bits- \_ Kosten \_ Zustand \_ nahe der \_ Obergrenze**
</dt> <dd> <dl> <dt>

0x8
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_CHARGED"></span><span id="bits_cost_state_overcap_charged"></span>**\_Kosten \_ Zustands überschreiung für Bits in \_ \_ Rechnung gestellt**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_THROTTLED"></span><span id="bits_cost_state_overcap_throttled"></span>**Außerbetriebsetzung des Bits- \_ Kosten \_ Zustands, \_ \_ gedrosselt**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_USAGE_BASED"></span><span id="bits_cost_state_usage_based"></span>**Verwendung von Bits- \_ Kosten \_ Zustands \_ \_ basiert**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_OPTION_IGNORE_CONGESTION"></span><span id="bits_cost_option_ignore_congestion"></span>**Bits \_ - \_ Kosten \_ Option \_ Überlastung ignorieren**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_RESERVED"></span><span id="bits_cost_state_reserved"></span>**Bits- \_ Kosten \_ Status \_ reserviert**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Reserviert.


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NOT_ROAMING"></span><span id="bits_cost_state_transfer_not_roaming"></span>**Bits- \_ Kosten \_ Zustands \_ Übertragung \_ nicht \_ Roaming**
</dt> <dd> <dl> <dt>

(Bits \_ Kosten \_ Option Lasten Zustands \_ \_ \| \_ \_ \_ Verwendung basierend auf Lasten Zustands \_ basierte \| Bits Kosten Status \_ \_ \_ \_ Drosselung gedrosselte Bits Kosten Zustand gebührenpflichtig abgerechnet Bits Kosten Status in der Nähe von Cap Bits Kosten Zustand unter Cap Bits Kosten Status begrenzte \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ Nutzung \_ unbekannter \| Bits \_ Kosten \_ Status \_ unbegrenzt) 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NO_SURCHARGE"></span><span id="bits_cost_state_transfer_no_surcharge"></span>**Bits \_ Cost \_ State \_ Transfer \_ No \_ Aufpreis**
</dt> <dd> <dl> <dt>

(Bits \_ Kosten Option Lasten Zustands Verwendungs basierte Bits-Kosten Zustands Beschränkung ignorieren gedrosselte Bits-Kosten Zustand near Cap Bits Kosten Zustand unter Cap Bits Kosten Zustand unter Cap Bits Kosten Status \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ begrenzt \_ Nutzung \_ unbekannter \| Bits \_ Kosten \_ Status \_ uneingeschränkt)
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_STANDARD"></span><span id="bits_cost_state_transfer_standard"></span>**Bits- \_ Kosten \_ Zustands \_ Übertragungs \_ Standard**
</dt> <dd> <dl> <dt>

(Bits \_ Kosten \_ Option \_ Überlastung der Lasten \_ \| \_ \_ Zustands \_ Nutzung \_ basierend auf dem \| Bits Kosten Zustand \_ \_ \_ \_ Drosselung gedrosselte Bits Kosten Zustand \| \_ \_ \_ unter Cap Bits Kosten Status \_ \| \_ \_ \_ begrenzt \_ Nutzung \_ unbekannter \| Bits \_ Kosten \_ Status \_ uneingeschränkt) 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_UNRESTRICTED"></span><span id="bits_cost_state_transfer_unrestricted"></span>**Bits \_ Cost \_ State \_ Transfer \_ uneingeschränkt**
</dt> <dd> <dl> <dt>

(Bits \_ Kosten \_ Option \_ Überlastung von Überlastung der Kosten \_ \| \_ \_ Status \_ \_ Drosselung gedrosselt \| Bits \_ Kosten \_ Status \_ uneingeschränkt)
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_ALWAYS"></span><span id="bits_cost_state_transfer_always"></span>**Bits- \_ Kosten \_ Zustands \_ Übertragung \_ immer**
</dt> <dd> <dl> <dt>

(Bits \_ Kosten \_ Option \_ \_ Überlastung der Lasten Zustands \| \_ \_ \_ roamingbits Kosten Status \| \_ \_ \_ Nutzung \_ basierend basierend Bits Kosten Zustand Drosselung gedrosselte Bits Kosten Zustand gebührenpflichtig abgerechnet Bits Kosten Zustand in der Nähe von Cap Bits Kosten Zustand unter Cap Bits Kosten Status begrenzte \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ \| \_ \_ \_ \_ Nutzung \_ unbekannter \| Bits \_ Kosten \_ Status \_ uneingeschränkt)
</dt> <dt>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Bits5 \_ 0. h (Include Bits. h)</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Bits5 \_ 0. idl</dt> </dl>                |



 

 





