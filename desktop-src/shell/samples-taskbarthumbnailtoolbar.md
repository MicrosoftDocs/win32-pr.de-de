---
description: Veranschaulicht die Miniaturansicht einer Miniaturansicht, ein aktives Symbolleisten-Steuerelement, das in die Miniaturansicht des Fensters eingebettet ist, um den Zugriff auf die Schlüsselbefehle eines Fensters zu ermöglichen, ohne dass der Benutzer das Fenster der Anwendung wiederherstellt oder aktiviert.
title: Symbolleistenbeispiel für die Miniaturbild-Taskleiste
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4936FF67-19EE-4963-BE4C-3D40350C64A9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e61208f15772a43138e6cd7a38fd6327445bdfa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980321"
---
# <a name="taskbar-thumbnail-toolbar-sample"></a>Symbolleistenbeispiel für die Miniaturbild-Taskleiste

Veranschaulicht die Miniaturansicht einer Miniaturansicht, ein aktives Symbolleisten-Steuerelement, das in die Miniaturansicht des Fensters eingebettet ist, um den Zugriff auf die Schlüsselbefehle eines Fensters zu ermöglichen, ohne dass der Benutzer das Fenster der Anwendung wiederherstellt oder aktiviert.

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>BESCHREIBUNG

In diesem Beispiel wird gezeigt, wie eine einfache Symbolleiste für eine Vorschau der Task leisten Vorschau bereitgestellt wird. Die Symbolleiste besteht aus drei Schaltflächen. Durch Klicken auf eine Schaltfläche wird ein Fenster angezeigt, um zu bestätigen, dass die Schaltfläche aktiviert Die folgenden APIs werden veranschaulicht:

-   [**ITaskbarList3:: ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**ITaskbarList3:: thumbbarsetimagelist**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   [**ThumbButton**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton) -Struktur

## <a name="requirements"></a>Requirements (Anforderungen)



| Produkt                                | Minimale Produkt Version |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Taskbarthumbnailtoolbar-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarThumbnailToolbar) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel von der Eingabeaufforderung aus:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **taskbarthumbnailtoolbar** .
2.  Geben Sie `msbuild ThumbnailToolbar.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **taskbarthumbnailtoolbar** .
2.  Doppelklicken Sie auf das Symbol für die Datei thumbnailtoolbar. sln, um das Projekt in Visual Studio zu öffnen.
3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie zu dem Verzeichnis, das die neue ausführbare Datei enthält (z.b. `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug` ), indem Sie die Eingabeaufforderung oder den Windows-Explorer verwenden.

    -   Wenn Sie die Befehlszeile verwenden, geben Sie ein `ThumbnailToolbar.exe` .
    -   Wenn Sie Windows-Explorer verwenden, doppelklicken Sie auf das Symbol für ThumbnailToolbar.exe.

    Ein neues Fenster wird mit einer zugeordneten Task leisten Schaltfläche geöffnet.

2.  Zeigen Sie mit dem Mauszeiger auf die Schaltfläche **thumbnailtoolbar** Taskleiste, sodass die Vorschau angezeigt wird. Klicken Sie auf eine der drei Schaltflächen (grün, gelb, rot), die auf der Symbolleiste der Vorschau angezeigt werden.
3.  Wählen Sie im Menü **Datei** des Fensters die Option **Beenden** aus, um das Programm zu beenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Task leisten Erweiterungen](taskbar-extensions.md)
</dt> </dl>

 

 



