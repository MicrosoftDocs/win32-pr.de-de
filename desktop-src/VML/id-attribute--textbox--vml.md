---
title: ID-Attribut (TextBox)(VML)
description: ID-Attribut (TextBox)(VML)
ms.assetid: b9eb75cc-4d0a-4e83-a897-e35995ae7c53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a3a7e88c847cf63a1362d43cb6acaf21a548b141b71ffd2724c779f8eebac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099290"
---
# <a name="id-attribute-textboxvml"></a>ID-Attribut (TextBox)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Ein Name, der einen eindeutigen Bezeichner für ein Textfeld enthält. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[TextBox](msdn-online-vml-textbox-element.md)

**Tagsyntax**

<v: *element* id=" *ausdruck* ">

**Skriptsyntax**

*element* .id="*expression*"

*expression* = *Element*.id

**Anmerkungen**

Verwenden **Sie ID,** um auf ein bestimmtes Textfeld zu verweisen. Nachdem Sie ein Textfeld erstellt und ihm eine ID gegeben haben, können Sie den ID-Namen verwenden, wenn Sie das Textfeld bearbeiten möchten.

*VML-Standardattribut*

**Beispiel**

Die Form verfügt über eine Textfeld-ID namens "mytextbox".


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



 

 