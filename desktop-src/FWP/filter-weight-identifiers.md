---
title: Filtern von Gewichtungs bezeichlern ("f")
description: Filtern von Gewichtungs Bezeichner, die von der Basis Filter-Engine (BFE) verwendet werden, um automatisch generierte Filter Gewichtungen zu berechnen.
ms.assetid: 73d2e9e0-0d3a-474e-b660-f91675f9000e
topic_type:
- apiref
api_name:
- FWPM_AUTO_WEIGHT_BITS
- FWPM_AUTO_WEIGHT_MAX
- FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS
- FWPM_WEIGHT_RANGE_IPSEC
- FWPM_WEIGHT_RANGE_MAX
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e8ea740c5087151418d50187ee3dc1097baad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346327"
---
# <a name="filter-weight-identifiers"></a>Filtern von Gewichtungs bezeichlern

Die Filter Gewichtungs-IDs, die von der Basis Filter-Engine (BFE) verwendet werden, um automatisch generierte Filter Gewichtungen zu berechnen, sind unten aufgeführt.

Weitere Informationen zur Filter Gewichtungs Generierung finden Sie unter [Filtern der Gewichtungs Zuweisung](filter-weight-assignment.md) .

<dl> <dt>

<span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**Bits für automatische f- \_ \_ Gewichtung \_**
</dt> <dd> <dl> <dt>

(60)
</dt> <dt>



Anzahl von Bits, die für automatisch generierte Filter Gewichtungen verwendet werden.


</dt> </dl> </dd> <dt>

<span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**maximale Größe für \_ Automatisches f- \_ Gewicht \_**
</dt> <dd> <dl> <dt>

(**MAXUINT64** >> 4)
</dt> <dt>



Maximale automatisch generierte Filter Gewichtung.


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**IKE-Ausnahmen für den f- \_ Gewichtungs \_ Bereich \_ \_**
</dt> <dd> <dl> <dt>

0xc
</dt> <dt>



BFE weist einem IKE-und AuthIP-Filter eine Gewichtung mit diesem Bereichs Wert zu.

Weitere Informationen zu IKE/AuthIP-Filtern finden Sie unter [IKE/AuthIP-Ausnahmen](ike-exemptions.md) .


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**swpm- \_ Gewichtungs \_ Bereich- \_ IPSec**
</dt> <dd> <dl> <dt>

(0x0)
</dt> <dt>



BFE weist den IPSec-Richtlinien Filtern eine Gewichtung mit diesem Bereichs Wert zu.


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**maximale Größe des gültigen f- \_ \_ Bereichs \_**
</dt> <dd> <dl> <dt>

(**MAXUINT64** >> 60)
</dt> <dt>



Maximal zulässiger Wert für Filter Gewichtungs Bereich.


</dt> </dl> </dd> </dl>

> [!Note]  
> **MAXUINT64** stellt den größtmöglichen Wert von **UINT64** dar. Der Wert dieser Konstante ist 0xFFFFFFFFFFFFFFFF.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>"F"</dt> </dl> |



 

 





