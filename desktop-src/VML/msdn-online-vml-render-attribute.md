---
title: VML-Renderattribut
description: VML-Renderattribut
ms.assetid: a05e7f6e-4784-4ff8-9deb-0501d3a5658e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17063d1e742a5b014e18d61d2d4290eb2511843ef24f1513bd3564ee83c5e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513340"
---
# <a name="vml-render-attribute"></a>VML-Renderattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Renderingmodus derExtrusion. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Tagsyntax**

<o: *element* render=" *expression* ">

**Skriptsyntax**

*element* .render="*expression*"

*expression* = *Element*.render

**Anmerkungen**

Mögliche Werte:



| Wert        | Beschreibung                                                   |
|--------------|---------------------------------------------------------------|
| Solide        | Beim Rendern wird eine Vollform angezeigt. Standard.                    |
| Drahtmodell    | Beim Rendern wird eine Wireframe-Form angezeigt.                         |
| boundingcube | Beim Rendern wird der umgebundene Cube angezeigt, der die Form enthält. |



 

*Microsoft Office Extensions-Attribut*

 

 