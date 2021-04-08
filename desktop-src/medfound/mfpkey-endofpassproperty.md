---
description: Gibt das Ende eines Codierungs Durchlaufs an.
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: MFPKEY_ENDOFPASS-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a38e03867e11cde944bf902ae52f98cda7b8313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864163"
---
# <a name="mfpkey_endofpass-property"></a>Mfpkey- \_ endofpass (Eigenschaft)

Gibt das Ende eines Codierungs Durchlaufs an.

## <a name="data-type"></a>Datentyp

**VT \_ bool**

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcendofpass

## <a name="data-type-for-ipropertybag"></a>Datentyp für IPropertyBag

Es ist kein Datentyp erforderlich. Um diese Eigenschaft festzulegen, übergeben Sie eine nicht initialisierte **Variante**.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist keine normale Eigenschaft, da Sie unabhängig davon, ob der Wert Variant \_ true oder Variant false ist, dieselbe Auswirkung hat \_ . Sie müssen diese Eigenschaft festlegen, nachdem Sie die letzten Eingabe Beispiele für einen Vorverarbeitungs Durchlauf verarbeitet haben. Wenn Sie mehrere Durchgänge ausführen, müssen Sie diese Eigenschaft am Ende jedes Vorverarbeitungs Durchsatzes festlegen (derzeit unterstützt keiner der Codecs mehr als einen). Wenn Sie diese Eigenschaft nicht festlegen, geht der Codec davon aus, dass Sie immer noch Beispiele für die Vorverarbeitung übergeben.

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

 

 




