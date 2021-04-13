---
title: Portieren von nursb-Objekten
description: Bei OpenGL werden nursb als Objekte behandelt, ähnlich der Art, wie viercs behandelt werden, indem Sie ein nursb-Objekt erstellen und dann angeben, wie es gerendert werden soll. In der folgenden Tabelle sind die OpenGL-Funktionen für die Verwaltung von nursb-Objekten aufgeführt.
ms.assetid: baddf81b-219f-44bb-aa17-37404028b258
keywords:
- IRIS GL portieren, nursb-Objekte
- Portieren von IRIS GL, nursb-Objekten
- Portieren auf OpenGL von IRIS GL, nursb-Objekten
- OpenGL-Portierung von IRIS GL, nursb-Objekten
- Nursb-Objekte
- NURBS (Non-Uniform Rational B-Spline)
- Nicht einheitlicher rationaler B-Spline (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0e56c06eea4e4a9a48f9062205277f8b999499
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388484"
---
# <a name="porting-nurbs-objects"></a>Portieren von nursb-Objekten

Bei OpenGL werden nursb als Objekte behandelt, ähnlich der Art und Weise, wie viercs behandelt werden: Sie erstellen ein nursb-Objekt und geben dann an, wie es gerendert werden soll. In der folgenden Tabelle sind die OpenGL-Funktionen für die Verwaltung von nursb-Objekten aufgeführt.



| OpenGL glu-Funktion                                      | Bedeutung                                                        |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**glunewnurbsrenderer**](glunewnurbsrenderer.md)       | Erstellt ein neues nursb-Objekt.                                    |
| [**gludeletenurbsrenderer**](gludeletenurbsrenderer.md) | Löscht ein nursb-Objekt.                                        |
| [*glunurbscallback*](glunurbs.md)                       | Verknüpft einen Rückruf mit einem nursb-Objekt für die Fehlerbehandlung. |



 

Beachten Sie bei der Portierung von IRIS GL nursb-Code in OpenGL die folgenden Punkte:

-   Nursb-Steuerungs Punkte sind Gleit Komma Zahlen und keine doppelte.
-   Der Stride-Parameter wird in Gleit Komma Zahlen und nicht in Bytes gezählt.
-   Wenn Sie Beleuchtung verwenden und keine normale angeben, rufen Sie [**glEnable**](glenable.md) mit GL \_ Auto \_ Normal als Parameter auf, um normale automatisch zu generieren.

??

 

 




