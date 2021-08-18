---
title: EFFECTS.currentEffect
description: Das attribut currentEffect gibt die aktuelle Visualisierung an oder ruft sie ab.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- EFFECTS.currentEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d9ac47ef88d1a0bce4982f71ce2e20e33f48933c9916bbb1e62085b5a1e5178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996870"
---
# <a name="effectscurrenteffect"></a>EFFECTS.currentEffect

Das **attribut currentEffect** gibt die aktuelle Visualisierung an oder ruft sie ab.

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein Lese-/Schreibobjekt. Der Standardwert ist die erste Visualisierung in der Erstellungsreihenfolge. Wenn in der Skin keine Visualisierungen erstellt wurden, ist die Standardeinstellung die erste Visualisierung in der Registrierung.

## <a name="remarks"></a>Hinweise

Sie können dieses Objekt verwenden, um auf benutzerdefinierte Visualisierungen zuzugreifen, die Sie erstellt haben. Beispielsweise können Sie eine Eigenschaft über die **IDispatch-Schnittstelle** in Ihrer Visualisierung verfügbar machen. Sie können dann den Eigenschaftswert von Ihrer Skin ändern, indem Sie die Visualisierung zum aktuellen Effekt machen und dann das **currentEffect-Objekt** verwenden, um einen neuen Wert für die Eigenschaft festzulegen. Wenn Ihre Visualisierung beispielsweise eine Eigenschaft mit dem Namen backgroundColor verfügbar macht, gibt der folgende JScript Code einen neuen Wert an:


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EFFECTS-Element**](effects-element.md)
</dt> <dt>

[**EFFECTS.currentEffectTitle**](effects-currenteffecttitle.md)
</dt> <dt>

[**EFFECTS.currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





