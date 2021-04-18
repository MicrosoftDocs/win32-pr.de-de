---
description: Gibt an, ob der sprach Erfassungs-DSP eine automatische Steuerungs Steuerung ausführt.
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: MFPKEY_WMAAECMA_FEATR_AGC-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f42c7abd854b8fe18b5cfd4fe23ededb28faa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345819"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a>Eigenschaft "mfpkey \_ wmaaecma \_ featr \_ AGC"

Gibt an, ob der sprach Erfassungs-DSP eine automatische Steuerungs Steuerung ausführt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ bool

## <a name="default-value"></a>Standardwert

Variant \_ false

## <a name="applies-to"></a>Gilt für

-   [Sprach Erfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Bemerkungen

Die automatische Gewinn Steuerung ist eine DSP-Komponente (Digital Signal Processing, digitale Signalverarbeitung), die den Zuwachs anpasst, sodass die Ausgabe Ebene des Signals innerhalb desselben ungefähren Bereichs verbleibt.

Diese Eigenschaft kann die folgenden Werte aufweisen.



| Wert          | BESCHREIBUNG                     |
|----------------|---------------------------------|
| Variant \_ false | Deaktivieren Sie die automatische Gewinn Steuerung. |
| Variant \_ true  | Aktivieren Sie die automatische Steuerelement Steuerung.  |



 

Der Standardwert dieser Eigenschaft ist Variant \_ false (deaktiviert). Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.

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

 

 
