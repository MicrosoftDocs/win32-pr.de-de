---
description: Diese Beispielanwendung verwendet die Core Audio-APIs, um Audiodaten von einem vom Benutzer angegebenen Eingabegerät zu erfassen und in eine eindeutig benannte WAV-Datei im aktuellen Verzeichnis zu schreiben. In diesem Beispiel wird die zeitgesteuerte Pufferung veranschaulicht.
ms.assetid: 06124b99-89b3-4dfa-b989-a54746ecd697
title: CaptureSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6d9e8cbd686bdd71804ed067a5b3d9ff36ed8271c8b0edb04b8077ca162fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957379"
---
# <a name="capturesharedtimerdriven"></a>CaptureSharedTimerDriven

Diese Beispielanwendung verwendet die Core Audio-APIs, um Audiodaten von einem vom Benutzer angegebenen Eingabegerät zu erfassen und in eine eindeutig benannte WAV-Datei im aktuellen Verzeichnis zu schreiben. In diesem Beispiel wird die zeitgesteuerte Pufferung veranschaulicht.

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>Beschreibung

In diesem Beispiel werden die folgenden Features veranschaulicht.

-   [MMDevice-API](mmdevice-api.md) für die Enumeration und Auswahl von Multimedia-Geräten.
-   [WASAPI für](wasapi.md) Datenstromverwaltungsvorgänge.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist an den folgenden Speicherorten verfügbar.



| Standort    | Pfad/URL                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programme \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Multimedia Audio \\ \\ \\ CaptureSharedTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

Führen Sie zum Erstellen des CaptureSharedTimerDriven-Beispiels die folgenden Schritte aus:

1.  Öffnen Sie die CMD-Shell für das Windows SDK, und wechseln Sie zum Beispielverzeichnis CaptureSharedTimerDriven.
2.  Führen Sie den Befehl im Verzeichnis CaptureSharedTimerDriven aus, um das `start WASAPICaptureSharedTimerDriven.sln` Projekt WASAPICaptureSharedTimerDriven im Visual Studio öffnen.
3.  Wählen Sie im Fenster die  Projektmappenkonfiguration **Debuggen** oder Release aus, wählen Sie in der Menüleiste das Menü **Erstellen** und dann die **Option Erstellen** aus. Wenn Sie die Visual Studio cmd-Shell für das SDK nicht öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung. In diesem Fall wird das Beispiel nur erstellt, wenn Sie explizit die Umgebungsvariable MSSdk festlegen, die in der Projektdatei WASAPICaptureSharedTimerDriven.vcproj verwendet wird.

## <a name="running-the-sample"></a>Ausführen des Beispiels

Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei WASAPICaptureSharedTimerDriven.exe generiert. Geben Sie zum Ausführen ein `WASAPICaptureSharedTimerDriven` Befehlsfenster gefolgt von erforderlichen oder optionalen Argumenten ein. Das folgende Beispiel zeigt, wie sie das Beispiel ausführen, indem Sie die Erfassungsdauer auf dem Multimedia-Standardgerät angeben.

`WASAPICaptureSharedTimerDriven.exe -d 20 -multimedia`

In der folgenden Tabelle sind die Argumente aufgeführt.

| Argument        | Beschreibung                                                |
|-----------------|------------------------------------------------------------|
| -?              | Zeigt Hilfe an.                                                |
| -H              | Zeigt Hilfe an.                                                |
| -l              | Audioaufnahmelatenz in Millisekunden.                     |
| -d              | Dauer der Audioaufnahme in Sekunden.                         |
| -M              | Deaktiviert die Verwendung von MMCSS.                                 |
| -console        | Verwenden Sie das Standardkonsolengerät.                            |
| -communications | Verwenden Sie das Standardkommunikationsgerät.                      |
| -multimedia     | Verwenden Sie das Multimedia-Standardgerät.                         |
| -endpoint       | Verwenden Sie den Endpunktbezeichner, der im Switchwert angegeben ist. |



 

Wenn die Anwendung ohne Argumente ausgeführt wird, werden die verfügbaren Geräte aufzählt und der Benutzer aufgefordert, ein Gerät für die Erfassungssitzung auszuwählen. Die Standardkonsolen-, Kommunikations- und Multimediageräte werden aufgeführt, gefolgt von Geräten und Endpunktbezeichnern. Wenn keine Dauer angegeben ist, wird der Audiodatenstrom vom angegebenen Gerät 10 Sekunden lang erfasst. Die Anwendung schreibt die erfassten Daten in eine WAV-Datei mit eindeutigem Namen.

CaptureSharedTimerDriven veranschaulicht die zeitgesteuerte Pufferung. In diesem Modus muss der Client für einen bestimmten Zeitraum warten (die Hälfte der Latenz, angegeben durch den Schalterwert -d in Millisekunden). Wenn der Client während des Verarbeitungszeitraums reaktiviert wird, werden die nächsten Stichproben aus der Engine gezogen. Bevor jede Verarbeitung in der Pufferschleife verläuft, muss der Client die Menge der verfügbaren Erfassungsdaten herausfinden, damit die Daten den Erfassungspuffer nicht überlaufen. Die Audiodaten, die vom angegebenen Gerät erfasst werden, können verarbeitet werden, indem die ereignisgesteuerte Pufferung ermöglicht wird. Dieser Modus wird im [CaptureSharedEventDriven-Beispiel](capturesharedeventdriven.md) gezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele, die die Kernaudio-APIs verwenden](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



