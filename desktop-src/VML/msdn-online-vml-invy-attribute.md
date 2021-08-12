---
title: VML-InvY-Attribut
description: VML-InvY-Attribut
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d012e8ac6afe0e7808236c36d8dd3088ce9fa3552b4b7efa0542ea8612e4d36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599868"
---
# <a name="vml-invy-attribute"></a>VML-InvY-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob die y-Position des Handles invertiert wird. Lese-/Schreibzugriff. **VgTriState**.

**Gilt für**

[H](msdn-online-vml-h-element.md) (Unterelement von [Handles](msdn-online-vml-handles-element.md))

**Tagsyntax**

<v: *element* invy=" *ausdruck* ">

**Anmerkungen**

**True** gibt an, dass die y-Position des Handles umgekehrt wird, indem der y-Wert vom y-Wert von **CoordOrigin** subtrahiert wird, der dem y-Wert von **CoordSize** hinzugefügt wurde. Der Standardwert ist **False**.

Dieses Attribut entspricht


```HTML
coordorigin.y + coordsize.y - h.position.y
```



*VML-Standardattribut*

 

 