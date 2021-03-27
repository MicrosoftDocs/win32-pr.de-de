---
description: Intern handelt es sich bei einer Metadatei um ein Array von Strukturen variabler Länge namens Metadatei-Datensätze.
ms.assetid: 222f9b8b-d759-49f9-a3ea-ac59f85263b8
title: Informationen zu Metadateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdba8b3c0a13c6c5799563b05e189829a0734427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753593"
---
# <a name="about-metafiles"></a>Informationen zu Metadateien

Intern handelt es sich bei einer Metadatei um ein Array von Strukturen variabler Länge namens *Metadatei-Datensätze*. Die ersten Datensätze in der Metadatei geben allgemeine Informationen an, z. b. die Auflösung des Geräts, auf dem das Bild erstellt wurde, die Abmessungen des Bilds usw. Die übrigen Datensätze, die den Großteil der Metadateien bilden, entsprechen den GDI-Funktionen (Graphics Device Interface), die zum Zeichnen des Bilds erforderlich sind. Diese Datensätze werden in der Metadatendatei gespeichert, nachdem ein spezieller Metadatei-Gerätekontext erstellt wurde. Dieser Metadatei-Gerätekontext wird dann für alle Zeichnungsvorgänge verwendet, die zum Erstellen des Bilds erforderlich sind. Wenn das System eine GDI-Funktion verarbeitet, die einem metadateidc zugeordnet ist, wird die Funktion in die entsprechenden Daten konvertiert, und diese Daten werden in einem Datensatz gespeichert, der an die Metadatendatei angehängt ist.

Nachdem ein Bild abgeschlossen und der letzte Datensatz in der Metadatei gespeichert wurde, können Sie die Metadatendatei an eine andere Anwendung übergeben, indem Sie Folgendes ausführen:

-   Verwenden der Zwischenablage
-   Einbetten in eine andere Datei
-   Speichern auf einem Datenträger
-   Wiederholte Wiedergabe

Eine Metadatei wird wieder *gegeben* , wenn die zugehörigen Datensätze in Geräte Befehle konvertiert und vom entsprechenden Gerät verarbeitet werden.

Es gibt zwei Arten von Metadateien:

-   [Metadateien mit erweitertem Format](enhanced-format-metafiles.md)
-   [Metadateien im Windows-Format](windows-format-metafiles.md)

 

 



