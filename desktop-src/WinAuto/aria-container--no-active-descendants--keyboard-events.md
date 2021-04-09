---
title: "\"Aria Container Role\" (ohne aktiven Nachfolger) Tastatur Zugriffsfehler"
description: "\"Aria Container Role\" (ohne aktiven Nachfolger) Tastatur Zugriffsfehler"
ms.assetid: 15EDD3CC-FC2A-42FC-95DD-B04D9AF3515E
keywords:
- Ariacontainerwithoutactivedescendantkeyboardaccessiblityid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9e30e0194f156426e2b61aa774ac1f3e0f5b91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856119"
---
# <a name="aria-container-role-without-active-descendant-keyboard-accessibility-error"></a>"Aria Container Role" (ohne aktiven Nachfolger) Tastatur Zugriffsfehler

## <a name="text"></a>Text

Das-Element ist ein Fokus nutzbarer Container ohne aktiven Nachfolger und ohne **OnKeyDown**- / **OnKeyPress**- /  Ereignishandler (weder im Container noch in einem der untergeordneten Elemente).

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gilt für Elemente, die über eine Container Rolle verfügen, nicht über ein **Aria-activenachfolger** -Attribut verfügen und nicht deaktiviert sind. Diese Elemente implementieren die Tastaturnavigation zwischen untergeordneten Elementen mithilfe des Konzepts, das als *mobilen Index* bezeichnet wird. In diesem Konzept werden die **TabIndex** -Attribute untergeordneter Elemente dynamisch verwaltet, sodass immer nur ein untergeordnetes Element in der Aktivier Reihenfolge ist.

Dieser Fehler gibt an, dass Tastatur Benutzer nicht auf ein Containerelement zugreifen können, das nicht über das Attribut " **Aria-activenachfolger** " verfügt und nicht deaktiviert ist. Das Problem ist aufgetreten, weil der Container nicht über die benötigten Tastaturereignis Handler (**KeyDown**, **KeyUp** oder **KeyPress**) verfügt und keines der untergeordneten Elemente des Containers vorliegt.

Um diesen Fehler zu beheben, definieren Sie einen **KeyDown**-, **KeyUp**-oder **KeyPress** -Ereignishandler für den Container oder eines seiner untergeordneten Elemente.

## <a name="example"></a>Beispiel


```HTML
<div role="listbox" id="listbox1" >
  <div role="option" id="listbox1-1" tabindex="0" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>

<script>

  ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = e.srcElement;
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;

    if (e.keyCode == 38 && prev) {
      // On arrow up move focus to the previous item.
      itm.setAttribute('tabindex', '-1');
      prev.setAttribute('tabindex','0');
      prev.focus();
    }

    else if (e.keyCode == 40 && next) {
      // On arrow down move focus to the next item.
      itm.setAttribute('tabindex', '-1');
      next.setAttribute('tabindex','0');
      next.focus();
    }
  });

</script>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugriffsfehler bei der Rolle "Aria Container Role"](aria-container-keyboard-events.md)
</dt> </dl>

 

 




