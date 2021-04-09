---
description: Diese Beispielanwendung veranschaulicht das Öffnen und Schließen von Kommunikationsstreams und bewirkt, dass Ducking-Ereignisse auftreten, die eine Anwendung zum Implementieren der Datenstrom Dämpfung erhalten kann.
ms.assetid: 9a2131b2-ec4a-492a-a277-bd26ec8d67e5
title: Duckingcapturesample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 636fe39e8fa27beee14ab17548f5929d1d937b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861691"
---
# <a name="duckingcapturesample"></a>Duckingcapturesample

Diese Beispielanwendung veranschaulicht das Öffnen und Schließen von Kommunikationsstreams und bewirkt, dass Ducking-Ereignisse auftreten, die eine Anwendung zum Implementieren der Datenstrom Dämpfung erhalten kann. Diese Anwendung implementiert einen Chat Client, der kernaudioapis verwendet, um Audiodaten von einem Kommunikationsgerät zu lesen und auf dem Ausgabegerät wiederzugeben.

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>BESCHREIBUNG

In diesem Beispiel werden die folgenden Funktionen veranschaulicht.

-   [Mmdevice-API](mmdevice-api.md) für die Enumeration und Auswahl von Multimedia-Geräten.
-   [WASAPI](wasapi.md) für den Zugriff auf Kommunikations Erfassungs-und Rendering-Geräte, streamverwaltungsvorgänge und Behandlung von Ducking-Ereignissen.
-   [Wave-APIs](/previous-versions//ms713499(v=vs.85)) für den Zugriff auf das Kommunikationsgerät und das Erfassen von Audioeingaben.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio 2008                                             |           |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist in den folgenden Speicherorten verfügbar.



| Standort    | Pfad/URL                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ Audiodatei \\ duckingcapturesample \\ ... |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

Führen Sie die folgenden Schritte aus, um das Beispiel "duckingcapturesample" zu erstellen:

1.  Öffnen Sie die Datei "duckingcapturesample. sln" in Visual Studio 2008.
2.  Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus. Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung. In diesem Fall wird das Beispiel nicht erstellt, es sei denn, Sie legen die Umgebungsvariable "Mssdk", die in der Projektdatei verwendet wird, "duckingcapturesample. vcproj" explizit fest.

## <a name="running-the-sample"></a>Ausführen des Beispiels

Wenn Sie die Anwendung erfolgreich erstellen, wird eine ausführbare Datei (DuckingCaptureSample.exe) generiert. Um es auszuführen, wählen Sie im Menü **Debuggen** die Option **Debugging starten** oder **Starten ohne Debuggen** aus, oder geben Sie `DuckingCaptureSample` ein Befehlsfenster ein

"Duckingcapturesample" bietet dem Benutzer zwei Implementierungen zum Erfassen von Audiodaten über das Standard Konsolen Gerät: WASAPI-und Wave-APIs. Wählen Sie zum Starten einer Aufzeichnungs Sitzung einen Modus aus, und klicken Sie auf der Benutzeroberfläche der Anwendung auf **Start** . Um die Sitzung zu beenden, klicken Sie auf **Beenden**. Abhängig vom Gerät, das vom Benutzer angegeben wird (Eingabe oder Ausgabe), verwendet die Anwendung die mmdevice-API, um einen Verweis auf das standardmäßige Rendering-oder Aufzeichnungs Kommunikationsgerät zu erhalten. Nachdem der Benutzer eine Chatsitzung gestartet hat, führt die Anwendung die folgenden Aufgaben aus:

-   Erstellt und initialisiert einen AudioClient im ereignisgesteuerten Modus.
-   Verknüpft den Client mit dem Ereignis handle, das signalisiert, dass die Beispiele für die Erfassung oder das Rendering bereit sind.
-   Richtet einen Erfassungs Client und einen renderingclient für den Transport ein.
-   Erstellt den chatthread und startet die Audioengine.

Zum Erfassen von Audiodaten verwendet das Beispiel den Erfassungs Client, um die Gesamtmenge der aufgezeichneten Daten, die im Puffer verfügbar ist, zu lesen, Daten vom Standardeingabe Gerät zu lesen und das Paket freizugeben und den Puffer zum Lesen des nächsten Satzes erfasster Daten verfügbar zu machen.

Zum Rendern bestimmt die Anwendung die Menge der Daten, die in die Warteschlange eingereiht werden, um im Erfassungs Endpunkt Puffer wiederzugeben. Entsprechend schreibt Sie in den Puffer und gibt den Puffer als Vorbereitung für den nächsten Verarbeitungs Durchlauf frei, bis alle Daten geschrieben wurden. Zum Rendern werden automatische Rahmen vorgerendert, um zu verhindern, dass die Audioengine beim Start einen Fehler verursacht. "Duckingcapturesample" zeigt auch, wie der Rendering-Stream aus dem volumemixer ausgeblendet wird.

Weitere Informationen zur Datenstrom Dämpfung finden [Sie unter Verwenden eines kommunikationsgeräts](using-the-communication-device.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele für die Verwendung der kernaudioapis](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 
