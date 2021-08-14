---
description: Veranschaulicht eine Miniaturansichtssymbolleiste, ein aktives Symbolleisten-Steuerelement, das in die Miniaturansichtsvorschau eines Fensters eingebettet ist und verwendet wird, um Zugriff auf die Schlüsselbefehle eines Fensters zu ermöglichen, ohne dass der Benutzer das Fenster der Anwendung wiederherstellen oder aktivieren muss.
title: Symbolleistenbeispiel für die Miniaturbild-Taskleiste
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4936FF67-19EE-4963-BE4C-3D40350C64A9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: cd16ee40bfb480b3e7eacef2bc4681e61fdb24ace1ac68985e2016ce11b7c0e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219629"
---
# <a name="taskbar-thumbnail-toolbar-sample"></a>Symbolleistenbeispiel für die Miniaturbild-Taskleiste

Veranschaulicht eine Miniaturansichtssymbolleiste, ein aktives Symbolleisten-Steuerelement, das in die Miniaturansichtsvorschau eines Fensters eingebettet ist und verwendet wird, um Zugriff auf die Schlüsselbefehle eines Fensters zu ermöglichen, ohne dass der Benutzer das Fenster der Anwendung wiederherstellen oder aktivieren muss.

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Requirements](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Erstellen des Beispiels](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="description"></a>BESCHREIBUNG

In diesem Beispiel wird gezeigt, wie Sie eine einfache Symbolleiste für eine Vorschau der Taskleistenminiatur bereitstellen. Die Symbolleiste besteht aus drei Schaltflächen. Wenn Sie auf eine Schaltfläche klicken, wird ein Fenster angezeigt, um zu bestätigen, dass die Schaltfläche aktiviert wurde. Die folgenden APIs werden veranschaulicht:

-   [**ITaskbarList3::ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**ITaskbarList3::ThumbBarSetImageList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   [**THUMBBUTTON-Struktur**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)

## <a name="requirements"></a>Anforderungen



| Product (Produkt)                                | Mindestversion des Produkts |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [TaskbarThumbnailToolbar-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarThumbnailToolbar) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel über die Eingabeaufforderung:

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum Projektverzeichnis **TaskbarThumbnailToolbar.**
2.  Geben Sie `msbuild ThumbnailToolbar.sln` ein.

So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows Explorer, und navigieren Sie zum Projektverzeichnis **TaskbarThumbnailToolbar.**
2.  Doppelklicken Sie auf das Symbol für die Datei ThumbnailToolbar.sln, um das Projekt in Visual Studio zu öffnen.
3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie mithilfe der Eingabeaufforderung oder Windows Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält (z. `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug` B. ).

    -   Wenn Sie die Befehlszeile verwenden, geben Sie `ThumbnailToolbar.exe` ein.
    -   Doppelklicken Sie bei Verwendung Windows Explorers auf das Symbol für ThumbnailToolbar.exe.

    Ein neues Fenster mit einer zugeordneten Taskleistenschaltfläche wird geöffnet.

2.  Zeigen Sie mit dem Mauszeiger auf die Taskleistenschaltfläche **ThumbnailToolbar,** damit die Vorschau angezeigt wird. Klicken Sie auf eine der drei Schaltflächen (grün, gelb, rot), die in der Symbolleiste der Vorschau angezeigt werden.
3.  Klicken Sie im Menü **Datei** des Fensters auf **Beenden,** um das Programm zu beenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskleistenerweiterungen](taskbar-extensions.md)
</dt> </dl>

 

 



