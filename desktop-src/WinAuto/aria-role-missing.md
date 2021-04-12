---
title: Aria-Rollen Fehler für Elemente mit Ereignis Handlern
description: Aria-Rollen Fehler für Elemente mit Ereignis Handlern
ms.assetid: 20BB874A-874B-4266-9C7B-49C07D4146DA
keywords:
- Ariacontainerroleerrormessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eede416392e8b4cb644938242a9975238118ff07
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104391156"
---
# <a name="aria-role-error-for-elements-with-event-handlers"></a><span data-ttu-id="ca3e9-104">Aria-Rollen Fehler für Elemente mit Ereignis Handlern</span><span class="sxs-lookup"><span data-stu-id="ca3e9-104">ARIA Role Error for elements with event handlers</span></span>

## <a name="text"></a><span data-ttu-id="ca3e9-105">Text</span><span class="sxs-lookup"><span data-stu-id="ca3e9-105">Text</span></span>

<span data-ttu-id="ca3e9-106">Das Element hat einen Ereignishandler, aber eine gültige Rolle "WAI-ARIA" ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="ca3e9-106">Element has an event handler but valid WAI-ARIA role is not defined.</span></span>

## <a name="type"></a><span data-ttu-id="ca3e9-107">type</span><span class="sxs-lookup"><span data-stu-id="ca3e9-107">Type</span></span>

<span data-ttu-id="ca3e9-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="ca3e9-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="ca3e9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca3e9-109">Description</span></span>

<span data-ttu-id="ca3e9-110">Dieser Fehler gilt für Elemente, die nicht über eine implizite webanbarrierefreiheits Initiative verfügen, die über die Rolle "Ria-Aria" verfügt.</span><span class="sxs-lookup"><span data-stu-id="ca3e9-110">This error applies to elements that do not have an implicit Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role.</span></span>

<span data-ttu-id="ca3e9-111">Dieser Fehler zeigt an, dass ein Element über einen Maus-oder Tastaturereignis Handler verfügt (**Klicken Sie auf**, **MouseDown**, **MouseUp**, **MouseMove**, **mouseout**, **MouseOver**, **KeyUp**, **KeyDown** oder **KeyPress**), aber nicht das [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) -Attribut festgelegt ist und kein HTML-Tag ist, das über eine implizite WAI-ARIA-Rolle verfügt (z. b. **a**, **Button**, **IMG**, **Input**, **Select** usw.).</span><span class="sxs-lookup"><span data-stu-id="ca3e9-111">This error indicates that an element has a mouse or keyboard event handler (**click**, **mousedown**, **mouseup**, **mousemove**, **mouseout**, **mouseover**, **keyup**, **keydown**, or **keypress**), but doesn’t have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute set, and is not one of the HTML tags that has an implicit WAI-ARIA role (for example, **a**, **button**, **img**, **input**, **select** and so on).</span></span>

<span data-ttu-id="ca3e9-112">Das Festlegen des [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) -Attributs für interaktive Elemente, die keine implizite Rolle haben (z. b. ein **div** -Tag), ist erforderlich, um die Verhaltensmuster des Elements für Sprachausgabe und andere Hilfstechnologien verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="ca3e9-112">Setting the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute for interactive elements that have no implicit role (such as a **div** tag) is necessary to expose the element's behavior patterns to screen readers and other assistive technologies.</span></span>

<span data-ttu-id="ca3e9-113">Um diesen Fehler zu beheben, legen Sie das [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) -Attribut auf eine gültige Rolle "WAI-ARIA" fest, die am besten zu den Verhaltensmustern und den erforderlichen Attributen dieses Elements passt.</span><span class="sxs-lookup"><span data-stu-id="ca3e9-113">To fix this error, set the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute to a valid WAI-ARIA role that best fits this element's behavior patterns and required attributes.</span></span> <span data-ttu-id="ca3e9-114">Wenn ein **div** -Tag z. b. als Schaltfläche fungiert, legen Sie das role-Attribut auf "Button" fest.</span><span class="sxs-lookup"><span data-stu-id="ca3e9-114">For example, if a **div** tag functions as a button, set the role attribute to "button".</span></span>

## <a name="example"></a><span data-ttu-id="ca3e9-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ca3e9-115">Example</span></span>


```HTML
<!-- Setting role attribute allows screen readers to know it can be clicked -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




