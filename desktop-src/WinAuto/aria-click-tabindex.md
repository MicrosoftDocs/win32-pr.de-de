---
title: Tabindexfehler bei ARIA
description: Tabindexfehler bei ARIA
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
# <a name="aria-tabindex-error"></a>Tabindexfehler bei ARIA

## <a name="text"></a>Text

Das Element ist nicht  deaktiviert und verfügt über einen Click-Ereignishandler, verfügt jedoch über **tabIndex** < 0 und befindet sich standardmäßig nicht in der Reihenfolge der Registerkarten.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gilt für Elemente, die über einen Click-Ereignishandler verfügen und nicht deaktiviert sind. Diese Elemente müssen in der Reihenfolge der Registerkarten sein. Dadurch wird sichergestellt, dass ein Element mithilfe der TAB-TASTE erreicht werden kann. Dies ist die Art und Weise, in der Benutzer der Sprachausgabe in der Regel durch die Benutzeroberfläche navigieren.

Um diesen Fehler zu beheben, legen Sie das [**tabindex-Attribut**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) auf einen Wert fest, der gleich oder größer als 0 ist. Sie müssen [](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)das **tabindex-Attribut** nicht explizit für Tags festlegen, die sich standardmäßig in der Registerkarten reihenfolge befinden, z. B. ein -Element (mit [**href-Attribut),**](https://developer.mozilla.org/docs/Web/HTML/Attributes) eine Schaltfläche, eine Eingabe (ohne "ausgeblendet"), die Option [**,**](https://developer.mozilla.org/docs/Web/HTML/Element/select)den Textbereich und den Bereich [**(als**](https://developer.mozilla.org/docs/Web/HTML/Element/area) Teil der Bildzuordnung). [](https://developer.mozilla.org/docs/Web/HTML/Element/a) [](https://developer.mozilla.org/docs/Web/HTML/Element/button) [](https://developer.mozilla.org/docs/Web/HTML/Element/input)

## <a name="example"></a>Beispiel


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




