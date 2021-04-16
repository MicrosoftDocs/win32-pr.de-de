---
title: Title-Attribut (Form) (VML)
description: Title-Attribut (Form) (VML)
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075b1cf078617abd3486ba55008794e1342efa63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474156"
---
# <a name="title-attribute-shapevml"></a>Title-Attribut (Form) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert den Text, der angezeigt wird, wenn der Mauszeiger über der Form bewegt wird. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Title = " *Ausdruck* " >

**Skript Syntax**

*Element* . Title = "*Ausdruck*"

*Ausdruck* = *Element*. Title

**Anmerkungen**

Das **Title** -Attribut ähnelt dem Standard-HTML- **Titel** Attribut. Das Verhalten eines Titels ähnelt einer Microsoft Windows-QuickInfo.

**VML-Standard Attribut**

**Beispiel**

Der Titel der Form ist "QuickInfo Display" und wird angezeigt, wenn der Mauszeiger über der Form bewegt wird.


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Beispiel für das Titel Attribut](/previous-versions/bb264097(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 