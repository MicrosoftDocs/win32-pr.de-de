---
description: Gibt den in Bewegungs suchen verwendeten Bereich an.
ms.assetid: b2026f47-ac39-4276-8359-c939b202f00c
title: MFPKEY_MOTIONSEARCHRANGE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c557ea1a462192434222e425dccb8b9a0e291986
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215509"
---
# <a name="mfpkey_motionsearchrange-property"></a>Mfpkey- \_ Eigenschaft "mutionsearchrange"

Gibt den in Bewegungs suchen verwendeten Bereich an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcmutionsearchrange

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden. H bezeichnet den horizontalen Bereich und V den vertikalen Bereich. Alle Bereiche werden in Pixel angegeben.



| Wert | Range                                |
|-------|--------------------------------------|
| 0     | + 63.75/-64,0 H, + 31.75/-32,0 V       |
| 1     | +127,75/-128,0 H, +63,75/-64,0 V     |
| 2     | + 511.75/-512.0 H, + 127.75/-128.0 V   |
| 3     | + 1023.75/-1024.0 H, + 255.75/-256.0 V |
| -1    | Macroblock-Adaptive (automatisch)      |



 

Diese Eigenschaft steuert die Größe des Frame Bereichs, den der Codec nach einem Element sucht, das möglicherweise eine Bewegung zwischen Frames feststellt. Ein größeres Suchfenster hilft, schnellere Bewegung zu finden, erfordert jedoch mehr CPU-Zeit. Die CPU-Anforderungen werden auf jeder Ebene ungefähr verdoppelt.

Im automatischen Modus (-1) wird dynamisch der effizienteste Modus ausgewählt.

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

 

 




