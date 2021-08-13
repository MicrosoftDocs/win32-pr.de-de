---
title: Informationen zum Abfrageobjekt
description: Informationen zum Abfrageobjekt
ms.assetid: 41488036-bdcf-4fe6-8f7e-f0897157d3d9
keywords:
- Windows Media Player,Query-Objekt
- Windows Media Player-Objektmodell, Abfrageobjekt
- Objektmodell, Abfrageobjekt
- Windows Media Player ActiveX,Abfrageobjekt
- ActiveX,Abfrageobjekt
- Windows Media Player Mobiles ActiveX-Steuerelement, Abfrageobjekt
- Windows Media Player Mobil, Abfrageobjekt
- Query-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d649263f981d02e106466c6e0fcada99c316054d4bf6e0acc0faca641c75dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470400"
---
# <a name="about-the-query-object"></a>Informationen zum Abfrageobjekt

Das **Query-Objekt** stellt eine zusammengesetzte Abfrage dar. Sie erstellen ein neues leeres **Abfrageobjekt,** indem Sie *mediaCollection aufrufen.* **createQuery**. Nachdem Sie ein **Query-Objekt erstellt** haben, können Sie **addCondition** aufrufen, um der Verbundabfrage eine Bedingung hinzuzufügen. Bei jedem nachfolgenden Aufruf **von addCondition** wird mithilfe der AND-Logik eine neue Bedingung an die vorhandene Abfrage angefügt.

Angenommen, Sie möchten eine Abfrage erstellen, die alle digitalen Medien darstellt, bei denen **WM/Genre** gleich "Jazz" und **Autor** "Jim" enthält. Sie können eine zusammengesetzte Abfrage erstellen, um diese Bedingungen mit dem folgenden Code JScript darstellen:


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");
```



Um einer zusammengesetzten Abfrage mithilfe der OR-Logik eine Bedingung hinzuzufügen, müssen Sie **Query.beginNextGroup aufrufen.** Diese Methode signalisiert, dass die vorherige Bedingungsgruppe abgeschlossen ist und dass der nächste Aufruf von **addCondition** den Anfang einer neuen Bedingungsgruppe darstellt.

Um beispielsweise eine Abfrage zu erstellen, die alle digitalen Medien darstellt, bei denen **WM/Genre** gleich "Jazz" ist und **Author** "Jim" oder **Author** "Dave" enthält, können Sie den folgenden Beispielcode verwenden:


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



Rufen Sie **mediaCollection.getPlaylistByQuery** auf, um Ihre Verbundabfrage auszuführen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**MediaCollection.getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**Player-Objektmodell für Skriptsprachen**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Abfrageobjekt**](query-object.md)
</dt> </dl>

 

 




