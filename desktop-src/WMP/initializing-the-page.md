---
title: Initialisieren der Seite
description: Initialisieren der Seite
ms.assetid: 66bd3810-01a3-4413-9dad-12cf71e72ed1
keywords:
- Windows Media Player Onlineshops, Download-Manager
- Onlineshops, Download-Manager
- Geben Sie 2 Onlineshops ein,Download-Manager
- Windows Media Player Onlineshops, Initialisieren von Seiten
- Onlineshops, Initialisieren von Seiten
- Geben Sie 2 Onlineshops ein, initialisieren Sie Seiten.
- Windows Media Player,Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
- Initialisieren von Seiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e929038c45e5f85a640b5c4ce5c86be56957fdb9067624feddf381ab5093623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748165"
---
# <a name="initializing-the-page"></a>Initialisieren der Seite

Wenn die Webseite geladen wird, wird die **Init-Funktion** ausgeführt. Dieser Code ruft zunächst alle Daten ab, die in einer vorherigen Sitzung gespeichert wurden. Weitere Informationen finden Sie unter [Verwalten von Sitzungsinformationen.](maintaining-session-information.md) Anschließend wird das **DownloadManager-Objekt** erstellt und in der globalen Variablen g \_ oManager gespeichert.


```C++
g_oManager = external.DownloadManager;

```



Als Nächstes verbindet die Funktion das **OnColorChange-Ereignis** mit der Funktion namens **OnAppColor** und ruft dann die Funktion direkt auf, um die Hintergrundfarbe zu initialisieren. Weitere Informationen finden Sie [unter Matching the Windows Media Player Colors (Abgleichen der Windows Media Player Farben).](matching-the-windows-media-player-colors.md)

Schließlich startet die Funktion einen Timer mit einem Intervall von einer Sekunde und initialisiert die Listenfelder, in denen die ausstehenden Downloadsammlungen und Downloadelemente angezeigt werden. Dies ist wichtig, da beim letzten Schließen des Onlineshops möglicherweise Sitzungen ausgeführt wurden und diese Informationen erneut angezeigt werden müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden des Download-Managers**](using-the-download-manager.md)
</dt> </dl>

 

 




