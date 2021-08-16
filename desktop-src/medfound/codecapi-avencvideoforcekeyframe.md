---
description: Erzwingt, dass der Encoder den nächsten Frame als Keyframe codt.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: CODECAPI_AVEncVideoForceKeyFrame -Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2e28738dcd7398ce04abe7f71778e94d7d5d4f49393365e92c43bbb347d98c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880706"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a>CODECAPI \_ AVEncVideoForceKeyFrame-Eigenschaft

Erzwingt, dass der Encoder den nächsten Frame als Keyframe codt.

## <a name="data-type"></a>Datentyp

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncVideoForceKeyFrame**

## <a name="property-value"></a>Eigenschaftswert

Wenn der Wert ungleich 0 (null) ist, codt der Encoder den nächsten Frame als Keyframe. Wenn der Wert 0 (null) ist, wählt der Encoder aus, ob der nächste Frame als Keyframe codiert werden soll.

Diese Eigenschaft gilt für den nächsten Frame, den der Encoder als Eingabe empfängt. Bei einer Media Foundation-Transformation (MFT) ist dies der nächste Frame, der an die [**METHODE ":P RocessInput"**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) übergeben wird. Die Einstellung wird nach dem nächsten Frame auf 0 (null) zurückgesetzt.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird auch mit [H.264 UVC 1.5-Kameraencodern](camera-encoder-h264-uvc-1-5.md)verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

