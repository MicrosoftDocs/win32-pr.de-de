---
description: Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten von einem vom Benutzer angegebenen Eingabegerät aufzuzeichnen und in eine eindeutig benannte WAV-Datei im aktuellen Verzeichnis zu schreiben. In diesem Beispiel wird die ereignisgesteuerte Pufferung veranschaulicht.
ms.assetid: 6ff3bc23-550e-41b7-b37c-35d552b29e20
title: Capturesharedebug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 339bd02fcb94f65be558c2dce767747ebf4fab98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126905"
---
# <a name="capturesharedeventdriven"></a>Capturesharedebug

Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten von einem vom Benutzer angegebenen Eingabegerät aufzuzeichnen und in eine eindeutig benannte WAV-Datei im aktuellen Verzeichnis zu schreiben. In diesem Beispiel wird die ereignisgesteuerte Pufferung veranschaulicht.

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
-   [WASAPI](wasapi.md) für Stream-Verwaltungsvorgänge, z. b. das Starten und Beenden des Streams und der Datenstrom Wechsel.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist in den folgenden Speicherorten verfügbar.



| Standort    | Pfad/URL                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmdateien \\ Microsoft sdgs \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ \\ audiocapturesharedeventgesteu. \\ .. |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

Führen Sie die folgenden Schritte aus, um das capturesharedeventgesteuerte-Beispiel zu erstellen:

1.  Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie zum Beispiel Verzeichnis "capturesharedeventgesteuerte".
2.  Führen Sie den Befehl `start WASAPICaptureSharedEventDriven.sln` im Verzeichnis capturesharedeventgesteuaus, um das Projekt wasapicapturesharedeventgesteuim Visual Studio-Fenster zu öffnen.
3.  Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus. Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung. In diesem Fall wird das Beispiel nur dann erstellt, wenn Sie die Umgebungsvariable "Mssdk" explizit festlegen, die in der Projektdatei "wasapicapturesharedeventcontroller. vcproj" verwendet wird.

## <a name="running-the-sample"></a>Ausführen des Beispiels

Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei (WASAPICaptureSharedEventDriven.exe) generiert. Um es auszuführen, geben Sie `WASAPICaptureSharedEventDriven` ein Befehlsfenster ein, gefolgt von den erforderlichen oder optionalen Argumenten. Im folgenden Beispiel wird gezeigt, wie Sie das Beispiel ausführen, indem Sie die Erfassungs Dauer für das standardmäßige Multimedia-Gerät angeben.

`WASAPICaptureSharedEventDriven.exe -d 20 -multimedia`

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

Capturesharetoventgesteuerte zeigt die ereignisgesteuerte Pufferung. Der für dieses Beispiel instanziierte AudioClient ist so konfiguriert, dass er im freigegebenen Modus ausgeführt wird, und die Verarbeitung des Audiopuffers durch den Client wird durch Festlegen des " **audclnt \_ StreamFlags \_ EventCallback** "-Flags im Aufrufen von " [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)" gesteuert. Das Beispiel zeigt, wie der Client ein Ereignis Handle für das System bereitstellen muss, indem er die [**iaudioclient:: setteventhandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) -Methode aufrufen. Nachdem die Aufzeichnungs Sitzung beginnt und der Stream gestartet wurde, signalisiert die Audioengine dem bereitgestellten Ereignis handle, dass der Client jedes Mal benachrichtigt wird, wenn ein Puffer für die Verarbeitung durch den Client bereit ist. Die Audiodaten können auch in einer Zeit Geber gesteuerten Schleife verarbeitet werden. Dieser Modus wird im [capturesharedtimergesteuerter](capturesharedtimerdriven.md) Beispiel herabgestuft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele für die Verwendung der kernaudioapis](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



