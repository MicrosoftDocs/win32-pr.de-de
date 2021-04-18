---
title: Effekte. Currency-ffect
description: Das Attribut "attributeffect" gibt die aktuelle Visualisierung an oder ruft Sie ab.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- Effekte. Currency-ffect-Fenster Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19398946906fb6c6ea43234c110383b27b16ede
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372279"
---
# <a name="effectscurrenteffect"></a>Effekte. Currency-ffect

Das Attribut " **attributeffect** " gibt die aktuelle Visualisierung an oder ruft Sie ab.

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein Lese- **/schreibjekt**. Der Standardwert ist die erste Visualisierung in der Erstellungs Reihenfolge. Wenn keine Visualisierungen in der Skin erstellt wurden, ist der Standardwert die erste Visualisierung in der Registrierung.

## <a name="remarks"></a>Bemerkungen

Mit diesem Objekt können Sie auf benutzerdefinierte Visualisierungen zugreifen, die Sie erstellt haben. Beispielsweise können Sie eine Eigenschaft über die **IDispatch** -Schnittstelle in der Visualisierung verfügbar machen. Anschließend können Sie den Eigenschafts Wert aus der Skin ändern, indem Sie die Visualisierung auf den aktuellen Effekt festlegen, und dann das Objekt " **setobffect** " verwenden, um einen neuen Wert für die Eigenschaft festzulegen. Wenn Ihre Visualisierung z. b. eine Eigenschaft mit dem Namen BackgroundColor verfügbar macht, gibt der folgende JScript-Code einen neuen Wert an:


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Effects-Element**](effects-element.md)
</dt> <dt>

[**Effekte. Currency-ffecttitle**](effects-currenteffecttitle.md)
</dt> <dt>

[**Effekte. Currency-ffecttype**](effects-currenteffecttype.md)
</dt> </dl>

 

 





