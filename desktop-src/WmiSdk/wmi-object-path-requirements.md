---
description: WMI verwendet Objekt Pfade in den Verweis Eigenschaften von Zuordnungs Klassen, um verknüpfte Objekte zu identifizieren, sowie die Verwendung von Objekt Pfaden in Eingabe-oder Ausgabeparametern für mehrere Methoden.
ms.assetid: 07fee6f8-810e-4dec-8f0f-787756ee3beb
ms.tgt_platform: multiple
title: WMI-Objekt Pfad Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b46195eae3e8351c9c611a34c28cc9d5dd58d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393569"
---
# <a name="wmi-object-path-requirements"></a>WMI-Objekt Pfad Anforderungen

WMI verwendet Objekt Pfade in den Verweis Eigenschaften von Zuordnungs Klassen, um verknüpfte Objekte zu identifizieren, sowie die Verwendung von Objekt Pfaden in Eingabe-oder Ausgabeparametern für mehrere Methoden. Da Objekt Pfade als Zeichen folgen für die Suche und den Vergleich behandelt werden, ist der Wert eines Objekt Pfads, wenn er als Verweis Eigenschaft verwendet wird, immer die Zeichenfolge selbst und nicht das Dereferenzierte Objekt. Bei Zeichen folgen vergleichen, bei denen Objekt Pfade behandelt werden, wird die Groß-/Kleinschreibung

Ein Objekt Pfad kann die folgende Syntax verwenden:

-   In einfache Anführungszeichen enthaltene Zeichen folgen.
-   Schrägstriche als Trennzeichen.
-   Umgekehrte Schrägstriche als Trennzeichen.
-   Hexadezimale Konstanten für ganze Zahlen.
-   Boolesche Konstanten für Klassen mit Schlüsseln, die boolesche Werte annehmen.
-   URL-Notation zur Darstellung nicht druckbarer Zeichen, z. b. %20 für einen leeren Bereich.

Außerdem muss eine Objekt Pfad Zeichenfolge die folgenden Einschränkungen einhalten:

-   Ein von einem angenommenen lokalen Server mit einem partiellen Namespace Pfad. Daher impliziert die Angabe des Stamm-und des Standard Namespace den Stamm-und den Standard Namespace auf dem lokalen Server.
-   Kein Leerraum innerhalb eines Elements oder zwischen Elementen.
-   Eingebettete Anführungszeichen in Objekt Pfaden sind zulässig, müssen jedoch das Anführungszeichen mit Escapezeichen begrenzen, wie in einer C-oder C++-Anwendung.
-   Nur Dezimalwerte werden als numerische Teile von Schlüsseln erkannt.

 

 



