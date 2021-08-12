---
title: VML TableProperties-Attribut
description: VML TableProperties-Attribut
ms.assetid: 10355742-13b9-4c08-bff7-f7f7501762e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050e290bc4b779fec40ebf3ad3fb202b34af23b10f70a0070038c56f5f8ea2c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597546"
---
# <a name="vml-tableproperties-attribute"></a>VML TableProperties-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt Tabelleneigenschaften. Lese-/Schreibzugriff. **Integer**.

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* o:tableproperties=" *ausdruck* ">

**Anmerkungen**

Wird von Microsoft PowerPoint für native Tabellen verwendet. Der Standardwert ist 0. Nur die ersten drei Bits dieser ganzen Zahl werden verwendet.

Obwohl der Wert in einer Form gespeichert wird, ist das Attribut nur nützlich, wenn die Tabelle aus gruppierten Formen besteht. Bits können kombiniert werden.

Die folgenden Bitwerte sind enthalten.



| bit | BESCHREIBUNG                              |
|-----|------------------------------------------|
| 1   | Legen Sie fest, ob die Gruppe von Formen eine Tabelle ist.   |
| 2   | Legen Sie fest, ob die Form ein Platzhalter ist.       |
| 3   | Legen Sie fest, ob der Tabellentext bidirektional ist. |



 

*Microsoft Office Extensions-Attribut*

 

 