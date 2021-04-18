---
title: Nicht kompatible Aria-Bereichs Steuerungs Attribute.
description: Nicht kompatible Aria-Bereichs Steuerungs Attribute.
ms.assetid: 265AE578-D841-4931-9F4A-97BB86ECEC88
keywords:
- Ariarangecontrolattributesincompatibleid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef55ee57c4966896e666dd5a7ac1d20eb5257c6
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104517189"
---
# <a name="aria-range-control-attributes-incompatible"></a><span data-ttu-id="796c8-104">Nicht kompatible Aria-Bereichs Steuerungs Attribute.</span><span class="sxs-lookup"><span data-stu-id="796c8-104">ARIA Range Control Attributes Incompatible</span></span>

## <a name="text"></a><span data-ttu-id="796c8-105">Text</span><span class="sxs-lookup"><span data-stu-id="796c8-105">Text</span></span>

<span data-ttu-id="796c8-106">Das Element hat die Rolle " **ProgressBar** " oder " **Slider** ", aber der Status " **Aria-valuenow** " liegt außerhalb des Aria- **valuemin** **-** Bereichs</span><span class="sxs-lookup"><span data-stu-id="796c8-106">Element has **progressbar** or **slider** role but exposed **aria-valuenow** value is outside of **aria-valuemin** **aria-valuemax** range.</span></span>

## <a name="type"></a><span data-ttu-id="796c8-107">type</span><span class="sxs-lookup"><span data-stu-id="796c8-107">Type</span></span>

<span data-ttu-id="796c8-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="796c8-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="796c8-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="796c8-109">Description</span></span>

<span data-ttu-id="796c8-110">Dieser Fehler gilt für Elemente, die eine (implizite oder explizite) [**Rolle**](https://developer.mozilla.org/docs/Web/HTML/Reference) aufweisen, die der **ProgressBar**, dem **Schieberegler** oder dem **SpinButton** entspricht.</span><span class="sxs-lookup"><span data-stu-id="796c8-110">This error applies to elements that have a [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicit or explicit) equal to **progressbar**, **slider**, or **spinbutton**.</span></span>

<span data-ttu-id="796c8-111">Dieser Fehler zeigt an, dass der verfügbar [**gemachte Aria-valuenow-**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) Wert nicht im Bereich liegt, der durch die Attribute " [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) " und " [**Aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) " definiert wird.</span><span class="sxs-lookup"><span data-stu-id="796c8-111">This error indicates that the exposed [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) value is not in the range defined by the [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) and [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>

<span data-ttu-id="796c8-112">Um diesen Fehler zu beheben, überprüfen Sie Ihre Implementierung, um sicherzustellen, dass die Attribute " [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) " und " [**Aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) " ordnungsgemäß festgelegt sind und der Wert des [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) -Attributs ordnungsgemäß verwaltet wird</span><span class="sxs-lookup"><span data-stu-id="796c8-112">To fix this error, check your implementation to ensure that the [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) and [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes are correctly set, and that the [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute value is properly maintained.</span></span>

## <a name="related-topics"></a><span data-ttu-id="796c8-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="796c8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="796c8-114">Aria-Bereichs Steuerungs Attribute fehlen</span><span class="sxs-lookup"><span data-stu-id="796c8-114">ARIA Range Control Attributes Missing</span></span>](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 




