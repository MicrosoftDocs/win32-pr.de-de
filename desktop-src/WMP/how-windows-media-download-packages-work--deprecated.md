---
title: Funktionsweise Windows Mediendownloadpakete (veraltet)
description: Funktionsweise Windows Mediendownloadpakete (veraltet)
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Windows Medienmetadateien,Windows Mediendownloadpakete
- Windows Media Player,Windows Mediendownloadpakete
- Metadateien, Windows Mediendownloadpakete
- Windows Medien Windows Mediendownloadpakete
- Windows Mediendownloadpakete, Informationen
- Windows Mediendownloadpakete,Funktionsweise von Paketen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8b1af3cd89ec5d9b232872747d53504a2ad07ddc15e740dc19fc4cb37e9322ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338970"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a>Funktionsweise Windows Mediendownloadpakete (veraltet)

Auf dieser Seite wird ein Feature dokumentiert, das in zukünftigen Versionen von Windows Media Player und dem Windows Media Player SDK möglicherweise nicht verfügbar ist.

Ein Windows Mediendownloadpaket wird von einer Website aus gestartet, wenn ein Benutzer in einem Webbrowser auf einen Link klickt, z. B. microsoft Internet Explorer. Diese Aktion öffnet Windows Media Player und lädt dann das Paket Windows Mediendownloads auf die Festplatte des Benutzers in einem Standardordner herunter und entpackt es.

Nachdem die Dateien aus dem Windows Mediendownloadpaket extrahiert wurden, sucht Windows Media Player eine Windows Media-Metadateiwiedergabeliste mit der Dateinamenerweiterung ASX unter den gepackten Dateien. Wenn eine gefunden wird, erstellt der Player eine Wiedergabeliste basierend auf der enthaltenen Metadatei. Dateien, die Multimediainhalte enthalten, werden dann der Bibliothek hinzugefügt.

Windows Media Player sucht auch in  der Metadatei nach einem SKIN-Element. Wenn das **SKIN-Element** einen Verweis auf eine Rahmendatei mit der Dateinamenerweiterung .wmz enthält, lädt der Player den Rahmen in den Bereich **Jetzt wiedergegeben.** Der Player beginnt dann mit der Wiedergabe des im Paket bereitgestellten Inhalts.

Das folgende Diagramm zeigt, wie Inhalte in einer Windows Mediendownloaddatei gepackt, auf einer Website bereitgestellt, heruntergeladen und mithilfe von Windows Media Player auf einem Clientcomputer wiedergegeben werden.

![wie eine Windows-Mediendownloaddatei abgerufen und wiedergegeben wird.](images/wmd-image.png) Windows Mediendownload

In der folgenden Tabelle werden die drei Elemente beschrieben, die ein Windows Mediendownloadpaket bilden.



| Package-Element    | Funktion                                                                                                                                                                                                                                        | Dateinamenerweiterungen                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Rahmen             | Eine feste, angepasste Benutzeroberfläche, die vom Inhaltsbesitzer zum Anzeigen, Verknüpfen und Wiedergeben aller Medien erstellt wurde, die im Windows Mediendownloadpaket gepackt sind. Die Verfahren zum Erstellen von Rahmen ähneln denen, die zum Erstellen von Skins verwendet werden. | .wmz                                     |
| Metafile-Wiedergabeliste  | Eine Windows Media-Metadatei, die **ENTRY-Elemente,** Wiedergabelisteninformationen und eine **SKIN-Elementidentität** für Inhaltsdateien enthält.                                                                                                             | .asx                                     |
| Multimediainhalte | Eine Datei mit einem beliebigen Audio- oder Videoformat, das von Windows Media Player unterstützt wird.                                                                                                                                                          | .wma, .wmv, .asf, .wav, .avi, .mpg, .mp3 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Windows Mediendownloadpakete (veraltet)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




