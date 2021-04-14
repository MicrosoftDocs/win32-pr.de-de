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
# <a name="aria-container-role-keyboard-accessibility-error"></a><span data-ttu-id="f55b0-104">Zugriffsfehler bei der Rolle "Aria Container Role"</span><span class="sxs-lookup"><span data-stu-id="f55b0-104">ARIA Container Role Keyboard Accessibility Error</span></span>

## <a name="text"></a><span data-ttu-id="f55b0-105">Text</span><span class="sxs-lookup"><span data-stu-id="f55b0-105">Text</span></span>

<span data-ttu-id="f55b0-106">Das-Element ist ein Container mit aktiver Nachfolger Funktion und benutzerdefinierter Maus Funktionalität, aber ohne die entsprechende Tastatur Funktionalität: JavaScript-Ereignishandler für **OnKeyDown** oder **OnKeyPress**.</span><span class="sxs-lookup"><span data-stu-id="f55b0-106">Element is a container with active descendant and custom mouse functionality but without the corresponding keyboard functionality: JavaScript event handlers for **OnKeyDown** or **OnKeyPress**.</span></span>

## <a name="type"></a><span data-ttu-id="f55b0-107">type</span><span class="sxs-lookup"><span data-stu-id="f55b0-107">Type</span></span>

<span data-ttu-id="f55b0-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="f55b0-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="f55b0-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f55b0-109">Description</span></span>

<span data-ttu-id="f55b0-110">Dieser Fehler gilt für-Elemente, die über das **Aria-activenachfolger** -Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="f55b0-110">This error applies to elements that have the **aria-activedescendant** attribute.</span></span> <span data-ttu-id="f55b0-111">Diese Elemente verfügen über einen oder mehrere Maus Ereignishandler (**MouseMove**, **MouseDown** oder **MouseUp**), die entsprechenden Tastaturereignis Handler (**KeyDown**, **KeyUp** oder **KeyPress**) fehlen.</span><span class="sxs-lookup"><span data-stu-id="f55b0-111">These elements have one or more mouse event handlers (**mousemove**, **mousedown** or **mouseup**), but are missing the equivalent keyboard event handlers (**keydown**, **keyup** or **keypress**).</span></span> <span data-ttu-id="f55b0-112">Die Tastaturereignis Handler sind erforderlich, um sicherzustellen, dass der Benutzer die Funktionalität des Elements mithilfe der Tastatur aufrufen kann, und um sicherzustellen, dass das Element das Attribut " **Aria-activenachfolger** " beibehält.</span><span class="sxs-lookup"><span data-stu-id="f55b0-112">The keyboard event handlers are needed to ensure that the user can invoke the element's functionality by using the keyboard, and to ensure that the element maintains the **aria-activedescendant** attribute.</span></span>

<span data-ttu-id="f55b0-113">Implementieren Sie einen der Tastaturereignis Handler, um diesen Fehler zu beheben.</span><span class="sxs-lookup"><span data-stu-id="f55b0-113">To fix this error, implement one of the keyboard event handlers.</span></span>

## <a name="example"></a><span data-ttu-id="f55b0-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f55b0-114">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f55b0-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f55b0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f55b0-116">"Aria Container Role" (ohne aktiven Nachfolger) Tastatur Zugriffsfehler</span><span class="sxs-lookup"><span data-stu-id="f55b0-116">ARIA Container Role (without active descendant) Keyboard Accessibility Error</span></span>](aria-container--no-active-descendants--keyboard-events.md)
</dt> </dl>

 

 




