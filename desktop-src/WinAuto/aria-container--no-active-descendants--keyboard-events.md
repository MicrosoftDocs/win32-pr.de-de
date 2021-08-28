---
title: ARIA-Containerrolle (ohne aktive Nachfolger) Tastaturzugriffsfehler
description: ARIA-Containerrolle (ohne aktive Nachfolger) Tastaturzugriffsfehler
ms.assetid: 15EDD3CC-FC2A-42FC-95DD-B04D9AF3515E
keywords:
- AriaContainerWithoutActiveDescendantKeyboardAccessiblityId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30b653ac3bf2dc8254b25c52a89cdb3503b89b9f05997a3ea9fb4f4ef3a77cb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071880"
---
# <a name="aria-container-role-without-active-descendant-keyboard-accessibility-error"></a>ARIA-Containerrolle (ohne aktive Nachfolger) Tastaturzugriffsfehler

## <a name="text"></a>Text

Das Element ist ein fokussierbarer Container ohne definierten aktiven Nachfolger und ohne **OnKeyDown** / **OnKeyPress OnKeyUp-Ereignishandler**(weder im Container noch in einem /  untergeordneten Element).

## <a name="type"></a>type

Fehler

## <a name="description"></a>Beschreibung

Dieser Fehler gilt für Elemente, die über eine Containerrolle verfügen, kein **aria-activedescendant-Attribut** haben und nicht deaktiviert sind. Diese Elemente implementieren die Tastaturnavigation zwischen untergeordneten Elementen mithilfe des Konzepts, das als *Genehmigungsindex bezeichnet wird.* In diesem Konzept werden die **tabindex-Attribute** untergeordneter Elemente dynamisch verwaltet, um sicherzustellen, dass immer nur ein untergeordnetes Element in der Reihenfolge der Registerkarten angezeigt wird.

Dieser Fehler weist darauf hin, dass Tastaturbenutzer nicht auf ein Containerelement ohne das **Attribut aria-activedescendant** und das nicht deaktiviert ist. Das Problem liegt vor, da der Container nicht über die erforderlichen Tastaturereignishandler **(Keydown,** **Keyup** oder **Keypress)** verfügt und keines der untergeordneten Elemente des Containers verwendet.

Um diesen Fehler zu beheben, definieren Sie einen **Keydown-,** **Keyup-** oder **Keypress-Ereignishandler** für den Container oder eines seiner untergeordneten Elemente.

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

[ARIA-Containerrolle: Tastaturzugriffsfehler](aria-container-keyboard-events.md)
</dt> </dl>

 

 




