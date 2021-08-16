---
description: Nachdem Sie eine INF-Datei erstellt haben, schreiben Sie in der Regel den Quellcode für Ihre Setupanwendung. Sie rufen die Setupfunktionen aus Ihrer Setupanwendung auf, um viele Installationsvorgänge auszuführen.
ms.assetid: 9f444564-d3a4-4b3c-8849-b56cd610356c
title: Erstellen von Setupanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e77f920a024a4414690baad7684af90a30ee4ca3c9f96a2c6f61b1b84430c072
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887437"
---
# <a name="creating-setup-applications"></a>Erstellen von Setupanwendungen

Nachdem Sie eine INF-Datei erstellt haben, schreiben Sie in der Regel den Quellcode für Ihre Setupanwendung. Sie rufen die Setupfunktionen aus Ihrer Setupanwendung auf, um viele Installationsvorgänge auszuführen.

In den folgenden Schritten wird eine Möglichkeit beschrieben, die Setupfunktionen zum Erstellen einer Setupanwendung zu verwenden. Sie können dieses Beispiel als Ausgangspunkt verwenden oder Einen eigenen Installationsalgorithmus entwickeln.

**Initialisierung**

-   [Öffnen Sie die INF, und fügen Sie ggf. andere INF-Dateien an.](opening-the-inf-file.md)
-   [Extrahieren Sie Dateiinformationen aus der INF-Datei.](extracting-file-information-from-the-inf-file.md)
-   [Sammeln Sie Setupinformationen vom Benutzer.](gathering-setup-information-from-the-user.md)
-   [Erstellen Sie eine Warteschlange.](creating-a-queue-and-queuing-file-operations.md)

**Installieren von Dateien**

-   [Committen Sie die Warteschlange, und geben Sie eine Rückrufroutine an.](committing-the-queue.md)
-   [Aktualisieren Sie die Registrierungsinformationen.](updating-registry-information.md)

**Bereinigen**

-   [Schließen Sie die Dateiwarteschlange und inf.](closing-the-file-queue-and-inf-file.md)
-   [Geben Sie alle anderen Systemressourcen frei, und beenden Sie das Programm.](releasing-other-system-resources.md)

 

 



