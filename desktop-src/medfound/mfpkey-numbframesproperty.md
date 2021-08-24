---
description: Gibt die Anzahl bidirektionaler Vorhersageframes (B-Frames) an.
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: MFPKEY_NUMBFRAMES-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfcf103da1d629c90209aef4badd604651d73af3e9101cac0f613b47c82883e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555419"
---
# <a name="mfpkey_numbframes-property"></a>MFPKEY \_ NUMBFRAMES-Eigenschaft

Gibt die Anzahl bidirektionaler Vorhersageframes (B-Frames) an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCNumBFrames

## <a name="data-type"></a>Datentyp

VT-I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Hinweise

Standardmäßig verwendet Windows Media Video 9 nur Intraframes (I-Frames), auch bekannt als Keyframes oder Ankerrahmen, die vollständig codierte Frames sind, und Vorhersageframes (P-Frames), die als Unterschied zum vorherigen I-Frame codiert sind. B-Frames unterscheiden sich von P-Frames, da sie sowohl die Unterschiede vom vorherigen Frame als auch die Unterschiede zum folgenden Frame speichern.

Wenn Sie den Codec für die Verwendung von B-Frames konfigurieren, wird die angegebene Anzahl von B-Frames zwischen jedem Framespaar vom Typ I oder P verwendet.

Wenn z. B. eine Sequenz von Frames ohne B-Frames "IPPPPPPLP" ist, wäre die gleiche Sequenzcodierung mit zwei B-Frames "IBBPBBPBBI".

Für die meisten Inhalte sind ein oder zwei B-Frames geeignet. Bei höheren Datenraten ist normalerweise ein B-Frame die optimale Wahl. Drei oder mehr sind selten nützlich.

Der gültige Wertebereich für diese Eigenschaft ist 0 bis 7.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




