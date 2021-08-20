---
description: Mergemodule stellen eine Standardmethode bereit, mit der Sie freigegebene Windows Installer-Komponenten und Setuplogik für Anwendungen bereitstellen können.
ms.assetid: 63ced106-12e3-4483-8bfe-22c54fe7a204
title: Verwenden von Automation zum Zusammenführen eines Mergemoduls in einer Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513a765670df44396c34537721eb6f75ed98796dd31ddefd5d26387e2a6b5d0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141329"
---
# <a name="using-automation-to-merge-a-merge-module-into-a-database"></a>Verwenden von Automation zum Zusammenführen eines Mergemoduls in einer Datenbank

[Mergemodule](merge-modules.md) stellen eine Standardmethode bereit, mit der Sie freigegebene Windows [*Installer-Komponenten*](c-gly.md)und Setuplogik für Anwendungen bereitstellen können.

Mergemodule müssen mithilfe eines Mergetools in ein Installationspaket zusammengeführt werden. Die bewährte Methode besteht darin, ein frei verteiltes Mergetool zu erhalten oder eines der Mergetools zu erwerben, die von unabhängigen Softwareanbietern zur Verfügung stehen, z. B. können Sie [Mergemod.dll](merge-module-automation.md)verwenden.

Das folgende Verfahren zeigt, wie Sie ein Mergemodul mithilfe von [MergeModulautomatisierung](merge-module-automation.md)in einer Windows Installer-Datenbank zusammenführen.

**So führen Sie ein Modul in einer Datenbank zusammen**

1.  Öffnen Sie eine Protokolldatei mithilfe der [**OpenLog-Methode.**](merge-openlog.md)

    Dieser Schritt ist nur erforderlich, wenn Sie eine Protokolldatei erstellen oder eine vorhandene Protokolldatei für den Mergeprozess anfügen müssen.

2.  Öffnen [](windows-installer-file-extensions.md) Sie die.msi-Installationsdatenbank mithilfe der [**OpenDatabase-Methode**](merge-opendatabase.md) des [**Mergeobjekts**](merge-object.md).

    Dieser Schritt ist erforderlich.

    Die Datenbank, die Sie öffnen, ist die Datenbank, die Sie das Mergemodul erhalten möchten.

3.  Öffnen Sie das [MSM-Mergemodul](windows-installer-file-extensions.md) mithilfe der [**OpenModule-Methode.**](merge-openmodule.md)

    Dieser Schritt ist erforderlich.

    Dies ist das Mergemodul, das mit der Datenbank zusammengeführt wird. Ein Modul muss geöffnet werden, bevor es mit einer Installationsdatenbank zusammengeführt werden kann.

4.  Führen Sie das Modul mit der Installationsdatenbank zusammen, indem Sie die [**Merge-Methode**](merge-object.md) oder die [**MergeEx-Methode**](merge-mergeex.md) aufrufen.

    Dieser Schritt ist erforderlich.

    Die [**Merge-Methode**](merge-object.md) oder [**mergeEx-Methode**](merge-mergeex.md) kann nur einmal aufgerufen werden, um eine bestimmte Kombination aus [.msi-](windows-installer-file-extensions.md) und MSM-Dateien zusammenzuführen.

    > [!Note]  
    > Die [**MergeEx-Methode**](merge-mergeex.md) ist nur in [Mergemod.dll Version 2.0](merge-module-automation.md) oder höher und nur bei Verwendung der [**IMsmMerge2-Schnittstelle**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) verfügbar.

     

5.  Rufen Sie die [**Errors-Eigenschaft**](merge-errors.md) ab, und untersuchen Sie die Auflistung von [**Error-Objekten,**](error-object.md) die sie auf Mergekonflikte oder andere Fehler zurückgibt.

    Sie müssen alle Fehler beheben.

    Der Abruf ist nicht destruktiv, und mehrere Instanzen der Fehlerauflistung können durch wiederholtes Lesen der [**Errors-Eigenschaft**](merge-errors.md) abgerufen werden.

6.  Ordnen Sie die Komponenten des Mergemoduls mithilfe der [**Verbinden-Methode**](merge-connect.md) den Features zu.

    Dieser Schritt ist nur erforderlich, wenn Sie über vorhandene Features verfügen und Features hinzufügen möchten, die mit der Installationsdatenbank zusammengeführt werden sollen.

    Ein Feature muss vorhanden sein, bevor Sie diese Methode aufrufen. Weitere Informationen finden Sie unter [Verbinden eines Mergemoduls mit mehreren Features.](connecting-a-merge-module-to-multiple-features.md)

7.  Extrahieren Sie bei Bedarf Quelldateien aus dem Modul, indem Sie eine oder mehrere der folgenden Schritte ausführen:
    -   Verwenden Sie [**ExtractFiles**](merge-extractfiles.md) oder [**ExtractFilesEx,**](merge-extractfilesex.md) um Dateien aus einer eingebetteten .cab Datei zu extrahieren und dann in ein angegebenes Verzeichnis zu kopieren.
        > [!Note]  
        > [**ExtractFilesEx**](merge-extractfilesex.md) erfordert [Mergemod.dll Version 2.0](merge-module-automation.md) oder höher.

         

    -   Verwenden Sie [**ExtractCAB,**](merge-extractcab.md) um Dateien aus einer eingebetteten .cab Datei zu extrahieren und dann in einer angegebenen Datei zu speichern.
    -   Verwenden [**Sie CreateSourceImage,**](merge-createsourceimage.md) um Dateien aus einem Modul zu extrahieren, und kopieren Sie nach der Zusammenführung in ein Quellimage auf dem Datenträger.
        > [!Note]  
        > [**CreateSourceImage**](merge-createsourceimage.md) ist nur in [Mergemod.dll Version 2.0](merge-module-automation.md) oder höher verfügbar.

         
8.  Schließen Sie das aktuelle geöffnete Mergemodul mithilfe der [**CloseModule-Methode.**](merge-closemodule.md)

    Dieser Schritt ist erforderlich.

9.  Schließen Sie die geöffnete Installationsdatenbank mithilfe der [**CloseDatabase-Methode.**](merge-closedatabase.md)

    Dieser Schritt ist erforderlich.

    Das Schließen einer Datenbank löscht alle Abhängigkeitsinformationen, wirkt sich jedoch nicht auf Fehler aus, die nicht abgerufen werden.

10. Schließen Sie die aktuelle Protokolldatei mithilfe der [**CloseLog-Methode.**](merge-closelog.md)

    Dieser Schritt ist erforderlich, wenn Sie über eine geöffnete Protokolldatei verfügen.

Nachdem das Modul mithilfe [Mergemod.dll](merge-module-automation.md)mit der Datenbank zusammengeführt wurde, muss die [Medientabelle](media-table.md) aktualisiert werden, um das gewünschte Quellbildlayout zu beschreiben. Der von Mergemod.dll bereitgestellte Mergeprozess aktualisiert die Medientabelle nicht, da der Consumer des Mergemoduls verschiedene Möglichkeiten zum Layout des Quellbilds auswählen kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Veröffentlichte Versionen, Tools und Redistributables](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



