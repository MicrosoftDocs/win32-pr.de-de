---
description: DVD-Befehle
ms.assetid: 1204c73e-c3de-4488-8ee3-e76edbf72da0
title: DVD-Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02f9c0b6a50b6d7eb67832286ee980b0faf69460621a46caf98089efc24b19c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820584"
---
# <a name="dvd-commands"></a>DVD-Befehle

Die Befehle zur DVD-Navigation und -Wiedergabe sind in einem Abschnitt der DVD-Spezifikation mit dem Namen Anhang J definiert. Aus diesem Grund bezieht sich die DirectShow-Dokumentation häufig auf "Anhang J-Befehle". Die in Anhang J angegebenen Namen sind jedoch nicht immer sehr intuitiv, sodass DirectShow Namen verwendet, die möglicherweise einfacher zu verstehen sind.

In der folgenden Tabelle sind die Befehle im Anhang J und ihre DirectShow-Entsprechungen aufgeführt.



| Befehl "Anhang J"                                                                           | Beschreibung                                                                  | IDvdControl2-Methode                                                                           |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| \_Titelplay                                                                               | Geben Sie einen Titel wieder.                                                                | [**PlayTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playtitle)                                                   |
| PTT \_ Play                                                                                 | Spielen Sie ein Kapitel in einem Titel.                                                   | [**PlayChapterInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapterintitle)                                 |
| \_Wiedergabezeit                                                                                | Gibt einen Titel ab einem angegebenen Zeitpunkt wieder.                                 | [**PlayAtTimeInTitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattimeintitle)                                   |
| Beenden                                                                                      | Beenden Sie die Wiedergabe.                                                               | [**Beenden**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stop)                                                             |
| GoUp                                                                                      | Kehren Sie von einem Untermenü zum übergeordneten Menü zurück.                                    | [**ReturnFromSubmenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-returnfromsubmenu)                                   |
| \_Zeitsuche                                                                              | Wiedergabe zu einem bestimmten Zeitpunkt innerhalb des aktuellen Titels.                           | [**PlayAtTime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime)                                                 |
| \_PTT-Suche                                                                               | Spielen Sie ein Kapitel innerhalb des aktuellen Titels ab.                                     | [**PlayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapter)                                               |
| PrevPG-Suche \_                                                                            | Wechseln Sie zum Anfang des vorherigen Kapitels, und setzen Sie die Wiedergabe wieder auf.                 | [**PlayPrevChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playprevchapter)                                       |
| \_TopPG-Suche                                                                             | Wechseln Sie zum Anfang des aktuellen Kapitels, und setzen Sie die Wiedergabe wieder auf.                  | [**ReplayChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-replaychapter)                                           |
| \_NextPG-Suche                                                                            | Wechseln Sie zum Anfang des nächsten Kapitels, und setzen Sie die Wiedergabe wieder auf.                     | [**PlayNextChapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playnextchapter)                                       |
| Forward \_ Scan                                                                             | Wiedergabe mit einer angegebenen Wiedergaberate. Die Standardwiedergaberate ist 1,0. | [**PlayForwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playforwards)                                             |
| \_Rückwärtsscan                                                                            | Wiedergabe rückwärts mit einer angegebenen Wiedergaberate.                                  | [**PlayBackwards**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playbackwards)                                           |
| \_Menüaufruf                                                                                | Anzeigen eines Menüs                                                                 | [**ShowMenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu)                                                     |
| Fortsetzen                                                                                    | Kehren Sie aus einem Menü zurück, und setzen Sie die Wiedergabe wieder auf.                                      | [**Fortsetzen**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-resume)                                                         |
| Obere \_ Schaltfläche \_ Auswählen, Untere \_ Schaltfläche \_ Auswählen, Linke \_ Schaltfläche \_ Auswählen, Rechte Schaltfläche \_ \_ auswählen | Wählen Sie eine Schaltfläche aus, deren Position relativ zur aktuell ausgewählten Schaltfläche ist. | [**SelectButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton)                                             |
| Schaltfläche \_ "Aktivieren"                                                                          | Aktivieren Sie die ausgewählte Schaltfläche.                                                | [**ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton)                                         |
| Schaltfläche \_ "Auswählen \_ und \_ Aktivieren"                                                             | Wählen Sie eine Schaltfläche aus, und aktivieren Sie sie.                                                | [**SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton)                       |
| Still \_ Off                                                                                | Fortsetzen der Wiedergabe beim Anzeigen eines Stillbilds.                               | [**StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff)                                                     |
| Anhalten \_ am                                                                                 | Anhalten der Wiedergabe.                                                              | [**Anhalten**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| Anhalten \_ deaktiviert                                                                                | Setzen Sie die Wiedergabe aus dem angehaltenen Zustand wieder auf.                                       | [**Anhalten**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| Menüsprache \_ \_ auswählen                                                                    | Wählen Sie die Sprache für Menüs aus.                                               | [**Wählen SieDefaultMenuLanguage aus.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectdefaultmenulanguage)                   |
| Änderung \_ des \_ Audiostreams                                                                     | Legen Sie den Audiostream fest.                                                        | [**Wählen SieAudioStream aus.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectaudiostream)                                   |
| Streamänderung im \_ \_ Unterbild                                                               | Legen Sie den Unterbilddatenstrom fest. Aktivieren oder Deaktivieren der Unterbildanzeige.             | [**SelectSubpictureStream**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectsubpicturestream)                         |
| \_Winkeländerung                                                                             | Legen Sie den Kamerawinkel fest.                                                        | [**Wählen SieVerschränken aus.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle)                                               |
| Auswahl \_ der \_ Elternebene                                                                   | Legen Sie die Elternebene fest.                                                      | [**Wählen SieParentalLevel aus.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentallevel)                               |
| Auswahl \_ des \_ Elternland                                                                 | Legen Sie das Land bzw. die Region für die Elternverwaltung fest.                              | [**Wählen SieParentalCountry aus.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentalcountry)                           |
| Änderung \_ des \_ \_ Präsentationsmodus für Audioinhalte \_                                                | Legen Sie den Audiomischungsmodus für Dies fest.                                       | [**SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode) |
| Änderung \_ des \_ Videopräsentationsmodus \_                                                         | Legen Sie den Seitenverhältnismodus auf Widescreen, Letterbox oder Pan Scan fest.             | [**Wählen SieVideoModeVorbereiten aus.**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectvideomodepreference)                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



