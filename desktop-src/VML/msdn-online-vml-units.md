---
title: VML-Einheiten
description: In diesem Artikel werden VML-Einheiten beschrieben. VML ist ein Feature, das ab Windows Internet Explorer 9 veraltet ist.
ms.assetid: f95e65ad-d92a-460f-baeb-30fd8a35f84e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184d577052412bde4a97148b51cab12a87b3672e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406943"
---
# <a name="vml-units"></a>VML-Einheiten

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Die folgenden CSS-Einheiten werden von VML verwendet.



Relative Längeneinheiten

Em

Die Höhe der Schriftart des Elements.

ex

Die Höhe des Buchstabens "x".

px

Pixel.

%

Prozentsatz.

Absolute Längeneinheiten

in

Zoll (1 Zoll = 2,54 Cm).

cm

Zentimeter.

mm

Millimeter.

pt

Punkte (1 Punkt = 1/72 Zoll ).

pc

Picas (1 Pica = 12 Punkte ).



 

Messungen und Positionen in CSS-Eigenschaften (Cascading Stylesheet) werden mithilfe von Längeneinheiten durchgeführt. Internet Explorer unterstützt zwei Typen von Längeneinheiten: relativ und absolut.

Eine relative Längeneinheit gibt eine Länge im Verhältnis zu einer anderen Length-Eigenschaft an. Einheiten mit relativer Länge werden von einem Ausgabegerät auf ein anderes besser skaliert, z. B. von einem Monitor zu einem Drucker. Prozentsätze und Schlüsselwörter haben eine ähnliche Leistung.

Eine Einheit mit absoluter Länge gibt eine absolute Messung an, z. B. Zoll oder Zentimeter. Absolute Längeneinheiten sind nützlich, wenn die physischen Eigenschaften des Ausgabegeräts bekannt sind.

## <a name="other-units-of-measurement"></a>Andere Maßeinheiten

**Wwu**

Die emu (englische Metrikeinheit) ist die kleinste nützliche Maßeinheit und wird von VML für den internen Einheitenspeicher verwendet. Es gibt 914400 EMU pro Zoll und 12.700 EMU an einem Punkt. EMUs dürfen nicht als Bruchteile verwendet werden.

Da EMUs durch 32-Bit-Ganzzahl mit Vorzeichen definiert werden, beträgt die größte Anzahl von EMUs 2348 Zoll (ca. 59 Meter oder 65 Meter). Da die Messungen immer auf ein Ausgabegerät im Bildschirm- oder Seitenformat passen, liegen sie immer innerhalb dieses Bereichs.

**Winkel**

Winkelmessungen können mit den folgenden Suffixen definiert werden.



Suffix

Fd

Fractional Degrees.

Keine

Grad

deg

Grad

rad

Radians



 

 

 