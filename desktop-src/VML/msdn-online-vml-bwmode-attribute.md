---
title: VML BWMode-Attribut
description: VML BWMode-Attribut
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5640680af40f4649f7ab34b2ec8cfd4e5cf94ee4c7c6ce3c3f2185e68bdac360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754965"
---
# <a name="vml-bwmode-attribute"></a>VML BWMode-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, wie eine Form für Schwarz-Weiß-Ausgabegeräte gerendert wird. Lese-/Schreibzugriff. [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* o:bwmode=" *ausdruck* ">

**Anmerkungen**

Wenn eine Form auf einem Schwarz-Weiß-Drucker gedruckt oder in einer Schwarz-Weiß-Ansicht in einer Anwendung angezeigt wird, sind mehrere Optionen möglich. Weitere Informationen zu den Werten dieses Attributs finden Sie im Thema [VgBlackWhiteMode.](msdn-online-vml-vgblackwhitemode.md) Der Standardwert ist **auto.**

Wenn **auto** angegeben wird, wird [BWNormal](msdn-online-vml-bwnormal-attribute.md) verwendet, um das Verhalten für die normale Schwarz-Weiß-Ausgabe zu bestimmen, und [BWPure](msdn-online-vml-bwpure-attribute.md) wird verwendet, um das Verhalten für reine Schwarz-Weiß-Ausgaben zu bestimmen.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Der Schwarz-Weiß-Modus der Form ist **auto.**


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 