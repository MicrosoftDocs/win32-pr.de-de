---
title: Matrix Attribut (Schatten) (VML)
description: Matrix Attribut (Schatten) (VML)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d599aa817e87481aefdec43dbe345b7235fc54bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390923"
---
# <a name="matrix-attribute-shadowvml"></a>Matrix Attribut (Schatten) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert eine perspektivische Transformation für einen Schatten. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Shadow](msdn-online-vml-shadow-element.md)

**Tagsyntax**

<v: *Element* Matrix = " *Ausdruck* " >

**Skript Syntax**

*Element* . Matrix = "*Ausdruck*"

*Ausdruck* = *Element*. Matrix

**Anmerkungen**

Eine perspektivische Transformationsmatrix in der Form "Sxx, sxy, syx, SYY, px, py", wobei s = Scale und p = Perspective ist. Wenn der Offset in absoluten Einheiten liegt, sind px und py in 1/Emu-Einheiten. andernfalls handelt es sich um einen umgekehrten Bruchteil der Shape-Größe.

*VML-Standard Attribut*

 

 