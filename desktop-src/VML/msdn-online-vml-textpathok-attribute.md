---
title: VML-TextPathOK-Attribut
description: VML-TextPathOK-Attribut
ms.assetid: 5d061258-1c4d-4391-81ce-13af90a4231c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2c14d613df36c314dea75275a4d60fe8792d6dea644ef2595422e74a73dc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597454"
---
# <a name="vml-textpathok-attribute"></a>VML-TextPathOK-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob ein Textpfad angezeigt wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Path](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: textpathok="-Ausdruck  "> 

**Skriptsyntax**

*-Element* . textpathok= "*expression*"

*expression* = *-Element*. textpathok

**Anmerkungen**

False **gibt an,** dass der Pfad keinen Textpfad haben darf. Der Standardwert ist **False**. Sie müssen dieses Attribut auf True **festlegen,** um Text in einem Pfad anzuzeigen.

*VML-Standardattribut*

**Beispiel**

Die Form verfügt über einen Textpfad. Der Text "Hello VML" wird entlang einer lächelnförmigen Kurve angezeigt.


```HTML
   <v:curve id="tc" style="position:relative"
   from="50px 100px" to="400px 100px"
   control1="200px 200px" control2="300px 200px">
   <v:stroke weight="1pt" color="blue"
   filltype="solid"/>
   <v:fill on="True" color="yellow" color2="green" type="gradient"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" id="mytp"
   style="font:normal normal normal 36pt Arial"
   fitpath="True" string="Hello VML"/>
   </v:curve>
```



 

 