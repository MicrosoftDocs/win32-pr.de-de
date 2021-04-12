---
description: Gibt an, ob der sprach Erfassungs-DSP das zentrale Abschneiden durchführt.
ms.assetid: 6830cadd-fa8d-41e1-ac11-a6c8f2795941
title: MFPKEY_WMAAECMA_FEATR_CENTER_CLIP-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0936ddfe9e34664e55a20efea35a3c06dd6990e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215049"
---
# <a name="mfpkey_wmaaecma_featr_center_clip-property"></a>Mfpkey \_ wmaaecma \_ featr \_ Center- \_ Clip (Eigenschaft)

Gibt an, ob der sprach Erfassungs-DSP das zentrale Abschneiden durchführt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ bool

## <a name="default-value"></a>Standardwert

Variant \_ true

## <a name="applies-to"></a>Gilt für

-   [Sprach Erfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Bemerkungen

Das zentrale Clipping ist ein Prozess, bei dem kleine Echo Restwerte entfernt werden, die nach der AEC-Verarbeitung in Single-Talk-Situationen verbleiben (wenn die Sprache nur an einem Ende der Zeile auftritt).

Diese Eigenschaft kann die folgenden Werte aufweisen.



| Wert          | BESCHREIBUNG              |
|----------------|--------------------------|
| Variant \_ false | Deaktivieren Sie das zentrale Clipping. |
| Variant \_ true  | Aktivieren Sie das zentrale Clipping.  |



 

Der Standardwert dieser Eigenschaft ist Variant \_ true (aktiviert). Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.

Der DSP verwendet diese Eigenschaft nur, wenn die AEC-Verarbeitung aktiviert ist.

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

 

 
