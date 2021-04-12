---
title: Aria-Rollen Fehler für Elemente mit Ereignis Handlern
description: Aria-Rollen Fehler für Elemente mit Ereignis Handlern
ms.assetid: 20BB874A-874B-4266-9C7B-49C07D4146DA
keywords:
- Ariacontainerroleerrormessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eede416392e8b4cb644938242a9975238118ff07
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104391156"
---
# <a name="aria-role-error-for-elements-with-event-handlers"></a>Aria-Rollen Fehler für Elemente mit Ereignis Handlern

## <a name="text"></a>Text

Das Element hat einen Ereignishandler, aber eine gültige Rolle "WAI-ARIA" ist nicht definiert.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gilt für Elemente, die nicht über eine implizite webanbarrierefreiheits Initiative verfügen, die über die Rolle "Ria-Aria" verfügt.

Dieser Fehler zeigt an, dass ein Element über einen Maus-oder Tastaturereignis Handler verfügt (**Klicken Sie auf**, **MouseDown**, **MouseUp**, **MouseMove**, **mouseout**, **MouseOver**, **KeyUp**, **KeyDown** oder **KeyPress**), aber nicht das [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) -Attribut festgelegt ist und kein HTML-Tag ist, das über eine implizite WAI-ARIA-Rolle verfügt (z. b. **a**, **Button**, **IMG**, **Input**, **Select** usw.).

Das Festlegen des [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) -Attributs für interaktive Elemente, die keine implizite Rolle haben (z. b. ein **div** -Tag), ist erforderlich, um die Verhaltensmuster des Elements für Sprachausgabe und andere Hilfstechnologien verfügbar zu machen.

Um diesen Fehler zu beheben, legen Sie das [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) -Attribut auf eine gültige Rolle "WAI-ARIA" fest, die am besten zu den Verhaltensmustern und den erforderlichen Attributen dieses Elements passt. Wenn ein **div** -Tag z. b. als Schaltfläche fungiert, legen Sie das role-Attribut auf "Button" fest.

## <a name="example"></a>Beispiel


```HTML
<!-- Setting role attribute allows screen readers to know it can be clicked -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




