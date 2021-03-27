---
description: Veranschaulicht Überlagerungen und Status leisten des Task leisten Symbols.
title: Peripheriestatus der Taskleiste (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E4B693FB-EE7D-47d0-A5D8-91205AD4A3DC
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 793c09853e3174f426b7b41685f2593daaae9b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995046"
---
# <a name="taskbar-peripheral-status-sample"></a>Peripheriestatus der Taskleiste (Beispiel)

Veranschaulicht Überlagerungen und Status leisten des Task leisten Symbols.

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>BESCHREIBUNG

In diesem Beispiel wird eine Beispiel-Task leisten Schaltfläche erstellt, die die Verwendung von [**ITaskbarList3:: setverlayicon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) veranschaulicht, indem Sie verschiedene über ein Menü ausgewählte Überlagerungen anwenden können.

Das Beispiel bietet außerdem die Option, eine Statusanzeige auf der Schaltfläche zu simulieren, die die Verwendung von [**ITaskbarList3:: setprogressstate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) und [**ITaskbarList3:: setprogressvalue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) veranschaulicht, indem zunächst eine unbedingte Statusanzeige (tbpf- \_ unbestimmt) und dann ein normaler proportionaler Indikator (tbpf \_ Normal) angezeigt wird.

## <a name="requirements"></a>Requirements (Anforderungen)



| Produkt                                | Minimale Produkt Version |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Taskbarperipheralstatus-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarPeripheralStatus) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel von der Eingabeaufforderung aus:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **taskbarperipheralstatus** .
2.  Geben Sie `msbuild PeripheralStatus.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **taskbarperipheralstatus** .
2.  Doppelklicken Sie auf das Symbol für die Datei "peripheralstatus. sln", um das Projekt in Visual Studio zu öffnen.
3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie zu dem Verzeichnis, das die neue ausführbare Datei enthält (z.b. `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug` ), indem Sie die Eingabeaufforderung oder den Windows-Explorer verwenden.

    -   Wenn Sie die Befehlszeile verwenden, geben Sie ein `PeripheralStatus.exe` .
    -   Wenn Sie Windows-Explorer verwenden, doppelklicken Sie auf das Symbol für PeripheralStatus.exe.

    Ein neues Fenster wird mit einer zugeordneten Task leisten Schaltfläche geöffnet.

2.  Um die Überlagerungen zu veranschaulichen, wählen Sie über **Lagerung 1** oder über **Lagerung 2** im Fenster **Peripherie Status** des Fensters aus. Das ausgewählte Overlay wird auf der Task leisten Schaltfläche angezeigt. Um das Overlay zu entfernen, wählen Sie **Overlay löschen** aus.
3.  Um die Status Anzeige zu veranschaulichen, wählen Sie im Fenster **Peripherie Status** des Fensters die Option Status **simulieren** aus. Die Task leisten Schaltfläche zeigt eine unbestimmende Statusanzeige an und wechselt dann zu einem normalen Indikator.
4.  Wählen Sie im Menü **Datei** des Fensters die Option **Beenden** aus, um das Programm zu beenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Task leisten Erweiterungen](taskbar-extensions.md)
</dt> </dl>

 

 



