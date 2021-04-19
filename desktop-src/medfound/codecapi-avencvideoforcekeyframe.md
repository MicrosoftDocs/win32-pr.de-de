---
description: Zwingt den Encoder, den nächsten Frame als Keyframe zu codieren.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: CODECAPI_AVEncVideoForceKeyFrame-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72c555d5680e822e9a8308b3e143a754eb22b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346883"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a>Codecapi \_ avencvideoforcekeyframe (Eigenschaft)

Zwingt den Encoder, den nächsten Frame als Keyframe zu codieren.

## <a name="data-type"></a>Datentyp

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencvideoforcekeyframe**

## <a name="property-value"></a>Eigenschaftswert

Wenn der Wert ungleich 0 (null) ist, codiert der Encoder den nächsten Frame als Keyframe. Wenn der Wert 0 (null) ist, wählt der Encoder aus, ob der nächste Frame als Keyframe codiert werden soll.

Diese Eigenschaft gilt für den nächsten Frame, den der Encoder als Eingabe empfängt. Bei einer Media Foundation Transformation (MFT) ist dies der nächste Frame, der an die [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) -Methode weitergegeben wird. Die Einstellung wird nach dem nächsten Frame auf 0 (null) zurückgesetzt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird auch mit [H. 264 UVC 1,5-Kamera Codierern](camera-encoder-h264-uvc-1-5.md)verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**Icodecapi**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

