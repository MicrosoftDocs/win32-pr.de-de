---
title: Effekte. Currency-ffecttype
description: Das Attribut "attributeffecttype" gibt den Registrierungs Namen der aktuellen Visualisierung an oder ruft ihn ab. Dieser Name ist eine eindeutige ID, die vom Visualisierungs Autor definiert wurde.
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- Effekte. Currency-ffecttype Windows-Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7c7671c4a5dce9df81cf8f9d770d71eba3325e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351228"
---
# <a name="effectscurrenteffecttype"></a>Effekte. Currency-ffecttype

Das Attribut " **attributeffecttype** " gibt den Registrierungs Namen der aktuellen Visualisierung an oder ruft ihn ab. Dieser Name ist eine eindeutige ID, die vom Visualisierungs Autor definiert wurde.

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Sie können dieses Attribut zur Laufzeit verwenden, um den aktuell angezeigten Effekt zu ändern. Gehen Sie hierzu folgendermaßen vor:

1.  Verwenden Sie **effectcount** , um die Anzahl der registrierten Effekte abzurufen.
2.  Rufen Sie in einer-Schleife den Namen jedes registrierten Effekts mithilfe von **EffectType** ab.
3.  Geben Sie einen der Namen **an, den** Sie für "" "" "" "" "" "" "" "" ""

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Effects-Element**](effects-element.md)
</dt> <dt>

[**Effekte. Currency-ffect**](effects-currenteffect.md)
</dt> <dt>

[**Effects. effectcount**](effects-effectcount.md)
</dt> <dt>

[**Effects. EffectType**](effects-effecttype.md)
</dt> </dl>

 

 





