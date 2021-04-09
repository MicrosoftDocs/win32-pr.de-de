---
description: Dvapp-Beispiel
ms.assetid: 80375170-d0d6-4371-abe3-078703e158b1
title: Dvapp-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86653781d08921bf638e7798fb34f3a86e8d34a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124826"
---
# <a name="dvapp-sample"></a>Dvapp-Beispiel

## <a name="description"></a>BESCHREIBUNG

Digital Video (DV) Capture-Anwendung.

In diesem Beispiel wird veranschaulicht, wie verschiedene Arten von Filter Diagrammen zum Steuern von DV-Camcordern erstellt werden. Außerdem wird gezeigt, wie Sie mit einem DV-Camcorder die Erfassung, Vorschau, Übertragung und Gerätesteuerung durchführen.

### <a name="usage"></a>Verbrauch

Die dvapp-Anwendung unterstützt die folgenden Modi:

-   Vorschau: rendert DV vom Camcorder in ein Videofenster.
-   DV-zu-1-Datei: Hiermit werden DV-Daten vom Camcorder in eine Type-1-DV-Datei erfasst.
-   Type-1 Datei in DV: überträgt Daten aus einer DV-Datei vom Typ 1 an den Camcorder.
-   DV in Type-2 file: zeichnet DV-Daten vom Camcorder bis zu einer Type-2-DV-Datei auf.
-   Type-2 Datei in DV: überträgt Daten aus einer DV-Datei vom Typ 2 an den Camcorder.

Die Aufzeichnungs-und Übertragungsmodi führen ebenfalls eine Vorschau aus. Jeder dieser Modi verfügt ebenfalls über eine **Vorschau** Option, mit der die Vorschau deaktiviert wird. Die Erfassung ohne Vorschau ist effizienter und kann die Anzahl der gelöschten Frames verringern.

Die Anwendung wird im Vorschaumodus gestartet. Wenn Sie einen anderen Modus auswählen möchten, wählen Sie im Menü **Diagramm Modus** einen Modus aus. Für jeden Modus erstellt dvapp ein Filter Diagramm, das die Funktionalität dieses Modus unterstützt. Um das Diagramm als GraphEdit-Datei (. GRF) zu speichern, wählen Sie im Menü **Datei** die Option **Diagramm in Datei speichern** aus. Beenden Sie dvapp, bevor Sie die Datei in GraphEdit öffnen.

So erfassen Sie in einer Datei:

1.  Wählen Sie im Menü **Datei** die Option **Ausgabedatei festlegen** aus, und geben Sie einen Dateinamen ein.
2.  Wählen Sie im Menü **Diagramm Modus** einen *DV-zu-Datei* -Modus aus (Typ 1 oder Typ 2, mit oder ohne Vorschau).
3.  Klicken Sie auf **Datensatz**.
4.  Wenn sich der Camcorder im VTR-Modus befindet **, klicken Sie** auf wiedergeben.
5.  Klicken Sie auf " **Abbrechen**", um die Erfassung anzuhalten.

So übertragen Sie aus einer Datei an den Camcorder:

1.  Klicken Sie im Menü **Datei** auf **Eingabedatei festlegen** , und wählen Sie eine DV-Datei aus. Die Datei muss mit dem ausgewählten Modus (Typ 1 oder Typ 2) identisch sein.
2.  Wählen Sie im Menü **Diagramm Modus** eine *Datei in den DV* -Modus aus (Typ 1 oder Typ 2, mit oder ohne Vorschau).
3.  Klicken Sie auf **Wiedergabe**.
4.  Klicken Sie auf **Datensatz**, um die Daten auf Band aufzuzeichnen.
5.  Klicken Sie auf " **Abbrechen**", um die Übertragung anzuhalten

Wenn sich der Camcorder im VTR-Modus befindet, kann der Benutzer den Transportmechanismus über die Schaltflächen im VCR-Stil der Anwendung steuern. Um das Band zu suchen, geben Sie den zieltimecode ein, und klicken Sie auf die Schaltfläche Suchen.

Wählen Sie im Menü **Datei** die Option **Größe erfassen** aus, um die von der Anwendung erfassten Daten einzuschränken.

Wählen Sie im Menü **Optionen die Option** **Band überprüfen** aus, um das Band Format (NTSC oder PAL) zu überprüfen.

Um die Größe des Vorschaufensters zu ändern, wählen Sie im Menü Optionen die **Option** **decodiergröße ändern** aus.

### <a name="programming-notes"></a>Programmier Hinweise

Der Hauptzweck dieser Anwendung besteht darin, zu zeigen, wie verschiedene DV-Erfassungs-und-Übertragungs Diagramme erstellt werden.

### <a name="device-arrival-and-removal"></a>Geräte Ankunft und-Entfernung

Die Anwendung übernimmt das eintreffen und Entfernen von Geräten mit zwei verschiedenen Techniken. Beim Eintreffen des Geräts antwortet die Nachrichten Schleife der Anwendung auf die "WM \_ devicechange"-Meldungen. Zum Entfernen des Geräts antwortet die Anwendung auf Ereignisse des EC-Geräts, die vom Filter Graph-Manager [**\_ \_ verloren gehen**](ec-device-lost.md) . Beide Ansätze sind funktionsfähig, obwohl das Ereignis "EC- \_ Gerät \_ verloren" davon abhängt, dass das Gerät im Filter Diagramm vorhanden ist.

Die Anwendung verarbeitet jeweils nur ein Gerät. Wenn das aktuelle Gerät entfernt wird, sucht die Anwendung im System nach einem anderen DV-Gerät.

Bei manchen DV-Camcordern muss der Benutzer das Gerät Herunterfahren, wenn es zwischen dem Kameramodus und dem VTR-Modus wechselt, wodurch eine Meldung zum Verlust von Geräten ausgelöst wird. Die Anwendung antwortet durch Aktivieren oder Deaktivieren der entsprechenden Menübefehle. Wenn der Benutzer jedoch schnell zwischen den Modi wechselt, generiert der Camcorder möglicherweise keine Geräte verlorene Nachricht. Sie können erzwingen, dass die Menüs aktualisiert werden, indem Sie im Menü **Optionen** den **Modus aktualisieren** auswählen. Einige DV-Camcorder können Modi umschalten, ohne dass Sie ausgeschaltet werden, aber eine Meldung zum Verlust von Geräten nur dann senden, wenn Sie in den VTR-Modus wechseln.

### <a name="device-control"></a>Gerätesteuerung

Die Funktionalität der Schaltfläche wieder **Gabe** und **Datensatz** hängt vom aktuellen Modus ab:

-   Vorschau: das Filter Diagramm wird automatisch ausgeführt. Die **Wiedergabe** Schaltfläche startet den Transport.
-   In Datei erfassen: die Schaltfläche **Datensatz** führt das Diagramm aus, und die **Wiedergabe** Schaltfläche startet den Transport.
-   An Gerät übertragen: die **Wiedergabe** Schaltfläche führt das Diagramm aus, und die Schaltfläche **Datensatz** startet den Transport.

Die Beispielanwendung führt keine Frame genaue Erfassung aus. An verschiedenen Punkten **Ruft die Anwendung** die Standbyfunktion auf, um zu warten, bis das Gerät antwortet. Neuere DV-Camcorder senden eine Benachrichtigung, wenn sich der Status des Geräts ändert. Ältere Geräte unterstützen möglicherweise keine Benachrichtigung. im Rahmen eines Beispiels ist das Aufrufen von **Sleep** eine einfachere Lösung.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK Root \]* \\ Samples \\ Multimedia \\ DirectShow \\ Capture \\ dvapp.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern eines DV-Camcorder](controlling-a-dv-camcorder.md)
</dt> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



