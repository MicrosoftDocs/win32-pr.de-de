---
title: Adj-Attribut
description: Adj-Attribut
ms.assetid: f0f31e6c-9dde-4082-88a2-da2d0012b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85869500cc3e9f86e0f48e67f63cfd9e6ed2cff5580caa04994169a9e4b50df8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137143"
---
# <a name="adj-attribute"></a>Adj-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Gibt einen Anpassungswert an, mit dem Werte für eine Formel definiert werden. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* adj="-Ausdruck "> 

**Skriptsyntax**

*element* .adj="*expression*"

*expression* = *Element*.adj

**Anmerkungen**

**Adj** wird verwendet, um anpassbare Punkte für eine Formel zur Verfügung zu stellen. Bei Verwendung in Tags ist **Adj** eine durch Trennzeichen getrennte Zeichenfolge mit bis zu 8 Werten. Einige Werte werden möglicherweise ausgelassen. Beispielsweise wäre "0,1,2,,4,5,,7" eine gültige Zeichenfolge, aber das vierte und das siebten Elemente hätten keine Werte (Elemente werden ab 0 gezählt).

Für die **Skripterstellung verwendet Adj** den [IVgAdjustments-Datentyp.](msdn-online-vml-ivgadjustments-data-type.md)

*VML-Standardattribut*

**Siehe auch**

[Formel](msdn-online-vml-formulas-element.md)

**Beispiel**

Ein einfaches Quadrat wird mit Anpassungen erstellt. Zuerst wird die **Adj-Zeichenfolge** erstellt, um acht Anpassungswerte zu definieren. Anschließend wird auf jeden Anpassungswert von einer der acht Formeln verwiesen, und jeder Anpassungswert wird durch ein Zahlenzeichen ( \# ) gekennzeichnet. Schließlich wird ein Pfad durch eine Zeichenfolge definiert, die auf die Formeln verweist, und jede Formel wird durch das Zeichen "at" (@) gekennzeichnet.


```HTML
   <v:shape id="rect01" type="#myshape"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:30;left:30;width:20;height:20"
   adj="1, 1, 1, 200, 200, 200, 200, 1">
   <v:path v="m @0,@1 l @2,@3, @4,@5, @6,@7 x e"/>
   <v:formulas>
   <v:f eqn="val #0"/>
   <v:f eqn="val #1"/>
   <v:f eqn="val #2"/>
   <v:f eqn="val #3"/>
   <v:f eqn="val #4"/>
   <v:f eqn="val #5"/>
   <v:f eqn="val #6"/>
   <v:f eqn="val #7"/>
   </v:formulas>
   </v:shape>
```



[Adj-Attributbeispiel](/previous-versions/bb229662(v=vs.85)) (erfordert Microsoft Internet Explorer 5 oder höher.)

 

 