---
title: Beispiel für Application-Driven Animation
description: Zeigt die Windows-Animation in der Anwendungs gesteuerten Konfiguration mithilfe von Direct2D zum Animieren der Hintergrundfarbe eines Fensters und zum Synchronisieren der Aktualisierungsrate.
ms.assetid: deefc473-6749-4e2b-ad34-33ccd206d231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b24905d09ac6559527146ebf572666a6a84f5
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/10/2020
ms.locfileid: "106337213"
---
# <a name="application-driven-animation-sample"></a>Beispiel für Application-Driven Animation

Zeigt die Windows-Animation in der Anwendungs gesteuerten Konfiguration mithilfe von Direct2D zum Animieren der Hintergrundfarbe eines Fensters und zum Synchronisieren der Aktualisierungsrate.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist in den folgenden Speicherorten verfügbar.



| Standort                               | Pfad/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Windows Software Development Kit (SDK) | [Microsoft Windows Software Development Kit 7,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Codegalerie                           | [Windows Animation Manager-Beispiel Code](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

Nachdem Sie die Windows SDK heruntergeladen und installiert haben, finden Sie die Beispiele im Installationsverzeichnis. Wenn Sie z. b. den Standard Installationspfad für die Windows SDK für Windows 7 verwenden, werden die Beispiele unter C: \\ Programme \\ Microsoft sdert \\ Windows \\ v 7.0 Samples installiert \\ .

## <a name="building-the-sample"></a>Erstellen des Beispiels

Verwenden Sie eine der folgenden Methoden, um das Beispiel zu erstellen.

**So erstellen Sie das Beispiel an der Eingabeaufforderung**

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis "appgesteuerte". Der Standard Installationspfad für dieses Beispiel lautet z. b. C: \\ Program Files \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ windowsanimation \\ appgesteu.

2.  Führen Sie den folgenden Befehl aus: **MSBuild apprun. sln**

**So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt)**

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis "appgesteuerte".

2.  Doppelklicken Sie auf das Symbol für die Datei appgesteuerte sln, um das Projekt in Visual Studio zu öffnen.

    > [!Note]  
    > Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt. In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.

     

3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

So führen Sie das Beispiel aus:

1.  Navigieren Sie zu dem Verzeichnis, das die neue ausführbare Datei enthält. verwenden Sie dazu entweder die Eingabeaufforderung oder den Windows-Explorer.

2.  Führen Sie **AppDriven.exe** an der Eingabeaufforderung aus, oder Doppelklicken Sie im Windows-Explorer auf das Symbol für AppDriven.exe.

3.  Klicken Sie im Client Bereich auf eine beliebige Stelle, und die Hintergrundfarbe des Fensters wechselt in eine zufällige Farbe.

 

 




