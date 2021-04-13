---
title: Windows Hallo Welt-Beispiel
description: Diese Beispielanwendung zeigt, wie ein minimales Windows-Programm erstellt wird.
ms.assetid: ec316ad8-d01d-4558-91b6-19fdbba3d520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932d3b0c524c643022904b08402507d4a603adb
ms.sourcegitcommit: e084958628fb997e9e11fe08574d82edbba07dbf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2019
ms.locfileid: "104311675"
---
# <a name="windows-hello-world-sample"></a>Windows Hallo Welt-Beispiel

Diese Beispielanwendung zeigt, wie ein minimales Windows-Programm erstellt wird.

## <a name="description"></a>BESCHREIBUNG

Die Beispielanwendung Windows Hallo Welt erstellt und zeigt ein leeres Fenster an, wie im folgenden Screenshot gezeigt. Dieses Beispiel wird in [Modul 1 erläutert. Ihr erstes Windows-Programm](your-first-windows-program.md).

![Screenshot des Beispiel Programms](images/window01.png)

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist [hier](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/begin/LearnWin32/HelloWorld)verfügbar.

Um es herunterzuladen, navigieren Sie zum Stamm des beispielrepository auf GitHub ([Microsoft/Windows-Classic-Samples](https://github.com/microsoft/Windows-classic-samples/)), und klicken Sie auf die Schaltfläche **Klonen oder herunterladen** , um die ZIP-Datei aller Beispiele auf Ihren Computer herunterzuladen. Entzippen Sie dann den Ordner.

Um das Beispiel in Visual Studio zu öffnen, wählen Sie Datei > Öffnen > Projekt > **Projekt** Mappe aus, und navigieren Sie zu dem Speicherort, an dem Sie den Ordner entzippt haben, und **Windows-Classic-Samples-Master/Samples/Win7Samples/BEGIN/LearnWin32/Hello** Öffnen Sie die Datei " **HelloWorld. sln**".

Nachdem das Beispiel geladen wurde, müssen Sie es aktualisieren, damit es mit Windows 10 funktioniert. Wählen Sie im Menü **Projekt** in Visual Studio die Option **Eigenschaften** aus. Aktualisieren Sie die **Windows SDK Version** in ein Windows 10 SDK, z. b. 10.0.17763.0 oder eine bessere Version. Ändern Sie dann das **Platt Form Toolset** in Visual Studio 2017 oder höher. Nun können Sie das Beispiel ausführen, indem Sie F5 drücken.


## <a name="related-topics"></a>Zugehörige Themen

* [Erlernen Sie das Program mieren für Windows: Beispiel Code](learn-to-program-for-windows--sample-code.md)
* [Modul 1. Ihr erstes Windows-Programm](your-first-windows-program.md)
