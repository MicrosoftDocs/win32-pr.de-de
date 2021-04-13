---
title: Verwenden des Download-Managers
description: Verwenden des Download-Managers
ms.assetid: f332a981-727f-4abc-a84e-76ab3e72b7f2
keywords:
- Windows Media Player Online Stores, Download-Manager
- Online Stores, Download-Manager
- Typ 2 Online Stores, Download-Manager
- Windows Media Player, Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecb7b99ae36d3881fdf80eaad7d851205b9b2e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388760"
---
# <a name="using-the-download-manager"></a>Verwenden des Download-Managers

Das Windows Media Player SDK enthält eine Beispiel Webseite, die die Verwendung des Download-Managers zum Herunterladen von Dateien auf den Computer des Benutzers veranschaulicht. Sie finden das Beispiel im Ordner mit dem Namen "Webseite", in dem Sie das SDK installiert haben. Der Name der Datei lautet Sample. ASP. Das Beispiel bietet die folgenden Funktionen:

-   Erstellt das **Download Manager** -Objekt.
-   Erstellt ein **downloadcollection** -Objekt.
-   Startet fünf Dateien herunter, wenn der Benutzer auf **herunterladen** klickt. Im Beispiel werden Standarddatei Pfade bereitgestellt. Sie sollten diese Standard Pfade durch die Speicherorte von Dateien auf dem eigenen Server ersetzen. Sie können die Pfade ändern, indem Sie die Werte ändern, die dem globalen Array mit dem Namen g \_ sfiles zugewiesen sind.
-   Zeigt Statusinformationen für einen Download an, wenn der Benutzer Sie auswählt.
-   Stellt Steuerelemente zum Anhalten, fortsetzen, Abbrechen und Entfernen eines Download Elements bereit.
-   Verwaltet Informationen zum Herunterladen von Sammlungen zwischen Sitzungen mithilfe von Cookies. Dies ist wichtig, da der Benutzer den Player jederzeit schließen kann. Außerdem wird die Online Store-Sitzung beendet, wenn der Benutzer Aufgabenbereiche im Player wechselt.
-   Verwendet standardmäßig das Herunterladen in Echtzeit. Sie können das Verhalten in das Herunterladen im Hintergrund ändern, indem Sie den Wert der Variablen mit dem Namen g \_ SdlType ändern. Das Herunterladen im Hintergrund ist für die Verwendung mit dem Betriebssystem Microsoft Windows XP verfügbar.
-   Synchronisiert die Hintergrundfarbe mit der Farbe des Players. Sie können diese Funktion verwenden, um die Darstellung des Online Stores zu ändern, wenn sich der Benutzer entscheidet, die Farbe des Players zu ändern.

In den folgenden Abschnitten finden Sie weitere Informationen:

-   [Die Seite wird initialisiert.](initializing-the-page.md)
-   [Starten der Downloads](starting-the-downloads.md)
-   [Abrufen von Status Informationen](retrieving-status-information.md)
-   [Verwalten von Sitzungsinformationen](maintaining-session-information.md)
-   [Debuggen der Seite](debugging-the-page.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmier Handbuch für den Typ 2-Online Speicher**](programming-guide-for-type-2-online-stores.md)
</dt> </dl>

 

 




