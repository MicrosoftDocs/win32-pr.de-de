---
description: Eine Anwendung kombiniert zwei Bereiche durch Aufrufen der combinergn-Funktion.
ms.assetid: d16f9ca5-33e2-4752-900e-743245838377
title: Kombinieren von Regionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f51db22daea448acfb02120844ca2859a5ba11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563907"
---
# <a name="combining-regions"></a>Kombinieren von Regionen

Eine Anwendung kombiniert zwei Bereiche durch Aufrufen der [**combinergn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) -Funktion. Mit dieser Funktion kann eine Anwendung die sich überschneidenden Teile von zwei Regionen kombinieren, wobei es sich um die überschneidenden Teile von zwei Regionen, die beiden ursprünglichen Bereiche in der Gesamtheit usw. handelt. Im folgenden sind fünf Werte aufgeführt, die die Regions Kombinationen definieren.



| Wert     | Bedeutung                                                                               |
|-----------|---------------------------------------------------------------------------------------|
| RGN \_ und  | Die sich überschneidenden Teile zweier ursprünglicher Regionen definieren einen neuen Bereich.                   |
| RGN- \_ Kopie | Eine Kopie des ersten (der beiden ursprünglichen Regionen) definiert einen neuen Bereich.               |
| RGN- \_ diff | Der Teil der ersten Region, der keine Schnittmenge überschneidet, definiert einen neuen Bereich. |
| RGN \_ oder   | In den beiden ursprünglichen Regionen wird eine neue Region definiert.                                         |
| RGN- \_ Xor  | Die Teile der beiden ursprünglichen Bereiche, die sich nicht überlappen, definieren eine neue Region.      |



 

Die folgende Abbildung zeigt die fünf möglichen Kombinationen eines Quadrats und einen kreisförmigen Bereich, der sich aus einem Rückruf von [**combinergn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn)ergibt.

![Abbildung, die die in der vorherigen Tabelle beschriebenen Ergebnisse veranschaulicht](images/csrgn-02.png)

 

 



