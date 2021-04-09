---
title: VML-facetattribut
description: VML-facetattribut
ms.assetid: 6b874d79-a34e-45f7-bbbf-44d652410b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d4fec254ff3e6af35d82cd45146c201701555b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101843"
---
# <a name="vml-facet-attribute"></a>VML-facetattribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Anzahl von Facetten, die zum Beschreiben von Kurven Oberflächen einer-Extrusion verwendet werden. Lese-/Schreibzugriff. **Vgnumber**.

**Gilt für**

[Schläuche](msdn-online-vml-extrusion-element.md)

**Tagsyntax**

<o: *Element* Face= " *Expression* " >

**Skript Syntax**

*Element* . Face= "*Ausdruck*"

*Ausdruck* = *Element*. Facette

**Anmerkungen**

Definiert die Art und Weise, wie sich ein Renderingmodul der Extrusion anweist. Eine niedrigere Zahl gibt eine niedrigere renderingtoleranz für die Rendering-Engine an und führt zu mehr Facetten. Eine höhere Anzahl von Zahlen führt zu einer größeren Darstellung der Extrusion. Der Standardwert ist 30.000.

*Microsoft Office Extensions-Attribut*

 

 