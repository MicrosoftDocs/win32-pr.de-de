---
title: Type-Attribut (Extrusion) (VML)
description: Type-Attribut (Extrusion) (VML)
ms.assetid: 2c7ad2f1-fb5d-49fb-b490-3efe59ee5177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14bc91f9348603bc89189debb2255f8fff39e135
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858359"
---
# <a name="type-attribute-extrusionvml"></a>Type-Attribut (Extrusion) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Art und Weise, in der die Form extrudiert wird. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Schläuche](msdn-online-vml-extrusion-element.md)

**Tagsyntax**

<o: *Elementtyp* = " *Ausdruck* " >

**Skript Syntax**

*Element* . Type = "*Ausdruck*"

*Ausdruck* = *Element*. Type

**Anmerkungen**

Mögliche Werte:



| Wert       | BESCHREIBUNG                                                                                                                                                            |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parallel    | Die-Extrusion wird gerendert, sodass der Mittelpunkt der Projektion unendlich weit entfernt ist. Das heißt, die extrusionlinien werden nicht aufeinander abgestimmt (im Gegensatz zu perspektivischen Projektionen). Standard. |
| Perspektive | Die-Extrusion wird in einen Mittelpunkt der Projektion gerendert, der mit dem Verschwinden Punkt für undrehte-Objekte identisch ist.                                                       |



 

**Microsoft Office Extensions-Attribut**

 

 