---
title: VML-bwmode-Attribut
description: VML-bwmode-Attribut
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f595159398e32fdb1c80ad5d949ef48758aea95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728296"
---
# <a name="vml-bwmode-attribute"></a>VML-bwmode-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, wie eine Form für schwarze und weiße Ausgabegeräte dargestellt wird. Lese-/Schreibzugriff. [Vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md).

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* o:bwmode = " *Ausdruck* " >

**Anmerkungen**

Wenn eine Form auf einem schwarzen und weißen Drucker gedruckt oder in einer schwarzen und weißen Ansicht in einer Anwendung angezeigt wird, sind mehrere Optionen möglich. Weitere Informationen zu den Werten dieses Attributs finden Sie im Thema [vgblackwhitemode](msdn-online-vml-vgblackwhitemode.md) . Der Standardwert ist " **Auto**".

Wenn **Auto** angegeben ist, wird [bwnormal](msdn-online-vml-bwnormal-attribute.md) verwendet, um das Verhalten für die normale schwarz-und weiße Ausgabe zu bestimmen, und [bwpure](msdn-online-vml-bwpure-attribute.md) wird verwendet, um das Verhalten für die reine schwarz-und weiße Ausgabe zu bestimmen.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Der schwarze und weiße Modus der Form ist " **Auto**".


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 