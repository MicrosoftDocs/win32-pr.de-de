---
title: Equalizersettings. Crossfade
description: Mit dem Crossfade-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Kreuz ausblenden aktiviert ist.
ms.assetid: 6c5a31f3-982e-4660-80ff-30b7a4290a15
keywords:
- Equalizersettings. Crossfade-Windows-Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.crossFade
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0472f90f94b5c4ba56948848476b6585502427c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367121"
---
# <a name="equalizersettingscrossfade"></a>Equalizersettings. Crossfade

Mit dem **Crossfade** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Kreuz ausblenden aktiviert ist.

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                      |
|-------|----------------------------------|
| true  | Cross-Fade ist aktiviert.           |
| false | Standard. Cross-Fade ist deaktiviert. |



 

## <a name="remarks"></a>Bemerkungen

Cross-Fade ist eine Funktion zur Audioverarbeitung, bei der das Volumen eines Medien Elements nach dem Ende der Wiedergabe allmählich verringert wird, während gleichzeitig die Wiedergabe des nächsten Medien Elements auf dem minimalen Volume gestartet wird und die Daten allmählich auf das normale Volume erhöht werden. Die Überlappung zwischen dem Start des zweiten Medien Elements und dem Ende des ersten Medien Elements wird durch das **crossfadewindow** -Attribut angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Equalizersettings-Element**](equalizersettings-element.md)
</dt> <dt>

[**Equalizersettings. crossfadewindow**](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





