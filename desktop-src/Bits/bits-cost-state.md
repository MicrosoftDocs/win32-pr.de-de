---
title: BITS_COST_STATE (Bits5 \_ 0.h)
description: Die BITS \_ COST \_ STATE-Enumeration definiert die konstanten Werte, die den BITS-Kostenzustand angeben.
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
ms.openlocfilehash: ecbe54966a54310af71a4c96a3d3c2423f524f9b8a8067b10350fba05675a54b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701980"
---
# <a name="bits_cost_state"></a>\_BITS-KOSTENSTATUS \_

Definiert Konstanten, die den BITS-Kostenzustand angeben.

<dl> <dt>

<span id="BITS_COST_STATE_UNRESTRICTED"></span><span id="bits_cost_state_unrestricted"></span>**BITS \_ COST \_ STATE \_ UNRESTRICTED**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_CAPPED_USAGE_UNKNOWN"></span><span id="bits_cost_state_capped_usage_unknown"></span>**BITS \_ COST \_ STATE \_ CAPPED \_ USAGE \_ UNKNOWN**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_BELOW_CAP"></span><span id="bits_cost_state_below_cap"></span>**BITS \_ COST STATE BELOW CAP (BITS-KOSTENSTATUS \_ \_ \_ UNTERHALB DER OBERGRENZE)**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_NEAR_CAP"></span><span id="bits_cost_state_near_cap"></span>**BITS \_ COST \_ STATE \_ NEAR \_ CAP**
</dt> <dd> <dl> <dt>

0x8
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_CHARGED"></span><span id="bits_cost_state_overcap_charged"></span>**BITS \_ COST \_ STATE \_ OVERCAP \_ CHARGED**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_OVERCAP_THROTTLED"></span><span id="bits_cost_state_overcap_throttled"></span>**BITS \_ COST \_ STATE \_ OVERCAP \_ THROTTLED**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_USAGE_BASED"></span><span id="bits_cost_state_usage_based"></span>**NUTZUNG DES \_ BITS-KOSTENZUSTANDS \_ \_ \_ BASIEREND**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_OPTION_IGNORE_CONGESTION"></span><span id="bits_cost_option_ignore_congestion"></span>**\_BITS-KOSTENOPTION \_ \_ ÜBERLASTUNG IGNORIEREN \_**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_RESERVED"></span><span id="bits_cost_state_reserved"></span>**RESERVIERTER \_ \_ BITS-KOSTENZUSTAND \_**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Reserviert.


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NOT_ROAMING"></span><span id="bits_cost_state_transfer_not_roaming"></span>**BITS \_ COST \_ STATE \_ TRANSFER \_ NOT \_ ROAMING**
</dt> <dd> <dl> <dt>

(BITS \_ KOSTENOPTION \_ \_ IGNORIEREN \_ \| ÜBERLASTUNGSBITS \_ \_ \_ KOSTENZUSTANDSNUTZUNG BASIEREND AUF \_ \| BITS \_ \_ KOSTENZUSTAND \_ \_ GEDROSSELTE \| BITS \_ \_ KOSTENZUSTAND \_ \_ ÜBERLASTETE \| BITS \_ \_ KOSTENSTATUS NAHE CAP \_ \_ \| BITS \_ \_ KOSTENSTATUS UNTER CAP \_ \_ \| BITS \_ \_ KOSTENSTATUS BEGRENZT NUTZUNG UNBEKANNTE \_ \_ \_ \| BITS \_ \_ KOSTENZUSTAND \_ UNEINGESCHRÄNKT) 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_NO_SURCHARGE"></span><span id="bits_cost_state_transfer_no_surcharge"></span>**BITS \_ COST STATE TRANSFER \_ \_ \_ \_ NOUM**
</dt> <dd> <dl> <dt>

(BITS \_ COST \_ OPTION \_ IGNORE \_ CONGESTION \| BITS \_ COST \_ STATE \_ USAGE \_ BASED \| BITS \_ COST \_ STATE \_ OVERCAP \_ THROTTLED \| BITS \_ COST \_ STATE \_ NEAR \_ CAP \| BITS \_ COST \_ STATE \_ BELOW \_ CAP \| BITS \_ COST \_ STATE \_ CAPPED \_ USAGE \_ UNKNOWN \| BITS \_ COST \_ STATE \_ UNRESTRICTED)
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_STANDARD"></span><span id="bits_cost_state_transfer_standard"></span>**BITS \_ COST \_ STATE \_ TRANSFER \_ STANDARD**
</dt> <dd> <dl> <dt>

(BITS \_ COST \_ OPTION \_ IGNORE \_ CONGESTION \| BITS \_ COST \_ STATE \_ USAGE \_ BASED \| BITS \_ COST \_ STATE \_ OVERCAP \_ THROTTLED \| BITS \_ COST \_ STATE \_ BELOW \_ CAP \| BITS \_ COST \_ STATE \_ CAPPED \_ USAGE \_ UNKNOWN \| BITS \_ COST \_ STATE \_ UNRESTRICTED) 
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_UNRESTRICTED"></span><span id="bits_cost_state_transfer_unrestricted"></span>**BITS \_ COST \_ STATE \_ TRANSFER \_ UNRESTRICTED**
</dt> <dd> <dl> <dt>

(BITS \_ COST \_ OPTION \_ IGNORE \_ CONGESTION \| BITS \_ COST \_ STATE \_ OVERCAP \_ THROTTLED \| BITS \_ COST \_ STATE \_ UNRESTRICTED)
</dt> <dt>


</dt> </dl> </dd> <dt>

<span id="BITS_COST_STATE_TRANSFER_ALWAYS"></span><span id="bits_cost_state_transfer_always"></span>**BITS \_ COST \_ STATE \_ TRANSFER \_ ALWAYS**
</dt> <dd> <dl> <dt>

(BITS \_ COST \_ OPTION \_ IGNORE \_ CONGESTION \| BITS \_ COST \_ STATE \_ ROAMING \| BITS \_ COST \_ STATE \_ USAGE \_ BASED \| BITS \_ COST \_ STATE \_ OVERCAP \_ THROTTLED \| BITS \_ COST \_ STATE \_ OVERCAP \_ CHARGED \| BITS \_ COST \_ STATE \_ NEAR \_ CAP \| BITS \_ COST \_ STATE \_ BELOW \_ CAP \| BITS \_ COST \_ STATE \_ CAPPED \_ USAGE \_ UNKNOWN \| BITS \_ COST \_ STATE \_ UNRESTRICTED)
</dt> <dt>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Bits5 \_ 0.h (einschließlich Bits.h)</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Bits5 \_ 0.idl</dt> </dl>                |



 

 





