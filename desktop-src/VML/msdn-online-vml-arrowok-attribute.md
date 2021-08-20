---
title: VML-PfeilOK-Attribut
description: VML-PfeilOK-Attribut
ms.assetid: 19b23544-4a72-4273-b48a-6aee39addcf6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac95b8fa7068f55246263e6622527a8ecec17d3351c284a0810cd77b085784aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124969"
---
# <a name="vml-arrowok-attribute"></a>VML-PfeilOK-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob Pfeilspitzen angezeigt werden. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Path](msdn-online-vml-path-element.md)

**Tagsyntax**

<v: *element* arrowok="-Ausdruck "> 

**Skriptsyntax**

*element* .arrowok="*expression*"

*expression* = *Element*.arrowok

**Anmerkungen**

False **gibt an,** dass der Pfad keine Pfeilspitzen hat. Der Standardwert ist **False**. Dieses Attribut überschreibt alle anderen Pfeilspitzenattribute im übergeordneten element oder **Stroke-Element.**

*VML-Standardattribut*

**Beispiel**

Der Pfad hat keine Pfeilspitze.


```HTML
   <v:line id="whatsmyline"
   style="position:relative"
   from="114pt,66pt" to="402pt,66pt"
   strokecolor="black">
   <v:stroke startarrow="block" endarrow="block"/>
   <v:path arrowok="False"/>
   </v:line>
```



 

 