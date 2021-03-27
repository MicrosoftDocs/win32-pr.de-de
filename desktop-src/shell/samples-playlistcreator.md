---
description: Veranschaulicht, wie ein Verb erstellt wird, das für ein ausgewähltes shellelement oder einen ausgewählten Container zum Erstellen einer Wiedergabeliste funktioniert.
title: Wiedergabelistenersteller (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B35B7A18-2163-4860-BC50-8918056C9F4A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c5e4f6570faff459126a32ea4680d41a3b8302e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980921"
---
# <a name="playlist-creator-sample"></a>Wiedergabelistenersteller (Beispiel)

Veranschaulicht, wie ein Verb erstellt wird, das für ein ausgewähltes shellelement oder einen ausgewählten Container zum Erstellen einer Wiedergabeliste funktioniert.

Dieses Thema enthält folgende Abschnitte:

-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)

## <a name="requirements"></a>Requirements (Anforderungen)



| Produkt                                | Minimale Produkt Version |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Playlistcreator-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlaylistCreator) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel von der Eingabeaufforderung aus:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **playlistcreator** .
2.  Geben Sie `msbuild PlaylistCreator.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

> [!Note]  
> Dieses Beispiel kann auch mit der Visual C++ Express Edition verwendet werden, wenn das vollständige Visual Studio nicht verfügbar ist.

 

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **playlistcreator** .
2.  Doppelklicken Sie auf das Symbol für die Datei playlistcreator. sln, um das Projekt in Visual Studio zu öffnen.
3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.
    > [!Note]  
    > Wenn Sie 64-Bit mithilfe der Visual C++ Express Edition kompilieren, müssen Sie den für die Windows SDK bereitgestellten x64-Cross-Compiler verwenden.

     

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2.  Geben Sie in der Befehlszeile ein `PlaylistCreator.exe` . Alternativ können Sie in Windows-Explorer auf das Symbol für PlaylistCreator.exe doppelklicken.
3.  Klicken Sie mit der rechten Maustaste auf eine beliebige Musikdatei oder einen Ordner mit Musikdateien im Windows-Explorer, um eine Wiedergabeliste für das Kontextmenü zu erstellen.
4.  Sie können eine. M3U-oder WPL-Wiedergabeliste erstellen. Wiedergabelisten werden im `%userprofile%\Music\Playlists` Ordner erstellt.
    > [!Note]  
    > Neue Verben im Kontextmenü finden Sie im Ordner " **Musik** ", Musik Stapel, Stapeln in der **Musikbibliothek** und Sammlungen von Musikdateien.

     

 

 



