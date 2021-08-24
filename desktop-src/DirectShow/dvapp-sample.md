---
description: DVApp-Beispiel
ms.assetid: 80375170-d0d6-4371-abe3-078703e158b1
title: DVApp-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72067c04e108354c1706690bc71e8b339ad5af071c46cc0e4102ae10e9a3643f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148723"
---
# <a name="dvapp-sample"></a>DVApp-Beispiel

## <a name="description"></a>Beschreibung

Dv-Erfassungsanwendung (Digital Video).

In diesem Beispiel wird veranschaulicht, wie verschiedene Arten von Filterdiagrammen zum Steuern von DV-Dv-Diagrammen entwickelt werden. Außerdem wird gezeigt, wie Sie erfassungs-, vorschau-, übertragungs- und gerätesteuerung mit einem DV-Dvd ausführen.

### <a name="usage"></a>Verbrauch

Die DVApp-Anwendung unterstützt die folgenden Modi:

-   Vorschau: Rendert DV aus dem Dv in ein Videofenster.
-   DV in Typ-1-Datei: Erfasst DV-Daten aus dem 1. Typ in einer DV-Datei vom Typ 1.
-   Type-1-Datei an DV: Überträgt Daten aus einer Typ-1-DV-Datei an den Virus.
-   DV in Typ-2-Datei: Erfasst DV-Daten aus dem -Programm in einer TYP-2-DV-Datei.
-   Type-2-Datei an DV: Überträgt Daten aus einer Typ-2-DV-Datei an den Virus.

Der Erfassungs- und Übertragungsmodus führt auch eine Vorschau aus. Jeder dieser Modi verfügt auch über die **Option Keine** Vorschau, wodurch die Vorschau deaktiviert wird. Das Erfassen ohne Vorschau ist effizienter und kann die Anzahl der gelöschten Frames reduzieren.

Die Anwendung wird im Vorschaumodus gestartet. Um einen anderen Modus auszuwählen, wählen Sie im Menü **Graphmodus einen Modus** aus. Für jeden Modus erstellt DVApp ein Filterdiagramm, das die Funktionalität dieses Modus unterstützt. Um das Diagramm als GraphEdit-Datei (GRF) zu speichern, wählen Sie im Menü Datei die Option **Diagramm** in **Datei speichern** aus. Beenden Sie DVApp, bevor Sie die Datei in GraphEdit öffnen.

So erfassen Sie eine Datei:

1.  Wählen Sie **im Menü** Datei die Option **Ausgabedatei festlegen aus,** und geben Sie einen Dateinamen ein.
2.  Wählen Sie **im Menü Graphmodus** einen *DV* in den Dateimodus aus (geben Sie 1 oder 2 ein, mit oder ohne Vorschau).
3.  Klicken Sie **auf Aufzeichnen.**
4.  Klicken Sie auf Wiedergabe, wenn sich der 100-000-2016-Modus **im VTR-Modus befindet.**
5.  Klicken Sie auf Beenden, um die Erfassung **zu beenden.**

So übertragen Sie aus einer Datei an den Virus:

1.  Klicken Sie **im Menü** Datei auf **Eingabedatei festlegen,** und wählen Sie eine DV-Datei aus. Die Datei muss mit dem ausgewählten Modus übereinstimmen (Typ 1 oder Typ 2).
2.  Wählen Sie **im Menü Diagrammmodus** eine Datei im *DV-Modus* aus (geben Sie 1 oder 2 ein, mit oder ohne Vorschau).
3.  Klicken Sie auf **Wiedergabe**.
4.  Klicken Sie zum Aufzeichnen der Daten auf Band **auf Aufzeichnen.**
5.  Klicken Sie auf Beenden, um die Übertragung **zu beenden.**

Wenn sich das Programm im VTR-Modus befindet, kann der Benutzer den Transportmechanismus über die VCR-Schaltflächen der Anwendung steuern. Um das Band zu suchen, geben Sie den Zielzeitcode ein, und klicken Sie auf die Schaltfläche "Suchen".

Um zu begrenzen, wie viele Daten die Anwendung erfasst, wählen Sie **im** Menü Datei die **Option Größe erfassen** aus.

Wählen Sie zum Überprüfen des Bandformats (NTSC oder PAL) im **Menü** Optionen die Option **Band überprüfen** aus.

Um die Größe des Vorschaufensters zu ändern,  wählen Sie im Menü Optionen die Option **Decodierungsgröße** ändern aus.

### <a name="programming-notes"></a>Programmierhinweise

Der Hauptzweck dieser Anwendung besteht in der Erstellung verschiedener DV-Erfassungs- und Übertragungsdiagramme.

### <a name="device-arrival-and-removal"></a>Ankunft und Entfernung des Geräts

Die Anwendung verarbeitet das Ein- und Entfernen von Geräten mithilfe von zwei verschiedenen Techniken. Bei Der Geräteanlauf reagiert die Nachrichtenschleife der Anwendung auf WM \_ DEVICECHANGE-Nachrichten. Beim Entfernen des Geräts antwortet die Anwendung auf [**EC \_ DEVICE \_ LOST-Ereignisse**](ec-device-lost.md) vom Filtergraph-Manager. Beide Ansätze funktionieren, obwohl das EC DEVICE LOST-Ereignis vom Vorhandensein des Geräts \_ \_ im Filterdiagramm abhängt.

Die Anwendung verarbeitet immer nur ein Gerät gleichzeitig. Wenn das aktuelle Gerät entfernt wird, sucht die Anwendung nach einem anderen DV-Gerät im System.

Bei einigen DV-Dvds muss der Benutzer das Gerät beim Wechseln zwischen Kameramodus und VTR-Modus abschalten, wodurch eine Nachricht ausgelöst wird, bei der das Gerät verloren geht. Die Anwendung antwortet, indem sie die entsprechenden Menübefehle aktivieren oder deaktivieren. Wenn der Benutzer jedoch schnell zwischen den Modi umschaltet, generiert der Laptops möglicherweise keine Gerät verloren gegangene Nachricht. Sie können erzwingen, dass die Menüs aktualisiert werden, indem **Sie** im Menü Optionen die **Option Aktualisierungsmodus** auswählen. Einige DV-Dv-Modi können den Modus umschalten, ohne abgeschaltet zu werden, aber eine Gerätemeldung senden, die verloren gegangen ist, nur wenn sie in den VTR-Modus wechseln.

### <a name="device-control"></a>Gerätesteuerung

Die Funktionalität der Schaltflächen **"Wiedergabe"** und **"Aufzeichnen"** hängt vom aktuellen Modus ab:

-   Vorschau: Das Filterdiagramm wird automatisch ausgeführt. Die **Wiedergabeschaltfläche** startet den Transport.
-   In Datei erfassen: Die **Schaltfläche Datensatz** führt das Diagramm aus, und die **Schaltfläche** Wiedergabe startet den Transport.
-   An Gerät übertragen: Die **Wiedergabeschaltfläche** führt das Diagramm aus, und die **Schaltfläche Datensatz** startet den Transport.

Die Beispielanwendung führt keine framegenaue Erfassung durch. An verschiedenen Punkten ruft die Anwendung die **Sleep-Funktion** auf, um auf die Antwort des Geräts zu warten. Neuere DV-Dv-Dv-Geräte senden eine Benachrichtigung, wenn sich der Zustand des Geräts ändert. Ältere Geräte unterstützen möglicherweise keine Benachrichtigungen. Im Rahmen eines Beispiels ist der Aufruf von **Sleep** eine einfachere Lösung.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Um die DirectShow SDK-Beispiele herunterzuladen, installieren Sie die neueste Version von [Windows SDK.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Dieses Beispiel wird unter dem folgenden Pfad installiert: *\[ SDK \] Root* Samples Multimedia \\ \\ \\ DirectShow Capture \\ \\ DVApp.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern eines DV-Dvd](controlling-a-dv-camcorder.md)
</dt> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



