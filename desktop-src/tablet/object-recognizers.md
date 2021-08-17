---
description: Neben der Texterkennung können Erkennungen auch eine Klasse verwandter Objekte erkennen.
ms.assetid: 53b6137d-2998-4a3b-b469-3d1204ea194b
title: Objekt-Recognizers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabfd44a5eb126d48df70efd1c391584d12afc94e5e21c714aa0c740a7d486f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449661"
---
# <a name="object-recognizers"></a>Objekt-Recognizers

Neben der Texterkennung können Erkennungen auch eine Klasse verwandter Objekte erkennen. Objekt-Recognizer erkennen allgemeine Formen entsprechend ihrem Zweck. Objekt-Recognizer werden verwendet, um:

-   Anmerkungen zu "Notes"
-   Geometrische Formen
-   Mathematische Gleichungen
-   Flow Diagrammelemente

In der Regel befinden sich die Objekte, die von einer solchen Erkennen erkannt werden, in einer zweidimensionalen räumlichen oder funktionalen Beziehung miteinander. Innerhalb der komplexen Beziehungen in einer mathematischen Gleichung kann eine Recognizer beispielsweise unterschiedliche Ergebnisse für eine Obergrenze für ein bestimmtes Integral zurückgeben, im Gegensatz zu einem Zähler in einem Bruch.

Aufgrund des sehr allgemeinen Charakters dieser Beziehungen ist es äußerst schwierig, den Satz von Schnittstellen zu definieren, der für jede Objekt erkannt werden kann.

Die Tablet PC-Technologie stellt ein grundlegendes Framework für Objekt erkennende Objekte in den Schnittstellen verwaltete Bibliothek und Automatisierung bereit. Sie müssen jedoch benutzerdefinierte Schnittstellen entwickeln, die komplexe räumliche Beziehungen zwischen erkannten Objekten für jede Objekt erkannt werden. Insbesondere für Objekterkennungen stellt die Plattform das grundlegende [**RecognizerContext-Objekt**](inkrecognizercontext-class.md) zum Zuordnen des [**Ink-Objekts**](inkdisp-class.md) zum Erkennungskontext und zum Aufrufen der Erkennung zum Durchführen der Erkennung zur Verfügung.

 

 



