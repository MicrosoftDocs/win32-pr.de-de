---
title: ADJ-Attribut
description: ADJ-Attribut
ms.assetid: f0f31e6c-9dde-4082-88a2-da2d0012b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff83371cbca29ee687875343976b312466d6a78c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339496"
---
# <a name="adj-attribute"></a>ADJ-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt einen Anpassungswert an, der verwendet wird, um Werte für eine Formel zu definieren. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* adj = " *Expression* " >

**Skript Syntax**

*Element* . adj = "*Ausdruck*"

*Ausdruck* = *Element*. ADJ

**Anmerkungen**

**ADJ** dient zum Bereitstellen von anpassbaren Punkten für eine Formel. Bei Verwendung in Tags ist **ADJ** eine durch Trennzeichen getrennte Zeichenfolge mit bis zu acht Werten. Einige Werte werden möglicherweise ausgelassen. Beispielsweise ist "0, 1, 2,, 4, 5,, 7" eine gültige Zeichenfolge, aber das vierte und das siebte Element enthalten keine Werte (Elemente werden beginnend mit 0 gezählt).

Bei der Skripterstellung verwendet **ADJ** den [ivganpassungen](msdn-online-vml-ivgadjustments-data-type.md) -Datentyp.

*VML-Standard Attribut*

**Siehe auch**

[Formel](msdn-online-vml-formulas-element.md)

**Beispiel**

Ein einfaches Quadrat wird mit Anpassungen erstellt. Zuerst wird die **ADJ** -Zeichenfolge erstellt, um acht Anpassungs Werte zu definieren. Dann wird auf jeden Anpassungswert durch eine der acht Formeln verwiesen, wobei jeder Anpassungswert durch ein Nummern Zeichen () vorangestellt wird \# . Schließlich wird ein Pfad durch eine Zeichenfolge definiert, die auf die Formeln verweist, wobei jeder Formel das Zeichen "at" (@) vorangestellt ist.


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



[ADJ-Attribut Beispiel](/previous-versions/bb229662(v=vs.85)) (erfordert Microsoft Internet Explorer 5 oder höher)

 

 