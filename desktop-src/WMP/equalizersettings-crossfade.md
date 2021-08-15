---
title: EQUALIZERSETTINGS.crossFade
description: Das crossFade-Attribut gibt einen Wert an, der angibt, ob Das Überblenden aktiviert ist, oder ruft einen Wert ab.
ms.assetid: 6c5a31f3-982e-4660-80ff-30b7a4290a15
keywords:
- EQUALIZERSETTINGS.crossFade Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.crossFade
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff38ee7634f31da7717bfca015ebaacd88796d9c8186faef155704a449bbb07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118838625"
---
# <a name="equalizersettingscrossfade"></a>EQUALIZERSETTINGS.crossFade

Das **crossFade-Attribut** gibt einen Wert an, der angibt, ob Das Überblenden aktiviert ist, oder ruft einen Wert ab.

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Lese-/Schreib-Wert.



| Wert | BESCHREIBUNG                      |
|-------|----------------------------------|
| true  | Das Überblenden ist aktiviert.           |
| false | Standard. Kreuzblenden ist deaktiviert. |



 

## <a name="remarks"></a>Hinweise

Das Überblenden ist ein Audioverarbeitungsfeature, das die Lautstärke eines Medienelements am Ende der Wiedergabe schrittweise verringert, während gleichzeitig die Wiedergabe des nächsten Medienelements bei minimaler Lautstärke gestartet und schrittweise auf die normale Lautstärke erhöht wird. Die Überlappung zwischen dem Anfang des zweiten Medienelements und dem Ende des ersten Medienelements wird durch das **crossFadeWindow-Attribut** angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EQUALIZERSETTINGS-Element**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.crossFadeWindow**](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





