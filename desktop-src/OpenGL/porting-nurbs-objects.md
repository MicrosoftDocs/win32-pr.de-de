---
title: Portieren von NURBS-Objekten
description: OpenGL behandelt NURBS als Objekte, ähnlich wie quadrierte Objekte, die Sie erstellen, und geben dann an, wie es gerendert werden soll. In der folgenden Tabelle sind die OpenGL-GLU-Funktionen zum Verwalten von NURBS-Objekten aufgeführt.
ms.assetid: baddf81b-219f-44bb-aa17-37404028b258
keywords:
- IRIS GL-Portierung, NURBS-Objekte
- Portieren von IRIS GL-, NURBS-Objekten
- Portieren von IRIS GL,NURBS-Objekten zu OpenGL
- OpenGL-Portierung von IRIS GL,NURBS-Objekten
- NURBS-Objekte
- NURBS (Non-Uniform Rational B-Spline)
- Non-Uniform Rational B-Spline (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6990d2292399cb1ccaf00ba6ec42d680c5ace887b2495daf8640db2da30ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132409"
---
# <a name="porting-nurbs-objects"></a>Portieren von NURBS-Objekten

OpenGL behandelt NURBS ähnlich wie Quadristiken als Objekte: Sie erstellen ein NURBS-Objekt und geben dann an, wie es gerendert werden soll. In der folgenden Tabelle sind die OpenGL-GLU-Funktionen zum Verwalten von NURBS-Objekten aufgeführt.



| OpenGL-GLU-Funktion                                      | Bedeutung                                                        |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)       | Erstellt ein neues NURBS-Objekt.                                    |
| [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) | Löscht ein NURBS-Objekt.                                        |
| [*gluNurbsCallback*](glunurbs.md)                       | Ordnet einem NURBS-Objekt einen Rückruf zur Fehlerbehandlung zu. |



 

Beachten Sie beim Portieren von IRIS GL NURBS-Code zu OpenGL folgende Punkte:

-   NURBS-Kontrollpunkte sind gleitkomma, nicht doubles.
-   Der stride-Parameter wird in Gleitkommawerte und nicht in Bytes gezählt.
-   Wenn Sie Beleuchtung verwenden und keine Normalwerte angeben, rufen Sie [**glEnable**](glenable.md) mit GL AUTO NORMAL als Parameter auf, um \_ \_ normals automatisch zu generieren.

??

 

 




