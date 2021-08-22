---
description: Gibt das Ende eines Codierungsdurchlaufs an.
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: MFPKEY_ENDOFPASS-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977c876d14c6757c5f1bc31e0d5b7cc58f6e13fad827cc23f821be8382a5e376
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738191"
---
# <a name="mfpkey_endofpass-property"></a>MFPKEY \_ ENDOFPASS-Eigenschaft

Gibt das Ende eines Codierungsdurchlaufs an.

## <a name="data-type"></a>Datentyp

**VT \_ BOOL**

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCEndOfPass

## <a name="data-type-for-ipropertybag"></a>Datentyp für IPropertyBag

Es ist kein Datentyp erforderlich. Um diese Eigenschaft festzulegen, übergeben Sie eine nicht initialisierte **VARIANT -Eigenschaft.**

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist keine normale Eigenschaft, da sie unabhängig davon, ob der Wert VARIANT TRUE oder VARIANT FALSE ist, den gleichen Effekt \_ \_ hat. Sie müssen diese Eigenschaft festlegen, nachdem Sie die letzten Eingabebeispiele für einen Vorverarbeitungsdurchlauf verarbeitet haben. Wenn Sie mehrere Durchläufe ausführen, müssen Sie diese Eigenschaft am Ende jedes Vorverarbeitungsdurchlaufs festlegen (derzeit unterstützt keiner der Codecs mehr als einen). Wenn Sie diese Eigenschaft nicht festlegen, geht der Codec davon aus, dass Sie weiterhin Stichproben für die Vorverarbeitung übergeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




