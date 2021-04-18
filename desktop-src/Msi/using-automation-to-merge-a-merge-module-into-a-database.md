---
description: Mergemodule stellen eine Standardmethode für die Bereitstellung von freigegebenen Windows Installer Komponenten und die Einrichtung von Logik für Anwendungen bereit.
ms.assetid: 63ced106-12e3-4483-8bfe-22c54fe7a204
title: Verwenden von Automation zum Zusammenführen eines Mergemoduls zu einer Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e28b8cfc1716cdbb296fd0a1410787ae55bb62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347252"
---
# <a name="using-automation-to-merge-a-merge-module-into-a-database"></a>Verwenden von Automation zum Zusammenführen eines Mergemoduls zu einer Datenbank

[Mergemodule](merge-modules.md) stellen eine Standardmethode für die Bereitstellung von freigegebenen Windows Installer [*Komponenten*](c-gly.md)und die Einrichtung von Logik für Anwendungen bereit.

Mergemodule müssen mithilfe eines Merge-Tools in ein Installationspaket zusammengeführt werden. Die bewährte Vorgehensweise besteht darin, ein frei verteiltes Mergetool zu erwerben oder eines der mergetools zu erwerben, die von unabhängigen Softwareanbietern verfügbar sind. Sie können z. b. [Mergemod.dll](merge-module-automation.md)verwenden.

Im folgenden Verfahren wird gezeigt, wie Sie ein Mergemodul in einer Windows Installer-Datenbank zusammenführen, indem Sie die [mergemodulautomatisierung](merge-module-automation.md)verwenden.

**So führen Sie ein Modul in einer Datenbank zusammen**

1.  Öffnen Sie eine Protokolldatei, indem Sie die [**OpenLog**](merge-openlog.md) -Methode verwenden.

    Dieser Schritt ist nur erforderlich, wenn Sie eine Protokolldatei erstellen oder eine vorhandene Protokolldatei für den Mergeprozess Anfügen müssen.

2.  Öffnen Sie die [MSI](windows-installer-file-extensions.md) -Installations Datenbank, indem Sie die [**OpenDatabase**](merge-opendatabase.md) -Methode des [**Merge-Objekts**](merge-object.md)verwenden.

    Dieser Schritt ist erforderlich.

    Die Datenbank, die Sie öffnen, ist die Datenbank, die Sie für das Mergemodul erhalten möchten.

3.  Öffnen Sie das [MSM](windows-installer-file-extensions.md) -Mergemodul mithilfe der [**OpenModule**](merge-openmodule.md) -Methode.

    Dieser Schritt ist erforderlich.

    Dies ist das Mergemodul, das in der Datenbank zusammengeführt wird. Ein Modul muss geöffnet werden, bevor es mit einer Installations Datenbank zusammengeführt werden kann.

4.  Führen Sie das Modul mit der [**Merge**](merge-object.md) -Methode oder der [**mergeex**](merge-mergeex.md) -Methode in der Installations Datenbank zusammen.

    Dieser Schritt ist erforderlich.

    Die [**Merge**](merge-object.md) -Methode oder die [**mergeex**](merge-mergeex.md) -Methode kann nur einmal aufgerufen werden, um eine bestimmte Kombination aus [MSI](windows-installer-file-extensions.md) -und MSM-Dateien zusammenzuführen.

    > [!Note]  
    > Die [**mergeex**](merge-mergeex.md) -Methode ist nur in [Mergemod.dll Version 2,0](merge-module-automation.md) oder höher und nur bei Verwendung der [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) -Schnittstelle verfügbar.

     

5.  Rufen Sie die [**Errors**](merge-errors.md) -Eigenschaft ab, und untersuchen Sie die Auflistung von [**Fehler**](error-object.md) Objekten, die für Mergekonflikte oder andere Fehler zurückgegeben

    Sie müssen alle Fehler beheben.

    Der Abruf ist nicht destruktiv, und mehrere Instanzen der Fehlersammlung können durch wiederholtes Lesen der [**Errors**](merge-errors.md) -Eigenschaft abgerufen werden.

6.  Ordnen Sie die Komponenten des Mergemoduls den Funktionen mithilfe der [**Connect**](merge-connect.md) -Methode zu.

    Dieser Schritt ist nur erforderlich, wenn Sie über vorhandene Features verfügen und Features zum Zusammenführen mit der Installations Datenbank hinzufügen möchten.

    Eine Funktion muss vorhanden sein, bevor Sie diese Methode aufzurufen. Weitere Informationen finden Sie unter [Verbinden eines Mergemoduls mit mehreren Features](connecting-a-merge-module-to-multiple-features.md).

7.  Extrahieren Sie ggf. Quelldateien aus dem Modul, indem Sie eine oder mehrere der folgenden Aktionen ausführen:
    -   Extrahieren Sie mithilfe von [**ExtractFiles**](merge-extractfiles.md) oder [**extractfilesex**](merge-extractfilesex.md) Dateien aus einer eingebetteten CAB-Datei, und kopieren Sie Sie in ein bestimmtes Verzeichnis.
        > [!Note]  
        > [**Extractfilesex**](merge-extractfilesex.md) erfordert [Mergemod.dll-Version 2,0](merge-module-automation.md) oder höher.

         

    -   Extrahieren Sie mithilfe von [**ExtractCab**](merge-extractcab.md) Dateien aus einer eingebetteten CAB-Datei, und speichern Sie Sie dann in einer angegebenen Datei.
    -   Verwenden Sie " [**kreatesourceimage**](merge-createsourceimage.md) ", um Dateien aus einem Modul zu extrahieren, und kopieren Sie dann nach dem Merge in ein Quell Abbild auf dem Datenträger.
        > [!Note]  
        > " [**Kreatesourceimage**](merge-createsourceimage.md) " ist nur in [Mergemod.dll Version 2,0](merge-module-automation.md) oder höher verfügbar.

         
8.  Schließen Sie das aktuelle geöffnete Mergemodul mit der [**closemodule**](merge-closemodule.md) -Methode.

    Dieser Schritt ist erforderlich.

9.  Schließen Sie die Open-Installations Datenbank mithilfe der [**CloseDatabase**](merge-closedatabase.md) -Methode.

    Dieser Schritt ist erforderlich.

    Durch das Schließen einer Datenbank werden alle Abhängigkeitsinformationen gelöscht, aber keine Fehler, die nicht abgerufen werden.

10. Schließen Sie die aktuelle Protokolldatei mit der [**closelog**](merge-closelog.md) -Methode.

    Dieser Schritt ist erforderlich, wenn Sie über eine geöffnete Protokolldatei verfügen.

Nachdem das Modul mithilfe von [Mergemod.dll](merge-module-automation.md)in der Datenbank zusammengeführt wurde, muss die [Medien Tabelle](media-table.md) aktualisiert werden, damit das gewünschte Layout des Quell Bilds beschrieben wird. Der von Mergemod.dll bereitgestellte Mergeprozess aktualisiert die Medien Tabelle nicht, da der Consumer des Mergemoduls verschiedene Möglichkeiten zum Layout des Quell Bilds auswählen kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Veröffentlichte Versionen, Tools und verteilbare Dateien](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



