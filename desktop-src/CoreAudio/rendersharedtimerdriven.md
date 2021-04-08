---
description: Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering.
ms.assetid: eae7d896-77ef-4340-bd77-1f3333166987
title: Rendersharedtimer-gesteuert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de4ce441a12d65b8bebb843c7b9a168443b34592
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748537"
---
# <a name="rendersharedtimerdriven"></a>Rendersharedtimer-gesteuert

Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering. Dieses Beispiel veranschaulicht die Zeit Geber gesteuerte Pufferung für einen renderingclient im freigegebenen Modus. Bei einem Stream im freigegebenen Modus verwendet der Client den Endpunkt Puffer mit der Audioengine.

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
-   WASAPI für Stream-Verwaltungsvorgänge.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist in den folgenden Speicherorten verfügbar.



| Standort    | Pfad/URL                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ \\ audiorendersharedtimer-gesteuert \\ ... |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

Führen Sie die folgenden Schritte aus, um das rendersharedtimergesteuerte-Beispiel zu erstellen:

1.  Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie in das Verzeichnis "rendersharedtimer. Sample".
2.  Führen Sie den Befehl `start WASAPIRenderSharedTimerDriven.sln` im Verzeichnis rendersharedtimercommand aus, um das Projekt wasapiriendersharedtimer-gesteuert im Visual Studio-Fenster zu öffnen.
3.  Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus. Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung. In diesem Fall wird das Beispiel nicht erstellt, es sei denn, Sie legen die Umgebungsvariable "Mssdk", die in der Projektdatei verwendet wird, "wasapiriendersharedtimercontroller. vcproj" explizit fest.

## <a name="running-the-sample"></a>Ausführen des Beispiels

Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei (WASAPIRenderSharedTimerDriven.exe) generiert. Um es auszuführen, geben Sie `WASAPIRenderSharedTimerDriven` ein Befehlsfenster ein, gefolgt von den erforderlichen oder optionalen Argumenten. Im folgenden Beispiel wird gezeigt, wie Sie das Beispiel ausführen, indem Sie die Wiedergabedauer für das standardmäßige Multimedia-Gerät angeben.

`WASAPIRenderSharedTimerDriven.exe -d 20 -multimedia`

In der folgenden Tabelle werden die Argumente angezeigt.

| Argument        | BESCHREIBUNG                                                |
|-----------------|------------------------------------------------------------|
| -?              | Zeigt die Hilfe an.                                                |
| -h              | Zeigt die Hilfe an.                                                |
| -f              | Sinuswellen Frequenz in Hz.                                 |
| -l              | Wartezeit für audiorendering in Millisekunden.                      |
| -d              | Sinuswellen Dauer in Sekunden.                             |
| -M              | Deaktiviert die Verwendung von MMCSS.                                 |
| -Konsole        | Verwenden Sie das Standard Konsolen Gerät.                            |
| -Kommunikation | Verwenden Sie das Standard Kommunikationsgerät.                      |
| -Multimedia     | Verwenden Sie das standardmäßige Multimedia-Gerät.                         |
| -Endpunkt       | Verwenden Sie den Endpunkt Bezeichner, der im Switch-Wert angegeben ist. |



 

Wenn die Anwendung ohne Argumente ausgeführt wird, listet Sie die verfügbaren Geräte auf und fordert den Benutzer auf, ein Gerät für die renderingsitzung auszuwählen. Nachdem der Benutzer ein Gerät angegeben hat, rendert die Anwendung eine Sinuswelle bei 440 Hz für 10 Sekunden. Diese Werte können durch Angabe von "-f" und "-d"-Schalter Werte geändert werden.

Rendersharedtimer-gesteuert zeigt eine Zeit Geber gesteuerte Pufferung. In diesem Modus muss der Client einen bestimmten Zeitraum (die Hälfte der Latenzzeit, die durch den Schalter-d angegeben wird, in Millisekunden) warten. Wenn der Client im Laufe der Zeit auf die gleiche Weise reaktiviert wird, ruft er den nächsten Satz von Beispielen aus der Engine ab. Vor jeder Verarbeitung in der Puffer Schleife muss der Client die Menge der zu rendernden Daten ermitteln, damit die Daten den Puffer nicht überschreiten.

Audiodaten, die auf dem angegebenen Gerät abgespielt werden sollen, können durch Aktivieren der ereignisgesteuerten Pufferung verarbeitet werden. Dieser Modus wird im [rendersharedeventgesteu-](rendersharedeventdriven.md) Beispiel veranschaulicht.

Weitere Informationen zum Rendern eines Streams finden Sie unter [Rendern eines Streams](rendering-a-stream.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele für die Verwendung der kernaudioapis](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



