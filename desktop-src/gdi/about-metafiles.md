---
description: Intern ist eine Metadatei ein Array von Strukturen variabler Länge, die als Metadateidatensätze bezeichnet werden.
ms.assetid: 222f9b8b-d759-49f9-a3ea-ac59f85263b8
title: Informationen zu Metadateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc573d54f1f89e2dfe06edb8e225516fe8f0946485592d7d6aaea1faa651de85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779460"
---
# <a name="about-metafiles"></a>Informationen zu Metadateien

Intern ist eine Metadatei ein Array von Strukturen variabler Länge, die als *Metadateidatensätze* bezeichnet werden. Die ersten Datensätze in der Metadatei geben allgemeine Informationen an, z. B. die Auflösung des Geräts, auf dem das Bild erstellt wurde, die Abmessungen des Bilds usw. Die verbleibenden Datensätze, die den Großteil jeder Metadatei bilden, entsprechen den GDI-Funktionen (Graphics Device Interface), die zum Zeichnen des Bilds erforderlich sind. Diese Datensätze werden in der Metadatei gespeichert, nachdem ein spezieller Metafile-Gerätekontext erstellt wurde. Dieser Metadatei-Gerätekontext wird dann für alle Zeichnungsvorgänge verwendet, die zum Erstellen des Bilds erforderlich sind. Wenn das System eine GDI-Funktion verarbeitet, die einem Metadatei-DC zugeordnet ist, konvertiert es die Funktion in die entsprechenden Daten und speichert diese Daten in einem Datensatz, der an die Metadatei angefügt ist.

Nachdem ein Bild abgeschlossen und der letzte Datensatz in der Metadatei gespeichert wurde, können Sie die Metadatei wie folgt an eine andere Anwendung übergeben:

-   Verwenden der Zwischenablage
-   Einbetten in eine andere Datei
-   Speichern auf dem Datenträger
-   Wiederholtes Wiedergeben

Eine Metadatei wird *wiedergegeben,* wenn ihre Datensätze in Gerätebefehle konvertiert und vom entsprechenden Gerät verarbeitet werden.

Es gibt zwei Arten von Metadateien:

-   [Erweiterte Formatmetadateien](enhanced-format-metafiles.md)
-   [Metadateien im Windows-Format](windows-format-metafiles.md)

 

 



