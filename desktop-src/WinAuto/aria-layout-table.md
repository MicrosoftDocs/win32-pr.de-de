---
title: ARIA Presentation Table Error
description: ARIA Presentation Table Error
ms.assetid: 3D5AE911-78E5-4C40-B77B-604E65839F63
keywords:
- AriaLayoutTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896c7ec4061119535ed544cfc41598c1387d98011eb275f6a0345d9334a7dc9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122284"
---
# <a name="aria-presentation-table-error"></a>ARIA Presentation Table Error

## <a name="text"></a>Text

Für die für das Layout verwendete Tabelle dürfen keine Header-, zugänglichen Namens- oder Zusammenfassungsinformationen definiert sein (**th**, **summary**, **aria-describedby**, **aria-labeldby**, **aria-label**, **title**, **caption** attributes).

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gilt für HTML-Tabellentags, für die das [**Rollenattribut**](https://developer.mozilla.org/docs/Web/HTML/Reference) auf "presentation" festgelegt ist, oder für eine Tabelle mit einer einzelnen Zelle (1×1-Tabelle).

Dieser Fehler weist darauf hin, dass eine Tabelle nur als Layout markiert ist (verfügt `role="presentation"` über ), enthält aber auch Informationen zur Barrierefreiheit, als ob es sich um eine Datentabelle handelt, was für Sprachausgabebenutzer verwirrend sein kann.

Um diesen Fehler zu beheben, bestimmen Sie, ob es sich bei der Tabelle tatsächlich nur um eine Layouttabelle handelt, und entfernen Sie in diesem Falle das markup, auf das zugegriffen werden kann:

-   [**CAPTION-Element,**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) [**aria-label-**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)oder [**title-Attribute.**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) [](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title)
-   [**summary**](https://www.bing.com/search?q=**summary**) oder [**aria-describedby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.
-   [**THEAD-Tags.**](https://developer.mozilla.org/docs/Web/HTML/Element/thead)

## <a name="example"></a>Beispiel

![HTML für ein Tabellenelement mit Attributen wie "summary", die den Aria-Präsentationstabellenfehler auslösen, der als unpräzesantes HTML-Markup angezeigt wird ](images/aria-layout-table.png)

## <a name="remarks"></a>Hinweise

Wenn Sie feststellen, dass eine Tabelle [](https://developer.mozilla.org/docs/Web/HTML/Reference) Informationen zur Barrierefreiheit benötigt, entfernen Sie das Rollenattribut, oder legen Sie es auf einen anderen Wert als "presentation" fest.

 

 




