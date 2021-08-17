---
title: VML-Attribut "MiterLimit"
description: VML-Attribut "MiterLimit"
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fef82ce7e8e0d3bf99fc532a9e746a94006a6bb9deba282ce8edd6ab91d41902
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119308370"
---
# <a name="vml-miterlimit-attribute"></a>VML-Attribut "MiterLimit"

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert die Glättung des Miter-Fugens. Lese-/Schreibzugriff. **VgNumber**.

**Gilt für**

[Takt](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *element* miterlimit=" *expression* ">

**Skriptsyntax**

*element* .miterlimit="*expression*"

*expression* = *Element*.miterlimit

**Anmerkungen**

Der maximale Abstand zwischen dem inneren und äußeren Punkt eines Fugens. Diese Zahl ist ein Vielfaches der Linienstärke.

Der Standardwert ist 8.

*VML-Standardattribut*

**Beispiel**

Die Fugen auf der Polylinie werden mit einem Grenzwert von 10,5-mal zwei Punkten geerbt.


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke miterlimit="5" joinstyle="miter"/>
   </v:polyline>
```



 

 