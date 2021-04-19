---
description: Ruft Qualitätsmetriken für den akustische Echo Abbruch (AEC) aus dem sprach Erfassungs-DSP ab.
ms.assetid: de2e86ae-0469-471f-9105-0bb38a59b428
title: MFPKEY_WMAAECMA_QUALITY_METRICS-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3740630bc23c4e3e0e824e55b4e34bcd8b1347f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356583"
---
# <a name="mfpkey_wmaaecma_quality_metrics-property"></a>Mfpkey \_ wmaaecma \_ Quality- \_ Metriken (Eigenschaft)

Ruft Qualitätsmetriken für den akustische Echo Abbruch (AEC) aus dem sprach Erfassungs-DSP ab.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT- \_ BLOB

## <a name="remarks"></a>Bemerkungen

Der Wert dieser Eigenschaft ist eine [aecqualitymetrics- \_ ](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) Struktur Struktur. Diese Eigenschaft ist schreibgeschützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Sprach Erfassungs-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
