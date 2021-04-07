---
title: VML-Einheiten
description: In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.
ms.assetid: f95e65ad-d92a-460f-baeb-30fd8a35f84e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e59ff91fb134edeba7e653be30141b3f72c6b65
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728240"
---
# <a name="vml-units"></a>VML-Einheiten

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Die folgenden CSS-Einheiten werden von VML verwendet.



Relative Längeneinheiten

Hold

Die Höhe der Schriftart des Elements.

ex

Die Höhe des Buchstabens "x".

px

Pixel.

%

Aler.

Einheiten der absoluten Länge

in

Zoll (1 Zoll = 2,54 Zentimeter).

cm

Länge.

MM

Millimeter.

pt

Punkte (1 Punkt = 1/72 Zoll).

pc

Picas (1 Pica = 12 Punkte).



 

Messungen und Positionen in CSS (Cascading Stylesheet)-Eigenschaften werden mithilfe von Längeneinheiten erstellt. Internet Explorer unterstützt zwei Typen von Längeneinheiten: relative und absolute.

Eine relative Längeneinheit gibt eine Länge in Relation zu einer anderen length-Eigenschaft an. Relative Längeneinheiten werden von einem Ausgabegerät zu einem anderen skaliert, z. b. von einem Monitor bis zu einem Drucker. Prozentsätze und Schlüsselwörter werden entsprechend durchgeführt.

Eine absolute Längeneinheit gibt eine absolute Messung an, z. b. Zoll oder Zentimeter. Einheiten der absoluten Länge sind nützlich, wenn die physischen Eigenschaften des Ausgabegeräts bekannt sind.

## <a name="other-units-of-measurement"></a>Weitere Maßeinheiten

**Emu**

Der Wert für "EMU" (englische metrische Einheit) ist die kleinste nützliche Maßeinheit und wird von VML für den internen Einheiten Speicher verwendet. Es gibt 914400 Emu pro Zoll und 12700 Emu an einem Punkt. Emus kann nicht in Sekundenbruchteilen angegeben werden.

Da Emus durch 32-Bit-ganzzahlige Zahlen mit Vorzeichen definiert werden, liegt die größte Anzahl von Emus bei 2348 Zoll (ca. 59 Meter oder 65 Meter). Da die Messungen immer in einen Bildschirm-oder seitenbasierten Ausgabegerät passen, liegen Sie immer innerhalb dieses Bereichs.

**Winkel**

Winkelmessungen können mit den folgenden Suffixen definiert werden.



Suffix

FD

Bruchteile.

none

Grad

deg

Grad

rad

Radians



 

 

 