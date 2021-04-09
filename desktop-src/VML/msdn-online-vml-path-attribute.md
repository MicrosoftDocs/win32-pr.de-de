---
title: VML-Pfad Attribut
description: VML-Pfad Attribut
ms.assetid: ecb64a2f-65f7-4eb9-8d67-d7909bf52d9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e43e453e982327549475de4643cc0ad21bc0b4db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858455"
---
# <a name="vml-path-attribute"></a>VML-Pfad Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt die Zeile an, aus der die Ränder einer Form gebildet werden. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Path = " *Expression* " >

**Skript Syntax**

*Element* . Path = "*Ausdruck*"

*Ausdruck* = *Element*. Path

**Anmerkungen**

Wenn eine Form das [path](msdn-online-vml-path-element.md) -Element enthält, haben die Pfad Befehle des Path-Elements Vorrang vor dem Shape-Attribut Wert. Weitere Informationen zu dem für Pfade verwendeten Befehlssatz finden Sie im Thema " **Pfad** Element".

*VML-Standard Attribut*

**Beispiel**

Ein geschlossener quadratischer Pfad wird in der Zeichenfolge des Path-Attributs definiert. Ein Anfangspunkt wird mit `m` (für den Befehl "  Befehl") bei 1, 1 definiert, und eine Linie wird mit `l` (dem Buchstaben "L", der für den Befehl " **LineTo**" verwendet wird) von der Startposition (1, 1) bis zu den anderen drei Punkten (in der Reihenfolge) gezeichnet: 1.200; 200.200; 200, 1. Die Zeile wird mit `x` (**Close**) geschlossen und endet mit `e` (**Ende**). Beachten Sie, dass Koordinaten im relativen Koordinaten Bereich angegeben werden und dass die tatsächliche Größe durch **Breite** und **Höhe** bestimmt wird.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Beispiel für ein Pfad Attribut](/previous-versions/bb264089(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 