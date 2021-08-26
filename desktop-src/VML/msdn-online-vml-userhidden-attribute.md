---
title: VML UserHidden-Attribut
description: VML UserHidden-Attribut
ms.assetid: 0e4616c7-a456-4157-b77a-56cd289e913c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb49b54c2463769286d11877e992bb30d4e431f351e39bf30b0ed6ab748a58e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959230"
---
# <a name="vml-userhidden-attribute"></a>VML UserHidden-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob ein Skriptanker ausgeblendet ist. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *Element* o:userhidden=" *Ausdruck* ">

**Anmerkungen**

Der Standardwert ist **False**. True **gibt an,** dass Skriptanker ausgeblendet bleiben, auch wenn die Form andernfalls sichtbar ist.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Der Skriptanker der Form ist ausgeblendet.


```HTML
   <v:rect id=myrect fillcolor="red" userhidden="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 