---
title: VML-Facetattribut
description: VML-Facetattribut
ms.assetid: 6b874d79-a34e-45f7-bbbf-44d652410b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b1ae12ba31d286f1e029dcd433820e8c50acb05c86a92b2c06e1df50c73a0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681010"
---
# <a name="vml-facet-attribute"></a>VML-Facetattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Anzahl der Facetten, die verwendet werden, um gekrümmte Oberflächen einerExtrusion zu beschreiben. Lese-/Schreibzugriff. **VgNumber**.

**Gilt für**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Tagsyntax**

<o: *element* facet="-Ausdruck "> 

**Skriptsyntax**

*element* .facet="*expression*"

*expression* = *Element*.facet

**Anmerkungen**

Definiert die Art und Weise, wie eine Rendering-Engine derExtrusion ungefähr entspricht. Eine niedrigere Zahl gibt eine niedrigere Renderingtoleranz für die Rendering-Engine an und gibt mehr Facetten zurück. Höhere Zahlen lassen dieExtrusion facettenreicher erscheinen. Der Standardwert ist 30.000.

*Microsoft Office Extensions-Attribut*

 

 