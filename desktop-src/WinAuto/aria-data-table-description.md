---
title: ARIA-Datentabellenwarnung
description: ARIA-Datentabellenwarnung
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- AriaDataTableWarningId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16fb9e8e97336199b5b133dc59ef7c5f0900f7bdeb0c7a8d8098a51707b107f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122390"
---
# <a name="aria-data-table-warning"></a>ARIA-Datentabellenwarnung

## <a name="text"></a>Text

Die Tabelle enthält Daten, verfügt jedoch weder über eine Zusammenfassung noch über ein gültiges **aria-describedby-Attribut.**

## <a name="type"></a>type

Warnung

## <a name="description"></a>Beschreibung

Diese Warnung gilt für HTML-Tabellen mit mehr als einer Zelle. Dies gilt nicht für Tabellen mit `role="presentation"` , da diese als Layouttabellen betrachtet werden.

Diese Warnung gibt an, dass die Tabelle als Datentabelle identifiziert wird, aber keine barrierefreie Beschreibung definiert ist.

> [!Note]  
> Nicht alle Datentabellen müssen über eine barrierefreie Beschreibung verfügen. Sie sollten eine barrierefreie Beschreibung definieren, wenn Benutzer weitere Informationen benötigen, um die Struktur und den Inhalt der Datentabelle zu verstehen.

 

Um diese Warnung zu ignorieren, definieren Sie mithilfe des Summary-Attributs oder des **aria-describedby-Attributs** eine beschreibung für eine Tabelle, auf die zugegriffen werden kann.

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



 

 




