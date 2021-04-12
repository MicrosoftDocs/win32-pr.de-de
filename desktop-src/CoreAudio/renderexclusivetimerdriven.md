---
description: Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering. In diesem Beispiel wird die Zeit Geber gesteuerte Pufferung für einen renderingclient im exklusiven Modus veranschaulicht.
ms.assetid: 9dcfccd2-a709-4b4e-bbb3-4c68a15cce03
title: Renderexclusivetimer-gesteuert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6145f65de3de9425f7ba2f023a669ec0b57a3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483483"
---
# <a name="renderexclusivetimerdriven"></a>Renderexclusivetimer-gesteuert

Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering. In diesem Beispiel wird die Zeit Geber gesteuerte Pufferung für einen renderingclient im exklusiven Modus veranschaulicht. Für einen Stream im exklusiven Modus gibt der Client den Endpunkt Puffer mit dem Audiogerät frei.

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Anzeigen der Beispieldateien](#view-the-sample-files)
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



| Standort    | Pfad/URL                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ \\ multimedioneaudiodatei \\ renderexclusivetimer-gesteuert \\ ... |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

Führen Sie die folgenden Schritte aus, um das renderexclusivetimergesteuert-Beispiel zu erstellen:

1.  Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie zum Verzeichnis "renderexclusivetimergesteudirectory".
2.  Führen Sie den Befehl `start WASAPIRenderExclusiveTimerDriven.sln` im Verzeichnis "renderexclusivetimercommand" aus, um das Projekt "wasapirienderexclusivetimer-gesteuert" im Visual Studio-Fenster zu öffnen.
3.  Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus. Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung. In diesem Fall wird das Beispiel nicht erstellt, es sei denn, Sie legen die Umgebungsvariable "Mssdk", die in der Projektdatei verwendet wird, "wasapirienderexclusivetimercontroller. vcproj" explizit fest.

## <a name="view-the-sample-files"></a>Anzeigen der Beispieldateien

Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei (WASAPIRenderExclusiveTimerDriven.exe) generiert. Um es auszuführen, geben Sie `WASAPIRenderExclusiveTimerDriven` ein Befehlsfenster ein, gefolgt von den erforderlichen oder optionalen Argumenten. Im folgenden Beispiel wird gezeigt, wie das Beispiel mit einem angegeben wird, indem die Wiedergabedauer auf dem Standard Konsolen Gerät angegeben wird.

`WASAPIRenderExclusiveTimerDriven.exe -d 20 -console`

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

Renderexclusivetimer-gesteuert zeigt eine Zeit Geber gesteuerte Pufferung. In diesem Modus muss der Client einen bestimmten Zeitraum (die Hälfte der Latenzzeit, die durch den Schalter-d angegeben wird, in Millisekunden) warten. Wenn der Client im Laufe der Zeit auf die gleiche Weise reaktiviert wird, ruft er den nächsten Satz von Beispielen aus der Engine ab. Vor jeder Verarbeitung in der Puffer Schleife muss der Client die Menge der zu rendernden Daten ermitteln, damit die Daten den Puffer nicht überschreiten.

Audiodaten, die auf dem angegebenen Gerät abgespielt werden sollen, können durch Aktivieren der ereignisgesteuerten Pufferung verarbeitet werden. Dieser Modus wird im renderexclusivetimergesteuert-Beispiel veranschaulicht.

Weitere Informationen zum Rendern eines Streams finden Sie unter [Rendern eines Streams](rendering-a-stream.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele für die Verwendung der kernaudioapis](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



