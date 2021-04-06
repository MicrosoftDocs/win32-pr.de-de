---
title: Portieren von Funktionen, die Matrizen und Transformationen erhalten
description: In der folgenden Tabelle werden die Iris GL-Funktionen aufgelistet, die den Status von Matrizen und Transformationen und deren OpenGL-Entsprechungen erhalten.
ms.assetid: 53546bc0-ce1d-47e0-ab5e-5d6789c6db2a
keywords:
- IRIS GL portieren, Matrizen
- Portieren von IRIS GL, Matrizen
- Portieren auf OpenGL von IRIS GL, Matrizen
- OpenGL-Portierung von IRIS GL, Matrizen
- Matrizen
- IRIS GL portieren, Transformationen
- Portieren von IRIS GL, Transformationen
- Portieren auf OpenGL von IRIS GL, Transformationen
- OpenGL-Portierung von IRIS GL, Transformationen
- Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b32ab017e81c9875666785786b29d9c94c7fd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947822"
---
# <a name="porting-functions-that-get-matrices-and-transformations"></a>Portieren von Funktionen, die Matrizen und Transformationen erhalten

In der folgenden Tabelle werden die Iris GL-Funktionen aufgelistet, die den Status von Matrizen und Transformationen und deren OpenGL-Entsprechungen erhalten.



| IRIS GL-Matrix Abfrage                  | OpenGL-glget-Matrix Abfrage         | Bedeutung                                                         |
|---------------------------------------|-----------------------------------|-----------------------------------------------------------------|
| **getmmode**                          | GL- \_ Matrix \_ Modus                  | Gibt den aktuellen Matrix Modus zurück.                                |
| **getMatrix** im **MVIEW** -Modus    | GL- \_ Modelview- \_ Matrix             | Gibt eine Kopie der aktuellen Modell Ansichts Matrix zurück.                |
| **getMatrix** im **mprojection** -Modus | GL- \_ Projektions \_ Matrix            | Gibt eine Kopie der aktuellen Projektions Matrix zurück.                |
| **getMatrix** im **mtexture** -Modus    | GL- \_ Textur \_ Matrix               | Gibt eine Kopie der aktuellen Textur Matrix zurück.                   |
| Nicht zutreffend                       | \_Max. maximale \_ Modelview- \_ Stapel \_ Tiefe  | Gibt die maximal unterstützte Tiefe des Modell Ansichts Matrix Stapels zurück. |
| Nicht zutreffend                       | \_Maximale maximale \_ Projektions \_ Stapel \_ Tiefe von GL | Gibt die maximal unterstützte Tiefe des Projektions Matrix Stapels zurück. |
| Nicht zutreffend                       | \_Maximale maximale \_ Textur \_ Stapel \_ Tiefe von GL    | Gibt die maximal unterstützte Tiefe des Textur Matrix Stapels zurück.    |
| Nicht zutreffend                       | \_ \_ Stapel Tiefe von GL Modelview \_       | Gibt die Anzahl von Matrizen im Modell Ansichts Stapel zurück.             |
| Nicht zutreffend                       | \_ \_ Stapel \_ Tiefe der GL-Projektion      | Gibt die Anzahl von Matrizen auf dem Projektions Stapel zurück.             |
| Nicht zutreffend                       | GL- \_ Textur \_ Stapel \_ Tiefe         | Gibt die Anzahl von Matrizen auf dem Textur Stapel zurück.                |



 

??

 

 




