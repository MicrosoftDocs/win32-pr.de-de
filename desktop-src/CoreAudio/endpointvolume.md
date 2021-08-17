---
description: Diese Beispielanwendung verwendet die Core Audio-APIs, um die Vom Benutzer angegebene Lautstärke des Geräts zu ändern.
ms.assetid: 2597f3b1-5339-4fd4-9938-39ff917626b4
title: EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c157149e6b15014b1228b2b5c97080fcdbdccd9acc2745ee5a986a7de7c997f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828271"
---
# <a name="endpointvolume"></a>EndpointVolume

Diese Beispielanwendung verwendet die Core Audio-APIs, um die Vom Benutzer angegebene Lautstärke des Geräts zu ändern.

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>Beschreibung

In diesem Beispiel werden die folgenden Features veranschaulicht.

-   [MMDevice-API](mmdevice-api.md) für multimediale Geräteenumeration und -auswahl.
-   [EndpointVolume-API](endpointvolume-api.md) zum Steuern der Volumeebenen des Geräteendpunkts.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist an den folgenden Speicherorten verfügbar.



| Standort    | Pfad/URL                                                                                        |
|-------------|-------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programme \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Multimedia Audio \\ \\ \\ EndpointVolume \\ ... |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

Um das x-Beispiel zu erstellen, verwenden Sie die folgenden Schritte:

Um das EndpointVolumeChanger-Beispiel zu erstellen, verwenden Sie die folgenden Schritte:

1.  Öffnen Sie die CMD-Shell für das Windows SDK, und wechseln Sie in das Beispielverzeichnis EndpointVolume.
2.  Führen Sie den Befehl `start EndpointVolumeChanger.sln` im Verzeichnis EndpointVolume aus, um das Projekt EndpointVolumeChanger im fenster Visual Studio zu öffnen.
3.  Wählen Sie im Fenster die Konfiguration **Debug-** oder **Releaselösung** aus, wählen Sie in der Menüleiste das Menü **Erstellen** und dann die Option **Erstellen** aus. Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, haben Visual Studio keinen Zugriff auf die SDK-Buildumgebung. In diesem Fall wird das Beispiel nur erstellt, wenn Sie die Umgebungsvariable MSSdk explizit festlegen, die in der Projektdatei WASAPIEndpointVolume.vcproj verwendet wird.

## <a name="running-the-sample"></a>Ausführen des Beispiels

Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei EndpointVolumeChanger.exe generiert. Geben Sie zum Ausführen `EndpointVolumeChanger` ein Befehlsfenster gefolgt von erforderlichen oder optionalen Argumenten ein. Das folgende Beispiel zeigt, wie Sie die Mute-Einstellung auf dem Standardkonsolengerät umschalten.

`EndpointVolumeChanger.exe -console -m`

In der folgenden Tabelle sind die Argumente aufgeführt.

| Argument        | Beschreibung                                                         |
|-----------------|---------------------------------------------------------------------|
| -?              | Zeigt Hilfe an.                                                         |
| -H              | Zeigt Hilfe an.                                                         |
| -+              | Erhöht die Lautstärke auf dem Audioendpunktgerät um einen Schritt. . |
| -up             | Erhöht die Lautstärke auf dem Audioendpunktgerät um einen Schritt.   |
| --              | Dekrementiert die Lautstärke auf dem Audioendpunktgerät um einen Schritt.   |
| -down           | Dekrementiert die Lautstärke auf dem Audioendpunktgerät um einen Schritt.   |
| -v              | Legt die Mastervolumeebene auf dem Audioendpunktgerät fest.          |
| -console        | Verwenden Sie das Standardkonsolengerät.                                     |
| -communications | Verwenden Sie das Standardkommunikationsgerät.                               |
| -multimedia     | Verwenden Sie das Standardmäßige Multimediagerät.                                  |
| -endpoint       | Verwenden Sie den Endpunktbezeichner, der im Switchwert angegeben ist.          |



 

Wenn die Anwendung ohne Argumente ausgeführt wird, listet sie die verfügbaren Geräte auf und fordert den Benutzer auf, ein Gerät auszuwählen. Nachdem der Benutzer das Gerät angegeben hat, zeigt die Anwendung die aktuellen Volumeeinstellungen für den Endpunkt an. Das Volume kann mithilfe der in der vorherigen Tabelle beschriebenen Schalter gesteuert werden.

Weitere Informationen zum Steuern der Lautstärke von Audioendpunktgeräten finden Sie unter [EndpointVolume-API.](endpointvolume-api.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele, die die Kernaudio-APIs verwenden](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



