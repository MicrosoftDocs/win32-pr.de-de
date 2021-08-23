---
title: Beispiel für Rasterlayout
description: Zeigt, wie Sie Windows Animation verwenden, indem Sie Direct2D verwenden, um ein Raster von Bildern zu animieren.
ms.assetid: f2f24058-c532-45ad-bde8-d05cfffcd505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf287dc7d6f96b9b5db4ce3fff7d30c34b1f8b998518dbdddc9d7abbda793330
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999680"
---
# <a name="grid-layout-sample"></a>Beispiel für Rasterlayout

Zeigt, wie Sie Windows Animation verwenden, indem Sie Direct2D verwenden, um ein Raster von Bildern zu animieren.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist an den folgenden Speicherorten verfügbar.



| Standort                               | Pfad/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Windows Software Development Kit (SDK) | [Microsoft Windows Software Development Kit 7.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Codegalerie                           | [Windows Beispielcode für den Animations-Manager](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

Nachdem Sie das Windows SDK heruntergeladen und installiert haben, finden Sie die Beispiele im Installationsverzeichnis. Wenn Sie beispielsweise den Standardinstallationspfad für das Windows SDK für Windows 7 verwenden, werden die Beispiele unter C: Programme \\ \\ Microsoft SDKs Windows v7.0 Samples( C: Programme Microsoft SDKs \\ Windows \\ v7.0 \\ Samples) installiert.

## <a name="building-the-sample"></a>Erstellen des Beispiels

Verwenden Sie eine der folgenden Methoden, um das Beispiel zu erstellen.

**So erstellen Sie das Beispiel an der Eingabeaufforderung**

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum GridLayout-Projektverzeichnis. Der Standardinstallationspfad für dieses Beispiel ist beispielsweise C: Programme \\ \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Multimedia \\ \\ WindowsAnimation \\ GridLayout

2.  Führen Sie den folgenden Befehl aus: **msbuild GridLayout.sln**

**So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt)**

1.  Öffnen Windows Explorer, und navigieren Sie zum GridLayout-Projektverzeichnis.

    > [!Note]  
    > Die Dateierweiterung SLN wird unter den Standardordnereinstellungen nicht angezeigt. In diesem Fall kann es durch sein eindeutiges Symbol oder durch seine Typbeschreibung identifiziert werden, "Microsoft Visual Studio Lösung".

     

2.  Doppelklicken Sie auf das Symbol für die Datei GridLayout.sln, um das Projekt in der Visual Studio.

3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

So führen Sie das Beispiel aus:

1.  Navigieren Sie zu dem Verzeichnis, das die neue ausführbare Datei enthält, indem Sie entweder die Eingabeaufforderung oder den Windows verwenden.

2.  Führen **GridLayout.exe** eingabeaufforderung aus, oder doppelklicken Sie auf das Symbol für GridLayout.exe im Windows Explorer.

3.  Beispielbilder werden aus der Bildbibliothek geladen. Ändern Sie die Größe des Fensters, und die Bilder werden in einem Raster angeordnet.

 

 




