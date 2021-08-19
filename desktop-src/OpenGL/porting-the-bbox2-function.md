---
title: Portieren der bbox2-Funktion
description: Es gibt kein OpenGL-Äquivalent für die IRIS GL bbox2-Funktion.
ms.assetid: 2d8082bf-c2c3-41d9-9bf7-b4ac2fdefbd6
keywords:
- IRIS GL-Portierung, bbox2-Funktion
- Portieren von IRIS GL,bbox2-Funktion
- Portieren von IRIS GL,bbox2-Funktion zu OpenGL
- OpenGL-Portierung über die IRIS GL,bbox2-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f34bc9035e9aa9fac884a14946a0593cb70702cf19f22d5d4c82011b58077e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012008"
---
# <a name="porting-the-bbox2-function"></a>Portieren der bbox2-Funktion

Es gibt kein OpenGL-Äquivalent für die IRIS GL **bbox2-Funktion.**

**So portieren Sie Code, der bbox2-Funktionen enthält**

1.  Erstellen Sie eine neue (OpenGL)-Anzeigeliste, die alles in der entsprechenden IRIS GL-Anzeigeliste mit Ausnahme des Aufrufs von **bbox2 enthält.**
2.  Verwenden Sie Windows Code, um ein Rechteck mit der gleichen Größe wie die IRIS **GL-Bbox zu zeichnen.**

 

 




