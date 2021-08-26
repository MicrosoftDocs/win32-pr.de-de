---
title: Beispiel für einen Prioritätsvergleich
description: Zeigt, wie Sie Windows Animation mit Ihrem eigenen Prioritätsvergleich verwenden, indem Sie Direct2D für das Rendering verwenden.
ms.assetid: aa09f8a7-1919-4a44-832f-be8b848d6a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafeb2332de02115cbb8af2f2afd69a2fc783be9908a91dbb4e9bb0615876bd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008190"
---
# <a name="priority-comparison-sample"></a>Beispiel für einen Prioritätsvergleich

Zeigt, wie Sie Windows Animation mit Ihrem eigenen Prioritätsvergleich verwenden, indem Sie Direct2D für das Rendering verwenden.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist an den folgenden Speicherorten verfügbar.



| Standort                               | Pfad/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Windows Software Development Kit (SDK) | [Microsoft Windows Software Development Kit 7.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Codegalerie                           | [Windows Beispielcode für den Animations-Manager](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

Nachdem Sie das Windows SDK heruntergeladen und installiert haben, finden Sie die Beispiele im Installationsverzeichnis. Wenn Sie beispielsweise den Standardinstallationspfad für das Windows SDK für Windows 7 verwenden, werden die Beispiele in C: Microsoft SDKs für \\ Programme \\ Windows \\ \\ v7.0-Beispiele \\ installiert.

## <a name="building-the-sample"></a>Erstellen des Beispiels

Verwenden Sie eine der folgenden Methoden, um das Beispiel zu erstellen.

**So erstellen Sie das Beispiel an der Eingabeaufforderung**

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum Projektverzeichnis PriorityComparison. Der Standardinstallationspfad für dieses Beispiel lautet z. B. C: \\ \\ Programme Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Multimedia \\ \\ WindowsAnimation \\ PriorityComparison.

2.  Führen Sie den folgenden Befehl aus: **msbuild PriorityComparison.sln**

**So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt)**

1.  Öffnen Sie Windows Explorer, und navigieren Sie zum Projektverzeichnis PriorityComparison.

2.  Doppelklicken Sie auf das Symbol für die Datei PriorityComparison.sln, um das Projekt in Visual Studio zu öffnen.

    > [!Note]  
    > Die Dateierweiterung .sln wird in den Standardordnereinstellungen nicht angezeigt. In diesem Fall kann es durch sein eindeutiges Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Solution" identifiziert werden.

     

3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

So führen Sie das Beispiel aus:

1.  Navigieren Sie über die Eingabeaufforderung oder Windows Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.

2.  Führen Sie **PriorityComparison.exe** an der Eingabeaufforderung aus, oder doppelklicken Sie auf das Symbol für PriorityComparison.exe in Windows Explorer.

3.  Beispielbilder werden aus der Bildbibliothek geladen. Ändern Sie die Größe des Fensters, oder drücken Sie die Leertaste, und die Bilder werden in die Mitte verschoben.

4.  Verwenden Sie die NACH-LINKS- und NACH-RECHTS-TASTE, um verschiedene Bilder auszuwählen (je schneller die Taste gedrückt wird, desto schneller ändert sich die Auswahl).

5.  Verwenden Sie die NACH-OBEN- und NACH-UNTEN-TASTE, um eine Welle durch die Bilder zu erstellen (je schneller die Taste gedrückt wird, desto schneller die Welle).

 

 




