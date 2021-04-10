---
description: Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering.
ms.assetid: 92e644be-df8b-415d-ac8e-c0c30c85f844
title: Rendersharedebug-gesteuert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9901896b962717ed72fd36d022eef9510d7cb916
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861303"
---
# <a name="rendersharedeventdriven"></a>Rendersharedebug-gesteuert

Diese Beispielanwendung verwendet die kernweb-APIs, um Audiodaten auf einem vom Benutzer angegebenen Ausgabegerät zu Rendering. Dieses Beispiel veranschaulicht die ereignisgesteuerte Pufferung für einen renderingclient im freigegebenen Modus. Bei einem Stream im freigegebenen Modus verwendet der Client den Endpunkt Puffer mit der Audioengine.

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
| Windows SDK | \\Programmdateien \\ Microsoft sdgs \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ \\ audiorendersharedeventgesteu. \\ .. |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

Führen Sie die folgenden Schritte aus, um das rendersharedeventgesteuerte-Beispiel zu erstellen:

1.  Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie zum Verzeichnis "rendersharedeventgesteudirectory".
2.  Führen Sie den Befehl `start WASAPIRenderSharedEventDriven.sln` im Verzeichnis rendersharedeventlab aus, um das Projekt wasapiriendersharedeventgesteuim Visual Studio-Fenster zu öffnen.
3.  Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus. Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung. In diesem Fall wird das Beispiel nicht erstellt, es sei denn, Sie legen die Umgebungsvariable "Mssdk", die in der Projektdatei verwendet wird, "wasapiriendersharedevent-Controller. vcproj" explizit fest.

## <a name="running-the-sample"></a>Ausführen des Beispiels

Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei (WASAPIRenderSharedEventDriven.exe) generiert. Um es auszuführen, geben Sie `WASAPIRenderSharedEventDriven` ein Befehlsfenster ein, gefolgt von den erforderlichen oder optionalen Argumenten. Im folgenden Beispiel wird gezeigt, wie Sie das Beispiel ausführen, indem Sie die Wiedergabedauer für das standardmäßige Multimedia-Gerät angeben.

`WASAPIRenderSharedEventDriven.exe -d 20 -multimedia`

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

Rendershareentventgesteuerte zeigt die ereignisgesteuerte Pufferung. Das Beispiel zeigt Folgendes:

-   Instanziieren Sie einen AudioClient, konfigurieren Sie ihn so, dass er im exklusiven Modus ausgeführt wird, und aktivieren Sie die ereignisgesteuerte Pufferung, indem Sie im Aufrufen von [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)das Flag " **audclnt \_ StreamFlags \_ EventCallback** " festlegen.
-   Ordnen Sie den Client die Beispiele zu, die gerendert werden können, indem Sie ein Ereignis Handle für das System bereitstellen, indem Sie die [**iaudioclient:: setteventhandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) -Methode aufrufen.
-   Erstellen Sie einen Renderthread, um Beispiele aus der Audioengine zu erstellen.
-   Überprüfen Sie das Mischungs Format des Geräte Endpunkts, um zu bestimmen, ob die Beispiele gerendert werden können Wenn das Gerät das Mischungs Format nicht unterstützt, werden die Daten in PCM konvertiert.
-   Handle des streamwechsels.

Nachdem die renderingsitzung beginnt und der Stream gestartet wurde, signalisiert die Audioengine dem bereitgestellten Ereignis handle, dass der Client jedes Mal benachrichtigt wird, wenn ein Puffer für die Verarbeitung durch den Client bereit ist. Die Audiodaten können auch in einer Zeit Geber gesteuerten Schleife verarbeitet werden. Dieser Modus wird im [rendersharedtimergesteuert](rendersharedtimerdriven.md) -Beispiel veranschaulicht.

Weitere Informationen zum Rendern eines Streams finden Sie unter [Rendern eines Streams](rendering-a-stream.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele für die Verwendung der kernaudioapis](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



