---
title: Ext-Attribut (schiefe) (VML)
description: Ext-Attribut (schiefe) (VML)
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153273f613d188ae9e6fe733b2d0337c5010295d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209280"
---
# <a name="ext-attribute-skewvml"></a>Ext-Attribut (schiefe) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert die Art und Weise, wie eine schiefe angezeigt wird. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Neigen](msdn-online-vml-skew-element.md)

**Tagsyntax**

<o: *Element* v:ext = " *Ausdruck* " >

**Skript Syntax**

*Element* . ext = "*Ausdruck*"

*Ausdruck* = *Element*. ext

**Anmerkungen**

Dieses Attribut wird verwendet, um grafischen Editoren mitzuteilen, wie das **schiefe** -Element verarbeitet werden soll. Mögliche Werte:

-   **edit**
-   **anzeigen** (Standard)
-   **backwardkompatibel**

Wenn eine Erweiterung auf **Bearbeiten** festgelegt ist, kann Sie von einem Software Viewer ignoriert werden. Wenn Sie auf **View** festgelegt ist, muss der Viewer stattdessen die Bitmap-Darstellung Rendering.

*Microsoft Office Extensions-Attribut*

 

 