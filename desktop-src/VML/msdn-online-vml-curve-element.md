---
title: VML-Kurven Element
description: VML-Kurven Element
ms.assetid: 37197ef0-7597-465a-bc37-7ffcde2e736b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b9e04086652bf9dde7d7e7f5ebdea0992f774c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209262"
---
# <a name="vml-curve-element"></a>VML-Kurven Element

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Vordefinierte Kurvenform.

Die **Kurve** verwendet die Attribute [to](to-attribute--curve--vml.md), [from](from-attribute--curve--vml.md), [Control1](msdn-online-vml-control1-attribute.md)und [Control2](msdn-online-vml-control2-attribute.md) .

Im folgenden finden Sie den minimalen Code, der zum Entwickeln eines Bilds erforderlich ist.


```HTML
   <v:curve
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```





 

 