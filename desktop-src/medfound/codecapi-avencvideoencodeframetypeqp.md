---
description: Gibt die Frame Typen (I, P oder B) an, auf die der quantifizierungsparameter (QP) angewendet wird.
ms.assetid: 6331033F-7EEB-41B3-B166-29686D4AADB6
title: CODECAPI_AVEncVideoEncodeFrameTypeQP-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76e68e0cb6cbdc076dbf523f3ae9dfd7b5870f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127976"
---
# <a name="codecapi_avencvideoencodeframetypeqp-property"></a>Codecapi \_ avencvideoencodeframetypeqp (Eigenschaft)

Gibt die Frame Typen (I, P oder B) an, auf die der quantifizierungsparameter (QP) angewendet wird.

## <a name="data-type"></a>Datentyp

**Ulongulong** (VT \_ UI8)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencvideoencodeframetypeqp**

## <a name="remarks"></a>Bemerkungen

Bei Encodern, die das Festlegen eines quantisierungsparameters (QP) für verschiedene Frame Typen (I, P, B) unterstützen, müssen Sie diese API zusätzlich zu [codecapi \_ avencvideoencodeqp](codecapi-avencvideoencodeqp.md)verfügbar machen. Wenn ein Encoder nur ein einzelnes QP für alle Frame Typen unterstützt, darf er nur codecapi \_ avencvideoencodeqp unterstützen.

Dies ist eine dynamische Codierungs Eigenschaft, die bedeutet, dass ein neuer Wert während der Codierungs Sitzung jederzeit festgelegt werden kann.

**H. 264/AVC-Encoder:**

Der Encoder muss " [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)", " [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)" und " [**getparameterrange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)" unterstützen.

Ein Satz von 4 16-Bit-Feldern wird verwendet, um die Frame-QPS in der Fixed-QP-Codierung anzugeben. Die Felder lauten:

-   **Bits 0-15:** Für I-Frames verwendeter QP, gültiger Bereich von \[ 0, 51 \] .
-   **Bits 16-31:** Für P-Frames verwendeter QP, gültiger Bereich von \[ 0, 51 \] .
-   **Bits 32-47:** Für B-Frames verwendeter QP, gültiger Bereich von \[ 0, 51\]
-   **Bits 48-63:** reserviert

Wenn diese codecapi unterstützt wird, unterstützen Encoder die QP-Einstellungen für den Frame-Typ I, P und B.

Der Standardwert muss 0x0000001a001a001a lauten. QP ist gleich 26 für I, P und B.

Wenn [codecapi \_ avencvideoselectlayer](codecapi-avencvideoselectlayer.md) eine bestimmte temporale Ebene auswählt, muss [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) von codecapi \_ avencvideoencodeframetypeqp QP für I-, P-und B-Frames auf dieser temporalen Ebene festlegen. Standardmäßig wird QP für I-, P-und B-Frames auf der temporalen Ebene 0 für temporale Temporale Ebenen festgelegt.

[Codecapi \_ Mithilfe von "avencvideomaxqp](codecapi-avencvideomaxqp.md) " und " [codecapi \_ avencvideominqp](codecapi-avencvideominqp.md) " können Sie den QP-Bereich für QPS aller Bildtypen (I, P und B) definieren und begrenzen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

