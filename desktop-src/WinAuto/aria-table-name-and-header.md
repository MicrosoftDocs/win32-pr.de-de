---
title: Aria-Datentabellen Fehler
description: Aria-Datentabellen Fehler
ms.assetid: 3D0448BB-50DC-4C85-93BD-D8E626475AB0
keywords:
- Ariadatatableerrorid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286f88a0b3a0d962fd6ac45581f94bc351cb507
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104391136"
---
# <a name="aria-data-table-error"></a><span data-ttu-id="42e2b-104">Aria-Datentabellen Fehler</span><span class="sxs-lookup"><span data-stu-id="42e2b-104">ARIA Data Table Error</span></span>

## <a name="text"></a><span data-ttu-id="42e2b-105">Text</span><span class="sxs-lookup"><span data-stu-id="42e2b-105">Text</span></span>

<span data-ttu-id="42e2b-106">Die Tabelle enthält Daten, aber es ist kein Barrierefreies Markup definiert, das durch die Elemente **Aria-Label**, **Aria-labelledby**, **Title**, **Caption** oder **th** definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="42e2b-106">Table contains data but doesn't have accessible markup defined though **aria-label**, **aria-labelledby**, **title**, **caption** or **th** elements.</span></span>

## <a name="type"></a><span data-ttu-id="42e2b-107">type</span><span class="sxs-lookup"><span data-stu-id="42e2b-107">Type</span></span>

<span data-ttu-id="42e2b-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="42e2b-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="42e2b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42e2b-109">Description</span></span>

<span data-ttu-id="42e2b-110">Dieser Fehler gilt für HTML-Tabellen mit mehr als einer Zelle.</span><span class="sxs-lookup"><span data-stu-id="42e2b-110">This error applies to HTML tables with more than one cell.</span></span> <span data-ttu-id="42e2b-111">Dieser Fehler gilt nicht für Tabellen mit, `role="presentation"` da diese als Layouttabellen angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="42e2b-111">This error does not apply to tables with `role="presentation"` because these are considered to be layout tables.</span></span>

<span data-ttu-id="42e2b-112">Dieser Fehler weist darauf hin, dass eine Datentabelle keinen zugänglichen Namen oder keine Header Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="42e2b-112">This error indicates that a data table doesn’t have an accessible name or header information.</span></span>

<span data-ttu-id="42e2b-113">Um diesen Fehler zu beheben, definieren Sie einen zugänglichen Namen mithilfe des [**Beschriftungs**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) Tags oder den Attributen " [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)", " [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)" oder " [**Title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) ".</span><span class="sxs-lookup"><span data-stu-id="42e2b-113">To fix this error, define an accessible name by using the [**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) tag, or the [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), or [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attributes.</span></span> <span data-ttu-id="42e2b-114">Wenn in der Tabelle keine Header Informationen vorhanden sind, markieren Sie Header Zellen mithilfe der [**AD**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) -Tags.</span><span class="sxs-lookup"><span data-stu-id="42e2b-114">If the table is missing header information, use [**THead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) tags to mark header cells.</span></span>

## <a name="example"></a><span data-ttu-id="42e2b-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="42e2b-115">Example</span></span>


```HTML
<!-- Data tables must contain an accessibile name and header information. -->
<table>
  <caption>ARIA Examples</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      ...
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Accessible tables</td>
      <td>This example illustrates how to make data tables accessible using ARIA</td>
      ...
    </tr>
  </tbody>
</table>
```



 

 




