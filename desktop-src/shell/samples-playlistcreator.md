---
description: Veranschaulicht, wie ein Verb erstellt wird, das für ein ausgewähltes Shellelement oder einen ausgewählten Container verwendet wird, um eine Wiedergabeliste zu erstellen.
title: Wiedergabelistenersteller (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B35B7A18-2163-4860-BC50-8918056C9F4A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 086cb0f3fbb4cb009cd156013ce3ea16a2a7dee3b2346824d51b79094c06c45e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592890"
---
# <a name="playlist-creator-sample"></a>Wiedergabelistenersteller (Beispiel)

Veranschaulicht, wie ein Verb erstellt wird, das für ein ausgewähltes Shellelement oder einen ausgewählten Container verwendet wird, um eine Wiedergabeliste zu erstellen.

Dieses Thema enthält folgende Abschnitte:

-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)

## <a name="requirements"></a>Anforderungen



| Produkt                                | Mindestproduktversion |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [PlaylistCreator-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlaylistCreator) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über die Eingabeaufforderung:

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum **Projektverzeichnis PlaylistCreator.**
2.  Geben Sie `msbuild PlaylistCreator.sln` ein.

So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt):

> [!Note]  
> Dieses Beispiel kann auch mit der Visual C++ Express Edition verwendet werden, wenn die vollständige Visual Studio nicht verfügbar ist.

 

1.  Öffnen Windows Explorer, und navigieren Sie zum **Projektverzeichnis PlaylistCreator.**
2.  Doppelklicken Sie auf das Symbol für die Datei PlaylistCreator.sln, um das Projekt in der Visual Studio.
3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).
    > [!Note]  
    > Wenn Sie 64-Bit mit der Visual C++ Express Edition kompilieren, müssen Sie den x64-Kreuzcompiler verwenden, der mit dem Windows SDK bereitgestellt wird.

     

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie über die Eingabeaufforderung oder den Explorer zu dem Verzeichnis, das die neue ausführbare Windows enthält.
2.  Geben Sie in der Befehlszeile `PlaylistCreator.exe` ein. Doppelklicken Sie alternativ Windows Explorer auf das Symbol für PlaylistCreator.exe.
3.  Klicken Sie mit der rechten Maustaste auf eine Musikdatei oder einen Ordner, die Musikdateien im Windows-Explorer enthält, um eine Wiedergabeliste zum Öffnen des Kontextmenüs zu erstellen.
4.  Sie können eine M3U- oder WPL-Wiedergabeliste erstellen. Wiedergabelisten werden im Ordner `%userprofile%\Music\Playlists` erstellt.
    > [!Note]  
    > Neue Verben im Kontextmenü finden Sie im Ordner **Musik,** musikstapeln, Stapeln in der **Musik Library** und Sammlungen von Musikdateien.

     

 

 



