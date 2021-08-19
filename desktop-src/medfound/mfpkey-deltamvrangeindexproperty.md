---
description: Gibt die Methode an, die zum Codieren der Bewegungsvektorinformationen verwendet wird.
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: MFPKEY_DELTAMVRANGEINDEX-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a21ac1a0bdaf859c93bca800d72f5e9ed155919bb07a24f5287b2436e57f94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113340"
---
# <a name="mfpkey_deltamvrangeindex-property"></a>MFPKEY \_ DELTAMVRANGEINDEX-Eigenschaft

Gibt die Methode an, die zum Codieren der Bewegungsvektorinformationen verwendet wird.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCDeltaMVRangeIndex

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="default-value"></a>Standardwert

0

## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft festgelegt ist, erhöht der Encoder den Deltabewegungsvektorbereich in Feldern. Bewegungsvektorinformationen sind nur für Felder mit Zeilensprung gültig.

Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden:



| Wert | BESCHREIBUNG                                                                          |
|-------|--------------------------------------------------------------------------------------|
| 0     | Verwenden Sie den vorhandenen Deltabewegungsvektorbereich.                                          |
| 1     | Doppelklicken Sie den Deltabewegungsvektorbereich in horizontaler Richtung.                    |
| 2     | Doppelklicken Sie den Deltabewegungsvektorbereich in vertikaler Richtung.                      |
| 3     | Doppelklicken Sie den Deltabewegungsvektorbereich in horizontaler und vertikaler Richtung. |



 

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

 

 




