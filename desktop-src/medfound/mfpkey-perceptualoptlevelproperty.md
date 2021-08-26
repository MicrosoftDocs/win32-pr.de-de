---
description: Gibt an, ob der Codec bei der Codierung eine konservative Perzepptuelloptimierung verwenden soll.
ms.assetid: f44fd932-d8f8-46c7-b17c-27e6141408ab
title: MFPKEY_PERCEPTUALOPTLEVEL-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f9eb74ae025dbddbdea7f76c2af8b15e912cf80ebd06e810a5214bf9798d1bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953850"
---
# <a name="mfpkey_perceptualoptlevel-property"></a>MFPKEY \_ PERCEPTUALOPTLEVEL-Eigenschaft

Gibt an, ob der Codec bei der Codierung eine konservative Perzepptuelloptimierung verwenden soll.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCPerceptualOptLevel

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Hinweise

Die konservativ wahrnehmliche Optimierung ist ein Prozess, bei dem der Codec versucht, "wichtige" und "unwichtige" Bereiche im Videoframe zu identifizieren. Nachdem diese Bereiche des Rahmens identifiziert wurden, hat der Codec der Qualität wichtiger Regionen eine höhere Priorität, was auf Kosten der Qualität unwichtiger Regionen geht.

Die perzeptische Optimierung legt den Wert darauf, dass das Bild für das menschliche Auge korrekt angezeigt wird, anstatt sich mit strikter mathematischer Genauigkeit zu begnähren.

Die Ergebnisse der Optimierung variieren je nach Art des zu codierten Videos erheblich. Dieses Feature eignet sich möglicherweise gut für die Codierung mit niedriger Bitrate und niedriger Auflösung (z. B. Webstreaming), sollte aber bei der Archivierung von Videoqualität wahrscheinlich vermieden werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




