---
description: Diese Beispielanwendung verwendet die kernweb-APIs, um das vom Benutzer angegebene Volume des Geräts zu ändern.
ms.assetid: 2597f3b1-5339-4fd4-9938-39ff917626b4
title: Endpointvolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e89efe89035ec272c68c6a9289672a249616e23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483491"
---
# <a name="endpointvolume"></a>Endpointvolume

Diese Beispielanwendung verwendet die kernweb-APIs, um das vom Benutzer angegebene Volume des Geräts zu ändern.

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
-   [Endpointvolume-API](endpointvolume-api.md) zum Steuern der volumeebenen des Geräte Endpunkts.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |
| Visual Studio                                                  | 2008      |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist in den folgenden Speicherorten verfügbar.



| Standort    | Pfad/URL                                                                                        |
|-------------|-------------------------------------------------------------------------------------------------|
| Windows SDK | \\Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ \\ audioendpointvolume \\ ... |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

Um das x-Beispiel zu erstellen, führen Sie die folgenden Schritte aus:

Um das endpointvolumechanger-Beispiel zu erstellen, führen Sie die folgenden Schritte aus:

1.  Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie zum Beispiel Verzeichnis "endpointvolume".
2.  Führen Sie den Befehl `start EndpointVolumeChanger.sln` im Verzeichnis "endpointvolume" aus, um das Projekt "endpointvolumechanger" im Visual Studio-Fenster zu öffnen.
3.  Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus. Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung. In diesem Fall wird das Beispiel nur dann erstellt, wenn Sie die Umgebungsvariable "Mssdk" explizit festlegen, die in der Projektdatei "wasapiendpointvolume. vcproj" verwendet wird.

## <a name="running-the-sample"></a>Ausführen des Beispiels

Wenn Sie die Demoanwendung erfolgreich erstellen, wird eine ausführbare Datei (EndpointVolumeChanger.exe) generiert. Um es auszuführen, geben Sie `EndpointVolumeChanger` ein Befehlsfenster ein, gefolgt von den erforderlichen oder optionalen Argumenten. Im folgenden Beispiel wird gezeigt, wie Sie die Einstellung stumm schalten auf dem Standard Konsolen Gerät umschalten können.

`EndpointVolumeChanger.exe -console -m`

In der folgenden Tabelle werden die Argumente angezeigt.

| Argument        | BESCHREIBUNG                                                         |
|-----------------|---------------------------------------------------------------------|
| -?              | Zeigt die Hilfe an.                                                         |
| -h              | Zeigt die Hilfe an.                                                         |
| -+              | Inkremente der Volumeebene auf dem audioendpunktgerät um einen Schritt. . |
| nach oben             | Inkremente der Volumeebene auf dem audioendpunktgerät um einen Schritt.   |
| --              | Verringert die Volumeebene auf dem audioendpunktgerät um einen Schritt.   |
| nach unten           | Verringert die Volumeebene auf dem audioendpunktgerät um einen Schritt.   |
| -v              | Legt die Master Volume-Ebene auf dem audioendpunktgerät fest.          |
| -Konsole        | Verwenden Sie das Standard Konsolen Gerät.                                     |
| -Kommunikation | Verwenden Sie das Standard Kommunikationsgerät.                               |
| -Multimedia     | Verwenden Sie das standardmäßige Multimedia-Gerät.                                  |
| -Endpunkt       | Verwenden Sie den Endpunkt Bezeichner, der im Switch-Wert angegeben ist.          |



 

Wenn die Anwendung ohne Argumente ausgeführt wird, werden die verfügbaren Geräte aufgelistet, und der Benutzer wird aufgefordert, ein Gerät auszuwählen. Nachdem der Benutzer das Gerät angegeben hat, zeigt die Anwendung die aktuellen Volumeeinstellungen für den Endpunkt an. Das Volume kann mithilfe der in der obigen Tabelle beschriebenen Switches gesteuert werden.

Weitere Informationen zum Steuern der volumeebenen von audioendpunktgeräten finden Sie unter [endpointvolume-API](endpointvolume-api.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele für die Verwendung der kernaudioapis](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



