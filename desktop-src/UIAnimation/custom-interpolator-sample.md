---
title: Beispiel für benutzerdefiniertes Interpolator
description: Zeigt, wie die Windows-Animation mit Ihrem eigenen benutzerdefinierten Interpolator verwendet wird, wobei Direct2D zum Rendern verwendet wird.
ms.assetid: 90c4a53a-5c5e-4dcc-8946-bc8f23a07ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a1a2ef09d603eaefac90b2ae25b3f533ba307
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/10/2020
ms.locfileid: "104101394"
---
# <a name="custom-interpolator-sample"></a>Beispiel für benutzerdefiniertes Interpolator

Zeigt, wie die Windows-Animation mit Ihrem eigenen benutzerdefinierten Interpolator verwendet wird, wobei Direct2D zum Rendern verwendet wird. Beispiel Bilder werden aus der Bildbibliothek geladen.

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

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis custominterpolator. Der Standard Installationspfad für dieses Beispiel lautet z. b. C: \\ Program Files \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ windowsanimation \\ custominterpolator.

2.  Führen Sie den folgenden Befehl aus: **MSBuild custominterpolator. sln**

**So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt)**

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis custominterpolator.

    > [!Note]  
    > Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt. In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.

     

2.  Doppelklicken Sie auf das Symbol für die Datei custominterpolator. sln, um das Projekt in Visual Studio zu öffnen.

3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

So führen Sie das Beispiel aus:

1.  Navigieren Sie zu dem Verzeichnis, das die neue ausführbare Datei enthält. verwenden Sie dazu entweder die Eingabeaufforderung oder den Windows-Explorer.

2.  Führen Sie **CustomInterpolator.exe** an der Eingabeaufforderung aus, oder Doppelklicken Sie im Windows-Explorer auf das Symbol für CustomInterpolator.exe.
3.  Ändern Sie die Größe des Fensters, oder drücken Sie die Leertaste, und die Bilder werden sich nach dem Zufallsprinzip in der Mitte des Client Bereichs anordnen.

4.  Drücken Sie die nach-oben-oder nach-unten-Taste, und die Bilder werden in Richtung oben oder unten im Client Bereich beschleunigt.

 

 




