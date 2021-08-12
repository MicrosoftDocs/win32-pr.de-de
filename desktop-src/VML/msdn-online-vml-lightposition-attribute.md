---
title: VML LightPosition-Attribut
description: VML LightPosition-Attribut
ms.assetid: 2ac3825d-319e-4761-905d-eb8127c4d4cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69fb361064e939e9438a917d9be37360cd446424e818e14bbdb43e521f46b09b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598482"
---
# <a name="vml-lightposition-attribute"></a>VML LightPosition-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt die Position des primären Lichts in einer Szene an. Lese-/Schreibzugriff. **VgVector3D**.

**Gilt für**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Tagsyntax**

<o: *element* lightposition=" *ausdruck* ">

**Skriptsyntax**

*element* .lightposition="*expression*"

*expression* = *Element*.lightposition

**Anmerkungen**

Verwenden Sie diesen Wert, um die Lichtquelle für eineExtrusion zu verschieben. Unterschiedliche Positionen werden jedes Gesicht derExtrusion auf- oder abdunkelt. Der Standardwert ist 50000,0,10000.

*Microsoft Office Extensions-Attribut*

 

 