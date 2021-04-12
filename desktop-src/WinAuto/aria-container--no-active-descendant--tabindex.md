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
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a><span data-ttu-id="822a2-104">TabIndex Fehler bei der Aria-Container Rolle (ohne aktiven Nachfolger)</span><span class="sxs-lookup"><span data-stu-id="822a2-104">ARIA Container Role (without active descendant) Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="822a2-105">Text</span><span class="sxs-lookup"><span data-stu-id="822a2-105">Text</span></span>

<span data-ttu-id="822a2-106">Das-Element ist ein Fokus nutzbarer Container ohne aktiven Nachfolger, aber für das untergeordnete-Element ist ' **TabIndex** ' größer oder gleich 0.</span><span class="sxs-lookup"><span data-stu-id="822a2-106">Element is a focusable container without active descendant defined, but no child element has **tabindex** greater or equal to 0.</span></span>

## <a name="type"></a><span data-ttu-id="822a2-107">type</span><span class="sxs-lookup"><span data-stu-id="822a2-107">Type</span></span>

<span data-ttu-id="822a2-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="822a2-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="822a2-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="822a2-109">Description</span></span>

<span data-ttu-id="822a2-110">Dieser Fehler gilt für Elemente, die über eine Container Rolle verfügen, nicht über ein **Aria-activenachfolger** -Attribut verfügen und nicht deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="822a2-110">This error applies to elements that have a container role, do not have an **aria-activedescendant** attribute, and are not disabled.</span></span> <span data-ttu-id="822a2-111">Diese Elemente implementieren die Tastaturnavigation zwischen untergeordneten Elementen mithilfe des Konzepts, das als *mobilen Index* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="822a2-111">These elements implement keyboard navigation among child elements by using the concept known as *roving index*.</span></span> <span data-ttu-id="822a2-112">In diesem Konzept werden die **TabIndex** -Attribute untergeordneter Elemente dynamisch verwaltet, sodass immer nur ein untergeordnetes Element in der Aktivier Reihenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="822a2-112">In this concept, the **tabindex** attributes of child elements are maintained dynamically, ensuring that at all times only one child element is in tab order.</span></span>

<span data-ttu-id="822a2-113">Legen Sie zum Beheben dieses Fehlers das **TabIndex** -Attribut eines der untergeordneten-Elemente auf einen Wert gleich oder größer als 0 fest.</span><span class="sxs-lookup"><span data-stu-id="822a2-113">To fix this error, set the **tabindex** attribute of one of the child elements to a value equal to or greater than 0.</span></span>

## <a name="example"></a><span data-ttu-id="822a2-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="822a2-114">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="822a2-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="822a2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="822a2-116">TabIndex-Fehler bei Aria-Container</span><span class="sxs-lookup"><span data-stu-id="822a2-116">ARIA Container Tabindex Error</span></span>](aria-container-tabindex.md)
</dt> </dl>

 

 




