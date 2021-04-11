---
description: Zusätzlich zum Erkennen von Text können Erkennungs Tools eine Klasse verwandter Objekte erkennen.
ms.assetid: 53b6137d-2998-4a3b-b469-3d1204ea194b
title: Objekterkenzer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a258c8486bcf773f5f94c4de51c501e107fac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960287"
---
# <a name="object-recognizers"></a>Objekterkenzer

Zusätzlich zum Erkennen von Text können Erkennungs Tools eine Klasse verwandter Objekte erkennen. Objekt erkenmentatoren erkennen allgemeine Formen entsprechend ihrem Zweck. Objekterkenatoren werden verwendet, um Folgendes zu erkennen:

-   Musik Notizen
-   Geometrische Formen
-   Mathematische Gleichungen
-   Flussdiagramm Elemente

In der Regel befinden sich die Objekte, die von einer solchen Erkennung erkannt werden, in einer zweidimensionalen räumlichen oder funktionalen Beziehung zueinander. Innerhalb der komplexen Beziehungen in einer mathematischen Gleichung kann eine Erkennung z. b. unterschiedliche Ergebnisse für eine Obergrenze für eine definitive Ganzzahl zurückgeben, im Gegensatz zu einem Zähler in einem Bruchteil.

Aufgrund der allgemeinen Natur dieser Beziehungen ist es äußerst schwierig, den Satz von Schnittstellen zu definieren, der für jede Objekterkennung funktioniert.

Die Tablet PC-Technologie stellt ein grundlegendes Framework für Objekt erkenzer in der verwalteten Bibliothek und in den Automatisierungs Schnittstellen bereit. Sie müssen jedoch benutzerdefinierte Schnittstellen entwickeln, die komplexe räumliche Beziehungen zwischen erkannten Objekten für jede Objekterkennung beschreiben. Speziell für Objekt erkennenungen stellt die Plattform das grundlegende [**Erkennungs**](inkrecognizercontext-class.md) Element-Objekt bereit, [**um das frei Hand Objekt dem**](inkdisp-class.md) Erkennungs Kontext zuzuordnen und den Erkennungs Modul zum Durchführen der Erkennung aufzurufenden.

 

 



