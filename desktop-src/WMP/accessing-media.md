---
title: Zugreifen auf Medien
description: Zugreifen auf Medien
ms.assetid: 18ea844d-98c9-4168-9af2-161dda52f6bd
keywords:
- Windows Media Metadatei-Wiedergabelisten, zugreifen auf Medien
- Wiedergabelisten, zugreifen auf Medien
- Metadatendatei-Wiedergabelisten, zugreifen auf Medien
- Windows Media Metadatei-Wiedergabelisten, Medien Zugriff
- Wiedergabelisten, Medien Zugriff
- Metadatei-Wiedergabelisten, Medien Zugriff
- Windows Media Metadatei-Wiedergabelisten, Steuern der Wiedergabe
- Wiedergabelisten, Steuern der Wiedergabe
- Metadatei-Wiedergabelisten, Steuern der Wiedergabe
- Windows Media Metadatei-Wiedergabelisten, Einstellungs Dauer
- Wiedergabelisten, Einstellungs Dauer
- Metadatei-Wiedergabelisten, Einstellungs Dauer
- Windows Media Player, zugreifen auf Medien
- Windows Media Player, Medien Zugriff
- Windows Media Player, Steuern der Wiedergabe
- Windows Media Player, Einstellungs Dauer
- Zugreifen auf Medien
- Medien Zugriff
- Steuern der Wiedergabe
- Einstellungs Dauer
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5a995a6816e3c46a002bd1ea924c9ea9a207000
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338003"
---
# <a name="accessing-media"></a>Zugreifen auf Medien

Verwenden Sie Wiedergabelisten, um die Streamingmedien oder Mediendateien anzugeben, die von Windows Media Player abgespielt werden.

Verwenden Sie das **Entry** -Element, um ein einzelnes Medien Element (eine Mediendatei oder einen Livestream) und alle untergeordneten Elemente (z. b. Bilder, **moreinfo** -Links und **abstrakten** Text) anzugeben. Verwenden Sie ein **ENTRYREF** -Element, um eine Wiedergabeliste anzugeben. Eine Wiedergabeliste kann ein oder mehrere **Entry** -oder **ENTRYREF** -Elemente enthalten. Windows Media Player führt eine Wiedergabeliste aus, indem Sie mit dem ersten Eintrag beginnt und dann jeden Eintrag nacheinander wieder gibt, bis die Liste abgeschlossen ist.

Ein **Eintrags** Element kann auf beliebige Medientypen verweisen, die von Windows Media Player wiedergegeben werden können. Dies schließt nicht nur die Dateien. WMA,. WMV,. ASF und. AVI ein, um nur ein paar, sondern auch Livestreams zu benennen. Indem Sie eine Reihe von **Entry** -oder **ENTRYREF** -Elementen verwenden, um auf Medieninhalte zu verweisen, können Sie eine Wiedergabeliste verwenden, um einen einzelnen Datenstrom zu senden, der aus mehreren Quellen besteht. Die referenzierten Streams werden sequenziell abgespielt und als ein fortlaufender Stream des Viewers angezeigt. Die Wiedergabeliste kann z. b. zwei **Einstiegs** Elemente enthalten: eine Standard Einführung aus einer Windows Media-Datei mit der Erweiterung ". wma" und ein Live-Windows Media-Stream.

> [!Note]  
> Eine Wiedergabeliste darf keine Links zu Mediendateien enthalten, die Inhalte enthalten, die mit verschiedenen Versionen von Digital Rights Management (DRM) erstellt wurden. Wenn in einer metadateiwiedergabe Links für Mediendateien mit DRM-Inhalt der Version 1 und Mediendateien vorhanden sind, die mit neueren DRM-Versionen erstellt wurden, gibt Windows Media Player nur den DRM-Inhalt der Version 1 wieder.

 

## <a name="controlling-playback"></a>Steuern der Wiedergabe

Verwenden Sie Wiedergabelisten, um nicht nur zu steuern, welche Medienclips abgespielt werden, sondern auch welche Teile des Clips abgespielt werden und wie. Mithilfe von Wiedergabelisten können Sie eine Reihe von Clips definieren, die Schleifen oder wiederholt werden sollen, um die Dauer der Wiedergabe festzulegen und Startzeiten sowie Start-und Endmarker für jeden Eintrag festzulegen. Die Elemente **StartTime**, **Startmarker** und **Endmarker** funktionieren in Verbindung mit Markern in der Mediendatei.

Beispielsweise verwendet die folgende Wiedergabeliste ein Werbebanner und den zugehörigen **moreinfo** -Link in einem **Eintrag** und verweist auf ein **Startmarker** und einen **Endmarker**.


```XML
<ASX version ="3.0">
<Title>Windows Media Example</Title>
<Abstract>Windows Media Technologies</Abstract>
<MoreInfo href = "https://www.proseware.com"/>
    <!--This is the first Entry -->
    <Entry>
        <Title>This is the ad</Title>
        <Author>Ad Department</Author>
        <Copyright>2000</Copyright>
        <Abstract>This is a description of the ad.</Abstract>
        <MoreInfo href = "https://www.proseware.com/"/>
        <Ref href="ad.wma"/>
        <Banner href ="purchase.gif">
           <Abstract>Click here to go to our website.</Abstract>
           <MoreInfo href = "https://www.litwareinc.com/" />
        </Banner>
     </Entry>        
    <!-- This is the second Entry -->
    <!-- The Windows Media file plays from Segment2 to Segment3 -->
    <Entry>
        <Title>Playlist Clip Number Two</Title>
        <Author>Windows Media</Author>
        <Copyright>2000</Copyright>
        <Ref href="show.wma"/>
        <StartMarker Name = "Segment2" />
        <EndMarker Name = "Segment3" />
    </Entry>
</ASX>

```



## <a name="setting-duration"></a>Einstellungs Dauer

Verwenden Sie das **Duration** -Element, um anzugeben, wie lange ein Clip oder eine Reihe von Clips wiedergegeben werden soll. Sie können auch das **PreviewMode** -Attribut des **ASX** -Elements in Verbindung mit dem **previewduration** -Element verwenden, um anzugeben, wie lange ein Clip oder eine Reihe von Clips wiedergegeben werden soll. Legen Sie das **PreviewMode** -Attribut auf "yes" fest, um mit dem **previewduration** -Element anzugeben, wie lange der zugeordnete Clip wiedergegeben werden soll Die Elemente " **previewduration** " und " **Duration** " weisen das gleiche Verhalten auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Verwenden von Metafile-Wiedergabelisten**](using-metafile-playlists.md)
</dt> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Leitfaden für Windows Media-Metadateien**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




