---
description: Die Directory-Tabelle gibt das Layout einer Installation an.
ms.assetid: 3f2e1cc2-6b36-4615-86e6-e78485edd2f7
title: Verwenden der Verzeichnistabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f550f32006df16db5811e0fbf5022253373a4b1551983ddda2db55655b4061f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141319"
---
# <a name="using-the-directory-table"></a>Verwenden der Verzeichnistabelle

Die [Directory-Tabelle](directory-table.md) gibt das Layout einer Installation an. Wenn die Verzeichnisse während der [CostFinalize-Aktion](costfinalize-action.md)aufgelöst werden, werden die Schlüssel in der Verzeichnistabelle zu [Eigenschaften,](properties.md) die auf Verzeichnispfade festgelegt sind. Beachten Sie, dass das Installationsprogramm eine Reihe von [Standardeigenschaften](properties.md) auf Systemordnerpfade festlegt. Eine Liste der Eigenschaften, die auf Systemordner festgelegt sind, finden Sie in der [Eigenschaftenreferenz.](property-reference.md)

Die beste Möglichkeit, den Zielspeicherort für ein Verzeichnis anzugeben, besteht darin, die [Verzeichnistabelle](directory-table.md) in Ihrem Installationspaket zu erstellen, um den richtigen Speicherort bereitzustellen, wie in diesem Abschnitt erläutert. Wenn der Verzeichnisspeicherort zum Zeitpunkt der Installation geändert werden muss, lesen Sie auch den Abschnitt [Ändern des Zielspeicherorts für ein Verzeichnis.](changing-the-target-location-for-a-directory.md)

Im Folgenden ist ein Beispiel für eine Directory-Tabelle aufgeführt.



| Verzeichnis     | \_Übergeordnetes Verzeichnis | DefaultDir |
|---------------|-------------------|------------|
| Targetdir     |                   | SourceDir  |
| EXEDIR        | Targetdir         | App        |
| DLLDIR        | EXEDIR            | Diskretisierung        |
| DesktopFolder | Targetdir         | Desktop    |



 

Jede Zeile der Directory-Tabelle gibt ein Verzeichnis sowohl an der Quelle als auch am Ziel an. Angenommen, das Installationspaket befindet sich in der \\ \\ \\ Anwendungsquelle \\ . Da das Feld Directory \_ Parent der ersten Zeile NULL ist, gibt dieser Datensatz die Stammverzeichnisse sowohl für die Quelle als auch für das Ziel an. Für die Quelle wird der Wert dieses Verzeichnisses durch das Feld DefaultDir angegeben. Die [**SourceDir-Eigenschaft**](sourcedir.md) verwendet standardmäßig den Speicherort des Installationspakets. Daher ist das Stammquellverzeichnis die Anwendungsquelle, es sei denn, die **SourceDir-Eigenschaft** wird \\ \\ \\ \\ überschrieben.

Das Feld Verzeichnis des ersten Datensatzes gibt den Speicherort des Stammzielverzeichnisses an. In diesem Fall gibt der Wert der [**TARGETDIR-Eigenschaft**](targetdir.md) dieses Verzeichnis an. In der Regel wird der Wert der **TARGETDIR-Eigenschaft** in der Befehlszeile oder über eine Benutzeroberfläche festgelegt. Nehmen Sie in diesem Fall an, dass die **TARGETDIR-Eigenschaft** auf C: Program Files Target festgelegt \\ \\ \\ ist.

Für den zweiten Datensatz ist das Feld Directory Parent (Übergeordnetes Verzeichnis) \_ nicht NULL. Daher gibt dieser Datensatz ein Nicht-Stammverzeichnis sowohl für die Quelle als auch für das Ziel an. Bei einem Nicht-Stammquellverzeichnis ist das Quellverzeichnis, das durch den im Feld Verzeichnis übergeordnet beschriebenen Datensatz angegeben \_ wird, das übergeordnete Verzeichnis. Für den zweiten Datensatz lautet das \_ Feld Directory Parent (Verzeichnis übergeordnet) TARGETDIR. Wie bereits gezeigt, wurde das quellverzeichnis, das durch den TARGETDIR-Datensatz angegeben wird, in die \\ \\ \\ Anwendungsquelle \\ aufgelöst. Daher ist das quellverzeichnis, das durch den zweiten Datensatz angegeben wird, \\ \\ die \\ Anwendungsquelle \\ App \\ .

Ein ähnlicher Prozess funktioniert für das Zielverzeichnis. Der Wert des übergeordneten Verzeichnisses für das zielverzeichnis, das im zweiten Datensatz beschrieben wird, ist das Zielverzeichnis, das durch das Feld Verzeichnis übergeordnet aufgelöst \_ wird. Auch hier enthält das Feld Verzeichnis \_ parent den Wert TARGETDIR. Dies gibt den ersten Datensatz an, der in ein Zielverzeichnis von C: Program Files Target aufgelöst \\ \\ \\ wird. Das Feld Verzeichnis enthält eine vom Autor definierte Eigenschaft namens EXEDIR. Wenn diese Eigenschaft festgelegt ist, gibt ihr Wert den vollständigen Pfad des Verzeichnisses an. Wenn diese Eigenschaft also auf C: Data Common festgelegt \\ \\ \\ ist, lautet der Wert des Zielverzeichnisses, das durch den zweiten Datensatz angegeben wird, C: \\ Data Common \\ \\ . Wenn es nicht festgelegt ist, nimmt das Zielverzeichnis den Namen an, der im Feld DefaultDir angegeben ist. In diesem Fall ist das Zielverzeichnis C: \\ Programmdateien \\ \\ Ziel-App \\ .

Der gleiche Prozess funktioniert für den dritten Datensatz. Wenn EXEDIR und DLLDIR nicht festgelegt sind, lautet das Zielverzeichnis C: \\ Programmdateien \\ \\ Ziel-App-Bin, \\ und das Quellverzeichnis ist \\ \\ \\ anwendungsquelle \\ \\ App-Bin. \\

Der vierte Datensatz verwendet die [**DesktopFolder-Eigenschaft.**](desktopfolder.md) Wenn der Speicherort des Desktops des Benutzers C: \\ Winnt \\ Profiles \\ User Desktop \\ \\ lautet, wird das Zielverzeichnis in C: \\ Winnt \\ Profiles User Desktop \\ \\ \\ aufgelöst. Das Quellverzeichnis wird in \\ \\ die \\ Anwendungsquelldesktop \\ \\ aufgelöst.

Es gibt zwei zusätzliche Syntaxfeatures, die in der DefaultDir-Spalte der Directory-Tabelle verwendet werden können. Bei einem Nicht-Stammquellverzeichnis gibt ein in der DefaultDir-Spalte eingegebener Punkt (.) an, dass sich das Verzeichnis im übergeordneten Verzeichnis ohne Unterverzeichnis befinden soll. Um verschiedene Quell- und Zielverzeichnispfade anzugeben, trennen Sie die Ziel- und Quellpfade in der DefaultDir-Spalte wie folgt durch einen Doppelpunkt: \[ targetpath \] : \[ sourcepath \] . Diese Features können zusammen verwendet werden, um Ebenen zu den Quell- oder Zielpfaden für ein einzelnes Verzeichnis hinzuzufügen. Sehen Sie sich das folgende Beispiel einer Directory-Tabelle an.



| Verzeichnis   | \_Übergeordnetes Verzeichnis | DefaultDir |
|-------------|-------------------|------------|
| Targetdir   |                   | SourceDir  |
| MyAppDir    | Targetdir         | MyApp      |
| BinDir      | MyAppDir          | Diskretisierung        |
| Binx86Dir   | BinDir            | .:x86      |
| BinAlphaDir | BinDir            | .:Alpha    |



 

Die Quell- und Zielpfade werden für die Zeilen MyAppDir, BinDir, Binx86Dir und BinAlphaDir wie folgt aufgelöst.



| Datensatz       | Zielpfade            | Quellpfade                   |
|--------------|-------------------------|--------------------------------|
| MyAppDir:    | \[TARGETDIR \] MyApp      | \[SourceDir \] MyApp             |
| BinDir:      | \[TARGETDIR \] MyApp \\ Bin | \[SourceDir \] MyApp \\ Bin        |
| Binx86Dir:   | \[TARGETDIR \] MyApp \\ Bin | \[SourceDir \] MyApp \\ Bin \\ x86   |
| BinAlphaDir: | \[TARGETDIR \] MyApp \\ Bin | \[SourceDir \] MyApp \\ Bin \\ Alpha |



 

> [!Note]  
> Die Alphaplattform wird vom Windows Installer nicht unterstützt.

 

 

 



