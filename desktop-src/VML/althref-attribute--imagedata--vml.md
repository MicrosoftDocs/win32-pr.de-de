---
title: Althref-Attribut (imagedata) (VML)
description: Althref-Attribut (imagedata) (VML)
ms.assetid: c55ede90-3d57-4f27-9940-1fe4751cef71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004625d769c12e67de024bf537ee04c377a18c8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039176"
---
# <a name="althref-attribute-imagedatavml"></a>Althref-Attribut (imagedata) (VML)

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt einen alternativen Verweis für ein Bild an. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[ImageData](msdn-online-vml-imagedata-element.md)

**Tagsyntax**

<v: *Element* o:althref = " *Ausdruck* " >

**Skript Syntax**

*Element* . althref = "*Ausdruck*"

*Ausdruck* = *Element*. althref

**Anmerkungen**

Unterstützt die Beibehaltung von Daten mithilfe von HTML-Roundtripping. Beim HTML-Schreibvorgang wird die alternative Darstellung (d. h. die ursprünglichen Daten, wenn die Datei vom Macintosh stammt) gespeichert. Bei einem HTML-Lesevorgang wird **althref** gegenüber **src** bevorzugt.

*Microsoft Office Extensions-Attribut*

 

 