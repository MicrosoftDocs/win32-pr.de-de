---
description: Gibt an, ob der sprach Erfassungs-DSP eine Rauschunterdrückung ausführt.
ms.assetid: d63e9ac1-9584-4f74-8404-c95d17eb8c2d
title: MFPKEY_WMAAECMA_FEATR_NS-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02218ce621123066e5e61435d93f8539de95e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368179"
---
# <a name="mfpkey_wmaaecma_featr_ns-property"></a>Mfpkey \_ wmaaecma \_ featr \_ NS-Eigenschaft

Gibt an, ob der sprach Erfassungs-DSP eine Rauschunterdrückung ausführt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

1

## <a name="applies-to"></a>Gilt für

-   [Sprach Erfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Bemerkungen

Bei der Rauschunterdrückung handelt es sich um eine DSP-Komponente (Digital Signal Processing, digitale Signalverarbeitung), mit der das Füll Zeichen im Audiosignal unterdrückt wird Die Rauschunterdrückung wird nach der Verarbeitung des akustischen Echo Abbruchs (AEC) und der Mikrofon Array Verarbeitung angewendet.

Diese Eigenschaft kann die folgenden Werte aufweisen.



| Wert | BESCHREIBUNG                |
|-------|----------------------------|
| 0     | Deaktivieren Sie die Rauschunterdrückung. |
| 1     | Aktivieren Sie die Rauschunterdrückung.  |



 

Der Standardwert dieser Eigenschaft ist 1 (aktiviert). Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.

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

 

 
