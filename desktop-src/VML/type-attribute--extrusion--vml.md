---
title: Type-Attribut (Extrusion)(VML)
description: Type-Attribut (Extrusion)(VML)
ms.assetid: 2c7ad2f1-fb5d-49fb-b490-3efe59ee5177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a14c3b69aa4156cbd94bb8598caa80ccd92721574daafe074486eb293059cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057583"
---
# <a name="type-attribute-extrusionvml"></a>Type-Attribut (Extrusion)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Art und Weise, wie die Form gekergt wird. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Tagsyntax**

<o: *element* type=" *ausdruck* ">

**Skriptsyntax**

*element* .type="*expression*"

*expression* = *Element*.type

**Anmerkungen**

Mögliche Werte:



| Wert       | Beschreibung                                                                                                                                                            |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parallel    | DieExtrusion wird gerendert, sodass der Mittelpunkt der Projektion unendlich weit entfernt ist. Das bedeutet, dass dieExtrusionslinien nicht konvergiert werden (im Gegensatz zu Perspektivenprojektionen). Standard. |
| Perspektive | DieExtrusion wird in eine Projektionsmitte gerendert, die mit dem Ausgangspunkt für nicht umgeschriebene Objekte identisch ist.                                                       |



 

**Microsoft Office Extensions-Attribut**

 

 