---
description: Diese Beispielanwendung veranschaulicht die Stream-Dämpfung, indem ein Media Player implementiert wird, der das vom System bereitgestellte Standardverhalten zur Dämpfung anzeigt, Abschrägeereignisse abbestellen und eine benutzerdefinierte Behandlung implementiert, wenn Abschrägeereignisse empfangen werden.
ms.assetid: 667c8751-1d17-4b59-8ced-ed5f0c333ae9
title: EntenmedienMedienplayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab5a469ec2a7fb1551980d0a08a758e8e8e8f522831dc2148b2d8fb222ecdfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828281"
---
# <a name="duckingmediaplayer"></a>EntenmedienMedienplayer

Diese Beispielanwendung veranschaulicht die Stream-Dämpfung, indem ein Media Player implementiert wird, der das vom System bereitgestellte Standardverhalten zur Dämpfung anzeigt, Abschrägeereignisse abbestellen und eine benutzerdefinierte Behandlung implementiert, wenn Abschrägeereignisse empfangen werden. Dieses Beispiel muss bei der Konjuktion mit ["EntschnaufenCaptureSample"](duckingcapturesample.md)verwendet werden. Weitere Informationen zum Entschnaufen oder zur Streamentschlangenung finden Sie unter [Default Ducking Experience](stream-attenuation.md).

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>Beschreibung

In diesem Beispiel werden die folgenden Features veranschaulicht.

-   DirectShow zum Wiedergeben einer Mediendatei.
-   [WASAPI](wasapi.md) für die Streamverwaltung und Behandlung von Ablageereignissen.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist an den folgenden Speicherorten verfügbar.



| Standort    | Pfad/URL                                                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|
| Windows SDK | \\Program Files \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Multimedia Audio \\ \\ \\ CardsingMediaPlayer \\ ... |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

Verwenden Sie die folgenden Schritte, um das Beispiel "DuckingMediaPlayer" zu erstellen:

1.  Öffnen Sie in Visual Studio 2008 die Datei "TigeringMediaPlayer.sln".
2.  Wählen Sie im Fenster die Konfiguration **Debug-** oder **Releaselösung** aus, wählen Sie in der Menüleiste das Menü **Erstellen** und dann die Option **Erstellen** aus. Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, haben Visual Studio keinen Zugriff auf die SDK-Buildumgebung. In diesem Fall wird das Beispiel nur erstellt, wenn Sie die Umgebungsvariable MSSdk explizit festlegen, die in der Projektdatei "EntwirftMediaPlayer.vcproj" verwendet wird.

## <a name="running-the-sample"></a>Ausführen des Beispiels

Wenn Sie die Anwendung erfolgreich erstellen, wird eine ausführbare Datei DuckingMediaPlayer.exe generiert. Um es auszuführen, wählen **Sie Debuggen starten** oder **Ohne Debuggen starten** aus dem Menü **Debuggen** aus, oder geben Sie `DuckingMediaPlayer` in einem Befehlsfenster ein.

Um eine Demonstration der Verzungung anzuzeigen, müssen Sie Gleichzeitig Die Entenmedienplayer und EntencaptureSample ausführen. Das EntenencaptureSample öffnet einen Kommunikationsdatenstrom und signalisiert dem System, ein Entenereignis zu generieren. Der DuckingMediaPlayer wird vom System benachrichtigt, wenn ein Entenereignis auftritt, und der Media Player führt die vom Benutzer angeforderte Aktion aus.

So deaktivieren Sie das Verhalten beim Abschalten:

1.  Wählen Sie im Fenster "EntriegelungCaptureSample" die Option **Standardeingabegerät verwenden** aus, und klicken Sie auf **Starten,** um eine Aufzeichnungssitzung vom Kommunikationsgerät aus zu starten.
2.  Wählen Sie auf dem TigeringMediaPlayer eine Mediendatei aus, die wiedergegeben werden soll, und geben Sie die Entenoption **Abwählen von Entleeren an.**

Beachten Sie, dass die Mediendatei ohne Unterbrechung wiedergegeben wird. Die Ereignisse, die vom System beim Öffnen des Kommunikationsdatenstroms generiert werden, werden ignoriert.

Gehen Sie wie folgt vor, um das vom System bereitgestellte Standardverhalten zu veranschaulichen:

1.  Wählen Sie in der Systemsteuerung die Option **Sounds** aus. Wählen Sie auf der Registerkarte **Kommunikation** die Option **Lautstärke anderer Sounds um 80 % reduzieren** aus.
2.  Wählen Sie im Fenster "EntriegelungCaptureSample" die Option **Standardeingabegerät verwenden** aus, und klicken Sie auf **Starten,** um eine Aufzeichnungssitzung vom Kommunikationsgerät aus zu starten.
3.  Wählen Sie auf dem MultiplayeringMediaPlayer eine Mediendatei aus, die wiedergegeben werden soll, ohne eine der Entzungsoptionen auszuwählen.
4.  Klicken Sie im Fenster "EntkapselungCaptureSample" auf **Beenden,** um den Kommunikationsstream zu beenden.

Beachten Sie, dass beim Öffnen des Kommunikationsdatenstroms durch "EntleerenCaptureSample" die von "TigeringMediaPlayer" wiedergegebene Mediendatei ohne Unterbrechung wiedergegeben wird, die Volumeebene jedoch herabgesetzt wird. Wenn die Kommunikationssitzung beendet wird, wird das Volume auf die ursprüngliche Einstellung zurückgesetzt. Dieses Stream-Dämpfungsverhalten ist das Standardverhalten, das vom System implementiert wird.

So zeigen Sie ein benutzerdefiniertes, vom Media Player implementiertes Verhalten an:

1.  Wählen Sie im Fenster "EntriegelungCaptureSample" die Option **Standardeingabegerät verwenden** aus, und klicken Sie auf **Starten,** um eine Aufzeichnungssitzung vom Kommunikationsgerät aus zu starten.
2.  Wählen Sie auf dem EntensingMediaPlayer eine mediendatei aus, die wiedergegeben werden soll, und geben Sie die Entenoption als **Pause on Ente** an.
3.  Klicken Sie im Fenster "EntkapselungCaptureSample" auf **Beenden,** um den Kommunikationsstream zu beenden.

Beachten Sie, dass beim Öffnen des Kommunikationsdatenstroms durch Die EntleerungCaptureSample die mediendatei, die von EinemMediaPlayer wiedergegeben wird, angehalten wird. Die Wiedergabe wird fortgesetzt, wenn die Kommunikationssitzung beendet wird. Dieses Streamentschlangenverhalten ist das vom Media Player implementierte Abschlangenverhalten.

Der Entenmedienplayer veranschaulicht auch, wie die Volumesteuerung für jede Anwendung in den Volumemixer integriert wird.

Weitere Informationen zur Streamentschlangenfunktion finden Sie unter [Default Ducking Experience](stream-attenuation.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele, die die Kernaudio-APIs verwenden](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



