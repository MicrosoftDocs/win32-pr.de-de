---
description: Nachdem Sie eine INF-Datei erstellt haben, schreiben Sie in der Regel den Quellcode für die Setup Anwendung. Sie müssen die Setup Funktionen von der Setup Anwendung aus ausführen, um viele Installations Vorgänge auszuführen.
ms.assetid: 9f444564-d3a4-4b3c-8849-b56cd610356c
title: Erstellen von Setup Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3aaca2b1d509795f625e67c18c13131d7e502b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373156"
---
# <a name="creating-setup-applications"></a>Erstellen von Setup Anwendungen

Nachdem Sie eine INF-Datei erstellt haben, schreiben Sie in der Regel den Quellcode für die Setup Anwendung. Sie müssen die Setup Funktionen von der Setup Anwendung aus ausführen, um viele Installations Vorgänge auszuführen.

In den folgenden Schritten wird eine Möglichkeit behandelt, mit den Setup Funktionen eine Setup Anwendung zu erstellen. Sie können dieses Beispiel als Ausgangspunkt verwenden oder einen eigenen Installations Algorithmus entwickeln.

**Initialisierung**

-   [Öffnen Sie die INF-Datei, und fügen Sie ggf. andere INF-Dateien an.](opening-the-inf-file.md)
-   [Extrahieren Sie Dateiinformationen aus der INF-Datei.](extracting-file-information-from-the-inf-file.md)
-   [Sammeln Sie Setup Informationen vom Benutzer.](gathering-setup-information-from-the-user.md)
-   [Erstellen Sie eine Warteschlange.](creating-a-queue-and-queuing-file-operations.md)

**Dateien installieren**

-   [Commit für die Warteschlange, wobei eine Rückruf Routine angegeben wird.](committing-the-queue.md)
-   [Aktualisieren von Registrierungsinformationen.](updating-registry-information.md)

**Bereinigen**

-   [Schließen Sie die Datei Warteschlange und inf.](closing-the-file-queue-and-inf-file.md)
-   [Geben Sie alle anderen Systemressourcen frei, und beenden Sie das Programm.](releasing-other-system-resources.md)

 

 



