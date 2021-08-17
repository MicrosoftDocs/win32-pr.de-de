---
description: Gibt den Quantisierungsparameter (QP) für die Videocodierung an.
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: CODECAPI_AVEncVideoEncodeQP (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ed7ba8e3cf522c1e3cfa07d22cf5e37639717c230ca571ffd89d9e1d513a0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974889"
---
# <a name="codecapi_avencvideoencodeqp-property"></a>CODECAPI \_ AVEncVideoEncodeQP (Eigenschaft)

Gibt den Quantisierungsparameter (QP) für die Videocodierung an.

## <a name="data-type"></a>Datentyp

**ULONGLONG** (VT \_ UI8)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncVideoEncodeQP**

## <a name="property-value"></a>Eigenschaftswert

Ein Satz von vier 16-Bit-Feldern, die verwendet werden, um die Frame-QPs in der Fixed QP-Codierung anzugeben.

Die Felder sind:

-   Bits 0-15: Standard-QP
-   Bits 16-31: QP für I-Frames
-   Bits 32-47: QP für P-Frames
-   Bits 48-63: QP für B-Frames

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird auch mit [H.264 UVC 1.5-Kameraencodern verwendet.](camera-encoder-h264-uvc-1-5.md)

Um eine konsistente Nutzung für verschiedene Encoder zu ermöglichen, sollten Sie davon ausgehen, dass Encoder nur den Standard-QP betrachten und QP-Werte für E/A-Bilder ignorieren können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

