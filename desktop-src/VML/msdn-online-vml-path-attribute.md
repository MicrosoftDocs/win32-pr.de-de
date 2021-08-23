---
title: VML-Pfadattribut
description: VML-Pfadattribut
ms.assetid: ecb64a2f-65f7-4eb9-8d67-d7909bf52d9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f314956452db5a88011a147fd05302483e50cbce3724cf8188068770ec492db6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136963"
---
# <a name="vml-path-attribute"></a>VML-Pfadattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt die Linie an, aus der die Ränder einer Form besteht. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* path=" *ausdruck* ">

**Skriptsyntax**

*element* .path="*expression*"

*expression* = *.path-Element*

**Anmerkungen**

Wenn eine Form das [Path-Element](msdn-online-vml-path-element.md) enthält, haben die Pfadbefehle des Path-Elements Vorrang vor dem Shape-Attributwert. Ausführliche Informationen **zum** Für Pfade verwendeten Befehlssatz finden Sie im Thema Path-Element.

*VML-Standardattribut*

**Beispiel**

Ein geschlossener quadratischer Pfad wird in der Zeichenfolge des Pfadattributs definiert. Ein Anfangspunkt wird mit `m` (für den **Moveto-Befehl** verwendet) bei 1,1 definiert, und eine Zeile wird mit `l` (dem Buchstaben "L" für die **Befehlszeile bis**) von der Anfangsposition (1,1) bis zu den anderen drei Punkten (in der Reihenfolge) gezeichnet: 1.200; 200.200; 200,1. Die Zeile wird mit ( close ) geschlossen `x` und mit ( end ) `e` beendet. Beachten Sie, dass Koordinaten im relativen Koordinatenraum angegeben werden und dass die tatsächliche Größe durch die **Breite** und **Höhe** bestimmt wird.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Pfadattribut – Beispiel.](/previous-versions/bb264089(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 