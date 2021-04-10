---
title: Matrix Attribut (schiefe) (VML)
description: Matrix Attribut (schiefe) (VML)
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8327acfebfe4d968e673060f2f3cbef69d3e9db6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039514"
---
# <a name="matrix-attribute-skewvml"></a>Matrix Attribut (schiefe) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert eine perspektivische Transformation einer Schiefe. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Neigen](msdn-online-vml-skew-element.md)

**Tagsyntax**

<o: *Element* Matrix = " *Ausdruck* " >

**Skript Syntax**

*Element* . Matrix = "*Ausdruck*"

*Ausdruck* = *Element*. Matrix

**Anmerkungen**

Die Matrix ist eine Zeichenfolge im Format "Sxx, sxy, syx, SYY, px, py", wobei s den Wert "Scale", "p" und "x" und "y" x-und y-Werte darstellen. Wenn [Offset](offset-attribute--skew--vml.md) in absoluten Einheiten ist, befinden sich px und py in den [Einheiten](msdn-online-vml-units.md) "EMU ^-1" (andernfalls handelt es sich um einen umgekehrten Bruchteil der Shape-Größe). Der Standardwert ist "1, 0, 0, 1, 0, 0".

*Microsoft Office Extensions-Attribut*

 

 