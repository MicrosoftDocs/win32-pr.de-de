---
title: VML-Clip-Attribut
description: VML-Clip-Attribut
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2702355ea93d8e87d173ee4c23406b12557dce4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339891"
---
# <a name="vml-clip-attribute"></a>VML-Clip-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob das Clipping auf ON festgelegt ist. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Vmlframe](msdn-online-vml-vmlframe-element.md)

**Tagsyntax**

<v: *Element* Clip = " *Expression* " >

**Skript Syntax**

*Element* . Clip = "*Ausdruck*"

*Ausdruck* = *Element*. Clip

**Anmerkungen**

Wenn **Clip** **false** ist, wird die Form so skaliert, dass Sie dem Frame entspricht. **True** gibt an, dass Teile der Form, die sich außerhalb des Rahmens befinden, nicht angezeigt werden.

Beachten Sie, dass [Origin](origin-attribute--vmlframe--vml.md) und [size](size-attribute--vmlframe.md) nicht verwendet werden, es sei denn, **Clip** ist **true**.

*VML-Standard Attribut*

**Beispiel**

Das in der externen Datei definierte Bild wird abgeschnitten.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 