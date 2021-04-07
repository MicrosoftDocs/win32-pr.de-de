---
description: DVD-Befehle
ms.assetid: 1204c73e-c3de-4488-8ee3-e76edbf72da0
title: DVD-Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bf06127ab3829ed6cdcbbb70c3b2c1d1b41cf0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747144"
---
# <a name="dvd-commands"></a>DVD-Befehle

Die DVD-Navigations-und Wiedergabe Befehle sind in einem Abschnitt der DVD-Spezifikation mit dem Namen Anhang J definiert, weshalb die DirectShow-Dokumentation häufig auf "Anhang J-Befehle" verweist. Die in Anhang J angegebenen Namen sind jedoch nicht immer sehr intuitiv, sodass DirectShow Namen verwendet, die möglicherweise leichter zu verstehen sind.

In der folgenden Tabelle sind die Anhang J-Befehle und deren DirectShow-Entsprechungen aufgelistet.



| Anhang J-Befehl                                                                           | BESCHREIBUNG                                                                  | IDvdControl2-Methode                                                                           |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| Titel \_ Wiedergabe                                                                               | Geben Sie einen Titel ein.                                                                | [**Playtitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playtitle)                                                   |
| PTT-wieder \_ Gabe                                                                                 | Wiedergeben eines Kapitels in einem Titel.                                                   | [**Playchapterintitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapterintitle)                                 |
| \_Wiedergabezeit                                                                                | Wiedergeben eines Titels ab einem bestimmten Zeitpunkt.                                 | [**Playattimeingetitle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattimeintitle)                                   |
| Stop                                                                                      | Wiedergabe wird beendet.                                                               | [**Stop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stop)                                                             |
| Gruppe                                                                                      | Kehren Sie von einem Untermenü zum übergeordneten Menü zurück.                                    | [**Returnfromsubmenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-returnfromsubmenu)                                   |
| Zeit \_ Suche                                                                              | Wiedergabe zu einem bestimmten Zeitpunkt innerhalb des aktuellen Titels.                           | [**Playattime**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playattime)                                                 |
| PTT- \_ Suche                                                                               | Wiedergeben eines Kapitels innerhalb des aktuellen Titels.                                     | [**Playchapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchapter)                                               |
| Prevpg- \_ Suche                                                                            | Wechseln Sie zum Anfang des vorherigen Kapitels, und setzen Sie die Wiedergabe fort.                 | [**Playprevchapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playprevchapter)                                       |
| Nach-unten- \_ Suche                                                                             | Wechseln Sie zum Anfang des aktuellen Kapitels, und setzen Sie die Wiedergabe fort.                  | [**Replaychapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-replaychapter)                                           |
| Nextpg- \_ Suche                                                                            | Wechseln Sie zum Anfang des nächsten Kapitels, und setzen Sie die Wiedergabe fort.                     | [**Playnextchapter**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playnextchapter)                                       |
| Forward- \_ Scan                                                                             | Wiedergabe an einer angegebenen Wiedergabe Rate. Die Standard Wiedergabe Rate ist 1,0. | [**Playforward**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playforwards)                                             |
| Rückwärts \_ Überprüfung                                                                            | Wiedergabe mit einer angegebenen Wiedergabe Rate.                                  | [**Playrückwärts**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playbackwards)                                           |
| Menü \_ Befehl                                                                                | Anzeigen eines Menüs                                                                 | [**Showmenu**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-showmenu)                                                     |
| Fortsetzen                                                                                    | Aus einem Menü zurückkehren und Wiedergabe fortsetzen.                                      | [**Fortsetzen**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-resume)                                                         |
| Obere \_ Schaltfläche \_ SELECT, untere \_ Schaltfläche \_ SELECT, Left \_ Button \_ SELECT, Right \_ Button \_ SELECT | Wählen Sie eine Schaltfläche aus, deren Position relativ zur aktuell ausgewählten Schaltfläche ist. | [**Selectbutton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectbutton)                                             |
| Schaltflächen \_ Aktivierung                                                                          | Aktiviert die ausgewählte Schaltfläche.                                                | [**Activatebutton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton)                                         |
| Schaltfläche \_ auswählen \_ und \_ aktivieren                                                             | Aktivieren und aktivieren Sie eine Schaltfläche.                                                | [**Selectandactivatebutton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton)                       |
| Immer noch \_ aus                                                                                | Wiedergabe fortsetzen, wenn ein Bild angezeigt wird.                               | [**Stilloff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff)                                                     |
| Anhalten \_ am                                                                                 | Wiedergabe anhalten.                                                              | [**Anhalten**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| Anhalten \_                                                                                | Wiedergabe im angehaltenen Zustand fortsetzen.                                       | [**Anhalten**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-pause)                                                           |
| Menü \_ Sprache \_ auswählen                                                                    | Wählen Sie die Sprache für Menüs aus.                                               | [**Selectdefaultmenulanguage**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectdefaultmenulanguage)                   |
| \_ \_ Audiostreamänderung                                                                     | Legen Sie den Audiodatenstrom fest.                                                        | [**Selectaudiostream**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectaudiostream)                                   |
| Änderung des untergeordneten Bild \_ Stroms \_                                                               | Legen Sie den subbildstream fest. Aktivieren oder Deaktivieren der Anzeige des Teil Bilds.             | [**Selectsubpicturestream**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectsubpicturestream)                         |
| Winkel \_ Änderung                                                                             | Legen Sie den Kamerawinkel fest.                                                        | [**Selectangle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle)                                               |
| Auswahl der Jugend \_ Stufe \_                                                                   | Legen Sie die elternebene fest.                                                      | [**Selectparser-allevel**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentallevel)                               |
| Eltern \_ Land \_ auswählen                                                                 | Legen Sie Land/Region für die Eltern Verwaltung fest.                              | [**Selectpartalcountry**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectparentalcountry)                           |
| Änderung des Karaoke \_ - \_ audiopräsentations \_ Modus \_                                                | Legen Sie den audiomischungs Modus für Karaoke fest.                                       | [**Selectkaraokeaudiopresentationmode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode) |
| Änderung des Video \_ Präsentations \_ Modus \_                                                         | Legen Sie den Seitenverhältnis Modus auf "Widescreen", "Letterbox" oder "Pan Scan" fest.             | [**Selectvideomodebug-Präferenz**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectvideomodepreference)                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



