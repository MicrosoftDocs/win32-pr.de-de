---
description: Wiedergeben von Audio Streams
ms.assetid: 1a8d0f42-35b8-4743-9ae7-619b99936f76
title: Wiedergeben von Audio Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10912761034feb9ed82c85625324cd3091514b2c492c66b4e49af711d7d2152
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119213300"
---
# <a name="playing-karaoke-audio-streams"></a>Wiedergeben von Audio Streams

Der DVD-Navigator kann DVD-Video-Datenträgern mit audiostreams wiedergeben, aber für die Wiedergabe von Dvdoke ist auch ein Decoder erforderlich, der das Multichannel-Decodiering unterstützt. Insbesondere muss der Decoder den [**DVD-Eigenschaftssatz ("DVD Quotimoke"**](dvd-karaoke-property-set.md) (AM \_ PROPERTY \_ DVDKARAOKE) unterstützen.

Datenträger sind eine Art von DVD-Video Datenträger und weisen die gleiche Navigationsstruktur auf. Titel werden im Allgemeinen als Titel formatiert, und Titel können basierend auf Performer, Stil oder anderen Kriterien in Titelsätze gruppiert werden. Der Hauptunterschied zwischen Demoke und anderen Arten von DVD-Videos ist der Audiostream. Dvdoke-Datenträger enthalten alle Mehrkanalaudio, in der Regel Dolby AC-3. Die Kanäle 0 und 1 enthalten immer die Musik im Hintergrund, während die Kanäle 2 bis 5 jeweils eine beliebige Kombination aus Führungsgesang, Guide-Sprechweise und Soundeffekten enthalten können. EineLaufoke-Anwendung kann das Volume und den Ziellautstärken für jeden Hilfskanal steuern.

Wenn der DVD-Navigator Denkinhalt auf einem Datenträger erkennt und in den Modus "Laufwerkoke" wechselt, informiert er den Decoder, der dann die oberen drei Kanäle (die Hilfskanäle) stummschalten sollte, bis eine oder alle kanäle explizit von einer Anwendung aktiviert werden. Die grundlegenden Aufgaben einer dhoke-Anwendung sind:

1.  Bestimmen Sie die Anzahl der Hilfskanäle und deren Inhalte mithilfe von [**IDvdInfo2-Methoden.**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)
2.  Stellen Sie eine Benutzeroberfläche bereit, die den Kanalinhalt anzeigt und es Benutzern ermöglicht, jeden zusätzlichen Kanal jederzeit mithilfe von [**IDvdControl2::SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode)zu aktivieren oder zu deaktivieren.

Diese Schritte werden in der DVD-Beispielanwendung in DVDCore.cpp in der **GetAudioAttributes-Methode** veranschaulicht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



