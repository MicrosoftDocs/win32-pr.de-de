---
description: Ruft Qualitätsmetriken zum Akustik-Echoabbruch (Acoustic Echo Cancellation, AEC) vom Spracherfassungs-DSP ab.
ms.assetid: de2e86ae-0469-471f-9105-0bb38a59b428
title: MFPKEY_WMAAECMA_QUALITY_METRICS-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2186876279ee45e34444866c206a7729c0674c8dff1bc57c255ca205e911edae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689265"
---
# <a name="mfpkey_wmaaecma_quality_metrics-property"></a>MFPKEY \_ WMAAECMA \_ QUALITY \_ METRICS-Eigenschaft

Ruft Qualitätsmetriken zum Akustik-Echoabbruch (Acoustic Echo Cancellation, AEC) vom Spracherfassungs-DSP ab.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

\_VT-BLOB

## <a name="remarks"></a>Hinweise

Der Wert dieser Eigenschaft ist eine Struktur der [AecQualityMetrics-Struktur. \_ ](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) Diese Eigenschaft ist schreibgeschützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Spracherfassungs-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
