---
title: Fehler bei der Aria-Präsentations Tabelle
description: Fehler bei der Aria-Präsentations Tabelle
ms.assetid: 3D5AE911-78E5-4C40-B77B-604E65839F63
keywords:
- Arialayouttableerrorid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae1ef7cae971e6dc365bd3f8ebe6135561f3ff3
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734585"
---
# <a name="aria-presentation-table-error"></a><span data-ttu-id="d3910-104">Fehler bei der Aria-Präsentations Tabelle</span><span class="sxs-lookup"><span data-stu-id="d3910-104">ARIA Presentation Table Error</span></span>

## <a name="text"></a><span data-ttu-id="d3910-105">Text</span><span class="sxs-lookup"><span data-stu-id="d3910-105">Text</span></span>

<span data-ttu-id="d3910-106">Für die Tabelle, die für das Layout verwendet wird, dürfen keine Header-, Barrierefreiheits-oder Zusammenfassungs Informationen definiert sein (**th**, **Summary**, **Aria-DescribedBy**, **Aria-labelledby**, **Aria-Label**, **Title**, **Caption** -Attribute).</span><span class="sxs-lookup"><span data-stu-id="d3910-106">Table used for layout must not have header, accessible name or summary information defined (**th**, **summary**, **aria-describedby**, **aria-labelledby**, **aria-label**, **title**, **caption** attributes).</span></span>

## <a name="type"></a><span data-ttu-id="d3910-107">type</span><span class="sxs-lookup"><span data-stu-id="d3910-107">Type</span></span>

<span data-ttu-id="d3910-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="d3910-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="d3910-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3910-109">Description</span></span>

<span data-ttu-id="d3910-110">Dieser Fehler gilt für HTML-Tabellen Tags, bei denen das [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) -Attribut auf "Presentation" oder eine Tabelle mit einer einzelnen Zelle (1 × 1 Tabelle) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d3910-110">This error applies to HTML table tags that have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute set to "presentation", or with a table that has a single cell (1×1 table).</span></span>

<span data-ttu-id="d3910-111">Dieser Fehler zeigt an, dass eine Tabelle nur als Layout (hat `role="presentation"` ) gekennzeichnet ist, aber auch Barrierefreiheits Informationen enthält, als ob es sich um eine Datentabelle handelt, die für Benutzer mit Bildschirmlesern verwirrend sein kann.</span><span class="sxs-lookup"><span data-stu-id="d3910-111">This error indicates that a table is marked as layout only (has `role="presentation"`), but it also contains accessibility information as if it was a data table, which can be confusing for screen reader users.</span></span>

<span data-ttu-id="d3910-112">Um diesen Fehler zu beheben, stellen Sie fest, ob die Tabelle tatsächlich nur eine Layouttabelle ist, und entfernen Sie ggf. das barrierefreie Markup:</span><span class="sxs-lookup"><span data-stu-id="d3910-112">To address this error, determine whether the table actually is just a layout table and, if so, remove the accessible markup:</span></span>

-   <span data-ttu-id="d3910-113">[**Caption**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) -Element, [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)oder [**Title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) -Attribute.</span><span class="sxs-lookup"><span data-stu-id="d3910-113">[**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) element, [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), or [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attributes.</span></span>
-   <span data-ttu-id="d3910-114">[**Summary**](https://www.bing.com/search?q=**summary**) [**-oder Aria-DescribedBy**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) -Attribute.</span><span class="sxs-lookup"><span data-stu-id="d3910-114">[**summary**](https://www.bing.com/search?q=**summary**) or [**aria-describedby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>
-   <span data-ttu-id="d3910-115">Die [**AD**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) -Tags.</span><span class="sxs-lookup"><span data-stu-id="d3910-115">[**THEAD**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) tags.</span></span>

## <a name="example"></a><span data-ttu-id="d3910-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d3910-116">Example</span></span>

![<span data-ttu-id="d3910-117">HTML für ein Table-Element mit Attributen, wie z. b. einer Zusammenfassung, die den Fehler der Aria-Präsentations Tabelle auslöst</span><span class="sxs-lookup"><span data-stu-id="d3910-117">html for a table element, with attributes such as summary that trigger the aria presentation table error shown as struck-out html markup</span></span> ](images/aria-layout-table.png)

## <a name="remarks"></a><span data-ttu-id="d3910-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3910-118">Remarks</span></span>

<span data-ttu-id="d3910-119">Wenn Sie feststellen, dass eine Tabelle Barrierefreiheits Informationen benötigt, entfernen Sie das [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) -Attribut, oder legen Sie es auf einen anderen Wert als "Presentation" fest.</span><span class="sxs-lookup"><span data-stu-id="d3910-119">If you determine that a table does need accessibility information, remove the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute or set it to a value other than "presentation".</span></span>

 

 




