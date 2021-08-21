---
title: Verwenden des Download-Managers
description: Verwenden des Download-Managers
ms.assetid: f332a981-727f-4abc-a84e-76ab3e72b7f2
keywords:
- Windows Media Player Onlineshops, Download-Manager
- Onlineshops, Download-Manager
- Geben Sie 2 Onlineshops ein,Download-Manager
- Windows Media Player,Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a271849e22d17ec406cea24aa0afb92631bf533b39ea2beb45d5cc74b635d0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830708"
---
# <a name="using-the-download-manager"></a>Verwenden des Download-Managers

Das Windows Media Player SDK enthält eine Beispielwebseite, die die Verwendung des Download-Managers zum Herunterladen von Dateien auf den Computer des Benutzers veranschaulicht. Sie finden das Beispiel im Ordner WebPage, in dem Sie das SDK installiert haben. Der Name der Datei lautet sample.asp. Das Beispiel bietet die folgenden Funktionen:

-   Erstellt das **DownloadManager-Objekt.**
-   Erstellt ein **DownloadCollection-Objekt.**
-   Beginnt mit dem Herunterladen von fünf Dateien, wenn der Benutzer auf **Herunterladen** klickt. Standarddateipfade werden im Beispiel bereitgestellt. Ersetzen Sie diese Standardpfade durch die Speicherorte von Dateien auf Ihrem eigenen Server. Sie können die Pfade ändern, indem Sie die Werte ändern, die dem globalen Array g \_ sFiles zugewiesen sind.
-   Zeigt Statusinformationen für einen Download an, wenn der Benutzer ihn auswählt.
-   Stellt Steuerelemente zum Anhalten, Fortsetzen, Abbrechen und Entfernen eines Downloadelements bereit.
-   Verwaltet Informationen zum Herunterladen von Sammlungen zwischen Sitzungen mithilfe von Cookies. Dies ist wichtig, da der Benutzer den Player jederzeit schließen kann. Wenn der Benutzer die Aufgabenbereiche im Player wechselt, wird die Sitzung des Onlineshops beendet.
-   Verwendet standardmäßig Das Herunterladen in Echtzeit. Sie können das Verhalten beim Herunterladen im Hintergrund ändern, indem Sie den Wert der Variablen g \_ sDLType ändern. Hintergrunddownloads sind für die Verwendung mit dem Betriebssystem Microsoft Windows XP verfügbar.
-   Synchronisiert die Hintergrundfarbe mit der Player-Farbe. Sie können dieses Feature verwenden, um die Darstellung Ihres Onlineshops zu ändern, wenn der Benutzer die Farbe des Players ändert.

Die folgenden Abschnitte enthalten weitere Informationen:

-   [Initialisieren der Seite](initializing-the-page.md)
-   [Starten der Downloads](starting-the-downloads.md)
-   [Abrufen von Statusinformationen](retrieving-status-information.md)
-   [Verwalten von Sitzungsinformationen](maintaining-session-information.md)
-   [Debuggen der Seite](debugging-the-page.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch für Onlineshops vom Typ 2**](programming-guide-for-type-2-online-stores.md)
</dt> </dl>

 

 




