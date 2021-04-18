---
description: Gibt an, ob der sprach Erfassungs-DSP die Vorverarbeitung eines mikrofonarrays ausführt.
ms.assetid: 0f197165-e6e5-456b-9615-1edc8ada7bb5
title: MFPKEY_WMAAECMA_FEATR_MICARR_PREPROC-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f992d8d26ba547eb1b5d1eac470536a963209f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347863"
---
# <a name="mfpkey_wmaaecma_featr_micarr_preproc-property"></a>Mfpkey \_ wmaaecma \_ featr \_ micarr \_ Preproc-Eigenschaft

Gibt an, ob der sprach Erfassungs-DSP die Vorverarbeitung eines mikrofonarrays ausführt.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ bool

## <a name="default-value"></a>Standardwert

Variant \_ true

## <a name="applies-to"></a>Gilt für

-   [Sprach Erfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Bemerkungen

Bei der Vorverarbeitung können Sie stationäre Töne entfernen, die die Verarbeitung beeinträchtigen, z. b. ein Ton mit fester Größe.

Diese Eigenschaft kann die folgenden Werte aufweisen.



| Wert          | BESCHREIBUNG            |
|----------------|------------------------|
| Variant \_ false | Deaktivieren Sie die Vorverarbeitung. |
| Variant \_ true  | Aktivieren der Vorverarbeitung.  |



 

Der Standardwert dieser Eigenschaft ist Variant \_ true (aktiviert). Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.

Der DSP verwendet diese Eigenschaft nur, wenn die Verarbeitung von mikrofonarrays aktiviert ist.

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

 

 
