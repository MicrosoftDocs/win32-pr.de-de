---
description: Wiedergabe von Karaoke-Audiostreams
ms.assetid: 1a8d0f42-35b8-4743-9ae7-619b99936f76
title: Wiedergabe von Karaoke-Audiostreams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907bfa3e359915cf537de75cdc739630fe607d97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343564"
---
# <a name="playing-karaoke-audio-streams"></a>Wiedergabe von Karaoke-Audiostreams

Der DVD-Navigator kann DVD-Video-CDs mit Karaoke-Audiostreams wiedergeben, aber die Karaoke-Wiedergabe erfordert auch einen Decoder, der eine Multichannel-Karaoke-Mischung Insbesondere muss der Decoder den DVD- [**Karaoke-Eigenschaften Satz**](dvd-karaoke-property-set.md) unterstützen (am \_ Eigenschaft \_ dvdkaraoke).

Bei den Karaoke-Festplatten handelt es sich um einen Typ von DVD-Video-CD und die gleiche Navigationsstruktur. Lieder werden im Allgemeinen als Titel formatiert, und Titel können auf der Grundlage von Interpreten, musikalischem Stil oder anderen Kriterien in Titel Gruppen gruppiert werden. Der Hauptunterschied zwischen Karaoke und anderen Typen von DVD-Videos ist der Audiodatenstrom. Alle Karaoke-Datenträger enthalten Multichannel-Audiodaten, normalerweise Dolby AC-3. Die Kanäle 0 und 1 enthalten immer die Hintergrund Instrumentalmusik, während die Kanäle 2 bis 5 jede beliebige Kombination aus Führungs Gesang, Führungs Melodien und Soundeffekten enthalten können. Eine Karaoke-Anwendung kann das Volume und den Ziel Sprecher für jeden hilfsanchannel steuern.

Wenn der DVD-Navigator einen Karaoke-Inhalt auf einer CD erkennt und in den Karaoke-Modus wechselt, wird der Decoder informiert, der die oberen drei Kanäle (die zusätzlichen Kanäle) stumm schalten sollte, bis eine oder alle davon explizit von einer Anwendung aktiviert werden. Die grundlegenden Aufgaben einer Karaoke-Anwendung sind:

1.  Bestimmen Sie die Anzahl von zusätzlichen Kanälen und deren Inhalt mithilfe der [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) -Methoden.
2.  Stellen Sie eine Benutzeroberfläche bereit, auf der der Kanal Inhalt angezeigt wird, und ermöglichen Sie es Benutzern, mithilfe von [**IDvdControl2:: selectkaraokeaudiopresentationmode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode)jederzeit einen beliebigen hilfsanchannel zu aktivieren bzw. zu deaktivieren.

Diese Schritte werden in der Anwendung "DVD-Beispiel" in "dvdcore. cpp" in der Methode " **getaudioattributs** " veranschaulicht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



