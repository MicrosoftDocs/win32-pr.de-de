---
description: Diese Beispielanwendung verwendet die Core Audio-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu rendern. In diesem Beispiel wird die zeitgesteuerte Pufferung für einen Renderingclient im exklusiven Modus veranschaulicht.
ms.assetid: 9dcfccd2-a709-4b4e-bbb3-4c68a15cce03
title: RenderExclusiveTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6876c448aa7737683aff4e495416020af7def54cb01109c3d6ad2d1c26d20780
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077444"
---
# <a name="renderexclusivetimerdriven"></a>RenderExclusiveTimerDriven

Diese Beispielanwendung verwendet die Core Audio-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu rendern. In diesem Beispiel wird die zeitgesteuerte Pufferung für einen Renderingclient im exklusiven Modus veranschaulicht. Bei einem Stream im exklusiven Modus teilt der Client den Endpunktpuffer mit dem Audiogerät.

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Anzeigen der Beispieldateien](#view-the-sample-files)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>Beschreibung

In diesem Beispiel werden die folgenden Features veranschaulicht.

-   [MMDevice-API](mmdevice-api.md) für die Enumeration und Auswahl von Multimedia-Geräten.
-   WASAPI für Datenstromverwaltungsvorgänge.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist an den folgenden Speicherorten verfügbar.



| Standort    | Pfad/URL                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programme \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Multimedia Audio \\ \\ \\ RenderExclusiveTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

Führen Sie zum Erstellen des RenderExclusiveTimerDriven-Beispiels die folgenden Schritte aus:

1.  Öffnen Sie die CMD-Shell für das Windows SDK, und wechseln Sie zum Beispielverzeichnis RenderExclusiveTimerDriven.
2.  Führen Sie den Befehl `start WASAPIRenderExclusiveTimerDriven.sln` im Verzeichnis RenderExclusiveTimerDriven aus, um das Projekt WASAPIRenderExclusiveTimerDriven im fenster Visual Studio öffnen.
3.  Wählen Sie im Fenster die  Projektmappenkonfiguration **Debuggen** oder Release aus, wählen Sie in der Menüleiste das Menü **Erstellen** und dann die **Option Erstellen** aus. Wenn Sie die Visual Studio cmd-Shell für das SDK nicht öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung. In diesem Fall wird das Beispiel nur erstellt, wenn Sie explizit die Umgebungsvariable MSSdk festlegen, die in der Projektdatei WASAPIRenderExclusiveTimerDriven.vcproj verwendet wird.

## <a name="view-the-sample-files"></a>Anzeigen der Beispieldateien

Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei WASAPIRenderExclusiveTimerDriven.exe generiert. Geben Sie zum Ausführen ein `WASAPIRenderExclusiveTimerDriven` Befehlsfenster gefolgt von erforderlichen oder optionalen Argumenten ein. Im folgenden Beispiel wird gezeigt, wie das Beispiel mit einer angegebenen Wiedergabedauer auf dem Standardkonsolengerät ausgeführt wird.

`WASAPIRenderExclusiveTimerDriven.exe -d 20 -console`

In der folgenden Tabelle sind die Argumente aufgeführt.

| Argument        | Beschreibung                                                |
|-----------------|------------------------------------------------------------|
| -?              | Zeigt Hilfe an.                                                |
| -H              | Zeigt Hilfe an.                                                |
| -f              | Sinus-Wellenfrequenz in Hz.                                 |
| -l              | Audiorenderinglatenz in Millisekunden.                      |
| -d              | Dauer der Sinus-Welle in Sekunden.                             |
| -M              | Deaktiviert die Verwendung von MMCSS.                                 |
| -console        | Verwenden Sie das Standardkonsolengerät.                            |
| -communications | Verwenden Sie das Standardkommunikationsgerät.                      |
| -multimedia     | Verwenden Sie das Multimedia-Standardgerät.                         |
| -endpoint       | Verwenden Sie den Endpunktbezeichner, der im Switchwert angegeben ist. |



 

Wenn die Anwendung ohne Argumente ausgeführt wird, werden die verfügbaren Geräte aufzählt und der Benutzer aufgefordert, ein Gerät für die Renderingsitzung auszuwählen. Nachdem der Benutzer ein Gerät angegeben hat, rendert die Anwendung 10 Sekunden lang eine Sinus-Welle mit 440 Hz. Diese Werte können durch Angabe der Schalterwerte -f und -d geändert werden.

RenderExclusiveTimerDriven veranschaulicht die zeitgesteuerte Pufferung. In diesem Modus muss der Client für einen bestimmten Zeitraum warten (die Hälfte der Latenz, angegeben durch den Schalterwert -d in Millisekunden). Wenn der Client während des Verarbeitungszeitraums reaktiviert wird, werden die nächsten Stichproben aus der Engine gezogen. Bevor jede Verarbeitung in der Pufferschleife verläuft, muss der Client die Menge der zu renderenden Daten herausfinden, damit die Daten den Puffer nicht überlaufen.

Audiodaten, die auf dem angegebenen Gerät abgespielt werden sollen, können durch Aktivieren der ereignisgesteuerten Pufferung verarbeitet werden. Dieser Modus wird im RenderExclusiveTimerDriven-Beispiel demonstriert.

Weitere Informationen zum Rendern eines Streams finden Sie unter [Rendern eines Streams.](rendering-a-stream.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele, die die Kernaudio-APIs verwenden](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



