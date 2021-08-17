---
title: Application-Driven Animation Sample
description: Zeigt Windows Animation in der anwendungsgesteuerten Konfiguration an, indem Direct2D verwendet wird, um die Hintergrundfarbe eines Fensters zu animieren und mit der Aktualisierungsrate zu synchronisieren.
ms.assetid: deefc473-6749-4e2b-ad34-33ccd206d231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfbb5ce71ddeff6a37c2d872e0e1e93fdc58cde9fcc8359560d9d386ba7a0834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137373"
---
# <a name="application-driven-animation-sample"></a>Application-Driven Animation Sample

Zeigt Windows Animation in der anwendungsgesteuerten Konfiguration an, indem Direct2D verwendet wird, um die Hintergrundfarbe eines Fensters zu animieren und mit der Aktualisierungsrate zu synchronisieren.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist an den folgenden Speicherorten verfügbar.



| Standort                               | Pfad/URL                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| Windows Software Development Kit (SDK) | [Microsoft Windows Software Development Kit 7.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| Codegalerie                           | [Windows Beispielcode für den Animations-Manager](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

Nachdem Sie das Windows SDK heruntergeladen und installiert haben, finden Sie die Beispiele im Installationsverzeichnis. Wenn Sie beispielsweise den Standardinstallationspfad für das Windows SDK für Windows 7 verwenden, werden die Beispiele unter C: Programme \\ \\ Microsoft SDKs Windows v7.0 Samples( C: Programme Microsoft SDKs \\ Windows \\ v7.0 \\ Samples) installiert.

## <a name="building-the-sample"></a>Erstellen des Beispiels

Verwenden Sie eine der folgenden Methoden, um das Beispiel zu erstellen.

**So erstellen Sie das Beispiel an der Eingabeaufforderung**

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum Projektverzeichnis AppDriven. Der Standardinstallationspfad für dieses Beispiel ist beispielsweise C: Programme \\ \\ Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Multimedia \\ \\ WindowsAnimation \\ AppDriven.

2.  Führen Sie den folgenden Befehl aus: **msbuild AppDriven.sln**

**So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt)**

1.  Öffnen Windows Explorer, und navigieren Sie zum Projektverzeichnis AppDriven.

2.  Doppelklicken Sie auf das Symbol für die Datei AppDriven.sln, um das Projekt in Visual Studio.

    > [!Note]  
    > Die Dateierweiterung SLN wird unter den Standardordnereinstellungen nicht angezeigt. In diesem Fall kann er anhand seines eindeutigen Symbols oder seiner Typbeschreibung "Microsoft Visual Studio identifiziert werden.

     

3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

So führen Sie das Beispiel aus:

1.  Navigieren Sie zu dem Verzeichnis, das die neue ausführbare Datei enthält, indem Sie entweder die Eingabeaufforderung oder den Windows verwenden.

2.  Führen **AppDriven.exe** eingabeaufforderung aus, oder doppelklicken Sie auf das Symbol für AppDriven.exe im Windows Explorer.

3.  Klicken Sie auf eine beliebige Stelle im Clientbereich, und die Hintergrundfarbe des Fensters ändert sich in eine zufällige Farbe.

 

 




