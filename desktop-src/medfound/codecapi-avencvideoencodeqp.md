---
description: Gibt den Quantisierungsparameter (QP) für die Videocodierung an.
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: CODECAPI_AVEncVideoEncodeQP-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec6c746f2f3c902ca416097571abaf5953956cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339723"
---
# <a name="codecapi_avencvideoencodeqp-property"></a>Codecapi \_ avencvideoencodeqp (Eigenschaft)

Gibt den Quantisierungsparameter (QP) für die Videocodierung an.

## <a name="data-type"></a>Datentyp

**ULONGLONG** (VT \_ UI8)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencvideoencodeqp**

## <a name="property-value"></a>Eigenschaftswert

Ein Satz von 4 16-Bit-Feldern, die verwendet werden, um die Frame-QPS in der Fixed-QP-Codierung anzugeben.

Die Felder lauten:

-   Bits 0-15: Standard-QP
-   Bits 16-31: für I-Frames verwendetes QP
-   Bits 32-47: für P-Frames verwendetes QP
-   Bits 48-63: für B-Frames verwendetes QP

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird auch mit [H. 264 UVC 1,5-Kamera Codierern](camera-encoder-h264-uvc-1-5.md)verwendet.

Um eine konsistente Verwendung für verschiedene Encoder sicherzustellen, sollten Sie davon ausgehen, dass Encoder nur das Standard-QP betrachten und QP-Werte für e/a/B-Bilder ignorieren können.

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

 

