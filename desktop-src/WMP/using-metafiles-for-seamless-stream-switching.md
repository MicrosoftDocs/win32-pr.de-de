---
title: Verwenden von Metadatendateien für den nahtlosen Datenstrom Wechsel
description: Verwenden von Metadatendateien für den nahtlosen Datenstrom Wechsel
ms.assetid: e632f670-54c4-4b5b-8396-1d5368f90e6d
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
ms.openlocfilehash: 29496c71c0c849480bae029f246bfd544667071e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341843"
---
# <a name="using-metafiles-for-seamless-stream-switching"></a>Verwenden von Metadatendateien für den nahtlosen Datenstrom Wechsel

Sie können den nahtlosen Datenstrom Wechsel mithilfe von Metadatei-Wiedergabelisten vereinfachen. Wenn ein Teil des Inhalts endet, erfolgt in der Regel eine Pufferung für den nächsten Clip oder Stream, bevor er geöffnet wird (wenn es sich um Inhalt handelt, der von einem Streaming Media-Server empfangen wird). Microsoft Windows Media Services ermöglicht es Ihnen, diese Pufferzeit zu eliminieren oder zumindest zu minimieren, und die Wiedergabe eines anderen Streaminginhalts beginnt fast sofort. Der normale Betriebsmodus für Windows-Media Player besteht darin, den nächsten Mediendaten Strom zu öffnen, auf den von der Wiedergabeliste 20 Sekunden vor dem Ende des aktuell gerenderten Streams verwiesen wird. Dies ermöglicht im Allgemeinen eine nahtlose Umstellung zwischen Mediendaten strömen, abhängig von anderen Faktoren wie z. b. Webzugriffs Zeiten.

Verwenden Sie das **Ereignis** Element in einer Wiedergabeliste zusammen mit OpenEvent-Befehlen aus dem Encoder, um das nahtlose wechseln zwischen Streams oder Dateien zu vereinfachen. Wenn ein OpenEvent-Befehl 20 Sekunden oder länger vor dem Ereignis Befehl gesendet wird, können Verzögerungen bei der Datenstrom Umstellung minimiert werden. Anschließend kann Windows Media Player einen Teil der bevorstehenden Streaming-Inhalte in einen Puffer laden.

Verwenden Sie Windows Media Encoder, um einen Skript Befehl im Stream im folgenden Format zu senden:


```XML
OPENEVENT eventname 

```



Der Ereignis Name muss der Name sein, der im **Ereignis** Element in der Wiedergabeliste definiert ist. Wenn Windows Media Player einen OpenEvent-Skript Befehl vom Encoder empfängt, wird das **Ereignis** Element in der Wiedergabeliste gesucht, und es wird begonnen, den Clip oder Stream zu puffern, der im **Ereignis** Element definiert ist. Windows Media Player speichert diese Informationen dann bis zum eigentlichen Ereignis desselben Namens. Wenn das benannte Ereignis empfangen wird, wechselt Windows Media Player zu diesem zuvor gepufferten Inhalt.

> [!Note]  
> Sie können keine Unicode-Zeichen für den OpenEvent Script-Befehl in der Mediendatei oder im- **Ereignis** Element in der Wiedergabeliste verwenden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen von Metafile-Wiedergabelisten**](creating-metafile-playlists.md)
</dt> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Player. ScriptCommand-Ereignis**](player-player-scriptcommand.md)
</dt> <dt>

[**Verwenden von Metafile-Wiedergabelisten**](using-metafile-playlists.md)
</dt> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Leitfaden für Windows Media-Metadateien**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




