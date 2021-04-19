---
description: Gibt die Anzahl der bidirektionalen Vorhersage Rahmen (B-Frames) an.
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: MFPKEY_NUMBFRAMES-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3b0655a4a5e24b92f9699b198f10232de8edf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372985"
---
# <a name="mfpkey_numbframes-property"></a>Mfpkey- \_ numbframes (Eigenschaft)

Gibt die Anzahl der bidirektionalen Vorhersage Rahmen (B-Frames) an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcnumbframes

## <a name="data-type"></a>Datentyp

VT-I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Bemerkungen

Standardmäßig verwendet Windows Media Video 9 nur die Rahmen (I-Frames) (I-Frames), die auch als Keyframes oder Anker Frames bezeichnet werden, bei denen es sich um vollständig codierte Frames und Vorhersage Rahmen (P-Frames) handelt, die als Unterschied zum vorherigen I-Frame codiert werden. B-Frames unterscheiden sich von P-Frames, da Sie sowohl die Unterschiede zwischen dem vorherigen Frame als auch die Unterschiede zwischen dem folgenden Frame speichern.

Wenn Sie den Codec so konfigurieren, dass er b-Frames verwendet, wird die angegebene Anzahl von b-Frames zwischen jedem Paar von Frames des Typs I oder P verwendet.

Wenn eine Sequenz von Frames ohne b-Frames z. b. "ippppppppi" ist, wäre dieselbe Sequenz Codierung mit zwei b-Frames "ibbpbbpbbi".

Für die meisten Inhalte sind entweder ein oder zwei B-Frames geeignet. Bei höheren Datenraten ist ein B-Frame normalerweise die optimale Wahl. Drei oder mehr sind selten nützlich.

Der gültige Wertebereich für diese Eigenschaft ist 0 bis 7.

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

 

 




