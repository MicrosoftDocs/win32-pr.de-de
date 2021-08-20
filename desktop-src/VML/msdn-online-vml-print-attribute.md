---
title: VML-Druckattribut
description: VML-Druckattribut
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfa364e573d887da2013f946ddf23e0a974e0f63211623de3d2046b0525b2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057728"
---
# <a name="vml-print-attribute"></a>VML-Druckattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob die Form gedruckt wird. Lese-/Schreibzugriff. [VgTriState](msdn-online-vml-vgtristate.md).

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* print=" *ausdruck* ">

**Skriptsyntax**

*element* .print="*expression*"

*expression* = *.print-Element*

**Anmerkungen**

Wird als Möglichkeit bereitgestellt, anzugeben, ob Formen gedruckt werden. Beachten Sie, dass eine Form weiterhin auf dem Bildschirm angezeigt werden kann, auch wenn sie nicht gedruckt wird, weil dieses Attribut **false** ist. Der Standardwert ist **True**.

Dieses Attribut wird von Microsoft Office verwendet, aber nicht von Microsoft Internet Explorer.

*Microsoft Office Extensions-Attribut*

 

 