---
title: Button. Kurznotiz
description: Mit dem Attribut "Kurznotiz" wird ein Wert angegeben oder abgerufen, der angibt, ob die Schaltfläche eine UMSCHALT Fläche ist, d. h. ob es sich um eine Schaltfläche mit zwei Zuständen oder einem Bundesstaat handelt
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- Button. Kurztaste für Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de9b4e1a8e4bab04e5729cb45662164e2dfa2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372247"
---
# <a name="buttonsticky"></a>Button. Kurznotiz

Mit **dem Attribut "** Kurznotiz" wird ein Wert angegeben oder abgerufen, der angibt, ob die **Schaltfläche** eine UMSCHALT Fläche ist, d. h. ob es sich um eine **Schaltfläche** mit zwei Zuständen oder einem Bundesstaat handelt

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                        |
|-------|------------------------------------|
| true  | Die **Schaltfläche** ist kurz.              |
| false | Standard. Die **Schaltfläche** ist nicht kurz. |



 

## <a name="remarks"></a>Bemerkungen

Wenn **für** "Kurznotiz" der Wert "true" festgelegt ist, wechselt die **Schaltfläche** in den Zustand "nach unten" und bleibt so lange in diesem Zustand Wenn sich die **Schaltfläche** im Zustand "herunter" befindet, ist das Attribut " **nach unten** " auf "true" festgelegt, und das **Fenster Mage** wird angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Button-Element**](button-element.md)
</dt> <dt>

[**Schaltfläche. nach unten**](button-down.md)
</dt> <dt>

[**Button. downImage**](button-downimage.md)
</dt> </dl>

 

 





