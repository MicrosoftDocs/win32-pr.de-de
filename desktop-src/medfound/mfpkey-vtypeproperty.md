---
description: Gibt die Logik an, die der Codec verwendet, um verschachtelte Quellvideos zu erkennen.
ms.assetid: 29c7fc1c-2047-4562-ba14-48f9cfbfe68c
title: MFPKEY_VTYPE-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f406f0bc91e3431672c2b7f92cc544273e2a64403017a22eb4567054cef0155
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973339"
---
# <a name="mfpkey_vtype-property"></a>\_MFPKEY-VTYPE-Eigenschaft

Gibt die Logik an, die der Codec verwendet, um verschachtelte Quellvideos zu erkennen.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCVType

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.



| Wert | BESCHREIBUNG                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Der Codec verwendet die standardmäßige Frametyperkennungslogik.                                                                                 |
| 1     | Der Codec behandelt alle Quellvideoframes als Interlacingframes.                                                                          |
| 2     | Der Codec behandelt alle Quellvideoframes als Felder für Interlacingvideos.                                                                 |
| 3     | Der Codec bestimmt automatisch, ob es sich bei Eingabevideoframes um Interlacingframes oder Felder von videoverschachtelten Videos handelt.                      |
| 4     | Der Codec bestimmt automatisch, ob es sich bei Eingabevideoframes um progressive Frames, Interlacingframes oder Felder von Videointerlacing handelt. |



 

Diese Eigenschaft bestimmt die Bildcodierungsmethode, die für die progressive oder interlaced-Videocodierung verwendet wird.

Wenn kein Videotyp angegeben wird, verwendet der Codec progressive Framecodierung für Sitzungen mit progressiver Codierung und feldübergreifende Codierung für Interlacing-Codierungssitzungen. Der Typ der Videocodierungssitzung (progressiv oder interlaced) wird mithilfe der [MFPKEY \_ INTERLACEDCODINGENABLED-Eigenschaft](mfpkey-interlacedcodingenabledproperty.md) festgelegt.

> [!Note]  
> Die [MFPKEY \_ INTERLACEDCODINGENABLED-Eigenschaft](mfpkey-interlacedcodingenabledproperty.md) muss auf VARIANT TRUE festgelegt werden, um eine \_ Ausgabe mit Zeilensprung zu erzeugen. Andernfalls hat das Festlegen der MPFKEY \_ VTYPE-Eigenschaft keine Auswirkungen.

 

Wenn videoverschachtelte Videos codiert werden, können mehrere Bildcodierungsmethoden angegeben werden. In der Regel ist die effizienteste Methode zum Codieren von videoverschachtelten Videos die Verwendung der Feld-Interlaced-Methode (2). Wenn das Quellvideo nur sehr wenig Bewegung enthält, ist die Frame-Interlaced-Methode (1) oder die Autoframe/Field-Methode (2) möglicherweise besser geeignet.

Beim Codieren gemischter Inhalte (die sowohl progressive als auch Interlacingframes enthalten) ist es am besten, den Wert auto frame/field/progressive method (4) zu verwenden.

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

 

 




