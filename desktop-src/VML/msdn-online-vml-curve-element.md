---
title: VML Curve-Element
description: VML Curve-Element
ms.assetid: 37197ef0-7597-465a-bc37-7ffcde2e736b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fd06480b0d4bcf062f1f64eb9fa0b22862cf2b338b2c2f5ea0bf1c3cd2a1b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655530"
---
# <a name="vml-curve-element"></a>VML Curve-Element

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Vordefinierte Kurvenform.

**Die Kurve** verwendet die [attribute to](to-attribute--curve--vml.md) [, von](from-attribute--curve--vml.md), [control1](msdn-online-vml-control1-attribute.md)und [control2.](msdn-online-vml-control2-attribute.md)

Der folgende Code ist der Mindestcode, der zum Erstellen eines Bilds erforderlich ist.


```HTML
   <v:curve
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```





 

 