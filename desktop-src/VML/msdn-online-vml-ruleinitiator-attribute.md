---
title: VML RuleInitiator-Attribut
description: VML RuleInitiator-Attribut
ms.assetid: 2c9b1131-b088-4b70-b132-bdb4296433ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b015ba3742eda42fd506d955bbc8d2b9d7285999581897952dede665c9eb3361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654960"
---
# <a name="vml-ruleinitiator-attribute"></a>VML RuleInitiator-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob eine Regel-Engine verwendet wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* o:ruleinitiator=" *Ausdruck* ">

**Anmerkungen**

Der Standardwert ist **False**. Wenn der Wert True **ist,** wird eine Regel-Engine verwendet.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Die Form wird von einer Regel-Engine verarbeitet.


```HTML
   <v:rect id=myrect fillcolor="red" rulesinitiator="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 