---
title: Zugreifen auf Medien
description: Zugreifen auf Medien
ms.assetid: 18ea844d-98c9-4168-9af2-161dda52f6bd
keywords:
- Windows Medienmetadatei-Wiedergabelisten,Zugreifen auf Medien
- Wiedergabelisten, Zugreifen auf Medien
- Metadatei-Wiedergabelisten,Zugreifen auf Medien
- Windows Medienmetadatei-Wiedergabelisten, Medienzugriff
- Wiedergabelisten, Medienzugriff
- Metadateiwiedergabelisten, Medienzugriff
- Windows Medienmetadatei-Wiedergabelisten, Steuern der Wiedergabe
- Wiedergabelisten, Steuern der Wiedergabe
- Metafile-Wiedergabelisten,Steuern der Wiedergabe
- Windows Medienmetadatei-Wiedergabelisten, Festlegen der Dauer
- Wiedergabelisten, Dauer festlegen
- Metafile-Wiedergabelisten, Festlegen der Dauer
- Windows Media Player,Zugreifen auf Medien
- Windows Media Player,Medienzugriff
- Windows Media Player,Steuern der Wiedergabe
- Windows Media Player,Festlegen der Dauer
- Zugreifen auf Medien
- Medienzugriff
- Steuern der Wiedergabe
- Festlegen der Dauer
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c1a0846be4e8b9b62e424ce24d1b1800bc361c6a28f52a323c6bfa8511ae040b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956400"
---
# <a name="accessing-media"></a>Zugreifen auf Medien

Verwenden Sie Wiedergabelisten, um die Streamingmedien oder Mediendateien anzugeben und zu steuern, die Windows Media Player wiedergegeben werden.

Verwenden  Sie das ENTRY-Element, um ein einzelnes Medienelement (eine Mediendatei oder einen Livestream) und alle untergeordneten Elemente (z. B. Bilder, **MOREINFO-Links** und **ABSTRACT-Text)** anzugeben. Verwenden Sie ein **ENTRYREF-Element,** um eine Wiedergabeliste anzugeben. Eine Wiedergabeliste kann ein oder mehrere **ENTRY-** oder **ENTRYREF-Elemente** enthalten. Windows Media Player führt eine Wiedergabeliste aus, indem sie mit dem ersten Eintrag beginnt und dann jeden Eintrag nacheinander abspielt, bis die Liste abgeschlossen ist.

Ein **ENTRY-Element** kann auf einen beliebigen Medientyp verweisen, den Windows Media Player wiedergeben können. Dies schließt nicht nur WMA-, WMV-, ASF- und .avi-Dateien ein, um nur einige zu nennen, sondern auch Livestreams. Indem Sie eine Reihe von **ENTRY-** oder **ENTRYREF-Elementen** verwenden, um auf Medieninhalte zu verweisen, können Sie eine Wiedergabeliste verwenden, um einen einzelnen Stream zu senden, der aus mehreren Quellen besteht. Die Referenzdatenströme werden sequenziell wiedergegeben und vom Viewer als ein kontinuierlicher Stream betrachtet. Die Wiedergabeliste kann beispielsweise zwei **ENTRY-Elemente** enthalten: eine Standardeinführung aus einer Windows Mediendatei mit der Erweiterung ".wma" und einen Live-Windows Medienstream.

> [!Note]  
> Eine Wiedergabeliste darf keine Links zu Mediendateien enthalten, deren Inhalt mit verschiedenen Versionen von Digital Rights Management (DRM) erstellt wurde. Wenn in einer Metadateiwiedergabeliste Links für Mediendateien mit DRM-Inhalten der Version 1 und für Mediendateien vorhanden sind, die mit späteren DRM-Versionen erstellt wurden, wird Windows Media Player nur den Inhalt der DRM-Version 1 wiedergeben.

 

## <a name="controlling-playback"></a>Steuern der Wiedergabe

Verwenden Sie Wiedergabelisten, um nicht nur zu steuern, welcher Medienclip wiedergegeben wird, sondern auch, welche Teile des Clips wiedergegeben werden und wie. Sie können Wiedergabelisten verwenden, um einen Satz von Clips zu definieren, die in schleifen- oder wiederholt werden sollen, um die Dauer der Wiedergabe festzulegen und Startzeiten sowie Start- und Endmarker für jeden Eintrag zuzuweisen. Die Elemente **STARTTIME,** **STARTMARKER** und **ENDMARKER** funktionieren in Verbindung mit Markern in der Mediendatei.

Die folgende Wiedergabeliste verwendet beispielsweise ein Werbebanner und den zugehörigen **MOREINFO-Link** in einem **EINTRAG** und verweist auf **EINEN STARTMARKER** und **ENDMARKER.**


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



## <a name="setting-duration"></a>Festlegen der Dauer

Verwenden  Sie das DURATION-Element, um anzugeben, wie lange ein Clip oder eine Gruppe von Clips wiedergegeben werden soll. Sie können auch das **PREVIEWMODE-Attribut** des **ASX-Elements** in Verbindung mit dem **PREVIEWDURATION-Element** verwenden, um anzugeben, wie lange ein Clip oder eine Gruppe von Clips wiedergegeben werden soll. Legen Sie das **PREVIEWMODE-Attribut** auf YES fest, um das **PREVIEWDURATION-Element** zu verwenden, um anzugeben, wie lange der zugeordnete Clip wiedergegeben werden soll. Die Elemente **PREVIEWDURATION** und **DURATION** weisen das gleiche Verhalten auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Verwenden von Metafile-Wiedergabelisten**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media Metafile Guide**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




