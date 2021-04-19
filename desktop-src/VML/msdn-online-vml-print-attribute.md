---
title: VML-Druck Attribut
description: VML-Druck Attribut
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55925621ab56f011c998f3feac21a892a4d7ea66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341306"
---
# <a name="vml-print-attribute"></a>VML-Druck Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob die Form gedruckt wird. Lese-/Schreibzugriff. [Vgder State](msdn-online-vml-vgtristate.md).

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Print = " *Expression* " >

**Skript Syntax**

*Element* . Print = "*Ausdruck*"

*Ausdruck* = *Element*. Print

**Anmerkungen**

Wird als Möglichkeit bereitgestellt, anzugeben, ob Formen gedruckt werden. Beachten Sie, dass eine Form weiterhin auf dem Bildschirm angezeigt werden kann, auch wenn Sie nicht als Ergebnis dieses Attributs gedruckt wird, das **false** ist. Der Standardwert ist **True**.

Dieses Attribut wird von Microsoft Office verwendet, wird aber nicht von Microsoft Internet Explorer verwendet.

*Microsoft Office Extensions-Attribut*

 

 