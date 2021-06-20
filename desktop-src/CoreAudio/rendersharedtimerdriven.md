---
description: Diese Beispielanwendung, die die zeitgebergesteuerte Pufferung veranschaulicht, verwendet die Core Audio-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu rendern.
ms.assetid: eae7d896-77ef-4340-bd77-1f3333166987
title: RenderSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89d2814f359668f8724d3deb65a7c2a9eeff5b06
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410093"
---
# <a name="rendersharedtimerdriven"></a>RenderSharedTimerDriven

Diese Beispielanwendung verwendet die Core Audio-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu rendern. In diesem Beispiel wird die zeitgebergesteuerte Pufferung für einen Renderingclient im freigegebenen Modus veranschaulicht. Für einen Stream im freigegebenen Modus teilt sich der Client den Endpunktpuffer mit der Audio-Engine.

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Verwandte Themen](#related-topics)

## <a name="description"></a>Beschreibung

In diesem Beispiel werden die folgenden Features veranschaulicht.

-   [MMDevice-API](mmdevice-api.md) für multimediale Geräteenumeration und -auswahl.
-   WASAPI für Datenstromverwaltungsvorgänge.

## <a name="requirements"></a>Requirements (Anforderungen)



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist an den folgenden Speicherorten verfügbar.



| Standort    | Pfad/URL                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programme \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Multimedia Audio \\ \\ \\ RenderSharedTimerDriven \\ ... |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

Führen Sie die folgenden Schritte aus, um das RenderSharedTimerDriven-Beispiel zu erstellen:

1.  Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie zum Beispielverzeichnis RenderSharedTimerDriven.
2.  Führen Sie den Befehl `start WASAPIRenderSharedTimerDriven.sln` im Verzeichnis RenderSharedTimerDriven aus, um das Projekt WASAPIRenderSharedTimerDriven im fenster Visual Studio zu öffnen.
3.  Wählen Sie im Fenster die Konfiguration **Debug-** oder **Releaselösung** aus, wählen Sie in der Menüleiste das Menü **Erstellen** und dann die Option **Erstellen** aus. Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, haben Visual Studio keinen Zugriff auf die SDK-Buildumgebung. In diesem Fall wird das Beispiel nur erstellt, wenn Sie die Umgebungsvariable MSSdk explizit festlegen, die in der Projektdatei WASAPIRenderSharedTimerDriven.vcproj verwendet wird.

## <a name="running-the-sample"></a>Ausführen des Beispiels

Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei WASAPIRenderSharedTimerDriven.exe generiert. Geben Sie zum Ausführen `WASAPIRenderSharedTimerDriven` ein Befehlsfenster gefolgt von erforderlichen oder optionalen Argumenten ein. Das folgende Beispiel zeigt, wie das Beispiel ausgeführt wird, indem die Wiedergabedauer auf dem Standardmäßigen Multimediagerät angegeben wird.

`WASAPIRenderSharedTimerDriven.exe -d 20 -multimedia`

In der folgenden Tabelle sind die Argumente aufgeführt.

| Argument        | Beschreibung                                                |
|-----------------|------------------------------------------------------------|
| -?              | Zeigt Hilfe an.                                                |
| -H              | Zeigt Hilfe an.                                                |
| -f              | Sinusfrequenz in Hz.                                 |
| -l              | Audiorenderinglatenz in Millisekunden.                      |
| -d              | Sinus-Wellendauer in Sekunden.                             |
| -M              | Deaktiviert die Verwendung von MMCSS.                                 |
| -console        | Verwenden Sie das Standardkonsolengerät.                            |
| -communications | Verwenden Sie das Standardkommunikationsgerät.                      |
| -multimedia     | Verwenden Sie das Standardmäßige Multimediagerät.                         |
| -endpoint       | Verwenden Sie den Endpunktbezeichner, der im Switchwert angegeben ist. |



 

Wenn die Anwendung ohne Argumente ausgeführt wird, listet sie die verfügbaren Geräte auf und fordert den Benutzer auf, ein Gerät für die Renderingsitzung auszuwählen. Nachdem der Benutzer ein Gerät angegeben hat, rendert die Anwendung eine Sinusbewegung bei 440 Hz für 10 Sekunden. Diese Werte können durch Angeben der Schalterwerte -f und -d geändert werden.

RenderSharedTimerDriven veranschaulicht die zeitgebergesteuerte Pufferung. In diesem Modus muss der Client einen Zeitraum warten (die Hälfte der Latenz, angegeben durch den Schalterwert -d, in Millisekunden). Wenn der Client reaktiviert wird, wird in der Mitte des Verarbeitungszeitraums die nächste Gruppe von Stichproben aus der Engine abgerufen. Bevor jeder Verarbeitungsdurchlauf in der Pufferungsschleife erfolgt, muss der Client die zu rendernde Datenmenge ermitteln, damit die Daten den Puffer nicht überlaufen.

Audiodaten, die auf dem angegebenen Gerät wiedergegeben werden sollen, können verarbeitet werden, indem die ereignisgesteuerte Pufferung aktiviert wird. Dieser Modus wird im [RenderSharedEventDriven-Beispiel](rendersharedeventdriven.md) veranschaulicht.

Weitere Informationen zum Rendern eines Streams finden Sie unter [Rendern eines Streams.](rendering-a-stream.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele, die die Kernaudio-APIs verwenden](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



