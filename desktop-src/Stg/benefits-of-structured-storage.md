---
title: Vorteile von strukturiertem Speicher
description: COM stellt eine Reihe von Diensten bereit, die kollektiv als strukturierte Speicherung bezeichnet werden.
ms.assetid: d05d2dbc-d1d2-4ef8-a773-5337e2746da3
keywords:
- Strukturierter Speicherplatz Halter, Vorteile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68b954fda33e18f654ccc0360f58ddb14e5d110
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708208"
---
# <a name="benefits-of-structured-storage"></a>Vorteile von strukturiertem Speicher

COM stellt eine Reihe von Diensten bereit, die kollektiv als strukturierte Speicherung bezeichnet werden. Zu den Vorteilen dieser Dienste gehört die Verringerung der Leistungseinbußen und des Aufwands, die mit dem Speichern von separaten Objekten in einer Flatfile verbunden sind. Anstelle einer Flatfile speichert com die separaten Objekte in einer einzelnen, strukturierten Datei, die aus zwei Hauptelementen besteht: Speicher Objekte und Streamobjekte. In der gleichen Weise funktionieren Sie wie ein Dateisystem in einer Datei.

Durch die strukturierte Speicherung werden Leistungsprobleme gelöst, da eine Datei nicht vollständig in den Speicher geschrieben werden muss, wenn einer Verbund Datei ein neues Objekt hinzugefügt wird oder ein vorhandenes Objekt vergrößert wird. Die neuen Daten werden an den nächsten verfügbaren Speicherort im permanenten Speicher geschrieben, und das Speicher Objekt aktualisiert die Tabelle mit den Zeigern, die Sie verwaltet, um die Speicherorte der Speicher Objekte und Streamobjekte zu verfolgen. Gleichzeitig ermöglicht die strukturierte Speicherung es Endbenutzern, eine Verbund Datei zu interagieren und zu verwalten, als ob es sich um eine einzelne Datei und nicht um eine geschachtelte Hierarchy von separaten Objekten handelt.

Die strukturierte Speicherung bietet auch andere Vorteile:

-   **Inkrementeller Zugriff** Wenn ein Benutzer Zugriff auf ein Objekt innerhalb einer Verbund Datei benötigt, kann der Benutzer nur dieses Objekt laden und speichern, und nicht die gesamte Datei.
-   **Mehrfache Verwendung**. Mehr als ein Endbenutzer oder eine Anwendung kann gleichzeitig Informationen in derselben Verbund Datei lesen und schreiben.
-   **Transaktionsverarbeitung**. Benutzer können com-Verbund Dateien im transaktiven Modus lesen oder schreiben, in dem die an der Datei vorgenommenen Änderungen gepuffert werden und anschließend entweder ein Commit in die Datei erfolgen oder umgekehrt werden kann.
-   Speicherungen mit **geringem Arbeitsspeicher**. Strukturierter Speicher bietet Funktionen zum Speichern von Dateien in Situationen mit geringem Arbeitsspeicher.

 

 




