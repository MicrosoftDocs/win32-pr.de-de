---
title: Die Seite wird initialisiert.
description: Die Seite wird initialisiert.
ms.assetid: 66bd3810-01a3-4413-9dad-12cf71e72ed1
keywords:
- Windows Media Player Online Stores, Download-Manager
- Online Stores, Download-Manager
- Typ 2 Online Stores, Download-Manager
- Windows Media Player Online Stores, Initialisieren von Seiten
- Online Stores, Initialisieren von Seiten
- Typ 2 Online Stores, Initialisieren von Seiten
- Windows Media Player, Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
- Initialisieren von Seiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1570d1b77abdc99ba2aee613ed8ddb88fc8097c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207061"
---
# <a name="initializing-the-page"></a>Die Seite wird initialisiert.

Wenn die Webseite geladen wird, wird die **Init** -Funktion ausgeführt. Mit diesem Code werden zuerst alle in einer vorherigen Sitzung gespeicherten Daten abgerufen. Weitere Informationen finden Sie unter Verwalten von [Sitzungsinformationen](maintaining-session-information.md). Anschließend wird das **Download Manager** -Objekt erstellt und in der globalen Variablen "g \_ omanager" gespeichert.


```C++
g_oManager = external.DownloadManager;

```



Als nächstes verbindet die-Funktion das **oncolorchange** -Ereignis mit der-Funktion mit dem Namen " **onappcolor** " und ruft dann die Funktion direkt auf, um die Hintergrundfarbe zu initialisieren. Weitere Informationen finden Sie [unter Übereinstimmung der Windows Media Player Farben](matching-the-windows-media-player-colors.md).

Schließlich startet die Funktion einen Timer mit einem Intervall von einer Sekunde und initialisiert die Listenfelder, in denen die ausstehenden Download Sammlungen und Download Elemente angezeigt werden. Dies ist wichtig, da während der letzten Schließung des Online Ladens Sitzungen ausgeführt wurden. diese Informationen müssen erneut angezeigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Download-Managers**](using-the-download-manager.md)
</dt> </dl>

 

 




