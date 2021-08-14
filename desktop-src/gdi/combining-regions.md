---
description: Eine Anwendung kombiniert zwei Regionen durch Aufrufen der CombineRgn-Funktion.
ms.assetid: d16f9ca5-33e2-4752-900e-743245838377
title: Kombinieren von Regionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6550f260a70bc0f49e6b181f9e1c82a64ce4eadbe643214362444d0dcbfccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887520"
---
# <a name="combining-regions"></a>Kombinieren von Regionen

Eine Anwendung kombiniert zwei Regionen durch Aufrufen der [**CombineRgn-Funktion.**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) Mit dieser Funktion kann eine Anwendung die sich überschneidenden Teile von zwei Regionen kombinieren, alle bis auf die sich überschneidenden Teile von zwei Regionen, die beiden ursprünglichen Regionen in ihrer Gesamtheit usw. Im Folgenden sind fünf Werte angegeben, die die Regionskombinationen definieren.



| Wert     | Bedeutung                                                                               |
|-----------|---------------------------------------------------------------------------------------|
| RGN \_ UND  | Die sich überschneidenden Teile von zwei ursprünglichen Regionen definieren eine neue Region.                   |
| RGN \_ COPY | Eine Kopie der ersten (der beiden ursprünglichen Regionen) definiert eine neue Region.               |
| RGN \_ DIFF | Der Teil des ersten Bereichs, der sich nicht überschneidet, definiert einen neuen Bereich. |
| RGN \_ ODER   | Die beiden ursprünglichen Regionen definieren eine neue Region.                                         |
| RGN \_ XOR  | Die Teile der beiden ursprünglichen Regionen, die sich nicht überschneiden, definieren eine neue Region.      |



 

Die folgende Abbildung zeigt die fünf möglichen Kombinationen eines Quadrats und eines kreisförmigen Bereichs, die sich aus einem Aufruf von [**CombineRgn ergeben.**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn)

![Abbildung, die die in der vorherigen Tabelle beschriebenen Ergebnisse veranschaulicht](images/csrgn-02.png)

 

 



