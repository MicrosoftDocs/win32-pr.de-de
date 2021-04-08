---
title: Warnung zu Aria-Datentabelle
description: Warnung zu Aria-Datentabelle
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- Ariadatatablewarningid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcd77983092983649d8bcd41357afb4756120e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037484"
---
# <a name="aria-data-table-warning"></a>Warnung zu Aria-Datentabelle

## <a name="text"></a>Text

Die Tabelle enthält Daten, hat aber weder eine Zusammenfassung noch ein gültiges **Aria-DescribedBy** -Attribut.

## <a name="type"></a>type

Warnung

## <a name="description"></a>BESCHREIBUNG

Diese Warnung gilt für HTML-Tabellen mit mehr als einer Zelle. Sie gilt nicht für Tabellen mit, `role="presentation"` da diese als Layouttabellen angesehen werden.

Diese Warnung gibt an, dass die Tabelle als Datentabelle identifiziert ist, aber keine barrierefreie Beschreibung definiert ist.

> [!Note]  
> Nicht für alle Datentabellen ist eine barrierefreie Beschreibung erforderlich. Sie sollten eine barrierefreie Beschreibung definieren, wenn Benutzer weitere Informationen benötigen, um die Struktur und den Inhalt der Datentabelle zu verstehen.

 

Um diese Warnung zu beheben, definieren Sie eine Tabelle, auf die zugegriffen werden kann, indem Sie das Summary-Attribut oder das **Aria-DescribedBy** -Attribut verwenden

## <a name="example"></a>Beispiel


```HTML
<!-- Define a table description by using the summary attribute. -->
<table summary="The first column contains the list of examples. In the second column ...">
...
</table>

<!-- Define a table description using the aria-describedby attribute. -->
<p id="tableHeader" >The first column contains the list of examples. In the second column ...</p>
<table aria-describedby="tableHeader" >
...
</table>
```



 

 




