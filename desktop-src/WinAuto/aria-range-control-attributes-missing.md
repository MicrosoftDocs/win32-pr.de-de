---
title: ARIA-Bereichssteuerelementattribute fehlen
description: ARIA-Bereichssteuerelementattribute fehlen
ms.assetid: B79F6277-5339-406A-B5FC-A3657BFC5034
keywords:
- AriaRangeControlAttributesAbsentId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b44e4e5c69ea6971846ed9ef5f3a6108bb488c6effb21a6cbc75953ed1bb780e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645119"
---
# <a name="aria-range-control-attributes-missing"></a>ARIA-Bereichssteuerelementattribute fehlen

## <a name="text"></a>Text

Das Element verfügt über **eine Progressbar-** oder **Schiebereglerrolle,** macht jedoch keine entsprechenden **aria-valuemin-,** **aria-valuemax-** und **aria-valuenow-Attribute** verfügbar.

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Dieser Fehler gilt für Elemente mit einer [**Rolle**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implizit oder explizit), die gleich **progressbar,** **slider** oder **spinbutton** ist.

Gemäß der Spezifikation web accessibility Initiative – Accessible Rich Internet Applications (CSV-ARIA) müssen Elemente mit der **Progressbar-,** **Slider-** oder **Spinbuttonrolle** die Attribute [**aria-valuemax,**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)und [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) verfügbar machen.

Um diesen Fehler zu beheben, legen Sie die Attribute [**aria-valuemax,**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)und [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) fest, und verwalten Sie den **aria-valuenow-Wert** dynamisch, um sicherzustellen, dass der aktuelle Wert verfügbar gemacht wird. Sie sollten auch das [**aria-valuetext-Attribut**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) festlegen, um dem verfügbar gemachten **aria-valuenow-Wert** eine weitere Bedeutung hinzuzufügen.

## <a name="example"></a>Beispiel


```HTML
<div role="slider" id="sl" aria-valuemin="1" aria-valuemax="5" aria-valuenow="3" aria-valuetext="good"…>
</div>

<script>
  // This function should be triggered when the slider value changes.
  function manageValue()
  {
    ...
    sl.setAttribute("aria-valuenow", currentValue);
    sl.setAttribute("aria-valuetext", currentValueText);
    ...
  }
</script>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Inkompatible ARIA-Bereichssteuerelementattribute](aria-range-control-attribute-out-of-range.md)
</dt> </dl>

 

 




