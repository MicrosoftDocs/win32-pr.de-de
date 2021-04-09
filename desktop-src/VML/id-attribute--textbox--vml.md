---
title: ID-Attribut (Textfeld) (VML)
description: ID-Attribut (Textfeld) (VML)
ms.assetid: b9eb75cc-4d0a-4e83-a897-e35995ae7c53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b39ac566e7b619c31cb12f4657bd86020dc12cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858332"
---
# <a name="id-attribute-textboxvml"></a>ID-Attribut (Textfeld) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Ein Name, der einen eindeutigen Bezeichner für ein TextBox-Steuer Tool bereitstellt. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[TextBox](msdn-online-vml-textbox-element.md)

**Tagsyntax**

<v: *Element* -ID = " *Ausdruck* " >

**Skript Syntax**

*Element* . ID = "*Ausdruck*"

*Ausdruck* = *Element*. ID

**Anmerkungen**

Verwenden Sie **ID** , um auf ein bestimmtes Textfeld zu verweisen. Nachdem Sie ein Textfeld erstellt und eine ID angegeben haben, können Sie den ID-Namen verwenden, wenn Sie das Textfeld bearbeiten möchten.

*VML-Standard Attribut*

**Beispiel**

Die Form hat eine Textfeld-ID mit dem Namen "MyTextBox".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 