---
title: Aria-Bereichs Steuerungs Attribute fehlen
description: Aria-Bereichs Steuerungs Attribute fehlen
ms.assetid: B79F6277-5339-406A-B5FC-A3657BFC5034
keywords:
- Ariarangecontrolattributesabwestid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8cd32a7a4807f06c26bd013ee3fd294d33cc57
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104039775"
---
# <a name="aria-range-control-attributes-missing"></a>Aria-Bereichs Steuerungs Attribute fehlen

## <a name="text"></a>Text

Das Element hat die Rolle " **ProgressBar** " oder " **Slider** ", aber keine entsprechenden Attribute " **Aria-valuemin** ", " **Aria-valuemax** " und " **Aria-valuenow** " verfügbar.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gilt für Elemente, die eine (implizite oder explizite) [**Rolle**](https://developer.mozilla.org/docs/Web/HTML/Reference) aufweisen, die der **ProgressBar**, dem **Schieberegler** oder dem **SpinButton** entspricht.

Gemäß der von Web Accessibility Initiative zugänglichen Spezifikation für Rich Internet Applications (WAI-ARIA) müssen Elemente, die über die Rollen " **ProgressBar**", " **Slider**" oder " **SpinButton** " verfügen, die Attribute " [**Aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)", " [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)" und " [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) " verfügbar machen.

Um diesen Fehler zu beheben, legen Sie die Attribute [**Aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)und [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) fest, und verwalten Sie den Wert von **Aria-valuenow** dynamisch, um sicherzustellen, dass der aktuelle Wert verfügbar gemacht wird. Sie sollten auch das [**Aria-ValueText**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) -Attribut festlegen, um dem verfügbar gemachten **Aria-valuenow-** Wert weitere Bedeutungen hinzuzufügen.

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

[Nicht kompatible Aria-Bereichs Steuerungs Attribute.](aria-range-control-attribute-out-of-range.md)
</dt> </dl>

 

 




