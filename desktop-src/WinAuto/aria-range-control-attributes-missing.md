---
title: Aria-Bereichs Steuerungs Attribute fehlen
description: Aria-Bereichs Steuerungs Attribute fehlen
ms.assetid: B79F6277-5339-406A-B5FC-A3657BFC5034
keywords:
- Ariarangecontrolattributesabwestid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8cd32a7a4807f06c26bd013ee3fd294d33cc57
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104039775"
---
# <a name="aria-range-control-attributes-missing"></a><span data-ttu-id="64d56-104">Aria-Bereichs Steuerungs Attribute fehlen</span><span class="sxs-lookup"><span data-stu-id="64d56-104">ARIA Range Control Attributes Missing</span></span>

## <a name="text"></a><span data-ttu-id="64d56-105">Text</span><span class="sxs-lookup"><span data-stu-id="64d56-105">Text</span></span>

<span data-ttu-id="64d56-106">Das Element hat die Rolle " **ProgressBar** " oder " **Slider** ", aber keine entsprechenden Attribute " **Aria-valuemin** ", " **Aria-valuemax** " und " **Aria-valuenow** " verfügbar.</span><span class="sxs-lookup"><span data-stu-id="64d56-106">Element has **progressbar** or **slider** role but is not exposing corresponding **aria-valuemin** , **aria-valuemax** , and **aria-valuenow** attributes.</span></span>

## <a name="type"></a><span data-ttu-id="64d56-107">type</span><span class="sxs-lookup"><span data-stu-id="64d56-107">Type</span></span>

<span data-ttu-id="64d56-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="64d56-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="64d56-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64d56-109">Description</span></span>

<span data-ttu-id="64d56-110">Dieser Fehler gilt für Elemente, die eine (implizite oder explizite) [**Rolle**](https://developer.mozilla.org/docs/Web/HTML/Reference) aufweisen, die der **ProgressBar**, dem **Schieberegler** oder dem **SpinButton** entspricht.</span><span class="sxs-lookup"><span data-stu-id="64d56-110">This error applies to elements that have a [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicit or explicit) that is equal to **progressbar**, **slider**, or **spinbutton**.</span></span>

<span data-ttu-id="64d56-111">Gemäß der von Web Accessibility Initiative zugänglichen Spezifikation für Rich Internet Applications (WAI-ARIA) müssen Elemente, die über die Rollen " **ProgressBar**", " **Slider**" oder " **SpinButton** " verfügen, die Attribute " [**Aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)", " [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)" und " [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) " verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="64d56-111">According to the Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) specification, elements that have the **progressbar**, **slider**, or **spinbutton** role must expose the [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), and [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>

<span data-ttu-id="64d56-112">Um diesen Fehler zu beheben, legen Sie die Attribute [**Aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)und [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) fest, und verwalten Sie den Wert von **Aria-valuenow** dynamisch, um sicherzustellen, dass der aktuelle Wert verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="64d56-112">To fix this error, set the [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), and [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes, and dynamically maintain the **aria-valuenow** value to ensure that the current value is exposed.</span></span> <span data-ttu-id="64d56-113">Sie sollten auch das [**Aria-ValueText**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) -Attribut festlegen, um dem verfügbar gemachten **Aria-valuenow-** Wert weitere Bedeutungen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="64d56-113">You should also set the [**aria-valuetext**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute to add more meaning to the exposed **aria-valuenow** value.</span></span>

## <a name="example"></a><span data-ttu-id="64d56-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="64d56-114">Example</span></span>


```HTML
<div role="slider" id="sl" aria-valuemin="1" aria-valuemax="5" aria-valuenow="3" aria-valuetext="good"…>
</div>

<script>
  // This function should be triggered when the slider value changes.
  function manageValue()
  {
    ...
    sl.setAttribute("aria-valuenow", currentValue);
    sl.setAttribute("aria-valuetext", currentValueText);
    ...
  }
</script>
```



## <a name="related-topics"></a><span data-ttu-id="64d56-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64d56-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64d56-116">Nicht kompatible Aria-Bereichs Steuerungs Attribute.</span><span class="sxs-lookup"><span data-stu-id="64d56-116">ARIA Range Control Attributes Incompatible</span></span>](aria-range-control-attribute-out-of-range.md)
</dt> </dl>

 

 




