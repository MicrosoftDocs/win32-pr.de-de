---
title: VML-Überlänzungsattribut
description: VML-Überlänzungsattribut
ms.assetid: 99c301ff-ed61-48ef-95bb-ceaed1a2553c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dea0abba3f605f749e07d247d207a50a6fe7b247ec54bd88024bad3915285e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099050"
---
# <a name="vml-shininess-attribute"></a>VML-Überlänzungsattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Konzentration des reflektierten Lichts auf einerExtrusionsoberfläche. Lese-/Schreibzugriff. **VgNumber**.

**Gilt für**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Tagsyntax**

<o: *elementiness="* *expression* ">

**Skriptsyntax**

*element* .iness="*expression*"

*expression* = *Element*".iness"

**Anmerkungen**

Hohe Werte (8-10) würden der Schläfrigkeit eines Spiegels und niedrigen Werten (2-3) einem gespiegelten Effekt ungefähren. Werte von 4 bis 7 sind typisch. Reflektionen spiegeln keine anderen Objekte wider. es werden nur punktgenaue Lichtquellen reflektiert. Der Standardwert ist 5.

*Microsoft Office Extensions-Attribut*

 

 