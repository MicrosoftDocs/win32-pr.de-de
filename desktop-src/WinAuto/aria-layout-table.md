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
# <a name="aria-presentation-table-error"></a>Fehler bei der Aria-Präsentations Tabelle

## <a name="text"></a>Text

Für die Tabelle, die für das Layout verwendet wird, dürfen keine Header-, Barrierefreiheits-oder Zusammenfassungs Informationen definiert sein (**th**, **Summary**, **Aria-DescribedBy**, **Aria-labelledby**, **Aria-Label**, **Title**, **Caption** -Attribute).

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gilt für HTML-Tabellen Tags, bei denen das [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) -Attribut auf "Presentation" oder eine Tabelle mit einer einzelnen Zelle (1 × 1 Tabelle) festgelegt ist.

Dieser Fehler zeigt an, dass eine Tabelle nur als Layout (hat `role="presentation"` ) gekennzeichnet ist, aber auch Barrierefreiheits Informationen enthält, als ob es sich um eine Datentabelle handelt, die für Benutzer mit Bildschirmlesern verwirrend sein kann.

Um diesen Fehler zu beheben, stellen Sie fest, ob die Tabelle tatsächlich nur eine Layouttabelle ist, und entfernen Sie ggf. das barrierefreie Markup:

-   [**Caption**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) -Element, [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)oder [**Title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) -Attribute.
-   [**Summary**](https://www.bing.com/search?q=**summary**) [**-oder Aria-DescribedBy**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) -Attribute.
-   Die [**AD**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) -Tags.

## <a name="example"></a>Beispiel

![HTML für ein Table-Element mit Attributen, wie z. b. einer Zusammenfassung, die den Fehler der Aria-Präsentations Tabelle auslöst ](images/aria-layout-table.png)

## <a name="remarks"></a>Bemerkungen

Wenn Sie feststellen, dass eine Tabelle Barrierefreiheits Informationen benötigt, entfernen Sie das [**Role**](https://developer.mozilla.org/docs/Web/HTML/Reference) -Attribut, oder legen Sie es auf einen anderen Wert als "Presentation" fest.

 

 




