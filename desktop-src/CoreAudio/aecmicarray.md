---
description: In diesem Beispiel werden die Kern-audioapis verwendet, um einen hochwertigen voicewaystream zu erfassen. Das Beispiel unterstützt die Verwendung von AEC (Akustik Echo Abbruch) und die Verarbeitung von mikrofonarrays mithilfe des AEC-DMO, auch als sprach Erfassungs-DSP bezeichnet von Microsoft.
ms.assetid: 932d3442-1beb-4938-9382-031c61cd9b05
title: Aecmicarray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe72351b9f8f61d939a9f73eaf85022d7f487bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127677"
---
# <a name="aecmicarray"></a>Aecmicarray

In diesem Beispiel werden die Kern-audioapis verwendet, um einen hochwertigen voicewaystream zu erfassen. Das Beispiel unterstützt die Verwendung von AEC (Akustik Echo Abbruch) und die Verarbeitung von mikrofonarrays mithilfe des AEC-DMO, auch als sprach Erfassungs-DSP bezeichnet von Microsoft.

In diesem Thema werden die folgenden Abschnitte behandelt.

-   [Beschreibung](#description)
-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>BESCHREIBUNG

In diesem Beispiel werden die folgenden Funktionen veranschaulicht.

-   [Mmdevice](mmdevice-api.md) für die Enumeration und Auswahl von Multimedia-Geräten.
-   [WASAPI](wasapi.md) für streamverwaltungsvorgänge wie das Starten und Beenden des Streams, streamumschaltung.
-   " [Opvicetopology](devicetopology-api.md) " zum Auflisten von audioadaptern.
-   [Endpointvolume](endpointvolume-api.md) steuern Sie die volumeebenen von [audiositzungen](audio-sessions.md).

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version                     |
|----------------------------------------------------------------|-----------------------------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista oder höher      |
| Visual Studio                                                  | 2005 (nicht-Express-Editionen) |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist in den folgenden Speicherorten verfügbar.



| Standort    | Pfad/URL                                                                                     |
|-------------|----------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ \\ audioaecmicarray \\ ... |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

Um das aecsdkdemo-Beispiel zu erstellen, führen Sie die folgenden Schritte aus:

1.  Öffnen Sie ein SDK-Befehlsfenster.
2.  Geben Sie **CD% MSSDK% \\ Setup** ein.
3.  Führen Sie VCIntegrate.exe aus.

    Ab diesem Zeitpunkt verfügen Befehlsfenster über die richtigen Umgebungseinstellungen zum Erstellen einer Anwendung, die das SDK nutzt.

4.  Erstellen Sie das Beispiel.

## <a name="running-the-sample"></a>Ausführen des Beispiels

Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei AecSDKDemo.exe generiert. Um es auszuführen, geben Sie `AecSDKDemo` in ein Befehlsfenster ein, gefolgt von den erforderlichen oder optionalen Argumenten, wie unten beschrieben.

`AecSDKDemo -out mic_out.pcm -mod system_mode [-option value] `

In der folgenden Tabelle werden die Argumente angezeigt.

| Argument  | BESCHREIBUNG                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| -out      | Erforderlich. Gibt den Ausgabe Dateinamen an.                                                                                                 |
| -mod      | Erforderlich. Gibt den System Modus für die sprach Erfassung an. Ausführliche Informationen finden Sie im Abschnitt "Konfigurieren des sprach Erfassungs-DMO" in der Beispiel-Info. |
| -feat     | Dies ist optional. Aktiviert den Funktionsmodus (1) oder deaktiviert (0).                                                                                       |
| -NS       | Dies ist optional. Wandelt die Rauschunterdrückung um (1) oder Off (0). Der Funktionsmodus muss auf ON festgelegt sein, um dies anzugeben.                                     |
| -AGC      | Dies ist optional. Wandelt Digital AGC um (1) oder Off (0). Der Funktionsmodus muss auf ON festgelegt sein, um dies anzugeben.                                           |
| -cntrclip | Dies ist optional. Schaltet die zentrale Clipping (1) oder Off (0) ein. Der Funktionsmodus muss auf ON festgelegt sein, um dies anzugeben.                                       |
| -spkdev   | Dies ist optional. Gibt den sprechergeräteindex an. Wenn nicht angegeben, wird der Benutzer aufgefordert, auszuwählen.                                         |
| -micdev   | Dies ist optional. Gibt den Mikrofon-Geräte Index an. Wenn nicht angegeben, wird der Benutzer aufgefordert, auszuwählen.                                      |
| -Dauer | Dies ist optional. Gibt an, wie lange die Anwendung ausgeführt wird.                                                                                    |



 

In dieser Beispielanwendung werden keine Signale abgespielt. Um die Demo ordnungsgemäß für AEC-aktivierte Modi (Modus 0 und 4) auszuführen, müssen Benutzer einige Audiosignale über das für den DMO angegebene sprechende Gerät (d. h. das Gerät, das durch die Option "-spkdev" angegeben wird) abspielen, das die bidirektionale Stimme in einem bidirektionalen Chat Szenario simuliert. Benutzer können beliebige Audiosignale mit jedem beliebigen Player abspielen. Wenn auf dem ausgewählten Redner Gerät kein aktiver Rendering-Stream vorhanden ist, kann der DMO nicht verarbeitet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele für die Verwendung der kernaudioapis](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



