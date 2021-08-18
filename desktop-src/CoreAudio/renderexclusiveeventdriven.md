---
description: Diese Beispielanwendung, die die ereignisgesteuerte Pufferung veranschaulicht, verwendet die Core Audio-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu rendern.
ms.assetid: 3a2e3fa6-2d6a-4ab0-a531-d1c968458e96
title: RenderExclusiveEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c23213e1e60d0fdf77de67a91ea3bba3c928a51f9e562876dd1a4e018595dfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119216550"
---
# <a name="renderexclusiveeventdriven"></a>RenderExclusiveEventDriven

Diese Beispielanwendung verwendet die Core Audio-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu rendern. In diesem Beispiel wird die ereignisgesteuerte Pufferung für einen Renderingclient im exklusiven Modus veranschaulicht. Bei einem Stream im exklusiven Modus teilt der Client den Endpunktpuffer mit dem Audiogerät.

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
| Windows SDK | \\Programme \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Multimedia Audio \\ \\ \\ RenderExclusiveEventDriven \\ ... |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

Führen Sie zum Erstellen des RenderExclusiveEventDriven-Beispiels die folgenden Schritte aus:

1.  Öffnen Sie die CMD-Shell für das Windows SDK, und wechseln Sie zum Beispielverzeichnis RenderExclusiveEventDriven.
2.  Führen Sie den Befehl `start WASAPIRenderExclusiveEventDriven.sln` im Verzeichnis RenderExclusiveEventDriven aus, um das Projekt WASAPIRenderExclusiveEventDriven im Visual Studio öffnen.
3.  Wählen Sie im Fenster die  Projektmappenkonfiguration **Debuggen** oder Release aus, wählen Sie in der Menüleiste das Menü **Erstellen** und dann die **Option Erstellen** aus. Wenn Sie die Visual Studio cmd-Shell für das SDK nicht öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung. In diesem Fall wird das Beispiel nur erstellt, wenn Sie die Umgebungsvariable MSSdk explizit festlegen, die in der Projektdatei WASAPIRenderExclusiveEventDriven.vcproj verwendet wird.

## <a name="running-the-sample"></a>Ausführen des Beispiels

Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei WASAPIRenderExclusiveEventDriven.exe generiert. Geben Sie zum Ausführen ein `WASAPIRenderExclusiveEventDriven` Befehlsfenster gefolgt von erforderlichen oder optionalen Argumenten ein. Das folgende Beispiel zeigt, wie sie das Beispiel ausführen, indem Sie die Wiedergabedauer auf dem Multimedia-Standardgerät angeben.

`WASAPIRenderExclusiveEventDriven.exe -d 20 -multimedia`

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

Das RenderExclusiveEventDriven-Beispiel veranschaulicht die ereignisgesteuerte Pufferung. Das Beispiel zeigt, wie Sie:

-   Instanziieren Sie einen Audioclient, konfigurieren Sie ihn für die Ausführung im exklusiven Modus, und aktivieren Sie die ereignisgesteuerte Pufferung, indem Sie das **AUDCLNT \_ STREAMFLAGS \_ EVENTCALLBACK-Flag** im Aufruf von [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)festlegen.
-   Ordnen Sie den Client den Beispielen zu, die gerendert werden können, indem Sie ein Ereignishandle für das System bereitstellen, indem Sie die [**IAudioClient::SetEventHandle-Methode**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) aufrufen.
-   Erstellen Sie einen Renderthread, um Beispiele aus der Audio-Engine zu verarbeiten.
-   Richten Sie die Puffer ordnungsgemäß an einer 128-Byte-Grenze aus, bevor Sie sie an das Gerät senden. Dies erfolgt durch Anpassen der Periodizität der Engine.
-   Überprüfen Sie das Mischungsformat des Geräteendpunkts, um zu bestimmen, ob die Beispiele gerendert werden können. Wenn das Gerät das Mischungsformat nicht unterstützt, werden die Daten in PCM konvertiert.
-   Verarbeiten des Datenstromwechsels.

Nachdem die Renderingsitzung gestartet und der Stream gestartet wurde, signalisiert die Audio-Engine dem angegebenen Ereignishand handle, den Client jedes Mal zu benachrichtigen, wenn ein Puffer für die Verarbeitung durch den Client bereit ist. Die Audiodaten können auch in einer zeitgesteuerten Schleife verarbeitet werden. Dieser Modus wird im [RenderExclusiveTimerDriven-Beispiel](renderexclusivetimerdriven.md) demonstriert.

Weitere Informationen zum Rendern eines Streams finden Sie unter [Rendern eines Streams.](rendering-a-stream.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele, die die Kernaudio-APIs verwenden](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



