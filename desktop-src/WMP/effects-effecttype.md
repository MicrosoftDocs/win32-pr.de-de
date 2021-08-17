---
title: EFFECTS.effectType
description: Die effectType-Methode ruft den Registrierungsnamen der Visualisierung mit dem angegebenen Registrierungsindex ab. Dieser Name ist eine eindeutige ID, die vom Autor der Visualisierung definiert wird.
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- EFFECTS.effectType-Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a452f9218c7004d1078ae6b9e878421a7cad301f3ee913ef6296aaa1c681b736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749232"
---
# <a name="effectseffecttype"></a>EFFECTS.effectType

Die **effectType-Methode** ruft den Registrierungsnamen der Visualisierung mit dem angegebenen Registrierungsindex ab. Dieser Name ist eine eindeutige ID, die vom Autor der Visualisierung definiert wird.

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Index*
</dt> <dd>

**Number** (**long**), die den Registrierungsindex einer Visualisierung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge zurück.**

## <a name="remarks"></a>Hinweise

Diese Methode ist nützlich, um zwischen Visualisierungen im Skript zu wechseln. Eine Benutzeroberfläche kann den Satz von Titeln anzeigen, aber wenn der Benutzer einen Titel auswählt, muss das Skript **currentEffectType** verwenden, um visualisierungen zu wechseln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EFFECTS-Element**](effects-element.md)
</dt> <dt>

[**EFFECTS.currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





