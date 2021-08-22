---
description: Gibt die Frametypen (I, P oder B) an, auf die der Quantisierungsparameter (QP) angewendet wird.
ms.assetid: 6331033F-7EEB-41B3-B166-29686D4AADB6
title: CODECAPI_AVEncVideoEncodeFrameTypeQP (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9ebd4a25f3779ce1c721eb3cb1188b487be4d313ae5dbeb02dd41e494f4c17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743851"
---
# <a name="codecapi_avencvideoencodeframetypeqp-property"></a>CODECAPI \_ AVEncVideoEncodeFrameTypeQP (Eigenschaft)

Gibt die Frametypen (I, P oder B) an, auf die der Quantisierungsparameter (QP) angewendet wird.

## <a name="data-type"></a>Datentyp

**ULONGULONG** (VT \_ UI8)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncVideoEncodeFrameTypeQP**

## <a name="remarks"></a>Hinweise

Für Encoder, die das Festlegen eines Quantisierungsparameters (QP) für verschiedene Frametypen (I, P, B) unterstützen, müssen sie diese API zusätzlich zu [CODECAPI \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)verfügbar machen. Wenn ein Encoder nur einen einzelnen QP für alle Frametypen unterstützt, sollte er nur CODECAPI \_ AVEncVideoEncodeQP unterstützen.

Dies ist eine dynamische Codierungseigenschaft, was bedeutet, dass ein neuer Wert jederzeit während der Codierungssitzung festgelegt werden kann.

**H.264/AVC-Encoder:**

Der Encoder muss [**GetValue,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)und [**GetParameterRange unterstützen.**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)

Ein Satz von vier 16-Bit-Feldern wird verwendet, um die Frame-QPs in der Fixed QP-Codierung anzugeben. Die Felder sind:

-   **Bits 0-15:** QP für I-Frames, gültiger Bereich \[ 0, 51 \] .
-   **Bits 16-31:** QP für P-Frames, gültiger Bereich \[ 0, 51 \] .
-   **Bits 32-47:** QP für B-Frames, gültiger Bereich \[ 0, 51\]
-   **Bits 48-63:** reserviert

Wenn diese CodecAPI unterstützt wird, müssen Encoder die QP-Einstellung für den Frametyp I, P und B unterstützen.

Der Standardwert muss 0x0000001a001a001a. QP entspricht 26 für I, P und B.

Wenn [CODECAPI \_ AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) eine bestimmte temporale Ebene auswählt, muss [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) von CODECAPI \_ AVEncVideoEncodeFrameTypeQP QP für I-, P- und B-Frames auf dieser temporalen Ebene festlegen. Standardmäßig wird QP für I-, P- und B-Frames auf temporaler Basisebene temporaler Ebene 0 festgelegt.

[CODECAPI \_ AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) und [CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md) müssen verwendet werden, um den QP-Bereich für QPs aller Bildtypen I, P und B zu definieren und zu beschränken.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Desktop-Apps \| UWP-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

