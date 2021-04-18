---
title: Verwenden von Live ereignisstreamumschaltung
description: Verwenden von Live ereignisstreamumschaltung
ms.assetid: fa8af007-2db6-438f-9551-8e748bb79ef4
keywords:
- Windows Media Metadatei-Wiedergabelisten, Live ereignisstreamwechsel
- Wiedergabelisten, Live ereignisstreamwechsel
- Metadatei-Wiedergabelisten, Live ereignisstreamwechsel
- Windows Media Metadatei-Wiedergabelisten, ereignisstreamwechsel
- Wiedergabelisten, ereignisstreamwechsel
- Metadatei-Wiedergabelisten, ereignisstreamwechsel
- Windows Media Metadatei-Wiedergabelisten, AD-Einfügung
- Wiedergabelisten, Werbe Einfügung
- Metadatei-Wiedergabelisten, AD-Einfügung
- Windows Media Player, Live ereignisstreamwechsel
- Windows Media Player, ereignisstreamwechsel
- Windows Media Player, Werbe Einfügung
- Live ereignisstreamwechsel
- ereignisstreamwechsel
- Werbe Einfügung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fd5c586e0f1ef2b36913dee822e461daeffbfcbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206465"
---
# <a name="using-live-event-stream-switching"></a>Verwenden von Live ereignisstreamumschaltung

Streamingmedien können auch durch die Interaktion von Skript Befehlen gesteuert werden, die in einem Mediendaten Strom mit Windows Media-Metadatei-Elementen in einer Metadatei-Wiedergabeliste eingebettet sind.

Ein Ereignis ist eine bestimmte Art von Skript Befehl, der in einen Mediendaten Strom oder eine Mediendatei eingebettet ist. Wenn das Windows Media Player-Steuerelement den Skript Befehl empfängt, verarbeitet es das Ereignis gemäß der Definition durch das **Ereignis** Element in der Metadatendatei-Wiedergabeliste. Windows Media Player schaltet aus dem aktuellen Stream, der gerendert wird, und rendert den Inhalt, auf den im metadatenwiedergabe- **Ereignis** Element verwiesen wird. Das **Ereignis** Element wird in der Regel in der aktiven Produktion verwendet.

Ein **Ereignis** Element ähnelt einem **Entry** -Element, aber jedes behandelt die Wiedergabe von Streams und Mediendateien anders. Das **Entry** -Element dient zum Erstellen von Wiedergabelisten. Ein Stream oder eine Mediendatei, auf die in einem **Entry** -Element verwiesen wird, beginnt, wenn der Stream oder die Mediendatei, auf die im vorherigen **Eintrag** verwiesen wird Ein in einem **Ereignis** referenzierter Stream wird nur wiedergegeben, wenn ein bestimmter Skript Befehl empfangen wird. Wenn Windows Media Player z. b. einen Skript Befehl mit dem Typ String "Event" und der Befehls Zeichenfolge "AdLINK" empfängt, wird die Wiedergabeliste nach den folgenden Elementen durchsucht.


```XML
<EVENT NAME="Adlink" WHENDONE="RESUME"> 
    <ENTRY HREF=mms://www.proseware.com/adlink.wma />
</EVENT>

```



Windows Media Player wechselt dann aus dem Livestream zum Wiedergeben des Streams oder der Mediendatei, die im **Ereignis** enthalten ist, in diesem Fall "AdLINK. wma". Der Code `WHENDONE="RESUME"` weist Windows Media Player an, die Wiedergabe des vorherigen Streams fortzusetzen, wenn "AdLINK. wma" abgeschlossen ist.

> [!Note]  
> Fehler bei der Behandlung von Ereignissen, die in einen Medienstrom oder eine Mediendatei eingebettet sind, können zu unerwarteten Ergebnissen führen.

 

Wenn Sie Live-ereignisstreamwechsel verwenden möchten, müssen Sie ein- **Ereignis** Element in die Wiedergabeliste einschließen, um jeden in den Mediendaten Strömen oder in den Mediendateien in der Wiedergabeliste eingebetteten Ereignis Skript Befehl zu verarbeiten. Bevor Sie die Wiedergabeliste erstellen, müssen Sie die Details darüber kennen, welche Skript Befehle in Ihren digitalen Medieninhalt eingebettet sind. Wenn ein Ereignis Skript Befehl ignoriert werden soll, der von Windows Media Player ignoriert werden soll, fügen Sie ein **Ereignis** Element in die Wiedergabeliste ein, um das Ereignis zu behandeln, aber verweisen Sie im Ereignishandler auf eine Pseudo-URL.

## <a name="ad-insertion"></a>Werbe Einfügung

Diese Technik kann für Werbe Einfügungs Vorgänge verwendet werden. Beispielsweise kann während eines Live-Internet Broadcast eines Ballspiels ein Befehl an den Anfang jeder kommerziellen Pause gesendet werden, der jeden Client (Windows Media Player) anweist, in der Wiedergabeliste aufgeführten Werbespots zu spielen. Wenn die Wiedergabe der Werbespots durch Clients abgeschlossen ist, weist die Wiedergabeliste jeden Client an, zur Liveübertragung zurückzukehren. Der Inhalt der **Ereignis** Medien wird nur dann gerendert, wenn die Streamingmedien, auf die zugegriffen wird, eingebettetes Skript mit dem passenden **Ereignis** Namen überträgt

Die Möglichkeiten für den **Ereignis** Wechsel sind am besten zu schätzen, indem Sie den Betrachter über den standardmäßigen Broadcast Übertragungen erreichen, um zu erfahren, wie ADS mithilfe von Windows Media-Technologien Betrachter erreichen können. In der Vergangenheit konnten Broadcast-Werbeeinblendungen nur annähernd an Betrachter gerichtet sein, wobei die Bewertungsdaten als primäre Kriterien verwendet werden. Mithilfe von Windows Media-Technologien gesendete anzeigen können direkt auf den Ziel Benutzer ausgerichtet werden, da **Ereignisse** und Wiedergabelisten basierend auf Benutzereingaben dynamisch erstellt werden können. Weitere Informationen finden Sie unter [Personalisieren der Medien Bereitstellung](personalizing-media-delivery.md).

Sie können auch Metadatei-Wiedergabelisten verwenden, um angepasste Grafiken, Audiodaten und Text für Werbung anzuzeigen. Sie können das **Banner** -Element als untergeordnetes Element eines **Ereignisses** verwenden, um eine Werbe Meldungs Grafik anzuzeigen. Das **Banner** -Element enthält den Pfad und die Datei mit den Grafiken für Ihr Werbe Banner. Mithilfe des untergeordneten **moreinfo** -Elements können Sie auch einen Link zu einer Website oder Datei bereitstellen. Die URL im **moreingefo** -Element kann einen Link zu weiteren Ankündigungen im Internet bereitstellen. Im folgenden Beispiel wird die Verwendung dieser Elemente veranschaulicht.

Beispielcode


```XML
<BANNER HREF="SomePath\2.gif">
    <ABSTRACT>Read This Ad and Buy.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



Im folgenden Beispiel wird die Werbe Einblendungs-Datei "AD" in den Broadcast-Unicastdatenstrom eingefügt, wenn ein Client ein Skript Befehls **Ereignis** empfängt, bei dem das Attribut " **Name** " auf "Timeout" festgelegt ist. **Clientskip** ist auf "Nein" festgelegt, um zu verhindern, dass die gestreamte Werbung ausgelassen wird. In diesem Beispiel muss die gestreamte-Werbe Einblendung vor dem zurückkehren zum ursprünglichen Stream abgespielt werden. Wenn die Werbe Einstellung abgeschlossen ist, setzt der Client die Wiedergabe des ursprünglichen Streams fort.

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

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Leitfaden für Windows Media-Metadateien**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




