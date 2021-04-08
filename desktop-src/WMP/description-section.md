---
title: Abschnitt "Beschreibung"
description: Abschnitt "Beschreibung"
ms.assetid: 280a9a4d-935f-440d-a606-94aeba0007db
keywords:
- Windows Media Player Mobile Skins, Beschreibungs Abschnitt
- Skins, Beschreibungs Abschnitt
- Erstellen von Skins, Beschreibungs Abschnitt
- Schreiben von Code für Skins, Beschreibungs Abschnitt
- Beschreibungs Abschnitt in Skins
- Skin-Definitions Dateien, Beschreibungs Abschnitt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9518b6b1de128457dc3e6b3738ddab9be2a873
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856796"
---
# <a name="description-section"></a>Abschnitt "Beschreibung"

Als nächstes müssen Sie einen Abschnitt bereitstellen, der die Größe und Ausrichtung der Skin beim Erstellen eines Skin für Windows Media Player 9-Reihe für Windows Mobile 2003 und spätere Versionen beschreibt:


```C++
[ Description ]
//              <X,Y>       <DPI>
//              ------      -----
    Dimensions  240, 320    96

//    <Orientation>
//    -------------
    Orientation Portrait

```



Der Beschreibungs Abschnitt muss mit der Wort Beschreibung in Klammern beginnen und dann eine Zeile einschließen, in der die Abmessungen und die Bildschirmauflösung für die Skin angegeben werden.

Zeilen, die mit zwei Schrägstrichen beginnen, werden nicht verarbeitet und können für Kommentare verwendet werden, oder, wie im vorherigen Code gezeigt, eine Vorlage, die Ihnen hilft, sich zu merken, was in einem Abschnitt passiert. Sie können auch Vorlagen verwenden, um alles in Spalten auszurichten.

Weitere Informationen zum Abschnitt Beschreibung finden Sie unter [Beschreibung](description.md) in der Skin-Referenz.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben des Codes**](writing-the-code.md)
</dt> </dl>

 

 




