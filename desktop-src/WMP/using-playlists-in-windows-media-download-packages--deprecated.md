---
title: Verwenden von Wiedergabelisten in Windows-Medien Download Paketen (veraltet)
description: Verwenden von Wiedergabelisten in Windows-Medien Download Paketen (veraltet)
ms.assetid: c40efe24-aaed-47fc-8a8a-f412dfc36af7
keywords:
- Windows Media-Metadatendateien, Windows-Medien Download Pakete
- Windows Media Player, Windows Media-Download Pakete
- Metafiles, Windows Media Download Packages
- Windows Media, Windows Media Download Packages
- Wiedergabelisten, Windows-Medien Download Pakete
- Metadatei-Wiedergabelisten, Windows-Medien Download Pakete
- Windows Media Metadatei-Wiedergabelisten, Windows Media-Download Pakete
- Windows Media Download Packages, Wiedergabelisten
- Windows Media-Download Pakete, metadateiwiedergabe Listen
- Windows Media-Download Pakete, Windows Media Metadatei-Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00c4daa26d18294c00aad7b4926a017d2f3f6343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388567"
---
# <a name="using-playlists-in-windows-media-download-packages-deprecated"></a>Verwenden von Wiedergabelisten in Windows-Medien Download Paketen (veraltet)

Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows Media Player und dem Windows Media Player SDK möglicherweise nicht verfügbar ist.

Wiedergabelisten sind Windows Media-Metadateien mit der Dateinamenerweiterung ". asx", die Informationen bereitstellen, die Windows Media Player, wie der gepackte Inhalt wiedergegeben wird. Durch die Kombination mehrerer Inhalts Dateien zu einem einzelnen Windows Media Download-Paket können Sie das Windows Media-Downloadpaket mithilfe der Wiedergabeliste Steuern und anpassen.

> [!Note]  
> Im Allgemeinen werden Metadatendatei-Wiedergabelisten von Windows Media-Download Paketen verwendet, um auf die Multimedia-Inhalte im Paket und nicht auf einen Stream von einem Server in einem Intranet oder im Internet zu verweisen. Allerdings werden URL-Verweise innerhalb der. ASX-Datei unterstützt.

 

Mithilfe von XML stellt die Metadatei die Informationen bereit, die von Windows Media Player zum wiedergeben und Anzeigen von Inhalten verwendet werden. Wiedergabelisten bestehen aus verschiedenen XML-Code Elementen mit ihren zugeordneten Tags und Attributen. Jedes Element in einer Windows Media Metadatei-Wiedergabeliste definiert eine bestimmte Einstellung oder Aktion in Windows Media Player.

Auf dem Computer des Benutzers wird eine Windows Media-Metadatendatei mit der Dateinamenerweiterung ". asx" mit Windows Media Player verknüpft. Windows Media Player öffnet und analysiert den XML-Code in der Metadatendatei, die den Pfad zum Suchen der verpackten Audiodateien oder Videodateien enthält. Das Metadatendatei-Skript steuert dann die Audiodarstellung, das Video und die grafische Darstellung. Die Metadatendatei enthält auch Informationen, die von Windows Media Player verarbeitet und im Dropdown Feld Wiedergabeliste angezeigt werden. Unmittelbar nach dem Anzeigen der Liste wird das erste Element in der Liste wiedergegeben.

Eine Metadatei-Wiedergabeliste ist eine Verknüpfung zu den Dateien, die ihren verpackten Inhalt enthalten. Der folgende Code ist ein Beispiel für eine Metadatei, die den Rahmen angibt, der mit dem **Skin** -Element angezeigt werden soll, zwei zu Wiedergabe Ende Lieder und die Wiedergabelisten Informationen für die einzelnen Lieder.


```XML
<ASX Version="3.0">
<AUTHOR>Name of content creator goes here</AUTHOR>
<TITLE>Album Title goes here</TITLE>
<PARAM name="Album" value="Album Title "/>
<PARAM name="Artist" value="Artist Name"/>
<PARAM name="Genre" value="Genre"/>
<SKIN HREF="myborder.wmz"/>
    <ENTRY>
        <REF HREF="song1.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #1 title</TITLE>
    </ENTRY>
    <ENTRY>
        <REF HREF="song2.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #2 name</TITLE>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Rahmen für Windows-Media Player (veraltet)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Windows Media-Download Pakete (veraltet)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Windows Media-Metadateien**](windows-media-metafiles.md)
</dt> </dl>

 

 




