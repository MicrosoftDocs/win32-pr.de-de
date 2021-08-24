---
title: VML-Zeichenfolgenattribut
description: VML-Zeichenfolgenattribut
ms.assetid: 99609814-29c9-4349-9509-8c91f2aaeff5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0428c6742b145b77afe5dce27017ffcdc04d1b021cfc7ce570c9db93dd218021
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654750"
---
# <a name="vml-string-attribute"></a>VML-Zeichenfolgenattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert den Text des Textpfads. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Textpath](msdn-online-vml-textpath-element.md)

**Tagsyntax**

<v: *element* string=" *ausdruck* ">

**Skriptsyntax**

*element* .string="*expression*"

*expression* = *.string-Element*

**Anmerkungen**

Sie müssen eine Textzeichenfolge zuweisen, um Text in einem Textpfad anzuzeigen.

VML-Standardattribut

**Beispiel**

Die angezeigte Zeichenfolge lautet "VML-Text".


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 