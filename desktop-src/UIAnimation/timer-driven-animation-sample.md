---
title: Beispiel für Timer-Driven Animation
description: Zeigt, wie die Windows-Animation mit dem Animations Timer verwendet wird, während GDI+ zum Animieren der Hintergrundfarbe eines Fensters verwendet wird.
ms.assetid: c50a4bfb-855b-4837-a117-84f412943b14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec145b087a112c7482de3a749c690a1824195ea3
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/10/2020
ms.locfileid: "104314583"
---
# <a name="timer-driven-animation-sample"></a>Beispiel für Timer-Driven Animation

Zeigt, wie die Windows-Animation mit dem Animations Timer verwendet wird, während GDI+ zum Animieren der Hintergrundfarbe eines Fensters verwendet wird.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist in den folgenden Speicherorten verfügbar.



| Standort                               | Pfad/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Windows Software Development Kit (SDK) | [Microsoft Windows Software Development Kit 7,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Codegalerie                           | [Windows Animation Manager-Beispiel Code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

Nachdem Sie die Windows SDK heruntergeladen und installiert haben, finden Sie die Beispiele im Installationsverzeichnis. Wenn Sie z. b. den Standard Installationspfad für die Windows SDK für Windows 7 verwenden, werden die Beispiele unter C: \\ Programme \\ Microsoft sdert \\ Windows \\ v 7.0 Samples installiert \\ .

## <a name="building-the-sample"></a>Erstellen des Beispiels

Verwenden Sie eine der folgenden Methoden, um das Beispiel zu erstellen.

**So erstellen Sie das Beispiel an der Eingabeaufforderung**

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum timergesteuerte Projektverzeichnis. Der Standard Installationspfad für dieses Beispiel lautet z. b. C: \\ Program Files \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ windowsanimation \\ Timer-gesteuert.

2.  Führen Sie den folgenden Befehl aus: **MSBuild Timer-gesteuerte. sln**

**So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt)**

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Verzeichnis "timergesteuerte Projekt".

2.  Doppelklicken Sie auf das Symbol für die Datei timergesteuerte. sln, um das Projekt in Visual Studio zu öffnen.

    > [!Note]  
    > Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt. In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.

     

3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

So führen Sie das Beispiel aus:

1.  Navigieren Sie zu dem Verzeichnis, das die neue ausführbare Datei enthält. verwenden Sie dazu entweder die Eingabeaufforderung oder den Windows-Explorer.

2.  Führen Sie **TimerDriven.exe** an der Eingabeaufforderung aus, oder Doppelklicken Sie im Windows-Explorer auf das Symbol für TimerDriven.exe.

3.  Klicken Sie im Client Bereich auf eine beliebige Stelle, und die Hintergrundfarbe des Fensters wechselt in eine zufällige Farbe.

 

 




