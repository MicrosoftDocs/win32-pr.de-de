---
title: Portieren von Funktionen zum Abrufen von Matrizen und Transformationen
description: In der folgenden Tabelle sind die IRIS GL-Funktionen aufgeführt, die den Status von Matrizen und Transformationen und deren OpenGL-Entsprechungen abrufen.
ms.assetid: 53546bc0-ce1d-47e0-ab5e-5d6789c6db2a
keywords:
- IRIS GL-Portierung,Matrizen
- Portieren von IRIS GL,Matrizen
- Portieren von IRIS GL zu OpenGL, Matrizen
- OpenGL-Portierung von IRIS GL,Matrizen
- Matrizen
- IRIS GL-Portierung, Transformationen
- Portieren von IRIS GL,Transformationen
- Portieren von IRIS GL zu OpenGL, Transformationen
- OpenGL-Portierung von IRIS GL,Transformationen
- Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68eed8722d982d8d93f47f4d2dc02b8f0f97d9c58512400353ab068015455e13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776970"
---
# <a name="porting-functions-that-get-matrices-and-transformations"></a>Portieren von Funktionen zum Abrufen von Matrizen und Transformationen

In der folgenden Tabelle sind die IRIS GL-Funktionen aufgeführt, die den Status von Matrizen und Transformationen und deren OpenGL-Entsprechungen abrufen.



| IRIS GL-Matrixabfrage                  | OpenGL glGet-Matrixabfrage         | Bedeutung                                                         |
|---------------------------------------|-----------------------------------|-----------------------------------------------------------------|
| **getmmode**                          | GL \_ \_ MATRIX-MODUS                  | Gibt den aktuellen Matrixmodus zurück.                                |
| **getmatrix** im **MVIEWING-Modus**    | GL \_ MODELVIEW \_ MATRIX             | Gibt eine Kopie der aktuellen Modellansichtsmatrix zurück.                |
| **getmatrix** im **MPROJECTION-Modus** | \_GL-PROJEKTIONSMATRIX \_            | Gibt eine Kopie der aktuellen Projektionsmatrix zurück.                |
| **getmatrix** im **MTEXTURE-Modus**    | GL \_ TEXTURE \_ MATRIX               | Gibt eine Kopie der aktuellen Texturmatrix zurück.                   |
| Nicht zutreffend                       | GL \_ MAX \_ MODELVIEW \_ STACK \_ DEPTH  | Gibt die maximal unterstützte Tiefe des Matrixstapels der Modellansicht zurück. |
| Nicht zutreffend                       | GL \_ MAX \_ \_ PROJEKTIONSSTAPELTIEFE \_ | Gibt die maximal unterstützte Tiefe des Projektionsmatrixstapels zurück. |
| Nicht zutreffend                       | GL \_ MAX \_ TEXTURE \_ STACK \_ DEPTH    | Gibt die maximal unterstützte Tiefe des Texturmatrixstapels zurück.    |
| Nicht zutreffend                       | GL \_ MODELVIEW \_ STACK \_ DEPTH       | Gibt die Anzahl der Matrizen im Modellansichtsstapel zurück.             |
| Nicht zutreffend                       | \_ \_ GL-PROJEKTIONSSTAPELTIEFE \_      | Gibt die Anzahl der Matrizen auf dem Projektionsstapel zurück.             |
| Nicht zutreffend                       | GL \_ \_ TEXTURSTAPELTIEFE \_         | Gibt die Anzahl der Matrizen auf dem Texturstapel zurück.                |



 

??

 

 




