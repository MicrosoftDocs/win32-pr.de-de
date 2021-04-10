---
description: Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten von einem vom Benutzer angegebenen Eingabegerät aufzuzeichnen und in eine eindeutig benannte WAV-Datei im aktuellen Verzeichnis zu schreiben. In diesem Beispiel wird die Zeit Geber gesteuerte Pufferung veranschaulicht.
ms.assetid: 06124b99-89b3-4dfa-b989-a54746ecd697
title: Capturesharedtimer-gesteuert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b635462767f22d3e31fe6deaa79b5c00911b378b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041444"
---
# <a name="capturesharedtimerdriven"></a>Capturesharedtimer-gesteuert

Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten von einem vom Benutzer angegebenen Eingabegerät aufzuzeichnen und in eine eindeutig benannte WAV-Datei im aktuellen Verzeichnis zu schreiben. In diesem Beispiel wird die Zeit Geber gesteuerte Pufferung veranschaulicht.

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
-   [WASAPI](wasapi.md) für Stream-Verwaltungsvorgänge.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist in den folgenden Speicherorten verfügbar.



| Standort    | Pfad/URL                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ \\ audiocapturesharedtimer-gesteuert \\ ... |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

Führen Sie die folgenden Schritte aus, um das capturesharedtimergesteuert-Beispiel zu erstellen:

1.  Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie zum Verzeichnis capturesharedtimer-gesteuerte Beispiele.
2.  Führen Sie den Befehl `start WASAPICaptureSharedTimerDriven.sln` im Verzeichnis capturesharedtimercommand aus, um das Projekt wasapicapturesharedtimer-gesteuert im Visual Studio-Fenster zu öffnen.
3.  Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus. Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung. In diesem Fall wird das Beispiel nur dann erstellt, wenn Sie die Umgebungsvariable "Mssdk" explizit festlegen, die in der Projektdatei "wasapicapturesharedtimerused. vcproj" verwendet wird.

## <a name="running-the-sample"></a>Ausführen des Beispiels

Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei (WASAPICaptureSharedTimerDriven.exe) generiert. Um es auszuführen, geben Sie `WASAPICaptureSharedTimerDriven` ein Befehlsfenster ein, gefolgt von den erforderlichen oder optionalen Argumenten. Im folgenden Beispiel wird gezeigt, wie Sie das Beispiel ausführen, indem Sie die Erfassungs Dauer für das standardmäßige Multimedia-Gerät angeben.

`WASAPICaptureSharedTimerDriven.exe -d 20 -multimedia`

In der folgenden Tabelle werden die Argumente angezeigt.

| Argument        | BESCHREIBUNG                                                |
|-----------------|------------------------------------------------------------|
| -?              | Zeigt die Hilfe an.                                                |
| -h              | Zeigt die Hilfe an.                                                |
| -l              | Wartezeit bei der Audioerfassung in Millisekunden.                     |
| -d              | Dauer der Audioerfassung in Sekunden.                         |
| -M              | Deaktiviert die Verwendung von MMCSS.                                 |
| -Konsole        | Verwenden Sie das Standard Konsolen Gerät.                            |
| -Kommunikation | Verwenden Sie das Standard Kommunikationsgerät.                      |
| -Multimedia     | Verwenden Sie das standardmäßige Multimedia-Gerät.                         |
| -Endpunkt       | Verwenden Sie den Endpunkt Bezeichner, der im Switch-Wert angegeben ist. |



 

Wenn die Anwendung ohne Argumente ausgeführt wird, listet Sie die verfügbaren Geräte auf und fordert den Benutzer auf, ein Gerät für die Erfassungs Sitzung auszuwählen. Die Standard Konsole, die Kommunikations-und multimediaregeräte sind aufgeführt, gefolgt von den Geräten und den Endpunkt bezeichern. Wenn keine Dauer angegeben ist, wird der Audiostream vom angegebenen Gerät 10 Sekunden lang aufgezeichnet. Die erfassten Daten werden von der Anwendung in eine eindeutig benannte WAV-Datei geschrieben.

Capturesharedtimer-gesteuert zeigt eine Zeit Geber gesteuerte Pufferung. In diesem Modus muss der Client einen bestimmten Zeitraum (die Hälfte der Latenzzeit, die durch den Schalter-d angegeben wird, in Millisekunden) warten. Wenn der Client im Laufe der Zeit auf die gleiche Weise reaktiviert wird, ruft er den nächsten Satz von Beispielen aus der Engine ab. Vor jeder Verarbeitung in der Puffer Schleife muss der Client die Menge der verfügbaren Aufzeichnungsdaten ermitteln, damit die Daten den Aufzeichnungs Puffer nicht überschreiten. Die Audiodaten, die vom angegebenen Gerät aufgezeichnet werden, können durch Aktivieren der ereignisgesteuerten Pufferung verarbeitet werden. Dieser Modus wird im [capturesharedeventgesteu-Beispiel veranschaulicht](capturesharedeventdriven.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele für die Verwendung der kernaudioapis](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



