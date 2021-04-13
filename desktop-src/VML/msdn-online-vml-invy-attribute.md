---
title: VML-Attribut "invy"
description: VML-Attribut "invy"
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a728d804d771f79b892ee6616cca527dba42bfa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315536"
---
# <a name="vml-invy-attribute"></a>VML-Attribut "invy"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob die y-Position des Handles invertiert ist. Lese-/Schreibzugriff. **Vgder State**.

**Gilt für**

[H](msdn-online-vml-h-element.md) (Unterelement von [Handles](msdn-online-vml-handles-element.md))

**Tagsyntax**

<v: *Element* invy = " *Expression* " >

**Anmerkungen**

**True** gibt an, dass die y-Position des Handles invertiert wird, indem der y-Wert vom y-Wert von **coordorigin** subtrahieren wird, der dem y-Wert von **coordsize** hinzugefügt wird. Der Standardwert ist **False**.

Dieses Attribut entspricht


```HTML
coordorigin.y + coordsize.y - h.position.y
```



*VML-Standard Attribut*

 

 