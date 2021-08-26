---
title: Verwenden von Metadateien für den nahtlosen Streamwechsel
description: Verwenden von Metadateien für den nahtlosen Streamwechsel
ms.assetid: e632f670-54c4-4b5b-8396-1d5368f90e6d
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
ms.openlocfilehash: d4efc4a23f0464446675d9de20d57750bd230d2eef26d31714e2129e380ae9e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001570"
---
# <a name="using-metafiles-for-seamless-stream-switching"></a>Verwenden von Metadateien für den nahtlosen Streamwechsel

Sie können den nahtlosen Streamwechsel mithilfe von Metadateiwiedergabelisten vereinfachen. In der Regel erfolgt beim Ende eines Inhalts eine Pufferung für den nächsten Clip oder Stream, bevor er geöffnet wird (wenn es sich um Inhalte handelt, die von einem Streamingmedienserver empfangen werden). Microsoft Windows Media-Dienste ermöglicht es Ihnen, diese Pufferungszeit zu beseitigen oder zumindest zu minimieren, damit ein weiterer Teil des gestreamten Inhalts nahezu sofort abspielt. Der normale Betriebsmodus für Windows Media Player besteht im Öffnen des nächsten Medienstreams, auf den die Wiedergabeliste 20 Sekunden vor dem Ende des aktuell gerenderten Streams verweist. Dies ermöglicht in der Regel einen nahtlosen Übergang zwischen Medienstreams, abhängig von anderen Faktoren wie Webzugriffszeiten.

Verwenden Sie **das EVENT-Element** in einer Wiedergabeliste in Verbindung mit OPENEVENT-Befehlen des Encoders, um den nahtlosen Wechsel zwischen Streams oder Dateien zu ermöglichen. Das Senden eines OPENEVENT-Befehls 20 Sekunden oder mehr vor dem EVENT-Befehl kann Verzögerungen beim Streamwechsel minimieren. Anschließend Windows Media Player einen Teil des bevorstehenden Streaminginhalts vorab in einen Puffer laden.

Verwenden Windows Media Encoder, um einen Skriptbefehl im Stream im folgenden Format zu senden:


```XML
OPENEVENT eventname 

```



Der Ereignisname muss der name sein, der im **EVENT-Element** in der Wiedergabeliste definiert ist. Wenn Windows Media Player einen OPENEVENT-Skriptbefehl vom Encoder empfängt, sucht er nach dem **EVENT-Element** in der Wiedergabeliste und beginnt mit dem Puffern des Im **EVENT-Elements** definierten Clips oder Streams. Windows Media Player enthält diese Informationen dann bis zum tatsächlichen Ereignis mit demselben Namen. Wenn das benannte Ereignis empfangen wird, Windows Media Player auf den zuvor gepufferten Inhalt um.

> [!Note]  
> Sie können keine Unicode-Zeichen für den OPENEVENT-Skriptbefehl in der Mediendatei oder im **EVENT-Element** in der Wiedergabeliste verwenden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen von Metadateiwiedergabelisten**](creating-metafile-playlists.md)
</dt> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Player.ScriptCommand-Ereignis**](player-player-scriptcommand.md)
</dt> <dt>

[**Verwenden von Metafile-Wiedergabelisten**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Leitfaden zur Medienmetadatei**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




