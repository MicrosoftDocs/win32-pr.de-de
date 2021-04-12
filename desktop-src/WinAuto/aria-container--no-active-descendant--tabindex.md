---
title: TabIndex Fehler bei der Aria-Container Rolle (ohne aktiven Nachfolger)
description: TabIndex Fehler bei der Aria-Container Rolle (ohne aktiven Nachfolger)
ms.assetid: E3CCA500-7104-4163-927C-94EA8F1E89D8
keywords:
- Ariacontainerwithoutactivedescendanttabindexerrorid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a01d3391d93b7e7f146f379bcfecd629e14bce7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206793"
---
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a>TabIndex Fehler bei der Aria-Container Rolle (ohne aktiven Nachfolger)

## <a name="text"></a>Text

Das-Element ist ein Fokus nutzbarer Container ohne aktiven Nachfolger, aber für das untergeordnete-Element ist ' **TabIndex** ' größer oder gleich 0.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gilt für Elemente, die über eine Container Rolle verfügen, nicht über ein **Aria-activenachfolger** -Attribut verfügen und nicht deaktiviert sind. Diese Elemente implementieren die Tastaturnavigation zwischen untergeordneten Elementen mithilfe des Konzepts, das als *mobilen Index* bezeichnet wird. In diesem Konzept werden die **TabIndex** -Attribute untergeordneter Elemente dynamisch verwaltet, sodass immer nur ein untergeordnetes Element in der Aktivier Reihenfolge ist.

Legen Sie zum Beheben dieses Fehlers das **TabIndex** -Attribut eines der untergeordneten-Elemente auf einen Wert gleich oder größer als 0 fest.

## <a name="example"></a>Beispiel


```HTML
<div id="listbox" role="listbox1">
  <div role="option" id="listbox1-1" tabindex="0" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
</div>

<script>

  ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = e.srcElement;
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;

    if (e.keyCode == 38 && prev) {
      // Arrow up to move focus to the previous item.
      itm.setAttribute('tabindex', '-1');
      prev.setAttribute('tabindex','0');
      prev.focus();
    } 

    else if (e.keyCode == 40 && next) {
      // Arrow down to move focus to the next item.
      itm.setAttribute('tabindex', '-1');
      next.setAttribute('tabindex','0');
      next.focus();
    }
  });

</script>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[TabIndex-Fehler bei Aria-Container](aria-container-tabindex.md)
</dt> </dl>

 

 




