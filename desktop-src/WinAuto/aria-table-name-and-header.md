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
# <a name="aria-data-table-error"></a>Aria-Datentabellen Fehler

## <a name="text"></a>Text

Die Tabelle enthält Daten, aber es ist kein Barrierefreies Markup definiert, das durch die Elemente **Aria-Label**, **Aria-labelledby**, **Title**, **Caption** oder **th** definiert wurde.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gilt für HTML-Tabellen mit mehr als einer Zelle. Dieser Fehler gilt nicht für Tabellen mit, `role="presentation"` da diese als Layouttabellen angesehen werden.

Dieser Fehler weist darauf hin, dass eine Datentabelle keinen zugänglichen Namen oder keine Header Informationen enthält.

Um diesen Fehler zu beheben, definieren Sie einen zugänglichen Namen mithilfe des [**Beschriftungs**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) Tags oder den Attributen " [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)", " [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)" oder " [**Title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) ". Wenn in der Tabelle keine Header Informationen vorhanden sind, markieren Sie Header Zellen mithilfe der [**AD**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) -Tags.

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



 

 




