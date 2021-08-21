---
title: VML TableLimits-Attribut
description: VML TableLimits-Attribut
ms.assetid: eef855de-23c5-4894-b7cf-2ea39e372e08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af52ba570b04e56f1dede169045f7ee1addf374fae5ca4f1cd5de4d9390f1235
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959250"
---
# <a name="vml-tablelimits-attribute"></a>VML TableLimits-Attribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Liste der Mindesthöhenwerte für jede Zeile in einer Tabelle. Lese-/Schreibzugriff. **VgLengthArray**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *element* o:tablelimits=" *ausdruck* ">

**Anmerkungen**

Wird von Microsoft PowerPoint für native Tabellen verwendet. Der Standardwert ist **NULL.**

Obwohl der Wert in einer Form gespeichert ist, ist das Attribut nur nützlich, wenn die Tabelle aus gruppierten Formen besteht. Wenn Tabellenzellen Text hinzugefügt wird, kann sich die Zeilenhöhe erhöhen. Das **TableLimits-Attribut** speichert die ursprüngliche Zeilenhöhe, sodass die Zeilenhöhe nicht unter den ursprünglichen Wert fällt, wenn Text gelöscht wird.

*Microsoft Office Extensions-Attribut*

 

 