---
title: Informationen zum Query-Objekt
description: Informationen zum Query-Objekt
ms.assetid: 41488036-bdcf-4fe6-8f7e-f0897157d3d9
keywords:
- Windows Media Player, Abfrageobjekt
- Windows Media Player-Objektmodell, Abfrageobjekt
- Objektmodell, Abfrageobjekt
- Windows Media Player ActiveX-Steuerelement, Abfrageobjekt
- ActiveX-Steuerelement, Abfrageobjekt
- Windows Media Player Mobile ActiveX-Steuerelement, Abfrageobjekt
- Windows Media Player Mobile, Abfrageobjekt
- Query-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a26f60c38e053b91c7e56f5cbd7ccaf2ba0fe2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710793"
---
# <a name="about-the-query-object"></a>Informationen zum Query-Objekt

Das **Query** -Objekt stellt eine Verbund Abfrage dar. Sie erstellen ein neues, leeres **Abfrage** Objekt durch Aufrufen von *mediacollection*. " **kreatequery**". Nachdem Sie ein **Abfrage** Objekt erstellt haben, können Sie **addcondition** aufzurufen, um der Verbund Abfrage eine Bedingung hinzuzufügen. Jeder nachfolgende Rückruf von **addcondition** fügt eine neue Bedingung mithilfe der-und der-Logik an die vorhandene Abfrage an.

Nehmen Sie beispielsweise an, Sie möchten eine Abfrage erstellen, die alle digitalen Medien repräsentiert, bei denen **WM/Genre** den Wert "Jazz" hat und der **Autor** "Jim" enthält. Sie können eine Verbund Abfrage erstellen, die diese Bedingungen mithilfe des folgenden JScript-Codes darstellt:


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");
```



Zum Hinzufügen einer Bedingung zu einer Verbund Abfrage mit der-oder-Logik müssen Sie **Query. beginnextgroup** aufrufen. Diese Methode signalisiert, dass die vorherige Bedingungs Gruppe abgeschlossen ist und dass der nächste **addcondition** -Rückruf den Anfang einer neuen Bedingungs Gruppe darstellt.

Beispielsweise können Sie den folgenden Beispielcode verwenden, um eine Abfrage zu erstellen, die alle digitalen Medien repräsentiert, bei denen **WM/Genre** den Wert "Jazz" hat, und der **Autor** "Jim" oder der **Autor** "Dave" enthält:


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");

// Start the next condition group. This group will be
// combined with the previous group using a logical OR operation.
Query.beginNextGroup();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Dave");
```



Um die Verbund Abfrage auszuführen, nennen Sie **mediacollection. getplaylistbyquery**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Mediacollection. getplaylistbyquery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**Player-Objektmodell für Skriptsprachen**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Query-Objekt**](query-object.md)
</dt> </dl>

 

 




