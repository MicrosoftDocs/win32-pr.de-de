---
title: Benutzeroberfläche des mciwnd-Fensters
description: Benutzeroberfläche des mciwnd-Fensters
ms.assetid: 422c5acb-bce5-4be2-96ba-5ab7f9dcc826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98c0b11b6868828625c6c6e605f005fe842d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036578"
---
# <a name="mciwnd-window-user-interface"></a>Benutzeroberfläche des mciwnd-Fensters

Mciwnd bietet zusätzliche Features zum Anpassen des Erscheinungsbild des mciwnd-Fensters, zum Anpassen des Verhaltens der Anwendung und zum Optimieren der Wiedergabe Leistung. Im mciwnd-Fenster sind folgende Features enthalten:

-   Eine Symbolleiste **mit** **Menü** Schaltflächen zum wiedergeben, **Abbrechen**, **aufzeichnen**
-   Eine TrackBar, die die Positionierung innerhalb des Wiedergabe Inhalts steuert.
-   Ein Popup Menü mit allgemeinen Befehlen
-   Ein Wiedergabe Bereich für Videos und andere Geräte, die Bilder anzeigen

In der folgenden Abbildung wird der anfängliche Status der benutzergesteuerten Videowiedergabe dargestellt. Die Beispieldatei wird CLOCK.AVI verwendet.

![Bild clock.avi](images/mciwnd1.gif)

Das mciwnd-Fenster enthält einen Wiedergabe Bereich für Videos und andere Geräte, auf denen Bilder während der Wiedergabe angezeigt werden. Mciwnd lässt den Wiedergabe Bereich von Waveform-Audiogeräten, von MIDI-Sequencern und anderen Geräten aus, die nicht in die Anzeige schreiben. In der folgenden Abbildung wird der Wiedergabe Bereich von Waveform-Audiodaten gezeigt.

![Bild des mciwnd-Fensters](images/mciwnd4.gif)

Die **Wiedergabe** Schaltfläche befindet sich in der unteren linken Ecke des mciwnd-Fensters. Sie wird angezeigt, wenn der Inhalt angehalten wird. Der Benutzer kann den Inhalt auf folgende Weise wiedergeben:

-   Um den Inhalt von der aktuellen Wiedergabe Position wiederzugeben, wählen Sie **die Wiedergabe Schaltfläche aus** .
-   Um den Inhalts Vollbild von der aktuellen Wiedergabe Position wiederzugeben, wählen Sie **die Wiedergabe Schaltfläche aus** , während Sie die STRG-Taste gedrückt halten.
-   Um den Inhalt von der aktuellen Wiedergabe Position rückwärts wiederzugeben, wählen Sie **die Wiedergabe Schaltfläche aus** , während Sie die UMSCHALTTASTE gedrückt halten.

Mit der **Menü** Schaltfläche neben der **Wiedergabe** Schaltfläche wird ein Menü aktiviert, das es dem Benutzer ermöglicht, Audiovideo-überlappende (AVI)-Dateien zu öffnen und zu schließen und die Bildgröße, Wiedergabegeschwindigkeit und das Volume anzupassen. (Der Benutzer kann das Menü auch aktivieren, indem er immer dann auf die Rechte Maustaste klickt, wenn sich der Cursor im Client Bereich des Fensters befindet.) Das Menü enthält auch Befehle, mit denen Sie die Konfiguration des aktuellen Geräts ändern, den Wiedergabe Inhalt in die Zwischenablage kopieren und MCI-Befehle ausgeben können.

Die TrackBar rechts neben der **Menü** Schaltfläche stellt die Dauer des Wiedergabe-(oder aufgezeichneten) Inhalts dar. Der Schieberegler auf der TrackBar stellt die aktuelle Wiedergabe Position innerhalb des Inhalts dar. Wenn sich der Schieberegler am linken Ende der Trackleiste befindet, ist die aktuelle Wiedergabe Position der Anfang des Inhalts. Der Benutzer kann an verschiedene Positionen im Inhalt wechseln, indem er den Schieberegler entlang der TrackBar zieht. Die Schaltfläche " **Abbrechen** " befindet sich in der unteren linken Ecke des mciwnd-Fensters. Sie wird angezeigt, wenn der Inhalt wiedergegeben wird. In der folgenden Abbildung wird die Wiedergabe des Videos gezeigt.

![Videowiedergabe Bild](images/mciwnd2.gif)

Die mciwnd-Steuerelemente können auch eine **Datensatz** -Schaltfläche für Geräte enthalten, die aufzeichnen können. Die Schaltfläche **Datensatz** ist mit einem roten Kreis gekennzeichnet und wird nur angezeigt, wenn das Gerät aufgezeichnet werden kann.

> [!Note]  
> Das Wiedergabe Fenster muss an einer Grenze von vier Pixeln ausgerichtet werden, um die beste Videowiedergabe Leistung zu erzielen. In der Regel richtet Windows das Fenster automatisch aus, wenn es erstellt wird. Wenn ein Benutzer das Fenster von seiner ursprünglichen Position aus bewegt oder verschiebt, wird die Videowiedergabegeschwindigkeit möglicherweise um die Hälfte reduziert.

 

 

 




