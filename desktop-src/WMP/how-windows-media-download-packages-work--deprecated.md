---
title: Funktionsweise von Windows Media-Download Paketen (veraltet)
description: Funktionsweise von Windows Media-Download Paketen (veraltet)
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Windows Media-Metadatendateien, Windows-Medien Download Pakete
- Windows Media Player, Windows Media-Download Pakete
- Metafiles, Windows Media Download Packages
- Windows Media, Windows Media Download Packages
- Windows Media Download Packages, Informationen zu
- Windows Media Download Packages, Funktionsweise von Paketen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1db477791bb93cd599dcef38a90b230c6cd7ddde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100679"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a>Funktionsweise von Windows Media-Download Paketen (veraltet)

Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows Media Player und dem Windows Media Player SDK möglicherweise nicht verfügbar ist.

Ein Windows Media-Download Paket wird von einer Website gestartet, wenn ein Benutzer auf einen Link in einem Webbrowser klickt (z. b. Microsoft Internet Explorer). Mit dieser Aktion wird Windows Media Player geöffnet. Anschließend wird das Windows Media-Download Paket auf der Festplatte des Benutzers in einem Standardordner heruntergeladen und entpackt.

Nachdem die Dateien aus dem Windows Media-Download Paket extrahiert wurden, wird in Windows Media Player eine Windows Media-Metadatendatei mit der Dateinamenerweiterung ". asx" unter den gepackten Dateien gesucht. Wenn ein solcher gefunden wird, erstellt der Spieler eine Wiedergabeliste basierend auf der enthaltenen Metadatendatei. Dateien, die Multimedia-Inhalte enthalten, werden dann der Bibliothek hinzugefügt.

Windows Media Player sucht auch nach einem **Skin** -Element in der Metadatei. Wenn das **Skin** -Element einen Verweis auf eine Rahmen Datei mit der Dateinamenerweiterung ". WMZ" enthält, lädt der Spieler den Rahmen in den Bereich " **jetzt Wiedergabe** ". Der Player startet dann den Inhalt, der im Paket bereitgestellt wird.

Das folgende Diagramm zeigt, wie Inhalte in einer Windows Media-Download Datei verpackt, auf einer Website veröffentlicht, heruntergeladen und auf einem Client Computer mit Windows Media Player abgespielt werden.

![wie eine Windows Media-Downloaddatei abgerufen und wiedergegeben wird.](images/wmd-image.png) Windows Media-Download

In der folgenden Tabelle werden die drei Elemente beschrieben, aus denen ein Windows Media-Download Paket besteht.



| Package-Element    | Funktion                                                                                                                                                                                                                                        | Dateinamen Erweiterungen                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Rahmen             | Eine benutzerdefinierte, angepasste Benutzeroberfläche, die vom Besitzer des Inhalts zum Anzeigen, verknüpfen und Abspielen aller Medien, die im Windows Media-Download Paket verpackt sind, erstellt wurde. Die Verfahren zum Erstellen von Rahmen ähneln denen, die zum Erstellen von Skins verwendet werden. | .wmz                                     |
| Metafile-Wiedergabeliste  | Eine Windows Media-Metadatendatei, die **Eintrags** Elemente, Wiedergabelisten Informationen und eine **Skin** -Element Identität für Inhalts Dateien enthält.                                                                                                             | .asx                                     |
| Multimedia-Inhalte | Eine Datei, die ein beliebiges Audio-oder Videoformat enthält, das von Windows Media Player unterstützt wird.                                                                                                                                                          | . WMA,. WMV,. ASF,. wav,. AVI,. mpg,. MP3 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Windows Media-Download Pakete (veraltet)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




