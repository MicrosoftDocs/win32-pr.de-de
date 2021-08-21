---
description: In diesem Beispiel werden die Core Audio-APIs verwendet, um eine Anzeige auf dem Bildschirm zu implementieren, die Volumeänderungen am Ausgabestream zeigt, der über das Standardgerät des Audiorenderingendpunkts abspielt.
ms.assetid: 33a1e843-f7c7-4da9-a51e-83a3f0a6ac70
title: Osd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bc0b93214cc547f0491d568abb88d696f76b494f2c562f4805f425acdcfd89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077514"
---
# <a name="osd"></a>Osd

In diesem Beispiel werden die Core Audio-APIs verwendet, um eine Anzeige auf dem Bildschirm zu implementieren, die Volumeänderungen am Ausgabestream zeigt, der über das Standardgerät des Audiorenderingendpunkts abspielt. Die Anzeige auf dem Bildschirm wird angezeigt, wenn der Benutzer die Volumeebene im Windows-Volumesteuerprogramm Sndvol.exe an passt und nicht mehr angezeigt wird, nachdem die Volumeebene für einen kurzen Zeitraum unverändert bleibt.

Dieses Thema enthält die folgenden Abschnitte.

-   [Beschreibung](#description)
-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>Beschreibung

In diesem Beispiel werden die folgenden Features veranschaulicht.

-   [MMDevice-API](mmdevice-api.md) für die Enumeration und Auswahl von Multimedia-Geräten.
-   [AudioendpunktVolume-API](endpointvolume-api.md)

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version                |
|----------------------------------------------------------------|------------------------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista oder höher |
| Visual Studio                                                  | 2005 oder höher          |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist an den folgenden Speicherorten verfügbar.



| Standort    | Pfad/URL                                                                             |
|-------------|--------------------------------------------------------------------------------------|
| Windows SDK | \\Programme \\ Microsoft SDKs \\ Windows \\ v7.0 \\ Samples Multimedia Audio \\ \\ \\ OSD \\ ... |



 

## <a name="building-the-sample"></a>Erstellen des Beispiels

1.  Öffnen Sie die CMD-Shell für das Windows SDK, und wechseln Sie zum OSD-Beispielverzeichnis.
2.  Führen Sie den Befehl "start OSD.sln" im OSD-Verzeichnis aus, um das OSD-Projekt im Visual Studio öffnen.
3.  Wählen Sie im Fenster die  Projektmappenkonfiguration **Debuggen** oder Release aus, wählen Sie in der Menüleiste das Menü **Erstellen** und dann die **Option Erstellen** aus. Wenn Sie die Visual Studio cmd-Shell für das SDK nicht öffnen, hat Visual Studio keinen Zugriff auf die SDK-Buildumgebung. In diesem Fall wird das Beispiel nur erstellt, wenn Sie die Umgebungsvariable MSSdk explizit festlegen, die in der Projektdatei OSD.vcproj verwendet wird.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Führen Sie die ausführbare OSD-Datei OSD.exe in Windows Vista oder höher aus. Beachten Sie, dass weder ein Taskleistensymbol noch ein Fenster für die Anwendung angezeigt wird, aber Sie können sehen, dass der Prozess mithilfe von TaskMgr.exe.
2.  Führen sndvol.exe aus, um das Volume zu ändern oder zu stummschalten, oder ändern Sie das Volume mithilfe von Tastatursteuerelementen oder einem HID-Steuerelement. Die OSD-Benutzeroberfläche wird angezeigt.
3.  Führen Sie zum Beenden der Anwendung TaskMgr.exe aus, markieren Sie den OSD.exe, und klicken Sie **auf End Process (Prozess beenden).**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[SDK-Beispiele, die die Kernaudio-APIs verwenden](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



