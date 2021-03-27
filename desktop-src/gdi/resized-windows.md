---
description: Das System ändert die Größe eines Fensters, wenn der Benutzermenü Befehle im Menü (z. b. Größe und Maximierung) auswählt, oder wenn die Anwendung Funktionen aufruft, wie z. b. die SetWindowPos-Funktion.
ms.assetid: 6f997cba-e4c9-4e27-8309-42b9892ec620
title: Fenstergröße geändert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f740191f8b85038f17a687ebc547305f882383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863627"
---
# <a name="resized-windows"></a>Fenstergröße geändert

Das System ändert die Größe eines Fensters, wenn der Benutzermenü Befehle im Menü (z. b. Größe und Maximierung) auswählt, oder wenn die Anwendung Funktionen aufruft, wie z. b. die [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) -Funktion. Wenn die Größe eines Fensters geändert wird, geht das System davon aus, dass der Inhalt des zuvor verfügbar gemachten Teils des Fensters nicht beeinträchtigt wird und nicht neu gezeichnet werden muss. Das System macht nur den neu verfügbar gemachten Teil des Fensters ungültig, was Zeit spart, wenn die [**endgültige \_ WM**](wm-paint.md) -Zeichnungs Nachricht von der Anwendung verarbeitet wird. In diesem Fall wird **WM \_ Paint** nicht generiert, wenn die Größe des Fensters reduziert wird.

Bei einigen Fenstern wird der Inhalt durch jede Änderung der Fenstergröße ungültig. Beispielsweise muss eine Clock-Anwendung, die das Gesicht der Uhr anpasst, damit Sie in das Fenster passt, die Uhr neu zeichnen, wenn die Größe des Fensters geändert wird. Um zu erzwingen, dass das System den gesamten Client Bereich des Fensters für ungültig erklärt, wenn eine vertikale, horizontale oder vertikale und horizontale Änderung vorgenommen wird, muss eine Anwendung \_ beim Registrieren der Fenster Klasse die CS-Klasse "vredraw" oder "CS \_ hredraw" oder beides angeben. Jedes Fenster, das zu einer Fenster Klasse gehört, in der diese Stile vorhanden sind, wird jedes Mal ungültig, wenn der Benutzer oder die Anwendung die Größe des Fensters ändert.

 

 
