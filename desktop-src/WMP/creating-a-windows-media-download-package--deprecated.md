---
title: Erstellen eines Windows Media-Download Pakets (veraltet)
description: Erstellen eines Windows Media-Download Pakets (veraltet)
ms.assetid: 95d6a214-9da6-496d-ba40-4476814b1d5a
keywords:
- Windows Media-Metadatendateien, Windows-Medien Download Pakete
- Windows Media Player, Windows Media-Download Pakete
- Metafiles, Windows Media Download Packages
- Windows Media, Windows Media Download Packages
- Windows Media-Download Pakete, erstellen
- Erstellen von Windows Media-Download Paketen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a8716e1783f0e00cb561c3aba1d15a2c3e5b147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037168"
---
# <a name="creating-a-windows-media-download-package-deprecated"></a>Erstellen eines Windows Media-Download Pakets (veraltet)

Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows Media Player und dem Windows Media Player SDK möglicherweise nicht verfügbar ist.

Führen Sie diese Schritte aus, um ein Windows Media-Download Paket zu erstellen.

1.  **Erstellen Sie einen Rahmen.** Verwenden Sie dieselben Techniken, die Sie zum Erstellen eines Skin für Windows-Media Player verwenden. Entwerfen Sie den Rahmen so, dass das Ändern der Größe von Windows-Media Player nicht die Komposition der Border-Elemente ruiniert. Verwenden Sie beispielsweise eine voll Tonfarbe oder Visualisierung als Hintergrund, da diese bei der Größenänderung von Windows Media Player gut skaliert werden.
2.  **Komprimieren Sie den Rahmen Inhalt.** Erstellen Sie einen komprimierten Ordner (mit der Dateinamenerweiterung ". zip"), der die Border-Dateien enthält: Bilder, JScript-Dateien und die Skin-Definitionsdatei mit der Dateinamenerweiterung ". WMS". Benennen Sie die komprimierte Datei so um, dass Sie die Dateinamenerweiterung. WMZ enthält.
3.  **Schreiben Sie eine Windows Media-Metadatendatei.** Windows Media Player lädt den Rahmen nur dann, wenn Sie eine Windows Media-Metadatendatei mit der Dateinamenerweiterung ". asx" erstellen, die das **Skin** -Element implementiert. Die Metadatei kann auch verwendet werden, um eine Wiedergabeliste zu erstellen, die den im Paket enthaltenen Inhalt beschreibt.
4.  **Assemblieren Sie Ihre Inhalte.** Legen Sie alle Dateien, die Sie verwenden möchten, in einem Ordner ab. Dies schließt Audiodateien, Videodateien, Metadateien und Rahmen Definitions Dateien ein.
5.  **Erstellen Sie das Paket.** Erstellen Sie einen komprimierten Ordner (mit der Dateinamenerweiterung ". zip"), der die Rand Datei, Inhalts Dateien und die Metadatendatei enthält. Ändern Sie die Dateinamenerweiterung dieser zip-Datei in die Dateinamenerweiterung. WMD.
6.  **Veröffentlichen Sie das Paket auf einer Website.** Das fertige Paket ist bereit für die Bereitstellung auf einer Website und von Benutzern heruntergeladen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Windows Media-Download Pakete (veraltet)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




