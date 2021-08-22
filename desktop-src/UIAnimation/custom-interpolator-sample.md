---
title: Beispiel für benutzerdefinierte Interpolatoren
description: Zeigt, wie Sie Windows Animation mit Ihrem eigenen benutzerdefinierten Interpolator verwenden, wobei Direct2D für das Rendering verwendet wird.
ms.assetid: 90c4a53a-5c5e-4dcc-8946-bc8f23a07ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c801822bd50eebe9f405cad00bc8ffcd7ac2d611924a3ff0bae91d30bc9f249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999700"
---
# <a name="custom-interpolator-sample"></a>Beispiel für benutzerdefinierte Interpolatoren

Zeigt, wie Sie Windows Animation mit Ihrem eigenen benutzerdefinierten Interpolator verwenden, wobei Direct2D für das Rendering verwendet wird. Beispielbilder werden aus der Bildbibliothek geladen.

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

1.  Öffnen Sie das Eingabeaufforderungsfenster, und navigieren Sie zum Projektverzeichnis CustomInterpolator. Der Standardinstallationspfad für dieses Beispiel lautet z. B. C: \\ \\ Programme Microsoft SDKs Windows \\ \\ v7.0 \\ Samples Multimedia \\ \\ WindowsAnimation \\ CustomInterpolator

2.  Führen Sie den folgenden Befehl aus: **msbuild CustomInterpolator.sln**

**So erstellen Sie das Beispiel mit Microsoft Visual Studio (bevorzugt)**

1.  Öffnen Sie Windows Explorer, und navigieren Sie zum Projektverzeichnis CustomInterpolator.

    > [!Note]  
    > Die Dateierweiterung .sln wird in den Standardordnereinstellungen nicht angezeigt. In diesem Fall kann es durch sein eindeutiges Symbol oder durch die Typbeschreibung "Microsoft Visual Studio Solution" identifiziert werden.

     

2.  Doppelklicken Sie auf das Symbol für die Datei CustomInterpolator.sln, um das Projekt in Visual Studio zu öffnen.

3.  Klicken Sie im Menü **Build** (Erstellen) auf **Build Solution** (Projektmappe erstellen).

## <a name="running-the-sample"></a>Ausführen des Beispiels

So führen Sie das Beispiel aus:

1.  Navigieren Sie über die Eingabeaufforderung oder Windows Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.

2.  Führen Sie **CustomInterpolator.exe** an der Eingabeaufforderung aus, oder doppelklicken Sie auf das Symbol für CustomInterpolator.exe in Windows Explorer.
3.  Ändern Sie die Größe des Fensters, oder drücken Sie die Leertaste, und die Bilder ordnen sich zufällig in der Mitte des Clientbereichs an.

4.  Drücken Sie den Pfeil nach oben oder unten, und die Bilder werden in Richtung oben oder unten im Clientbereich beschleunigt.

 

 




