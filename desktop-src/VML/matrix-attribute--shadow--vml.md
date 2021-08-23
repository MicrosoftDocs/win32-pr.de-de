---
title: Matrixattribut (Shadow)(VML)
description: Matrixattribut (Shadow)(VML)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6124005ef3202e11dc8a4e7eeeaacba8e87e9c3a7cb3a1dd1eee55c595e40ecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057928"
---
# <a name="matrix-attribute-shadowvml"></a>Matrixattribut (Shadow)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert eine Perspektiventransformation für einen Schatten. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *element* matrix=" *ausdruck* ">

**Skriptsyntax**

*element* .matrix="*expression*"

*expression* = *Element*.matrix

**Anmerkungen**

Eine perspektivische Transformationsmatrix im Format "sxx,sxy,syx,syy,px,py", wobei s= scale und p = perspective sind. Wenn offset in absoluten Einheiten und dann px ist, liegt py bei 1/emul-Einheiten. andernfalls sind sie ein umgekehrter Bruchteil der Formgröße.

*VML-Standardattribut*

 

 