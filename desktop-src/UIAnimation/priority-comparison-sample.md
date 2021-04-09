---
title: Beispiel für Prioritäts Vergleich
description: Zeigt, wie die Windows-Animation mit einem eigenen Prioritäts Vergleich verwendet wird, wobei Direct2D für das Rendering verwendet wird.
ms.assetid: aa09f8a7-1919-4a44-832f-be8b848d6a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfcb20785d6a4c3c3384b85327a0e27d93c58d7
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/10/2020
ms.locfileid: "104101391"
---
# <a name="priority-comparison-sample"></a>Beispiel für Prioritäts Vergleich

Zeigt, wie die Windows-Animation mit einem eigenen Prioritäts Vergleich verwendet wird, wobei Direct2D für das Rendering verwendet wird.

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

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis prioritycomparison. Der Standard Installationspfad für dieses Beispiel lautet z. b. C: \\ Program Files \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ windowsanimation \\ prioritycomparison.

2.  Führen Sie den folgenden Befehl aus: **MSBuild prioritycomparison. sln**

**So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt)**

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis prioritycomparison.

2.  Doppelklicken Sie auf das Symbol für die Datei prioritycomparison. sln, um das Projekt in Visual Studio zu öffnen.

    > [!Note]  
    > Die Dateinamenerweiterung. sln wird unter den Standardordner Einstellungen nicht angezeigt. In dieser Situation kann Sie durch das eindeutige Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Lösung" identifiziert werden.

     

3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

So führen Sie das Beispiel aus:

1.  Navigieren Sie zu dem Verzeichnis, das die neue ausführbare Datei enthält. verwenden Sie dazu entweder die Eingabeaufforderung oder den Windows-Explorer.

2.  Führen Sie **PriorityComparison.exe** an der Eingabeaufforderung aus, oder Doppelklicken Sie im Windows-Explorer auf das Symbol für PriorityComparison.exe.

3.  Beispiel Bilder werden aus der Bildbibliothek geladen. Ändern Sie die Größe des Fensters, oder drücken Sie die Leertaste, und die Bilder werden in die Mitte verschoben.

4.  Verwenden Sie die nach-links-und nach-rechts-Taste, um unterschiedliche Bilder auszuwählen (je schneller die Taste gedrückt wird, desto schneller wird die Auswahl geändert).

5.  Verwenden Sie die nach-oben-und nach-unten-Taste, um eine Welle durch die Bilder zu erstellen (desto schneller wird die Taste gedrückt, desto schneller wird die Welle).

 

 




