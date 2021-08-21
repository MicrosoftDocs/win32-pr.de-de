---
title: ARIA Container Role (without active descendant) Tabindex Error
description: ARIA Container Role (without active descendant) Tabindex Error
ms.assetid: E3CCA500-7104-4163-927C-94EA8F1E89D8
keywords:
- AriaContainerWithoutActiveDescendantTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6eb2198b5ad28cf8a2dd1c625342fef399eefbe3f93ed5e09f4796e06d16338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994340"
---
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a>ARIA Container Role (without active descendant) Tabindex Error

## <a name="text"></a>Text

Das Element ist ein fokussierbarer Container, ohne dass ein aktiver Nachfolger definiert ist, aber kein untergeordnetes Element hat **tabindex** größer oder gleich 0.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gilt für Elemente, die über eine Containerrolle verfügen, nicht über ein **aria-activedescendant-Attribut** verfügen und nicht deaktiviert sind. Diese Elemente implementieren die Tastaturnavigation zwischen untergeordneten Elementen mithilfe des Konzepts , das als *"roving index"* bezeichnet wird. In diesem Konzept werden die **tabindex-Attribute** von untergeordneten Elementen dynamisch verwaltet, um sicherzustellen, dass immer nur ein untergeordnetes Element in der Tabstoppreihenfolge ist.

Um diesen Fehler zu beheben, legen Sie das **tabindex-Attribut** eines der untergeordneten Elemente auf einen Wert größer oder gleich 0 fest.

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

[ARIA Container Tabindex Error](aria-container-tabindex.md)
</dt> </dl>

 

 




