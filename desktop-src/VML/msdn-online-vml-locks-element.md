---
title: VML Locks-Element
description: VML Locks-Element
ms.assetid: 1dfdc23a-0ad1-468f-a850-2068f3cc1803
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 258ad050ea59427e43faba5b92ddc93dfd62e5065c874a0c5f5d25d88e30fecc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573980"
---
# <a name="vml-locks-element"></a>VML Locks-Element

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert eine Sperre für eine Form.

Die folgenden Attribute ändern eine Sperre.



| attribute                                                    | BESCHREIBUNG                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------|
| [AdjustHandles](msdn-online-vml-adjusthandles-attribute.md) | Bestimmt, ob die Handles einer Form bearbeitet werden können.                    |
| [AspectRatio](msdn-online-vml-aspectratio-attribute.md)     | Bestimmt, ob das Seitenverhältnis einer Form von einem Editor geändert werden kann. |
| [Zuschneiden](msdn-online-vml-cropping-attribute.md)           | Bestimmt, ob zuschneiden in einem Editor zulässig ist.                   |
| [Extern](ext-attribute--lock--vml.md)                          | Definiert das Verhalten von Sperraktionen für einen grafischen Editor.             |
| [Gruppierung](msdn-online-vml-grouping-attribute.md)           | Bestimmt, ob Formen in einem Editor gruppiert werden können.                      |
| [Position](position-attribute--lock--vml.md)                | Bestimmt, ob die Position einer Form in einem Editor gesperrt ist.          |
| [Drehung](rotation-attribute--lock--vml.md)                | Bestimmt, ob die Drehung von Formen in einem Editor zulässig ist.         |
| [Auswahl](msdn-online-vml-selection-attribute.md)         | Bestimmt, ob die Form in einem Editor ausgewählt werden kann.                    |
| [ShapeType](msdn-online-vml-shapetype-attribute.md)         | Bestimmt, ob der AutoShapes-Typ von einem Editor geändert werden kann.         |
| [Text](msdn-online-vml-text-attribute.md)                   | Bestimmt, ob der an eine Form angefügte Text bearbeitet werden kann.              |
| [Scheitelpunkte](msdn-online-vml-vertices-attribute.md)           | Bestimmt, ob die Scheitelungen eines Pfads von einem Editor geändert werden können.      |



 

**Anmerkungen**

Dieses Element muss innerhalb eines [Shape-Elements definiert](shape-element--vml.md) werden.

Das **Locks-Element** ist eine Microsoft Office Erweiterung für VML.

 

 