---
title: Speicherort und ausgewähltes Element
description: Speicherort und ausgewähltes Element
ms.assetid: 9556e01f-1f75-4089-9e62-b41a9aa53e93
keywords:
- Windows Media Player Online Stores, Standorte
- Online Stores, Standorte
- Typ 1 Online Stores, Standorte
- Windows Media Player Online Stores, Bibliotheks Standorte
- Online Stores, Bibliotheks Standorte
- Typ 1 Online Stores, Bibliotheks Standorte
- Windows Media Player Online Stores, ausgewählte Elemente
- Online Stores, ausgewählte Elemente
- Typ 1 Online Stores, ausgewählte Elemente
- Windows Media Player-Bibliothek, Standorte
- Windows Media Player-Bibliothek, ausgewählte Elemente
- Bibliothek, Standorte
- Bibliothek, ausgewählte Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d665b11e7509e369224d3e85db30dddb4a988a14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206672"
---
# <a name="location-and-selected-item"></a>Speicherort und ausgewähltes Element

In Windows Media Player werden die folgenden fünf Elemente verwendet, um die aktuelle Ansicht des Online Store-Inhalts zu bezeichnen:

-   task
-   bibliothekationstyp
-   Bibliotheks Speicherort-ID
-   Typ des ausgewählten Elements
-   ID des ausgewählten Elements

In der Regel können Sie sich die Ansicht in Windows Media Player als Container von Elementen vorstellen. Der Container weist einen Typ auf, und ein Element weist einen Typ auf. Alle Elemente in einem Container haben denselben Typ. Location-und Elementtypen werden von den [Bibliotheks Speicherort Konstanten](library-location-constants.md)angegeben. Wenn die aktuelle Ansicht z. b. ein einzelnes Album anzeigt, ist der Speicherort der Bibliothek cpalbumid, und da ein Album nachverfolgt, ist der ausgewählte Elementtyp cptrackid.

In der folgenden Tabelle sind die Speicherort-und Elementtypen für mehrere Container aufgeführt.



| Beschreibung des Containers                              | Bibliothekationstyp | Typ des ausgewählten Elements |
|-------------------------------------------------------|-----------------------|--------------------|
| Ein Album, das ein Container von Spuren ist.                | Cpalbumid             | Cptrackid          |
| Eine Liste, die ein Container von Spuren ist.                  | Cplistid              | Cptrackid          |
| Eine Liste, die ein Container von Alben ist.                  | Cplistid              | Cpalbumid          |
| Eine Radio Station, bei der es sich um einen Container von Listen handelt          | Cpradioid             | Cplistid           |
| Der Satz aller Alben, bei dem es sich um einen Container von Alben handelt | Allcpalbumids         | Cpalbumid          |
| Der Satz aller Genres, bei dem es sich um einen Container von Genres handelt. | Allcpgenreids         | Cpgenreid          |



 

Die Registerkarten in Windows Media Player die verschiedene Aufgaben darstellen. Der Player zeigt Online Store-Inhalte in drei verschiedenen Aufgabenbereichen an: **Bibliothek**, **Brennen** und **Synchronisierung**. Der Aufgabenbereich Bibliothek wird auch als Aufgabenbereich **Durchsuchen** bezeichnet. Manchmal wird ein Aufgabenbereich als *Feature* bezeichnet, sodass Sie in dieser Dokumentation Begriffe wie " *Burn Feature* " und " *Sync Feature* " sehen können.

In den folgenden Beispielen wird veranschaulicht, wie Windows Media Player die fünf Informationen verwendet (Task, bibliothekationsort, Bibliotheks Speicherort-ID, ausgewählter Elementtyp, ausgewählte Element-ID), um unterschiedliche Ansichten zu bezeichnen.

Im Aufgabenbereich " **Burn** " zeigt der Spieler ein Album als Container für Titel an. Das Album weist die ID 250 auf. In der Ansicht ist das ausgewählte Element der Titel mit der ID 800. Beachten Sie, dass 800 die ID des Titels im Katalog des Online Stores ist, nicht die Nummer des Titels im Album.



| Element                  | Wert     |
|-----------------------|-----------|
| task                  | Brenn      |
| bibliothekationstyp | Cpalbumid |
| Bibliotheks Speicherort-ID   | 250       |
| Typ des ausgewählten Elements    | Cptrackid |
| ID des ausgewählten Elements      | 800       |



 

Im Aufgabenbereich **Synchronisieren** zeigt der Player den Satz aller Alben an, bei dem es sich um einen Container von Alben handelt. Das ausgewählte Element in der Ansicht ist das Album mit der ID 300. Beachten Sie, dass die Bibliotheks Speicherort-ID für diese Sicht nicht anwendbar ist.



| Element                  | Wert         |
|-----------------------|---------------|
| task                  | Synchronisierung          |
| bibliothekationstyp | Allcpalbumids |
| Bibliotheks Speicherort-ID   | –           |
| Typ des ausgewählten Elements    | Cpalbumid     |
| ID des ausgewählten Elements      | 300           |



 

Im Strukturansicht-Steuerelement ist der Stamm Knoten für den Online Store ausgewählt. In diesem Fall gibt es keinen Container, und folglich gibt es keine Elemente. Im Aufgabenbereich gesamte **Bibliothek** wird eine Ermittlungs Seite angezeigt.



| Element                  | Wert           |
|-----------------------|-----------------|
| task                  | Durchsuchen          |
| bibliothekationstyp | Rootlocation    |
| Bibliotheks Speicherort-ID   | –             |
| Typ des ausgewählten Elements    | Unknownlocation |
| ID des ausgewählten Elements      | –             |



 

Im Aufgabenbereich **Synchronisieren** zeigt der Spieler das Jahr 2002 als Container für Titel an. In der Ansicht ist das ausgewählte Element der Titel mit der ID 450.



| Element                  | Wert           |
|-----------------------|-----------------|
| task                  | Synchronisierung            |
| bibliothekationstyp | Releasedateyear |
| Bibliotheks Speicherort-ID   | 2002            |
| Typ des ausgewählten Elements    | Cptrackid       |
| ID des ausgewählten Elements      | 450             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Typ 1 Online Stores**](about-type-1-online-stores.md)
</dt> <dt>

[**Ermittlungs Seiten**](discovery-pages.md)
</dt> </dl>

 

 




