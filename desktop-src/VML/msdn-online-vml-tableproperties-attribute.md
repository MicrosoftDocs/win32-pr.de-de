---
title: VML TableProperties-Attribut
description: VML TableProperties-Attribut
ms.assetid: 10355742-13b9-4c08-bff7-f7f7501762e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0f010f673b2663764814150f7a38fc06f23e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338664"
---
# <a name="vml-tableproperties-attribute"></a>VML TableProperties-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt Tabellen Eigenschaften. Lese-/Schreibzugriff. **Integer**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* o:TableProperties = " *Expression* " >

**Anmerkungen**

Wird von Microsoft PowerPoint für Native Tabellen verwendet. Der Standardwert ist 0. Nur die ersten drei Bits dieser Ganzzahl werden verwendet.

Obwohl der Wert in einer Form gespeichert ist, ist das-Attribut nur nützlich, wenn die Tabelle aus Formen besteht, die gruppiert sind. Bits können kombiniert werden.

Die folgenden Bitwerte sind enthalten.



| bit | BESCHREIBUNG                              |
|-----|------------------------------------------|
| 1   | Legen Sie fest, wenn die Gruppe von Formen eine Tabelle ist.   |
| 2   | Legen Sie fest, wenn die Form ein Platzhalter ist.       |
| 3   | Legen Sie fest, ob der Tabellen Text bidirektional ist. |



 

*Microsoft Office Extensions-Attribut*

 

 