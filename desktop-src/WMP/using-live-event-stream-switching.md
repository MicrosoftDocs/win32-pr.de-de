---
title: Verwenden von Live Event Stream Switching
description: Verwenden von Live Event Stream Switching
ms.assetid: fa8af007-2db6-438f-9551-8e748bb79ef4
keywords:
- Windows Wiedergabelisten von Medienmetadateien, Wechseln des Liveereignisstreams
- Wiedergabelisten,Liveereignisstreamwechsel
- Metafile-Wiedergabelisten,Liveereignisstreamwechsel
- Windows Wiedergabelisten der Medienmetadatei, Wechseln des Ereignisdatenstroms
- Wiedergabelisten, Wechseln des Ereignisdatenstroms
- Metafile-Wiedergabelisten, Wechseln des Ereignisdatenstroms
- Windows Wiedergabelisten von Medienmetadateien,Ad-Einfügung
- Wiedergabelisten,Werbeeinfügung
- Metafile-Wiedergabelisten, Werbeeinfügung
- Windows Media Player,Liveereignisstreamwechsel
- Windows Media Player,Ereignisstreamwechsel
- Windows Media Player,Ad-Einfügung
- Liveereignisstreamwechsel
- Ereignisdatenstromwechsel
- Werbeeinfügung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d8524fe1a83a6b3276c274726fa27fa7fcccb97b88f0384a54e5433d09380501
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134363"
---
# <a name="using-live-event-stream-switching"></a>Verwenden von Live Event Stream Switching

Streamingmedien können auch durch die Interaktion von Skriptbefehlen gesteuert werden, die in einen Medienstream eingebettet sind, Windows Medienmetadateielemente in einer Metadateiwiedergabeliste enthalten.

Ein Ereignis ist ein bestimmter Typ von Skriptbefehl, der in einen Medienstream oder eine Mediendatei eingebettet ist. Wenn das Windows Media Player-Steuerelement den Skriptbefehl empfängt, verarbeitet es das Ereignis gemäß definition des **EVENT-Elements** in der Metadateiwiedergabeliste. Windows Media Player aus dem aktuellen Stream, der gerendert wird, und rendert den Inhalt, auf den im EVENT-Element der Metadateiwiedergabeliste **verwiesen** wird. Das **EVENT-Element** wird normalerweise in der Liveproduktion verwendet.

Ein **EVENT-Element** ähnelt einem **ENTRY-Element,** aber jedes behandelt die Wiedergabe von Streams und Mediendateien unterschiedlich. Das **ENTRY-Element** wird verwendet, um Wiedergabelisten zu erstellen. Ein Stream oder eine Mediendatei, auf die in einem **ENTRY-Element** verwiesen wird, beginnt mit der Wiedergabe, wenn der Stream oder die Mediendatei, auf die im vorherigen **ENTRY-Element** verwiesen wird, abgeschlossen ist. Ein Stream, auf den in einem **EVENT verwiesen** wird, wird nur dann wieder verwendet, wenn ein bestimmter Skriptbefehl empfangen wird. Wenn Windows Media Player beispielsweise einen Skriptbefehl mit der Typzeichenfolge "EVENT" und der Befehlszeichenfolge "Adlink" empfängt, durchsucht er die Wiedergabeliste nach den folgenden Elementen.


```XML
<EVENT NAME="Adlink" WHENDONE="RESUME"> 
    <ENTRY HREF=mms://www.proseware.com/adlink.wma />
</EVENT>

```



Windows Media Player dann aus dem Livestream, um den Stream oder die Mediendatei aus **dem EVENT** wiederderherzustellen , in diesem Fall Adlink.wma. Der Code weist Windows Media Player, die Wiedergabe des vorherigen Streams wieder `WHENDONE="RESUME"` aufzunehmen, wenn "Adlink.wma" abgeschlossen ist.

> [!Note]  
> Wenn nicht jedes in einen Medienstream oder eine Mediendatei eingebettete Ereignis behandelt wird, kann dies zu unerwarteten Ergebnissen führen.

 

Wenn Sie den Liveereignisstreamwechsel verwenden möchten, müssen Sie ein **EVENT-Element** in Ihre Wiedergabeliste einbetten, um jeden Ereignisskriptbefehl zu verarbeiten, der in die Medienstreams oder Mediendateien in Ihrer Wiedergabeliste eingebettet ist. Bevor Sie Ihre Wiedergabeliste erstellen, müssen Sie die Details darüber kennen, welche Skriptbefehle in Ihre digitalen Medieninhalte eingebettet sind. Wenn es einen Ereignisskriptbefehl gibt, den Windows Media Player ignorieren soll, schließen Sie ein **EVENT-Element** in Ihre Wiedergabeliste ein, um das Ereignis zu behandeln, verweisen sie jedoch im Ereignishandler auf eine Dummy-URL.

## <a name="ad-insertion"></a>Werbeeinfügung

Diese Technik kann zum Einfügen von Werbeeinblendung verwendet werden. Beispielsweise kann während einer Liveübertragung eines Ballspiels im Internet ein Befehl zu Beginn jeder kommerziellen Pause gesendet werden, der jeden Client (Windows Media Player) anweisen soll, in seiner Wiedergabeliste aufgeführte Werbespots zu spielen. Wenn clients die Wiedergabe der Werbespots abgeschlossen hat, weist die Wiedergabeliste jeden Client an, die Liveübertragung wieder zu verwenden. Der  EVENT-Medieninhalt wird nur gerendert, wenn das Streamingmedium, auf das zugegriffen wird, eingebettete Skripts mit dem entsprechenden **EVENT-Namen** sendet.

Die Möglichkeiten des **EREIGNISwechsels** werden am besten geschätzt, indem sie gegenüber stellen, wie Anzeigen über die standardmäßige, over-the-air-Übertragung zu erreichenden Viewern gegenüber stehen, wie Anzeigen mithilfe von Medientechnologien Windows erreichen können. In der Vergangenheit konnten Broadcastanzeigen nur grob auf Betrachter ausgerichtet sein, indem Bewertungsdaten als primäre Kriterien verwendet werden. Anzeigen, die mithilfe Windows Media Technologies gesendet werden, können direkt auf den Zielbenutzer ausgerichtet werden, da **EVENTs** und Wiedergabelisten basierend auf Benutzereingaben direkt erstellt werden können. Weitere Informationen finden Sie unter [Personalizing Media Delivery (Personalisieren der Medienbereitstellung).](personalizing-media-delivery.md)

Sie können auch Wiedergabelisten für Metadateien verwenden, um benutzerdefinierte Grafiken, Audiodaten und Text für Werbung anzuzeigen. Sie können das **BANNER-Element** als untergeordnetes Element eines **EREIGNISSEs verwenden,** um eine Werbemeldungsgrafik anzuzeigen. Das **BANNER-Element** stellt den Pfad und die Datei mit den Grafiken für Ihr Werbebanner dar. Sie können auch einen Link zu einer Website oder Datei bereitstellen, indem Sie das **untergeordnete MOREINFO-Element** verwenden. Die URL im **MOREINFO-Element** kann einen Link zu noch mehr Ankündigungen im Web bereitstellen. Im folgenden Beispiel wird die Verwendung dieser Elemente veranschaulicht.

Beispielcode


```XML
<BANNER HREF="SomePath\2.gif">
    <ABSTRACT>Read This Ad and Buy.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



Im folgenden Beispiel wird die Ad-Datei "Streams.wma" in den Broadcast-Unicaststream BallGame eingefügt, wenn ein Client einen Skriptbefehl **EVENT** empfängt, bei dem das **NAME-Attribut** auf "Time-Out" festgelegt ist. **CLIENTSKIP ist** auf NO festgelegt, um zu verhindern, dass die gestreamte Werbeanzeige übersprungen wird. In diesem Beispiel muss die gestreamte Werbeanzeige vor der Rückkehr zum ursprünglichen Stream abgespielt werden. Wenn die Werbeanzeige abgeschlossen ist, setzt der Client die Wiedergabe des ursprünglichen Streams wieder.

Beispielcode


```XML
<ASX VERSION="3.0">
    <ENTRY>
        <REF HREF="mms://proseware.com/BallGame" />
    </ENTRY>
    <EVENT NAME="Time-Out" WHENDONE="RESUME">
        <ENTRY>
            <REF HREF = "mms://proseware.com/Advert.wma" 
                CLIENTSKIP = "NO" />
       </ENTRY>
    </EVENT>
</ASX>

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Verwenden von Metafile-Wiedergabelisten**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Leitfaden zur Medienmetadatei**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




