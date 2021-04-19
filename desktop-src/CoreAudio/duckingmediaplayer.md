---
description: In dieser Beispielanwendung wird die Datenstrom Dämpfung durch Implementieren eines Media Player veranschaulicht, der das vom System bereitgestellte standardmäßige debugierungsverhalten anzeigt, die Verarbeitung von Ducking-Ereignissen durchführt und die benutzerdefinierte Handhabung implementiert, wenn Ducking-Ereignisse empfangen werden.
ms.assetid: 667c8751-1d17-4b59-8ced-ed5f0c333ae9
title: Duckingmediaplayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86952f1aa7b81c9a7dc711f0c4f36fc8531bd63
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106367272"
---
# <a name="duckingmediaplayer"></a>Duckingmediaplayer

In dieser Beispielanwendung wird die Datenstrom Dämpfung durch Implementieren eines Media Player veranschaulicht, der das vom System bereitgestellte standardmäßige debugierungsverhalten anzeigt, die Verarbeitung von Ducking-Ereignissen durchführt und die benutzerdefinierte Handhabung implementiert, wenn Ducking-Ereignisse empfangen werden. Dieses Beispiel muss in der Konturierung mit " [duckingcapturesample](duckingcapturesample.md)" verwendet werden. Weitere Informationen über das ducken oder die streamdämpfung finden Sie unter [standardmäßige Ducking](stream-attenuation.md)-Darstellung.

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>BESCHREIBUNG

In diesem Beispiel werden die folgenden Funktionen veranschaulicht.

-   DirectShow zum Wiedergeben einer Mediendatei.
-   [WASAPI](wasapi.md) für die streamverwaltung und Behandlung von Ducking-Ereignissen.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist in den folgenden Speicherorten verfügbar.



| Standort    | Pfad/URL                                                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ \\ audiooneingmediaplayer \\ ... |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

Führen Sie die folgenden Schritte aus, um das Beispiel "duckingmediaplayer" zu erstellen:

1.  Öffnen Sie die Datei "duckingmediaplayer. sln" in Visual Studio 2008.
2.  Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus. Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung. In diesem Fall wird das Beispiel nicht erstellt, es sei denn, Sie legen die Umgebungsvariable "Mssdk", die in der Projektdatei verwendet wird, "duckingmediaplayer. vcproj" explizit fest.

## <a name="running-the-sample"></a>Ausführen des Beispiels

Wenn Sie die Anwendung erfolgreich erstellen, wird eine ausführbare Datei (DuckingMediaPlayer.exe) generiert. Um es auszuführen, wählen Sie im Menü **Debuggen** die Option **Debugging starten** oder **Starten ohne Debuggen** aus, oder geben Sie `DuckingMediaPlayer` ein Befehlsfenster ein

Um eine Demonstration von Ducking anzuzeigen, müssen Sie "duckingmediaplayer" und "duckingcapturesample" gleichzeitig ausführen. "Duckingcapturesample" öffnet einen Kommunikationsstream und signalisiert dem System, ein Ducking-Ereignis zu generieren. Der duckingmediaplayer wird vom System benachrichtigt, wenn ein duckereignis auftritt, und der Media Player führt die vom Benutzer angeforderte Aktion aus.

So deaktivieren Sie das Ducking-Verhalten:

1.  Wählen Sie im Fenster "duckingcapturesample" die Option **Standardeingabe Gerät verwenden** aus, und klicken Sie auf **starten** , um eine Aufzeichnungs Sitzung vom Kommunikationsgerät zu starten.
2.  Wählen Sie auf dem duckingmediaplayer eine Mediendatei aus, die Sie wiedergeben möchten, und geben Sie die Option für das ducken als **Abmelde** Option an.

Beachten Sie, dass die Mediendatei ohne Unterbrechung wiedergegeben wird. Die vom System generierten Ereignisse beim Öffnen des Kommunikationsstreams werden ignoriert.

Gehen Sie folgendermaßen vor, um das vom System bereitgestellte Standardverhalten zu veranschaulichen:

1.  Wählen Sie in der Systemsteuerung die Option **Sounds** aus. Wählen Sie auf der Registerkarte **Kommunikation** **die Option verringern Sie die Anzahl anderer Sounds um 80% aus**.
2.  Wählen Sie im Fenster "duckingcapturesample" die Option **Standardeingabe Gerät verwenden** aus, und klicken Sie auf **starten** , um eine Aufzeichnungs Sitzung vom Kommunikationsgerät zu starten.
3.  Wählen Sie auf dem duckingmediaplayer eine Mediendatei aus, die Sie wiedergeben möchten, ohne eine der Optionen für das ducken auszuwählen.
4.  Klicken Sie im Fenster "duckingcapturesample" auf " **Abbrechen** ", um den Kommunikationsstream zu verhindern.

Beachten Sie, dass beim Öffnen des Kommunikationsstreams durch "duckingcapturesample" die von duckingmediaplayer wiedergegebene Mediendatei ohne Unterbrechung abgespielt wird, die Volumeebene jedoch verringert wird. Wenn die Kommunikationssitzung angehalten wird, wird das Volume auf die ursprüngliche Einstellung zurückgesetzt. Dieses streamdäsierungsverhalten ist das Standardverhalten, das vom System implementiert wird.

So zeigen Sie ein angepasstes, vom Media Player implementiertes duckverhalten an:

1.  Wählen Sie im Fenster "duckingcapturesample" die Option **Standardeingabe Gerät verwenden** aus, und klicken Sie auf **starten** , um eine Aufzeichnungs Sitzung vom Kommunikationsgerät zu starten.
2.  Wählen Sie auf dem duckingmediaplayer eine Mediendatei aus, die Sie wiedergeben möchten, und geben Sie die Option Ducking als **Pause on Duck** an.
3.  Klicken Sie im Fenster "duckingcapturesample" auf " **Abbrechen** ", um den Kommunikationsstream zu verhindern.

Beachten Sie, dass die von duckingmediaplayer ausgespielte Mediendatei angehalten wird, wenn "duckingcapturesample" den Kommunikationsstream öffnet. Die Wiedergabe wird fortgesetzt, wenn die Kommunikationssitzung angehalten wird. Dieses streamdäsierungsverhalten ist das vom Media Player implementierte duckverhalten.

Duckingmediaplayer zeigt außerdem, wie Sie die volumesteuerung für jede Anwendung mit dem volumemixer integrieren können.

Weitere Informationen zur Datenstrom Dämpfung finden Sie unter standardmäßige [Ducking](stream-attenuation.md)-Funktionalität.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele für die Verwendung der kernaudioapis](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



