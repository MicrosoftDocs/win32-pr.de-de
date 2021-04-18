---
description: Gibt die audioframe-Größe an, die vom sprach Erfassungs-DSP verwendet wird.
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: MFPKEY_WMAAECMA_FEATR_FRAME_SIZE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5623cf3d26b968c7e7745fa0c01c69c034505cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347275"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a>Eigenschaft "mfpkey \_ wmaaecma \_ featr \_ Frame \_ size"

Gibt die audioframe-Größe an, die vom sprach Erfassungs-DSP verwendet wird.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="applies-to"></a>Gilt für

-   [Sprach Erfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Bemerkungen

Der Algorithmus für akustische Echo Abbruch (AEC) verarbeitet PCM-Audiobeispiele jeweils einen Frame. Der Wert dieser Eigenschaft ist die Größe des Audioframes in den Beispielen. Vor dem Festlegen dieser Eigenschaft müssen Sie die Eigenschaft [mfpkey \_ wmaaecma \_ Feature \_ Mode](mfpkey-wmaaecma-feature-modeproperty.md) auf Variant \_ true festlegen.

Der sprach Erfassungs-DSP unterstützt die folgenden Frame Größen:

-   80
-   128
-   160
-   240
-   256
-   320

Wenn der Wert dieser Eigenschaft NULL ist, wählt der DSP die Frame Größe basierend auf dem System Modus und dem Ausgabeformat aus.

Für eine optimale Leistung wird jedoch empfohlen, dass Anwendungen den Standardwert verwenden. Wenn der Verarbeitungsmodus nur Mikrofon Array ist, ist der Standardwert 320 Samples. Der Standardwert für alle anderen Verarbeitungsmodi ist 160 Samples. Weitere Informationen zu den Verarbeitungsmodi des sprach Erfassungs-DSP finden Sie unter [mfpkey \_ wmaaecma \_ System \_ Mode](mfpkey-wmaaecma-system-modeproperty.md).

Nach dem ersten Aufrufe von [**imediaobject:: zudepaseestreamingresources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) oder [**imediaobject::P rocess Output**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput)können Sie diese Eigenschaft lesen, um die tatsächlich verwendete Frame Größe zu erhalten, auch wenn der [**mfpkey \_ wmaaecma- \_ Funktions \_ Modus**](mfpkey-wmaaecma-feature-modeproperty.md) false ist.

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

 

 
