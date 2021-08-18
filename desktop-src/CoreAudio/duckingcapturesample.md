---
description: Diese Beispielanwendung veranschaulicht das Öffnen und Schließen von Kommunikationsdatenströmen und das Verursachen von Veraltungsereignissen, die eine Anwendung erhalten kann, um die Streamenuierung zu implementieren.
ms.assetid: 9a2131b2-ec4a-492a-a277-bd26ec8d67e5
title: TigeringCaptureSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76515f9d20e31bf4583b715e09da38c29bfdac34f6c975087f64bf2617696542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018458"
---
# <a name="duckingcapturesample"></a>TigeringCaptureSample

Diese Beispielanwendung veranschaulicht das Öffnen und Schließen von Kommunikationsdatenströmen und das Verursachen von Veraltungsereignissen, die eine Anwendung erhalten kann, um die Streamenuierung zu implementieren. Diese Anwendung implementiert einen Chatclient, der Core Audio-APIs verwendet, um Audiodaten von einem Kommunikationsgerät zu lesen und auf dem Ausgabegerät wiederzugeben.

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>BESCHREIBUNG

In diesem Beispiel werden die folgenden Features veranschaulicht.

-   [MMDevice-API](mmdevice-api.md) für multimediale Geräteenumeration und -auswahl.
-   [WASAPI](wasapi.md) für den Zugriff auf das Kommunikationserfassungs- und -rendergerät, Datenstromverwaltungsvorgänge und die Behandlung von Abfangensereignissen.
-   [WAVE-APIs](/previous-versions//ms713499(v=vs.85)) für den Zugriff auf das Kommunikationsgerät und die Erfassung von Audioeingaben.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio 2008                                             |           |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist an den folgenden Speicherorten verfügbar.



| Standort    | Pfad/URL                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Program Files \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Multimedia Audio \\ \\ \\ EntleerenCaptureSample \\ ... |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

Verwenden Sie die folgenden Schritte, um das Beispiel "DuckingCaptureSample" zu erstellen:

1.  Öffnen Sie die Datei "TigeringCaptureSample.sln" in Visual Studio 2008.
2.  Wählen Sie im Fenster die Konfiguration **Debug-** oder **Releaselösung** aus, wählen Sie in der Menüleiste das Menü **Erstellen** und dann die Option **Erstellen** aus. Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, haben Visual Studio keinen Zugriff auf die SDK-Buildumgebung. In diesem Fall wird das Beispiel nur erstellt, wenn Sie explizit die Umgebungsvariable MSSdk festlegen, die in der Projektdatei "EntwirftCaptureSample.vcproj" verwendet wird.

## <a name="running-the-sample"></a>Ausführen des Beispiels

Wenn Sie die Anwendung erfolgreich erstellen, wird eine ausführbare Datei DuckingCaptureSample.exe generiert. Um es auszuführen, wählen **Sie Debuggen starten** oder **Ohne Debuggen starten** aus dem Menü **Debuggen** aus, oder geben Sie `DuckingCaptureSample` in einem Befehlsfenster ein.

Die EntenungCaptureSample bietet dem Benutzer zwei Implementierungen zum Erfassen von Audiodaten vom Standardkonsolengerät: WASAPI und Wave-APIs. Um eine Aufzeichnungssitzung zu starten, wählen Sie einen Modus aus, und klicken Sie auf der Benutzeroberfläche der Anwendung auf **Starten.** Klicken Sie auf **Beenden,** um die Sitzung zu beenden. Abhängig vom vom Benutzer angegebenen Gerät (Eingabe oder Ausgabe) verwendet die Anwendung die MMDevice-API, um einen Verweis auf das Standardmäßige Rendering- oder Aufzeichnungskommunikationsgerät abzurufen. Nachdem der Benutzer eine Chatsitzung gestartet hat, führt die Anwendung die folgenden Aufgaben aus:

-   Erstellt und initialisiert einen Audioclient im ereignisgesteuerten Modus.
-   Ordnet den Client dem Ereignishandle zu, das signalisiert, dass Die Stichproben für die Erfassung oder das Rendering bereit sind.
-   Richtet einen Erfassungsclient und einen Renderingclient für den Transport ein.
-   Erstellt den Chatthread und startet die Audio-Engine.

Zum Erfassen von Audiodaten verwendet das Beispiel bei jedem Verarbeitungsdurchlauf den Erfassungsclient, um die Gesamtmenge der erfassten Daten abzurufen, die im Puffer verfügbar sind, Daten vom Standardeingabegerät zu lesen, das Paket freizugeben und den Puffer zum Lesen des nächsten Satzes erfasster Daten verfügbar zu machen.

Für das Rendering bestimmt die Anwendung die Datenmenge, die in die Warteschlange eingereiht wird, um im Erfassungsendpunktpuffer wiedergegeben zu werden. Er schreibt entsprechend in den Puffer und gibt den Puffer als Vorbereitung für den nächsten Verarbeitungsdurchlauf frei, bis alle Daten geschrieben wurden. Für das Rendering werden automatische Frames vorabrolliert, um zu verhindern, dass die Audio-Engine beim Start glimmt. "HideingCaptureSample" zeigt auch, wie der Renderstream aus dem Volumemixer ausgeblendet wird.

Weitere Informationen zum Stream-Dämpfungsfeature finden Sie unter [Verwenden eines Kommunikationsgeräts.](using-the-communication-device.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele, die die Kernaudio-APIs verwenden](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 
