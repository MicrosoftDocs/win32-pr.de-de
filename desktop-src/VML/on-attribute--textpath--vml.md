---
title: On-Attribut (TextPath) (VML)
description: On-Attribut (TextPath) (VML)
ms.assetid: b4a88473-6d5f-42b3-afd6-86f602c83724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ae791b1144046a1c29e92d11663cd15d696bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517090"
---
# <a name="on-attribute-textpathvml"></a>On-Attribut (TextPath) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert, ob der Text angezeigt wird. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[TextPath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *Element* on = " *Expression* " >

**Skript Syntax**

*Element* . on = "*Ausdruck*"

*Ausdruck* = *Element*. on

**Anmerkungen**

Der Standardwert ist **False**. Dieser Wert muss auf **true** festgelegt werden, um Text in einem Textpfad anzuzeigen.

*VML-Standard Attribut*

**Beispiel**

Der Text im Textpfad wird angezeigt.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 