---
title: VML preferrelative-Attribut
description: VML preferrelative-Attribut
ms.assetid: 7de616e8-4fc3-4bcb-8e5e-ea153d6d4b54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa425321c1937c4df1bb766c554dbd73cc384b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039084"
---
# <a name="vml-preferrelative-attribute"></a>VML preferrelative-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob die ursprüngliche Größe eines Objekts nach der Neuformatierung gespeichert wird. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* o:preferrelative = " *Expression* " >

**Anmerkungen**

Der Standardwert ist **False**. Wenn der Wert **true** ist, wird die ursprüngliche Größe des Objekts gespeichert, und die Größenänderung basiert auf einem Prozentsatz der ursprünglichen Größe. Andernfalls wird die Skalierung durch jede Größenänderung auf 100% zurückgesetzt.

*Microsoft Office Extensions-Attribut*

**Beispiel**

Wenn die Größe der Form geändert wird, wird die ursprüngliche Größe nicht gespeichert.


```HTML
   <v:rect id=myrect fillcolor="red" preferrelative="False"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 