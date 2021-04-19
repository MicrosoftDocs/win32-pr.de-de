---
description: Gibt an, ob der sprach Erfassungs-DSP Zeitstempel Statistiken in der Registrierung speichert.
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: MFPKEY_WMAAECMA_RETRIEVE_TS_STATS-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8e4efad8def035c7282e3ade8045bdbfd7e34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353176"
---
# <a name="mfpkey_wmaaecma_retrieve_ts_stats-property"></a>Mfpkey \_ wmaaecma \_ Abrufen der \_ TS \_ Stats-Eigenschaft

Gibt an, ob der sprach Erfassungs-DSP Zeitstempel Statistiken in der Registrierung speichert.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ bool

## <a name="default-value"></a>Standardwert

Variant \_ false

## <a name="applies-to"></a>Gilt für

-   [Sprach Erfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Bemerkungen

AEC-Algorithmen (Akustik Echo Abbruch) hängen von exakten Zeitstempeln in den Audiostreams ab. In der Praxis sind Zeitstempel oft nicht perfekt, und unterschiedliche Audiogeräte können unterschiedliche Raten von Varianz und Abweichung aufweisen. Wenn AEC aktiviert ist, sammelt der DSP Statistiken zu den Zeitstempeln und verwendet diese Informationen, um Ungenauigkeiten zu kompensieren.

Wenn der Wert dieser Eigenschaft Variant true ist \_ , speichert der DSP die in der Registrierung gesammelten Statistiken. Beim nächsten Ausführen von AEC mit dem gleichen Paar von Audiogeräten liest der DSP die statistischen Informationen aus der Registrierung, sodass der DSP effizienter durchgeführt werden kann.

Wenn Sie den Wert dieser Eigenschaft auf Variant true festgelegt \_ haben und Sie den DSP im Filter Modus verwenden, sollten Sie auch die Eigenschaft " [mfpkey \_ wmaaecma \_ devicepair \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) " festlegen. Im Quell Modus ist dies nicht erforderlich.

Der Standardwert dieser Eigenschaft ist Variant \_ false. Der DSP verwendet diese Eigenschaft nur, wenn die AEC-Verarbeitung aktiviert ist.

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

 

 
