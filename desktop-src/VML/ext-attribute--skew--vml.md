---
title: Ext-Attribut (Schiefe)(VML)
description: Ext-Attribut (Schiefe)(VML)
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b0a001812a5504940509fac82333b2ca637ae76a913218f44cd3a06b4c18bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125360"
---
# <a name="ext-attribute-skewvml"></a>Ext-Attribut (Schiefe)(VML)

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert, wie eine Schiefe angezeigt wird. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Neigen](msdn-online-vml-skew-element.md)

**Tagsyntax**

<o: *element* v:ext="-Ausdruck "> 

**Skriptsyntax**

*element* .ext="*expression*"

*expression* = *Element*.ext

**Anmerkungen**

Dieses Attribut wird verwendet, um grafischen Editoren zu zeigen, wie das **Skew-Element zu verarbeiten** ist. Mögliche Werte:

-   **edit**
-   **view** (Standard)
-   **backwardCompatible**

Wenn eine Erweiterung zum Bearbeiten von **festgelegt ist,** kann sie von einem Software-Viewer ignoriert werden. Wenn diese Option auf **view festgelegt** ist, muss der Viewer stattdessen die Bitmapdarstellung rendern.

*Microsoft Office Extensions-Attribut*

 

 