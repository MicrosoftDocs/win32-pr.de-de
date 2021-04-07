---
title: ID-Attribut (Schatten) (VML)
description: ID-Attribut (Schatten) (VML)
ms.assetid: ca20b6b9-a41c-4073-9178-77eb0f918327
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d51a5917f9ef71e3c4acea7ec1ed2e5cf90aef8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728344"
---
# <a name="id-attribute-shadowvml"></a>ID-Attribut (Schatten) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt einen Namen an, der einen eindeutigen Bezeichner für einen Schatten bereitstellt. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *Element* -ID = " *Ausdruck* " >

**Skript Syntax**

*Element* . ID = "*Ausdruck*"

*Ausdruck* = *Element*. ID

**Anmerkungen**

Verwenden Sie **ID** , um auf einen bestimmten Schatten zu verweisen. Nachdem Sie einen Schatten erstellt und ihm eine ID zugewiesen haben, können Sie den ID-Namen verwenden, wenn Sie den Schatten bearbeiten möchten.

*VML-Standard Attribut*

**Beispiel**

Die Form hat eine Schatten-ID namens "MyShadow".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow id="myshadow" on="True"/>
   </v:shape>
```



 

 