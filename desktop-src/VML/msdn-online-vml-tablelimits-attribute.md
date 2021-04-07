---
title: VML-tablelimits-Attribut
description: VML-tablelimits-Attribut
ms.assetid: eef855de-23c5-4894-b7cf-2ea39e372e08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b35a7449cc2f348e6040161c1fb599c29972803
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727577"
---
# <a name="vml-tablelimits-attribute"></a>VML-tablelimits-Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Liste der minimalen Höhenwerte für jede Zeile in einer Tabelle. Lese-/Schreibzugriff. **Vglengtharray**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* o:tablelimits = " *Ausdruck* " >

**Anmerkungen**

Wird von Microsoft PowerPoint für Native Tabellen verwendet. Der Standardwert ist **null**.

Obwohl der Wert in einer Form gespeichert ist, ist das-Attribut nur nützlich, wenn die Tabelle aus Formen besteht, die gruppiert sind. Wenn den Tabellenzellen Text hinzugefügt wird, kann sich die Zeilenhöhe erhöhen. Das **tablelimits** -Attribut speichert die ursprüngliche Zeilenhöhe, sodass die Zeilenhöhe, wenn der Text gelöscht wird, nicht unter den ursprünglichen Wert fällt.

*Microsoft Office Extensions-Attribut*

 

 