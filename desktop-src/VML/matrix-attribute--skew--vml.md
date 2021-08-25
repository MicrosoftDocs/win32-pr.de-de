---
title: Matrixattribut (Schiefe)(VML)
description: Matrixattribut (Schiefe)(VML)
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d7fd3989807951f06df963c6899a2c81ce6e7faaa76432172e4391a4ce11029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768449"
---
# <a name="matrix-attribute-skewvml"></a>Matrixattribut (Schiefe)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert eine Perspektivtransformation einer Schiefe. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Neigen](msdn-online-vml-skew-element.md)

**Tagsyntax**

<o: *element* matrix="-Ausdruck "> 

**Skriptsyntax**

*element* .matrix="*expression*"

*expression* = *Element*.matrix

**Anmerkungen**

Die Matrix ist eine Zeichenfolge im Format "sxx, sxy, syx, syy, px, py", wobei s für scale, p für perspective und x und y für x- und y-Werte steht. Wenn [Offset](offset-attribute--skew--vml.md) in absoluten Einheiten angegeben ist, befinden sich px und py in emu^-1-Einheiten (andernfalls sind sie ein umgekehrter Bruchteil der Formgröße). [](msdn-online-vml-units.md) Der Standardwert ist "1,0,0,1,0,0".

*Microsoft Office Extensions-Attribut*

 

 