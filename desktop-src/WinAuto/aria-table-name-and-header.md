---
title: ARIA-Datentabellenfehler
description: ARIA-Datentabellenfehler
ms.assetid: 3D0448BB-50DC-4C85-93BD-D8E626475AB0
keywords:
- AriaDataTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 025443ab452ff0103c8808c27dce834a03cb8c96e0d9106a7abb4409b64a0697
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133973"
---
# <a name="aria-data-table-error"></a>ARIA-Datentabellenfehler

## <a name="text"></a>Text

Die Tabelle enthält Daten, verfügt aber nicht über zugängliches Markup, das durch **aria-label,** **aria-captionby**, **title,** **caption** oder **th-Elemente definiert** wurde.

## <a name="type"></a>type

Fehler

## <a name="description"></a>Beschreibung

Dieser Fehler gilt für HTML-Tabellen mit mehr als einer Zelle. Dieser Fehler gilt nicht für Tabellen mit `role="presentation"` , da diese als Layouttabellen betrachtet werden.

Dieser Fehler weist darauf hin, dass eine Datentabelle keinen zugänglichen Namen oder Headerinformationen hat.

Um diesen Fehler zu beheben, definieren Sie einen barrierefreien Namen, indem Sie das [**CAPTION-Tag**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) oder die [**Attribute aria-captionby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)oder [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) verwenden. Wenn in der Tabelle Headerinformationen fehlen, verwenden Sie [**THead-Tags,**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) um Headerzellen zu markieren.

## <a name="example"></a>Beispiel


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



 

 




