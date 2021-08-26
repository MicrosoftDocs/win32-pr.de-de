---
title: beispiel für Timer-Driven Animation
description: Zeigt, wie Windows Animation mit dem Animationszeitgeber verwendet wird, während GDI+ verwendet wird, um die Hintergrundfarbe eines Fensters zu animieren.
ms.assetid: c50a4bfb-855b-4837-a117-84f412943b14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8071d51906ba2d0d7b59acb7b1b5531fcb5c577fbbf0d47ab5039d3f43e2eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008160"
---
# <a name="timer-driven-animation-sample"></a>beispiel für Timer-Driven Animation

Zeigt, wie Windows Animation mit dem Animationszeitgeber verwendet wird, während GDI+ verwendet wird, um die Hintergrundfarbe eines Fensters zu animieren.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist an den folgenden Speicherorten verfügbar.



| Standort                               | Pfad/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Windows Software Development Kit (SDK) | [Microsoft Windows Software Development Kit 7.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Codegalerie                           | [Windows Beispielcode für den Animations-Manager](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

Nachdem Sie das Windows SDK heruntergeladen und installiert haben, finden Sie die Beispiele im Installationsverzeichnis. Wenn Sie beispielsweise den Standardinstallationspfad für das Windows SDK für Windows 7 verwenden, werden die Beispiele in C: Microsoft SDKs für \\ Programmdateien \\ Windows \\ \\ v7.0-Beispiele \\ installiert.

## <a name="building-the-sample"></a>Erstellen des Beispiels

Verwenden Sie eine der folgenden Methoden, um das Beispiel zu erstellen.

**So erstellen Sie das Beispiel an der Eingabeaufforderung**

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum Projektverzeichnis TimerDriven. Der Standardinstallationspfad für dieses Beispiel lautet z. B. C: \\ \\ Programme Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Multimedia \\ \\ WindowsAnimation \\ TimerDriven.

2.  Führen Sie den folgenden Befehl aus: **msbuild TimerDriven.sln**

**So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt)**

1.  Öffnen Sie Windows Explorer, und navigieren Sie zum Projektverzeichnis TimerDriven.

2.  Doppelklicken Sie auf das Symbol für die Datei TimerDriven.sln, um das Projekt in Visual Studio zu öffnen.

    > [!Note]  
    > Die Dateierweiterung .sln wird in den Standardordnereinstellungen nicht angezeigt. In diesem Fall kann es durch sein eindeutiges Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Solution" identifiziert werden.

     

3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

So führen Sie das Beispiel aus:

1.  Navigieren Sie entweder über die Eingabeaufforderung oder Windows Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.

2.  Führen Sie **TimerDriven.exe** an der Eingabeaufforderung aus, oder doppelklicken Sie auf das Symbol für TimerDriven.exe in Windows Explorer.

3.  Klicken Sie auf eine beliebige Stelle im Clientbereich, und die Hintergrundfarbe des Fensters ändert sich in eine zufällige Farbe.

 

 




