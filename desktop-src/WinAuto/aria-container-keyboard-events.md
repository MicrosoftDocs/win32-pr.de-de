---
title: Zugriffsfehler bei der Rolle "Aria Container Role"
description: Zugriffsfehler bei der Rolle "Aria Container Role"
ms.assetid: 364F26D7-7B65-418B-9DA5-F3B7B59284F7
keywords:
- Ariacontainerkeyboardaccessibilityerrorid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085591e4f4834e8088b5ca199918d621f518e678
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310512"
---
# <a name="aria-container-role-keyboard-accessibility-error"></a>Zugriffsfehler bei der Rolle "Aria Container Role"

## <a name="text"></a>Text

Das-Element ist ein Container mit aktiver Nachfolger Funktion und benutzerdefinierter Maus Funktionalität, aber ohne die entsprechende Tastatur Funktionalität: JavaScript-Ereignishandler für **OnKeyDown** oder **OnKeyPress**.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gilt für-Elemente, die über das **Aria-activenachfolger** -Attribut verfügen. Diese Elemente verfügen über einen oder mehrere Maus Ereignishandler (**MouseMove**, **MouseDown** oder **MouseUp**), die entsprechenden Tastaturereignis Handler (**KeyDown**, **KeyUp** oder **KeyPress**) fehlen. Die Tastaturereignis Handler sind erforderlich, um sicherzustellen, dass der Benutzer die Funktionalität des Elements mithilfe der Tastatur aufrufen kann, und um sicherzustellen, dass das Element das Attribut " **Aria-activenachfolger** " beibehält.

Implementieren Sie einen der Tastaturereignis Handler, um diesen Fehler zu beheben.

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

["Aria Container Role" (ohne aktiven Nachfolger) Tastatur Zugriffsfehler](aria-container--no-active-descendants--keyboard-events.md)
</dt> </dl>

 

 




