---
title: Effects. EffectType
description: Die EffectType-Methode ruft den Registrierungs Namen der Visualisierung mit dem angegebenen Registrierungs Index ab. Dieser Name ist eine eindeutige ID, die vom Visualisierungs Autor definiert wurde.
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- Effekte. EffectType-Fenster Media Player
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3eda9cbd1a4634062683536f1f132393a2874691
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366700"
---
# <a name="effectseffecttype"></a>Effects. EffectType

Die **EffectType** -Methode ruft den Registrierungs Namen der Visualisierung mit dem angegebenen Registrierungs Index ab. Dieser Name ist eine eindeutige ID, die vom Visualisierungs Autor definiert wurde.

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Sin*
</dt> <dd>

**Zahl** (**Long**), die den Registrierungs Index einer Visualisierung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ist hilfreich für den Wechsel zwischen Visualisierungen im Skript. Eine Benutzeroberfläche könnte den Satz von Titeln anzeigen. wenn der Benutzer jedoch eine solche Tabelle auswählt, muss das Skript für die Visualisierung von Visualisierungen die Verwendung von " **einstellerffecttype** " verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Effects-Element**](effects-element.md)
</dt> <dt>

[**Effekte. Currency-ffecttype**](effects-currenteffecttype.md)
</dt> </dl>

 

 





