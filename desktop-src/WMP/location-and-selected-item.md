---
title: Speicherort und ausgewähltes Element
description: Speicherort und ausgewähltes Element
ms.assetid: 9556e01f-1f75-4089-9e62-b41a9aa53e93
keywords:
- Windows Media Player Onlineshops, Standorte
- Onlineshops, Standorte
- Geben Sie 1 Onlineshops, Standorte ein.
- Windows Media Player Onlineshops, Bibliotheksspeicherorte
- Onlineshops, Bibliotheksspeicherorte
- Geben Sie 1 Onlineshops, Bibliotheksspeicherorte ein.
- Windows Media Player Onlineshops, ausgewählte Elemente
- Onlineshops, ausgewählte Elemente
- Geben Sie 1 Onlineshops ein, ausgewählte Elemente.
- Windows Media Player Bibliothek, Speicherorte
- Windows Media Player Bibliothek, ausgewählte Elemente
- Bibliothek, Speicherorte
- Bibliothek, ausgewählte Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6532c6417b6e95632aa21fa8d4a3a9ed943ad844eb1324f34eb80191043eeb80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003379"
---
# <a name="location-and-selected-item"></a>Speicherort und ausgewähltes Element

Windows Media Player verwendet die folgenden fünf Elemente, um die aktuelle Ansicht der Inhalte des Onlineshops zu charakterisieren:

-   task
-   Typ des Bibliotheksspeicherorts
-   Id des Bibliotheksspeicherorts
-   Ausgewählter Elementtyp
-   Ausgewählte Element-ID

In der Regel können Sie sich die Ansicht in Windows Media Player als Container mit Elementen vorstellen. Der Container hat einen Typ, und ein Element hat einen Typ. Alle Elemente in einem Container haben den gleichen Typ. Speicherorttypen und Elementtypen werden beide durch die [Speicherortkonstanten](library-location-constants.md)der Bibliothek angegeben. Wenn beispielsweise in der aktuellen Ansicht ein einzelnes Album angezeigt wird, lautet der Bibliotheksspeicherorttyp CPKategorieID, und da ein Album Spuren enthält, ist der ausgewählte Elementtyp CPTrackID.

Die folgende Tabelle zeigt die Speicherort- und Elementtypen für mehrere Container.



| Beschreibung des Containers                              | Typ des Bibliotheksspeicherorts | Ausgewählter Elementtyp |
|-------------------------------------------------------|-----------------------|--------------------|
| Ein Album, das ein Container mit Spuren ist                | CPIedID             | CPTrackID          |
| Eine Liste, die ein Container von Spuren ist                  | CPListID              | CPTrackID          |
| Eine Liste, bei der es sich um einen Container mit Alben handelt                  | CPListID              | CPIedID          |
| Ein Radiosender, bei dem es sich um einen Container mit Listen handelt          | CPRadioID             | CPListID           |
| Die Gruppe aller Alben, bei denen es sich um einen Container mit Alben handelt | AllCPBeständeIDs         | CPIedID          |
| Die Gruppe aller Terminals, bei denen es sich um einen Container von Terminals handelt. | AllCPGenreIDs         | CPGenreID          |



 

Die Registerkarten in Windows Media Player stellen verschiedene Aufgaben dar. Der Player zeigt Inhalte des Onlineshops in drei verschiedenen Aufgabenbereichen an: **Bibliothek,** **Burn** und **Synchronisieren.** Der Aufgabenbereich Bibliothek wird auch als Aufgabenbereich **Durchsuchen** bezeichnet. Manchmal wird ein Aufgabenbereich als *Feature* bezeichnet, sodass In dieser Dokumentation Begriffe wie *"Feature "Burn"* und *"Synchronisierung"* angezeigt werden.

Die folgenden Beispiele zeigen, wie Windows Media Player die fünf Informationen (Aufgabe, Bibliotheksspeicherorttyp, Bibliotheksspeicherort-ID, ausgewählter Elementtyp, ausgewählte Element-ID) verwendet, um verschiedene Ansichten zu charakterisieren.

Im Aufgabenbereich **"Burn"** zeigt der Player ein Album als Container mit Spuren an. Das Album hat die ID 250. In der Ansicht ist das ausgewählte Element die Spur mit der ID 800. Beachten Sie, dass 800 die ID der Spur im Katalog des Onlineshops ist, nicht die Nummer des Titels auf dem Album.



| Element                  | Wert     |
|-----------------------|-----------|
| task                  | Brennen      |
| Typ des Bibliotheksspeicherorts | CPIedID |
| Id des Bibliotheksspeicherorts   | 250       |
| Ausgewählter Elementtyp    | CPTrackID |
| Ausgewählte Element-ID      | 800       |



 

Im Aufgabenbereich **Synchronisieren** zeigt der Player den Satz aller Alben an, bei dem es sich um einen Container mit Alben handelt. In der Ansicht ist das ausgewählte Element das Album mit der ID 300. Beachten Sie, dass die Bibliotheksspeicherort-ID nicht auf diese Ansicht anwendbar ist.



| Element                  | Wert         |
|-----------------------|---------------|
| task                  | Synchronisierung          |
| Typ des Bibliotheksspeicherorts | AllCPBeständeIDs |
| Id des Bibliotheksspeicherorts   | Nicht zutreffend           |
| Ausgewählter Elementtyp    | CPIedID     |
| Ausgewählte Element-ID      | 300           |



 

Im Strukturansichtssteuerelement wird der Stammknoten für den Onlineshop ausgewählt. In diesem Fall gibt es keinen Container und folglich keine Elemente. Im gesamten Aufgabenbereich **Bibliothek** wird eine Ermittlungsseite angezeigt.



| Element                  | Wert           |
|-----------------------|-----------------|
| task                  | Durchsuchen          |
| Typ des Bibliotheksspeicherorts | RootLocation    |
| Id des Bibliotheksspeicherorts   | Nicht zutreffend             |
| Ausgewählter Elementtyp    | UnknownLocation |
| Ausgewählte Element-ID      | Nicht zutreffend             |



 

Im Aufgabenbereich **Synchronisierung** zeigt der Player das Jahr 2002 als Container mit Spuren an. In der Ansicht ist das ausgewählte Element die Spur mit der ID 450.



| Element                  | Wert           |
|-----------------------|-----------------|
| task                  | Synchronisierung            |
| Speicherorttyp der Bibliothek | ReleaseDateYear |
| Speicherort-ID der Bibliothek   | 2002            |
| Ausgewählter Elementtyp    | CPTrackID       |
| Ausgewählte Element-ID      | 450             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Onlineshops vom Typ 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Ermittlungsseiten**](discovery-pages.md)
</dt> </dl>

 

 




