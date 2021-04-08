---
description: Ermöglicht es der Anwendung, die Standardeinstellungen für verschiedene Eigenschaften des sprach Erfassungs-DSP zu überschreiben.
ms.assetid: 1c11e817-36bd-4a5d-9c2b-6a91e86f623f
title: MFPKEY_WMAAECMA_FEATURE_MODE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a47ef86a2acf83131800e9cb55b86de2cd3d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753960"
---
# <a name="mfpkey_wmaaecma_feature_mode-property"></a>Mfpkey- \_ wmaaecma- \_ Funktions \_ Modus (Eigenschaft)

Ermöglicht es der Anwendung, die Standardeinstellungen für verschiedene Eigenschaften des sprach Erfassungs-DSP zu überschreiben.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ bool

## <a name="default-value"></a>Standardwert

Variant \_ false

## <a name="applies-to"></a>Gilt für

-   [Sprach Erfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft Variant \_ true ist, kann die Anwendung die folgenden Eigenschaften für den DSP festlegen:

-   [mfpkey \_ wmaaecma \_ featr \_ AES](mfpkey-wmaaecma-featr-aesproperty.md)
-   [mfpkey \_ wmaaecma \_ featr \_ AGC](mfpkey-wmaaecma-featr-agcproperty.md)
-   [mfpkey \_ wmaaecma \_ featr \_ Center- \_ Clip](mfpkey-wmaaecma-featr-center-clipproperty.md)
-   [mfpkey \_ wmaaecma \_ featr- \_ Echo \_ Länge](mfpkey-wmaaecma-featr-echo-lengthproperty.md)
-   [mfpkey \_ wmaaecma \_ featr- \_ Frame \_ Größe](mfpkey-wmaaecma-featr-frame-sizeproperty.md)
-   [mfpkey \_ wmaaecma \_ featr \_ micarr- \_ Modus](mfpkey-wmaaecma-featr-micarr-modeproperty.md)
-   [mfpkey \_ wmaaecma \_ featr \_ micarr \_ Preproc](mfpkey-wmaaecma-featr-micarr-preprocproperty.md)
-   [mfpkey \_ wmaaecma \_ featr \_ \_ Füll Füll Füll Zeichen](mfpkey-wmaaecma-featr-noise-fillproperty.md)
-   [mfpkey \_ wmaaecma \_ featr \_ NS](mfpkey-wmaaecma-featr-nsproperty.md)
-   [mfpkey \_ wmaaecma \_ featr \_ VAD](mfpkey-wmaaecma-featr-vadproperty.md)

Wenn diese Eigenschaft Variant \_ false ist, ignoriert der DSP diese Eigenschaften und verwendet seine Standardeinstellungen. Der Standardwert dieser Eigenschaft ist Variant \_ false.

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

 

 
