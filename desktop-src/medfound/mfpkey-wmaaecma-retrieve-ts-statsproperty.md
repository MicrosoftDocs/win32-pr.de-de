---
description: Gibt an, ob der Spracherfassungs-DSP Zeitstempelstatistiken in der Registrierung speichert.
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: MFPKEY_WMAAECMA_RETRIEVE_TS_STATS-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c28f9812bb5f1324fcb1153b84f5a6704c7481c8356073fd02b8d95b57a8e497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953500"
---
# <a name="mfpkey_wmaaecma_retrieve_ts_stats-property"></a>MFPKEY \_ WMAAECMA \_ RETRIEVE TS \_ \_ STATS-Eigenschaft

Gibt an, ob der Spracherfassungs-DSP Zeitstempelstatistiken in der Registrierung speichert.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ BOOL

## <a name="default-value"></a>Standardwert

VARIANT \_ FALSE

## <a name="applies-to"></a>Gilt für

-   [Spracherfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Hinweise

Akustik-Echoabbruchalgorithmen (Acoustic Echo Cancellation, AEC) hängen von genauen Zeitstempeln in den Audiostreams ab. In der Praxis sind Zeitstempel oft nicht perfekt, und verschiedene Audiogeräte können unterschiedliche Abweichungs- und Abweichungsraten aufweisen. Wenn AEC aktiviert ist, erfasst der DSP Statistiken zu den Zeitstempeln und verwendet diese Informationen, um Ungenauigkeiten zu kompensieren.

Wenn der Wert dieser Eigenschaft VARIANT \_ TRUE ist, speichert der DSP die Statistiken, die er erfasst, in der Registrierung. Wenn der DSP das nächste Mal AEC mit demselben Audiogerät ausführt, liest er die statistischen Informationen aus der Registrierung, wodurch der DSP effizienter ausgeführt werden kann.

Wenn Sie den Wert dieser Eigenschaft auf VARIANT TRUE festlegen \_ und den DSP im Filtermodus verwenden, sollten Sie auch die [MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID-Eigenschaft](mfpkey-wmaaecma-devicepair-guidproperty.md) festlegen. Im Quellmodus ist dies nicht erforderlich.

Der Standardwert dieser Eigenschaft ist VARIANT \_ FALSE. Der DSP verwendet diese Eigenschaft nur, wenn die AEC-Verarbeitung aktiviert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Spracherfassungs-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
