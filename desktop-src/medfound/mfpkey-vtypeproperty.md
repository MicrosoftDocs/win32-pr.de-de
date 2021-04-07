---
description: Gibt die Logik an, die der Codec zum Erkennen von Zeilen Sprung-Quellvideos verwendet.
ms.assetid: 29c7fc1c-2047-4562-ba14-48f9cfbfe68c
title: MFPKEY_VTYPE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e95bab3120e60a2faa1a3be47c6459205f5f34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863440"
---
# <a name="mfpkey_vtype-property"></a>Mfpkey- \_ VType (Eigenschaft)

Gibt die Logik an, die der Codec zum Erkennen von Zeilen Sprung-Quellvideos verwendet.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcvtype

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.



| Wert | BESCHREIBUNG                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Der Codec verwendet die standardmäßige Erkennungs Logik für Frame Typen.                                                                                 |
| 1     | Der Codec behandelt alle Quellvideo Frames als Zeilen Sprung Rahmen.                                                                          |
| 2     | Der Codec behandelt alle Quellvideo Frames als Felder mit Zeilen Sprung Video.                                                                 |
| 3     | Der Codec ermittelt automatisch, ob Eingabe Videorahmen Zeilen Sprung Rahmen oder Felder mit Zeilen Sprung Video sind.                      |
| 4     | Der Codec ermittelt automatisch, ob eingabevideoframes progressive Frames, Zeilen Sprung Rahmen oder Felder mit Zeilen Sprung Videos sind. |



 

Diese Eigenschaft bestimmt die Bild Codierungsmethode, die für die Progressive oder Zeilen Sprung Videocodierung verwendet wird.

Wenn kein Videotyp angegeben wird, verwendet der Codec die Progressive Frame Codierung für Progressive Codierungs Sitzungen und die Feld Zeilen Sprung-Codierung für Zeilen Sprung-Codierungs Sitzungen. Der Typ der Video Codierungs Sitzung (progressiv oder Zeilen Sprung) wird mithilfe der [mfpkey \_ interlacedcodingenabled](mfpkey-interlacedcodingenabledproperty.md) -Eigenschaft festgelegt.

> [!Note]  
> Die [mfpkey \_ interlacedcodingenabled](mfpkey-interlacedcodingenabledproperty.md) -Eigenschaft muss auf Variant true festgelegt werden, um eine Zeilen Sprung \_ Ausgabe zu erzielen. andernfalls hat das Festlegen der "mpfkey"- \_ Eigenschaft "VType" keine Auswirkung.

 

Wenn das Zeilen Sprung Video codiert wird, können mehrere Bild Codierungs Methoden angegeben werden. In der Regel die effizienteste Methode zum Codieren von Zeilen Sprung Videos ist die Verwendung der Methode "Field interschnür" (2). Wenn das Quellvideo sehr wenig Bewegung enthält, kann die Frame-interschnür Methode (1) oder die automatische Frame-/Feldmethode (2) besser geeignet sein.

Beim Codieren gemischter Inhalte (die sowohl Progressive als auch Zeilen Sprung Rahmen enthalten) ist es am besten, den Wert Auto-Frame/Feld/Progressive-Methode (4) zu verwenden.

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

 

 




