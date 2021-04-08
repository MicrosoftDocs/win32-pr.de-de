---
title: Fehler bei der Aria-Raster Struktur
description: Fehler bei der Aria-Raster Struktur
ms.assetid: 8B2AEC98-1056-4560-AD6E-C6ECA0B94692
keywords:
- Ariagridstructureerrorid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd692c5fb82675b8fdcc6bf88fe35695113c9ef0
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734593"
---
# <a name="aria-grid-structure-error"></a>Fehler bei der Aria-Raster Struktur

## <a name="text"></a>Text

Das Element mit der **Raster** Rolle verfügt nicht über eine entsprechende Raster Struktur oder ein barrierefreies Markup.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Dieser Fehler gilt für benutzerdefinierte Elemente, für die das **Role** -Attribut auf "Grid" festgelegt ist. Es gilt nicht für HTML-Tabellen Tags, die die implizite **Rolle** "Grid" aufweisen.

Für ein Element, für das das **Role** -Attribut auf "Grid" festgelegt ist, muss die Struktur definiert sein, die von der Web-Barrierefreiheits Initiative, auf die eine RIA-Aria-Raster Rolle zugreifen kann

Um diesen Fehler zu beheben, überprüfen Sie Ihre Implementierung, um sicherzustellen, dass Sie der Spezifikation "WAI-ARIA" entspricht. Stellen Sie insbesondere sicher, dass die Struktur die folgenden Regeln erfüllt.

-   Das **Raster** enthält Zeilen-oder **Zeilen** **Gruppen** Elemente.
-   Zeilen **Gruppe** enthält **Zeilen** Elemente.
-   **Zeilen** Elemente enthalten **ColumnHeader** -oder **gridcell** -oder **RowHeader** -Elemente.

Ein Barrierefreiheits Name sollte für **Raster**-, **ColumnHeader**-, **gridcell** -und **RowHeader** -Elemente mithilfe eines der folgenden Attribute definiert werden.

-   Das [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) -Attribut für den Verweis auf das Element, das Text enthält.
-   das Attribut " [**Aria-Label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) ", um den barrierefreien Namen direkt festzulegen.
-   [**Titel**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) zum Erstellen einer QuickInfo, die zur gleichen Zeit als Name verwendet wird.

 

 




