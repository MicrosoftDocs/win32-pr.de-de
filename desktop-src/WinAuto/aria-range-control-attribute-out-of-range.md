---
title: Nicht kompatible Aria-Bereichs Steuerungs Attribute.
description: Nicht kompatible Aria-Bereichs Steuerungs Attribute.
ms.assetid: 265AE578-D841-4931-9F4A-97BB86ECEC88
keywords:
- Ariarangecontrolattributesincompatibleid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef55ee57c4966896e666dd5a7ac1d20eb5257c6
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104517189"
---
# <a name="aria-range-control-attributes-incompatible"></a>Nicht kompatible Aria-Bereichs Steuerungs Attribute.

## <a name="text"></a>Text

Das Element hat die Rolle " **ProgressBar** " oder " **Slider** ", aber der Status " **Aria-valuenow** " liegt außerhalb des Aria- **valuemin** **-** Bereichs

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gilt für Elemente, die eine (implizite oder explizite) [**Rolle**](https://developer.mozilla.org/docs/Web/HTML/Reference) aufweisen, die der **ProgressBar**, dem **Schieberegler** oder dem **SpinButton** entspricht.

Dieser Fehler zeigt an, dass der verfügbar [**gemachte Aria-valuenow-**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) Wert nicht im Bereich liegt, der durch die Attribute " [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) " und " [**Aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) " definiert wird.

Um diesen Fehler zu beheben, überprüfen Sie Ihre Implementierung, um sicherzustellen, dass die Attribute " [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) " und " [**Aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) " ordnungsgemäß festgelegt sind und der Wert des [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) -Attributs ordnungsgemäß verwaltet wird

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aria-Bereichs Steuerungs Attribute fehlen](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 




