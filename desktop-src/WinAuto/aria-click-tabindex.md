---
title: ARIA– Tabindexfehler
description: ARIA– Tabindexfehler
ms.assetid: CCBC56E8-8899-4962-8315-762538CA666C
keywords:
- AriaTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1637008b6679f196f7bba0701606e0514abe44410032e1a5ffc063977ddf10e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326745"
---
# <a name="aria-tabindex-error"></a>ARIA– Tabindexfehler

## <a name="text"></a>Text

Das Element ist nicht  deaktiviert und verfügt über einen Click-Ereignishandler, verfügt jedoch über **tabIndex** < 0 und befindet sich standardmäßig nicht in der Tabstoppreihenfolge.

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Dieser Fehler gilt für Elemente, die über einen Click-Ereignishandler verfügen und nicht deaktiviert sind. Diese Elemente müssen in der Reihenfolge der Registerkarten sein. Dadurch wird sichergestellt, dass ein Element mithilfe der TAB-TASTE erreicht werden kann. Auf diese Weise navigieren Benutzer der Sprachausgabe in der Regel auf der Benutzeroberfläche.

Um diesen Fehler zu beheben, legen Sie das [**tabindex-Attribut**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) auf einen Wert fest, der gleich oder größer als 0 ist. Sie müssen das **tabindex-Attribut** nicht explizit für Tags festlegen, die sich standardmäßig in der Tabstoppreihenfolge befinden, z. B. [**ein**](https://developer.mozilla.org/docs/Web/HTML/Element/a) -Element (mit [**href-Attribut),**](https://developer.mozilla.org/docs/Web/HTML/Attributes) [**Schaltfläche**](https://developer.mozilla.org/docs/Web/HTML/Element/button), [**Eingabe**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (mit Ausnahme von "ausgeblendet"), [**Auswählen**](https://developer.mozilla.org/docs/Web/HTML/Element/select)von , [**Textbereich**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)und [**Bereich**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (als Teil der Bilderkarte).

## <a name="example"></a>Beispiel


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




