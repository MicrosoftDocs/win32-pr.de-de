---
title: EFFECTS.currentEffectType
description: Das attribut currentEffectType gibt den Registrierungsnamen der aktuellen Visualisierung an oder ruft den Namen ab. Dieser Name ist eine eindeutige ID, die vom Autor der Visualisierung definiert wird.
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- EFFECTS.currentEffectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8df55ae806781fa0924349cfe472f355cdabd2be6723148fc6100dc39efd9062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996750"
---
# <a name="effectscurrenteffecttype"></a>EFFECTS.currentEffectType

Das **attribut currentEffectType** gibt den Registrierungsnamen der aktuellen Visualisierung an oder ruft den Namen ab. Dieser Name ist eine eindeutige ID, die vom Autor der Visualisierung definiert wird.

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Zeichenfolge mit **Lese-/Schreibzugriff.**

## <a name="remarks"></a>Hinweise

Sie können dieses Attribut zur Laufzeit verwenden, um den derzeit angezeigten Effekt zu ändern. Gehen Sie hierzu folgendermaßen vor:

1.  Verwenden **Sie effectCount,** um die Anzahl registrierter Effekte abzurufen.
2.  Rufen Sie in einer Schleife den Namen jedes registrierten Effekts mit **effectType ab.**
3.  Geben Sie einen der Namen an, die Sie für **currentEffectType abgerufen haben,** um den aktuellen Effekt festzulegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EFFECTS-Element**](effects-element.md)
</dt> <dt>

[**EFFECTS.currentEffect**](effects-currenteffect.md)
</dt> <dt>

[**EFFECTS.effectCount**](effects-effectcount.md)
</dt> <dt>

[**EFFECTS.effectType**](effects-effecttype.md)
</dt> </dl>

 

 





