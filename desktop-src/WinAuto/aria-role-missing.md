---
title: ARIA-Rollenfehler für Elemente mit Ereignishandlern
description: ARIA-Rollenfehler für Elemente mit Ereignishandlern
ms.assetid: 20BB874A-874B-4266-9C7B-49C07D4146DA
keywords:
- AriaContainerRoleErrorMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cebaa2e6f4526d0a1e820e60adc1d28439d3f361c7ffb58a0c4d855861ea46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133993"
---
# <a name="aria-role-error-for-elements-with-event-handlers"></a>ARIA-Rollenfehler für Elemente mit Ereignishandlern

## <a name="text"></a>Text

Das -Element verfügt über einen Ereignishandler, aber die gültige ROLLE "TS-ARIA" ist nicht definiert.

## <a name="type"></a>type

Fehler

## <a name="description"></a>Beschreibung

Dieser Fehler gilt für Elemente, die nicht über die implizite Rolle Web Accessibility Initiative - Accessible Rich Internet Applications (TS-ARIA) verfügen.

Dieser Fehler gibt **an,** dass ein Element über einen Maus- oder Tastaturereignishandler **verfügt**( klicken Sie auf , **mousedown**, **mouseup** [](https://developer.mozilla.org/docs/Web/HTML/Reference) , **mousemove**, **mouseout**, **mouseover**, **keyup**, **keydown** oder **keypress**), aber nicht das Rollenattribut festgelegt ist und nicht eines der HTML-Tags ist, das über eine implizite ROLLE-ARIA-Rolle verfügt (z. B. eine **,** Schaltfläche, **img** **,** eingabe **,** select und so weiter).

Das [](https://developer.mozilla.org/docs/Web/HTML/Reference) Festlegen des Rollenattributs für interaktive Elemente, die keine implizite Rolle haben (z. B. ein **div-Tag),** ist erforderlich, um die Verhaltensmuster des Elements für Sprachbildschirme und andere Hilfstechnologien verfügbar zu machen.

Um diesen Fehler zu [](https://developer.mozilla.org/docs/Web/HTML/Reference) beheben, legen Sie das Rollenattribut auf eine gültige ROLLE VOM-ARIA-Element fest, die am besten zu den Verhaltensmustern und erforderlichen Attributen dieses Elements passt. Wenn ein **div-Tag beispielsweise** als Schaltfläche fungiert, legen Sie das Rollenattribut auf "button" fest.

## <a name="example"></a>Beispiel


```HTML
<!-- Setting role attribute allows screen readers to know it can be clicked -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




