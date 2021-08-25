---
title: 'ARIA-Containerrolle: Tastaturzugriffsfehler'
description: 'ARIA-Containerrolle: Tastaturzugriffsfehler'
ms.assetid: 364F26D7-7B65-418B-9DA5-F3B7B59284F7
keywords:
- AriaContainerKeyboardAccessibilityErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591098ba6e38836f1f39d13e72495bc1d7a3d5f9fe088873661e3dd3a7e65d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122400"
---
# <a name="aria-container-role-keyboard-accessibility-error"></a>ARIA-Containerrolle: Tastaturzugriffsfehler

## <a name="text"></a>Text

Das -Element ist ein Container mit aktiver Nachfolger- und benutzerdefinierter Mausfunktion, aber ohne die entsprechende Tastaturfunktionalität: JavaScript-Ereignishandler für **OnKeyDown** oder **OnKeyPress**.

## <a name="type"></a>type

Fehler

## <a name="description"></a>Beschreibung

Dieser Fehler gilt für Elemente mit dem **Attribut aria-activedescendant.** Diese Elemente verfügen über einen oder mehrere Mausereignishandler (**mousemove**, **mousedown** oder **mouseup**), aber es fehlen die entsprechenden Tastaturereignishandler (**Keydown,** **Keyup** oder **Keypress**). Die Tastaturereignishandler sind erforderlich, um sicherzustellen, dass der Benutzer die Funktionalität des Elements mithilfe der Tastatur aufrufen kann, und um sicherzustellen, dass das Element das **aria-activedescendant-Attribut** verwaltet.

Implementieren Sie einen der Tastaturereignishandler, um diesen Fehler zu beheben.

## <a name="example"></a>Beispiel


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1"> 
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
</div>

<script>

   ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = document.getElementById(this.getAttribute('aria-activedescendant'));
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;
    
    if ( e.keyCode  38 && prev ) {
      // Arrow up to move active descendant to the previous item
      itm.removeAttribute('class’);
      prev.setAttribute("class", "selected");
      this.setAttribute ('aria-activedescendant', prev.id)
    } 

    else if ( e.keyCode == 40 && next) {
      // Arrow down to move focus to the next item
      itm.removeAttribute('class’);
      next.setAttribute("class", "selected");
      this.setAttribute ('aria-activedescendant', next.id)
    }
  });      

</script>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ARIA-Containerrolle (ohne aktive Nachfolger) Tastaturzugriffsfehler](aria-container--no-active-descendants--keyboard-events.md)
</dt> </dl>

 

 




