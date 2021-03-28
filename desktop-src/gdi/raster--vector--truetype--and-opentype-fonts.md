---
description: Raster-, Vektor-, TrueType-und OpenType-Schriftarten
ms.assetid: 4fe98f04-3fb0-4a03-86c3-d0ea6f07f8f0
title: Raster-, Vektor-, TrueType-und OpenType-Schriftarten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9b4be20ac7d02075fcd5c6cdbefe9eb516ea21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993911"
---
# <a name="raster-vector-truetype-and-opentype-fonts"></a>Raster-, Vektor-, TrueType-und OpenType-Schriftarten

Anwendungen können vier verschiedene Arten von Schriftart Technologien zum Anzeigen und Drucken von Text verwenden:

-   RA
-   Vektor
-   TrueType
-   Microsoft OpenType

Die Unterschiede zwischen diesen Schriftarten spiegeln die Art und Weise wider, *in der das Symbol für jedes* Zeichen oder Symbol in der jeweiligen Schriftart Ressourcen Datei gespeichert wird:

-   In Raster Schriftarten ist ein Symbol eine Bitmap, die das System verwendet, um ein einzelnes Zeichen oder Symbol in der Schriftart zu zeichnen.
-   In Vektor Schriftarten ist ein Symbol eine Auflistung von Zeilen Endpunkten, die die Liniensegmente definieren, die vom System zum Zeichnen eines Zeichens oder Symbols in der Schriftart verwendet werden.
-   In TrueType-und OpenType-Schriftarten ist ein Symbol eine Auflistung von Zeilen-und Kurven Befehlen sowie eine Auflistung von hinweisen.

Das System verwendet die Zeilen-und Kurven Befehle zum Definieren der Gliederung der Bitmap für ein Zeichen oder Symbol in der TrueType-oder Microsoft OpenType-Schriftart. Das System verwendet die Hinweise, um die Länge der Linien und Formen der Kurven anzupassen, die zum Zeichnen des Zeichens oder Symbols verwendet werden. Diese Hinweise und die entsprechenden Anpassungen basieren auf dem Umfang der Skalierung, mit der die Größe der Bitmap reduziert oder vergrößert wird. Eine OpenType-Schriftart ist äquivalent zu einer TrueType-Schriftart, mit dem Unterschied, dass eine OpenType-Schriftart zusätzlich zu TrueType-Glyphe-Definitionen auch PostScript-Symbol Definitionen zulässt.

Da die Bitmaps für jedes Symbol in einer Raster Schriftart für eine bestimmte Geräte Auflösung entworfen wurden, werden Raster Schriftarten in der Regel als Geräte abhängig betrachtet. Vektor Schriftarten hingegen sind nicht Geräte abhängig, da jedes Symbol als eine Auflistung skalierbarer Zeilen gespeichert wird. Vektor Schriftarten werden jedoch im Allgemeinen langsamer gezeichnet als Raster-oder TrueType-und OpenType-Schriftarten. TrueType-und OpenType-Schriftarten bieten sowohl eine relativ schnelle Zeichnungs Geschwindigkeit als auch echte Geräteunabhängigkeit. Mithilfe der mit einem Symbol verknüpften Hinweise kann ein Entwickler die Zeichen aus einer TrueType-oder OpenType-Schriftart nach oben oder unten skalieren und die ursprüngliche Form beibehalten.

Wie bereits erwähnt, werden die Symbole für eine Schriftart in einer Schriftart Ressourcen Datei gespeichert. Eine Schriftart Ressourcen Datei ist tatsächlich eine DLL, die nur Daten enthält, es ist kein Code vorhanden. Für Raster-und Vektor Schriftarten sind diese Daten in zwei Teile unterteilt: ein Header, der die Metriken der Schriftart und die Symbol Daten beschreibt. Eine Schriftart Ressourcen Datei für eine Raster-oder Vektor Schriftart wird durch die Dateinamenerweiterung. FON identifiziert. Für TrueType-und OpenType-Schriftarten gibt es zwei Dateien für jede Schriftart: die erste Datei enthält einen relativ kurzen Header und der zweite die eigentlichen Schriftart Daten. Die erste Datei wird durch die Erweiterung ". fot" identifiziert, die zweite wird durch die Erweiterung ". ttf" identifiziert.

 

 



