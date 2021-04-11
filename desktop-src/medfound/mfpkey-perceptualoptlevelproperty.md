---
description: Gibt an, ob der Codec beim Codieren die konservative perzeptive Optimierung verwenden soll.
ms.assetid: f44fd932-d8f8-46c7-b17c-27e6141408ab
title: MFPKEY_PERCEPTUALOPTLEVEL-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d86857ca9d7e4205afc0baf9c212e92606511ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215504"
---
# <a name="mfpkey_perceptualoptlevel-property"></a>Mfpkey- \_ Eigenschaft ' peraloptlevel '

Gibt an, ob der Codec beim Codieren die konservative perzeptive Optimierung verwenden soll.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcperperaloptlevel

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Bemerkungen

Die konservative perzeptive Optimierung ist ein Prozess, bei dem der Codec versucht, "wichtige" und "unbedeutende" Bereiche im Videoframe zu identifizieren. Nachdem Sie diese Bereiche des Frames identifiziert haben, erhält der Codec die Qualität wichtiger Regionen auf Kosten der Qualität wichtiger Regionen.

Die perzeptive Optimierung hebt hervor, dass das Bild für das menschliche Auge richtig angezeigt wird, anstatt auf eine strikte mathematische Genauigkeit zu beharren.

Die Ergebnisse der Optimierung variieren in Abhängigkeit vom Typ des codierten Videos erheblich. Diese Funktion eignet sich gut für die Codierung mit geringem Bitrate und niedriger Auflösung (z. b. Webstreaming), sollte aber wahrscheinlich vermieden werden, wenn Sie auf die Archivierung von Videoqualität abzielen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




