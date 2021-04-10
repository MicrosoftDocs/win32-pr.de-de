---
description: In diesem Beispiel werden die Kern-audioapis verwendet, um eine Bildschirm Anzeige zu implementieren, die volumeänderungen an dem Ausgabedatenstrom anzeigt, die über das standardmäßige audiorenderingendpunkt-Gerät abgespielt werden.
ms.assetid: 33a1e843-f7c7-4da9-a51e-83a3f0a6ac70
title: OSD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c4c04daf5d2dd333a25150821a831695e06a06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041460"
---
# <a name="osd"></a>OSD

In diesem Beispiel werden die Kern-audioapis verwendet, um eine Bildschirm Anzeige zu implementieren, die volumeänderungen an dem Ausgabedatenstrom anzeigt, die über das standardmäßige audiorenderingendpunkt-Gerät abgespielt werden. Die Anzeige auf dem Bildschirm wird angezeigt, wenn der Benutzer die Volumeebene im Windows-Programm zur volumesteuerung (Sndvol.exe) anpasst, und er verschwindet, wenn die Volumeebene für einen kurzen Zeitraum unverändert bleibt.

In diesem Thema werden die folgenden Abschnitte behandelt.

-   [Beschreibung](#description)
-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>BESCHREIBUNG

In diesem Beispiel werden die folgenden Funktionen veranschaulicht.

-   [Mmdevice-API](mmdevice-api.md) für die Enumeration und Auswahl von Multimedia-Geräten.
-   [Audioendpointvolume-API](endpointvolume-api.md)

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version                |
|----------------------------------------------------------------|------------------------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista oder höher |
| Visual Studio                                                  | 2005 oder höher          |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist in den folgenden Speicherorten verfügbar.



| Standort    | Pfad/URL                                                                             |
|-------------|--------------------------------------------------------------------------------------|
| Windows SDK | \\Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ \\ audioosd \\ ... |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

1.  Öffnen Sie die CMD-Shell für die Windows SDK, und wechseln Sie zum OSD-Beispiel Verzeichnis.
2.  Führen Sie den Befehl "Start OSD. sln" im OSD-Verzeichnis aus, um das OSD-Projekt im Visual Studio-Fenster zu öffnen.
3.  Wählen Sie im Fenster die **Debug** -oder **releaseprojektmappenkonfiguration** aus, wählen Sie das Menü **Erstellen** in der Menüleiste aus, und wählen Sie die Option **Erstellen** aus. Wenn Sie Visual Studio nicht über die CMD-Shell für das SDK öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung. In diesem Fall wird das Beispiel nur dann erstellt, wenn Sie die Umgebungsvariable "Mssdk" explizit festlegen, die in der Projektdatei "OSD. vcproj" verwendet wird.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Führen Sie die ausführbare OSD-Datei OSD.exe in Windows Vista oder höher aus. Beachten Sie, dass kein Task leisten Symbol oder ein Fenster für die Anwendung angezeigt wird, aber Sie können den Prozess anzeigen, der mit TaskMgr.exe ausgeführt wird.
2.  Führen Sie sndvol.exe aus, um das Volume zu ändern oder das Volume mithilfe von Tastatur Steuerelementen oder einem HID-Steuerelement zu ändern. Die Benutzeroberfläche von OSD wird angezeigt.
3.  Führen Sie TaskMgr.exe aus, markieren Sie den OSD.exe Prozess, und klicken Sie auf **Prozess beenden**, um die Anwendung zu beenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele für die Verwendung der kernaudioapis](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



