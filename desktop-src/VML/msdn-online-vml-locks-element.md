---
title: VML-Sperren-Element
description: VML-Sperren-Element
ms.assetid: 1dfdc23a-0ad1-468f-a850-2068f3cc1803
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a3d246e486d1b7db99484777355b9160b71b6b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101974"
---
# <a name="vml-locks-element"></a>VML-Sperren-Element

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert eine Sperre für eine Form.

Die folgenden Attribute ändern eine Sperre.



| Attribut                                                    | BESCHREIBUNG                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Adjusthandles](msdn-online-vml-adjusthandles-attribute.md) | Bestimmt, ob die Handles einer Form bearbeitet werden können.                    |
| [AspectRatio](msdn-online-vml-aspectratio-attribute.md)     | Bestimmt, ob das Seitenverhältnis einer Form von einem Editor geändert werden kann. |
| [Zuschneiden](msdn-online-vml-cropping-attribute.md)           | Bestimmt, ob das Zuschneiden in einem Editor zulässig ist.                   |
| [Antrags](ext-attribute--lock--vml.md)                          | Definiert das Verhalten von Sperr Aktionen für einen grafischen Editor.             |
| [Gruppierung](msdn-online-vml-grouping-attribute.md)           | Bestimmt, ob Formen in einem Editor gruppiert werden können.                      |
| [Position](position-attribute--lock--vml.md)                | Bestimmt, ob die Position einer Form in einem Editor gesperrt ist.          |
| [Drehung](rotation-attribute--lock--vml.md)                | Bestimmt, ob die Drehung von Formen in einem Editor zulässig ist.         |
| [Auswahl](msdn-online-vml-selection-attribute.md)         | Bestimmt, ob die Form in einem Editor auswählbar ist.                    |
| [ShapeType](msdn-online-vml-shapetype-attribute.md)         | Bestimmt, ob der AutoShapes-Typ von einem Editor geändert werden kann.         |
| [Text](msdn-online-vml-text-attribute.md)                   | Bestimmt, ob der an eine Form angefügte Text bearbeitet werden kann.              |
| [Vertices](msdn-online-vml-vertices-attribute.md)           | Bestimmt, ob die Scheitel Punkte eines Pfades von einem Editor geändert werden können.      |



 

**Anmerkungen**

Dieses Element muss innerhalb eines [Shape](shape-element--vml.md) -Elements definiert werden.

Das **Locks** -Element ist eine Microsoft Office Erweiterung von VML.

 

 