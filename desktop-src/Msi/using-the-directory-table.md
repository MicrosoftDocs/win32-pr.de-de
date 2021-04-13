---
description: Die Verzeichnis Tabelle gibt das Layout einer-Installation an.
ms.assetid: 3f2e1cc2-6b36-4615-86e6-e78485edd2f7
title: Verwenden der Verzeichnis Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7218fe6f6e2ca36bc0c52e74b564ad07d87053a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216348"
---
# <a name="using-the-directory-table"></a>Verwenden der Verzeichnis Tabelle

Die [Verzeichnis Tabelle](directory-table.md) gibt das Layout einer-Installation an. Wenn die Verzeichnisse während der [costfinalize-Aktion](costfinalize-action.md)aufgelöst werden, werden die Schlüssel in der Verzeichnis Tabelle zu [Eigenschaften](properties.md) , die auf Verzeichnispfade festgelegt sind. Beachten Sie, dass das Installationsprogramm eine Reihe von Standard [Eigenschaften](properties.md) für Systemordner Pfade festlegt. Eine Liste der Eigenschaften, die auf Systemordner festgelegt sind, finden Sie in der [Eigenschafts Referenz](property-reference.md) .

Die beste Möglichkeit, den Zielort für ein Verzeichnis anzugeben, besteht darin, die [Verzeichnis Tabelle](directory-table.md) in Ihrem Installationspaket zu erstellen, um den richtigen Speicherort bereitzustellen, wie in diesem Abschnitt erläutert. Wenn es erforderlich ist, den Verzeichnis Speicherort zum Zeitpunkt der Installation zu ändern, lesen Sie auch den Abschnitt: [Ändern des Zielspeicher Orts für ein Verzeichnis](changing-the-target-location-for-a-directory.md) .

Im folgenden finden Sie ein Beispiel für eine Verzeichnis Tabelle.



| Verzeichnis     | Über \_ geordnetes Verzeichnis | DefaultDir |
|---------------|-------------------|------------|
| TARGETDIR     |                   | SourceDir  |
| Exedir        | TARGETDIR         | App        |
| Dlldir        | Exedir            | Diskretisierung        |
| DesktopFolder | TARGETDIR         | Desktop    |



 

Jede Zeile der Verzeichnis Tabelle gibt ein Verzeichnis an, das sowohl an der Quelle als auch am Ziel liegt. Nehmen wir beispielsweise an, dass sich das Installationspaket in der \\ \\ Anwendungs \\ Quelle befindet \\ . Da das \_ übergeordnete Verzeichnis des Verzeichnisses der ersten Zeile NULL ist, gibt dieser Datensatz die Stamm Verzeichnisse für die Quelle und das Ziel an. Für die Quelle wird der Wert dieses Verzeichnisses durch das Feld DefaultDir angegeben. Die [**SourceDir**](sourcedir.md) -Eigenschaft ist standardmäßig auf den Speicherort des Installationspakets eingestellt. Wenn die **SourceDir** -Eigenschaft daher nicht überschrieben wird, ist das Stamm Quellverzeichnis die \\ \\ Anwendungs \\ Quelle \\ .

Das Verzeichnis Feld des ersten Datensatzes gibt den Speicherort des Stammverzeichnis Verzeichnisses an. In diesem Fall gibt der Wert der Eigenschaft [**TARGETDIR**](targetdir.md) dieses Verzeichnis an. In der Regel wird der Wert der Eigenschaft **TARGETDIR** in der Befehlszeile oder über eine Benutzeroberfläche festgelegt. Nehmen Sie in diesem Fall an, dass die Eigenschaft **TARGETDIR** auf C: \\ Program Files Target festgelegt ist \\ \\ .

Für den zweiten Datensatz ist das übergeordnete Verzeichnis des Verzeichnisses \_ nicht NULL. Daher gibt dieser Datensatz ein nicht-Stammverzeichnis für die Quelle und das Ziel an. Bei einem nicht Stamm Quellverzeichnis ist das Quellverzeichnis, das durch den Datensatz angegeben wird, der im übergeordneten Verzeichnis des Verzeichnisses beschrieben \_ wird, das übergeordnete Verzeichnis. Für den zweiten Datensatz lautet das über \_ geordnete Verzeichnis "TARGETDIR". Wie bereits erwähnt, wurde das vom TARGETDIR-Datensatz angezeigte Quellverzeichnis in die \\ \\ Anwendungs \\ Quelle aufgelöst \\ . Folglich ist das Quellverzeichnis, das durch den zweiten Datensatz angegeben wird, " \\ \\ Applications \\ Source \\ app" \\ .

Ein ähnlicher Prozess funktioniert für das Zielverzeichnis. Der Wert des übergeordneten Verzeichnisses für das Zielverzeichnis, das im zweiten Datensatz beschrieben wird, ist das Zielverzeichnis, das durch das übergeordnete Verzeichnis des Verzeichnisses aufgelöst wird \_ . Das übergeordnete Verzeichnis des Verzeichnisses \_ enthält wiederum den Wert TARGETDIR. Dies gibt den ersten Datensatz an, der zu einem Zielverzeichnis des C: \\ Program Files-Ziels aufgelöst wird \\ \\ . Das Verzeichnis Feld enthält eine vom Autor definierte Eigenschaft mit dem Namen "exedir". Wenn diese Eigenschaft festgelegt ist, gibt ihr Wert den vollständigen Pfad des Verzeichnisses an. Wenn diese Eigenschaft auf C: data common festgelegt \\ ist \\ \\ , ist der Wert des Zielverzeichnisses, der durch den zweiten Datensatz angegeben wird, "c: \\ Data Common" \\ \\ . Wenn Sie nicht festgelegt ist, nimmt das Zielverzeichnis den im Feld DefaultDir angegebenen Namen. In diesem Fall ist das Zielverzeichnis C: \\ Programmdateien \\ Ziel- \\ App \\ .

Der gleiche Vorgang funktioniert für den dritten Datensatz. Wenn exedir und dlldir nicht festgelegt sind, ist das Zielverzeichnis C: \\ Program Files \\ Target \\ App \\ bin, und das Quellverzeichnis ist \\ \\ Applications \\ Source \\ App \\ bin \\ .

Der vierte Datensatz verwendet die [**DesktopFolder**](desktopfolder.md) -Eigenschaft. Wenn der Speicherort des Benutzer Desktops C: \\ Winnt \\ Profiles \\ User Desktop ist \\ \\ , wird das Zielverzeichnis in c: \\ Winnt \\ Profiles \\ User Desktop aufgelöst \\ \\ . Das Quellverzeichnis wird in \\ \\ Anwendungs \\ Quell \\ Desktop aufgelöst \\ .

In der DefaultDir-Spalte der Verzeichnis Tabelle können zwei zusätzliche Syntax Funktionen verwendet werden. Bei einem nicht stammenden Quellverzeichnis gibt ein in der Spalte DefaultDir eingegebener Zeitraum (.) an, dass sich das Verzeichnis in seinem übergeordneten Verzeichnis ohne Unterverzeichnis befinden soll. Um verschiedene Quell-und Zielverzeichnis Pfade anzugeben, trennen Sie die Ziel-und Quell Pfade in der DefaultDir-Spalte wie folgt mit einem Doppelpunkt: \[ TargetPath \] : \[ SourcePath \] . Diese Funktionen können verwendet werden, um dem Quell-oder Zielpfad für ein einzelnes Verzeichnis Ebenen hinzuzufügen. Sehen Sie sich das folgende Beispiel einer Verzeichnis Tabelle an.



| Verzeichnis   | Über \_ geordnetes Verzeichnis | DefaultDir |
|-------------|-------------------|------------|
| TARGETDIR   |                   | SourceDir  |
| Myappdir    | TARGETDIR         | MyApp      |
| BINDIR      | Myappdir          | Diskretisierung        |
| Binx86Dir   | BINDIR            | .: x86      |
| Binalphadir | BINDIR            | .: Alpha    |



 

Der Quell-und Zielpfad wird wie folgt für die Zeilen myappdir, BINDIR, Binx86Dir und binalphadir aufgelöst.



| Datensatz       | Zielpfade            | Quellpfade                   |
|--------------|-------------------------|--------------------------------|
| Myappdir:    | \[TARGETDIR \] myapp      | \[SourceDir \] myapp             |
| BINDIR:      | \[TARGETDIR \] myapp- \\ bin | \[SourceDir \] myapp- \\ bin        |
| Binx86Dir:   | \[TARGETDIR \] myapp- \\ bin | \[SourceDir \] myapp \\ bin \\ x86   |
| Binalphadir: | \[TARGETDIR \] myapp- \\ bin | \[SourceDir \] myapp \\ bin \\ Alpha |



 

> [!Note]  
> Die Alpha Plattform wird vom Windows Installer nicht unterstützt.

 

 

 



