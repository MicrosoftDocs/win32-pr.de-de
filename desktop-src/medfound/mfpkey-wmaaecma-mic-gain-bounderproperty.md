---
description: Gibt an, ob der sprach Erfassungs-DSP eine Mikrofon-zuschließung anwendet.
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c1b09f2095f5accb44e4e0edaff2b8c94941d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360135"
---
# <a name="mfpkey_wmaaecma_mic_gain_bounder-property"></a>Mfpkey \_ wmaaecma \_ MIC \_ - \_ bounter-Eigenschaft

Gibt an, ob der sprach Erfassungs-DSP eine Mikrofon-zuschließung anwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ bool

## <a name="default-value"></a>Standardwert

Variant \_ true

## <a name="applies-to"></a>Gilt für

-   [Sprach Erfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Bemerkungen

Die Mikrofon-Gewinngrenze stellt sicher, dass das Mikrofon über das richtige Maß an Gewinn verfügt. Wenn der Gewinn zu hoch ist, ist das erfasste Signal möglicherweise erschöpft und wird abgeschnitten. Clipping ist ein nichtlinearer Effekt, der dazu führt, dass der Algorithmus für den akustische Echo Abbruch (AEC) fehlschlägt. Wenn der Gewinn zu niedrig ist, ist das Signal-zu-Rauschen-Verhältnis gering, was auch bewirken kann, dass der AEC-Algorithmus fehlschlägt oder nicht gut funktioniert.

Diese Eigenschaft kann die folgenden Werte aufweisen.



| Wert          | BESCHREIBUNG                       |
|----------------|-----------------------------------|
| Variant \_ true  | Ermöglicht das Begrenzen des Mikrofons.  |
| Variant \_ false | Deaktivieren Sie das Ende des Mikrofons. |



 

Der Standardwert dieser Eigenschaft ist Variant \_ true (aktiviert).

Das Begrenzen des Mikrofons wird nur angewendet, wenn der DSP im Quell Modus betrieben wird. Im Filter Modus muss die Anwendung sicherstellen, dass das Mikrofon über die richtige Gewinn Ebene verfügt.

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

 

 
