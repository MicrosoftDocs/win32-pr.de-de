---
title: Vorteile strukturierter Storage
description: COM stellt eine Reihe von Diensten zur Verfügung, die zusammen als strukturierter Speicher bezeichnet werden.
ms.assetid: d05d2dbc-d1d2-4ef8-a773-5337e2746da3
keywords:
- Structured Storage Strctd Stg , Vorteile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a52159f37b3bf443419beaadbcf9f76aa9c5d7209e04b25506eea850c4d3d98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663562"
---
# <a name="benefits-of-structured-storage"></a>Vorteile strukturierter Storage

COM stellt eine Reihe von Diensten zur Verfügung, die zusammen als strukturierter Speicher bezeichnet werden. Zu den Vorteilen dieser Dienste zählen die Verringerung von Leistungsproblemen und mehr Aufwand im Zusammenhang mit dem Speichern separater Objekte in einer Flatdatei. Anstelle einer Flatdatei speichert COM die separaten Objekte in einer einzelnen, strukturierten Datei, die aus zwei Hauptelementen besteht: Speicherobjekte und Streamobjekte. Zusammen funktionieren sie wie ein Dateisystem innerhalb einer Datei.

Strukturierter Speicher löst Leistungsprobleme, indem es nicht mehr erforderlich ist, eine Datei vollständig in den Speicher umschreiben zu müssen, wenn einer Verbunddatei ein neues Objekt hinzugefügt wird oder ein vorhandenes Objekt an Größe zunimmt. Die neuen Daten werden an den nächsten verfügbaren Speicherort im permanenten Speicher geschrieben, und das Speicherobjekt aktualisiert die Tabelle mit Zeigern, die es verwaltet, um die Speicherorte seiner Speicherobjekte und Streamobjekte nachverfolgung. Gleichzeitig ermöglicht der strukturierte Speicher Endbenutzern die Interaktion und Verwaltung einer Verbunddatei, als ob es sich um eine einzelne Datei und nicht um eine geschachtelte Hierarchie separater Objekte würde.

Strukturierter Speicher hat auch andere Vorteile:

-   **Inkrementeller Zugriff.** Wenn ein Benutzer Zugriff auf ein Objekt in einer Verbunddatei benötigt, kann der Benutzer anstelle der gesamten Datei nur dieses Objekt laden und speichern.
-   **Verwenden Sie mehrfach**. Mehrere Endbenutzer oder Anwendungen können Informationen gleichzeitig in derselben Verbunddatei lesen und schreiben.
-   **Transaktionsverarbeitung.** Benutzer können COM-Verbunddateien im transaktiven Modus lesen oder in diese schreiben, wobei an der Datei vorgenommene Änderungen gepuffert werden und anschließend entweder in die Datei ausgeführt oder umgekehrt werden können.
-   **Mit wenig Arbeitsspeicher wird gespeichert.** Strukturierter Speicher bietet Möglichkeiten zum Speichern von Dateien in Situationen mit wenig Arbeitsspeicher.

 

 




