---
title: VML RuleProxy-Attribut
description: VML RuleProxy-Attribut
ms.assetid: 040e80f8-65b6-491d-812d-421800801374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fe97afee190d87b5e6f8b74d942a72d3bf11914373931e32cbb9459915b7d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099130"
---
# <a name="vml-ruleproxy-attribute"></a>VML RuleProxy-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob ein Proxy für die Regel-Engine verwendet wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* ruleproxy=" *ausdruck* ">

**Anmerkungen**

Der Standardwert ist **False**. **True** gibt an, dass ein Proxy verwendet wird.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Ein Proxy wird verwendet, um die Form zu verarbeiten.


```HTML
   <v:rect id=myrect fillcolor="red" ruleproxy="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 