---
description: Mergemodule bieten Entwicklern eine Standardmethode zum Bereitstellen freigegebener Windows Installer-Komponenten und der Setuplogik für ihre Anwendungen.
ms.assetid: 3eb087b1-0f44-40d8-a950-67d489f09408
title: Verwenden der API zum Zusammenführen eines Mergemoduls in einer Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdbeb68b193cceff10fbd1cd3f56f4c8804a4e1fb4f7c169fd2d893dc0b4bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039030"
---
# <a name="using-the-api-to-merge-a-merge-module-into-a-database"></a>Verwenden der API zum Zusammenführen eines Mergemoduls in einer Datenbank

[Mergemodule](merge-modules.md) bieten Entwicklern eine Standardmethode, um freigegebene Windows [*Installer-Komponenten*](c-gly.md) und Setuplogik an ihre Anwendungen zu liefern. Mergemodule müssen mithilfe eines Mergetools in einem Installationspaket zusammengeführt werden. Die beste Alternative besteht in der Beschaffung eines frei verteilten Mergetools oder dem Erwerb eines der Zusammenführungstools, die von unabhängigen Softwareherstellern zur Verfügung stehen. Sie können z. B. die funktionalität verwenden, die von [Mergemod.dll. ](merge-module-automation.md)

Führen Sie die folgenden Schritte nacheinander aus, um ein Mergemodul mithilfe der API von Windows Installer-Installationsdatenbank mit [Mergemod.dll. ](merge-module-automation.md)

**So führen Sie ein Mergemodul in einer Windows Installer-Installationsdatenbank zusammen**

1.  Öffnen Sie mit OpenLog eine [**Protokolldatei.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) Dieser Schritt ist nur erforderlich, wenn Sie eine Protokolldatei für den Mergeprozess erstellen oder eine vorhandene Protokolldatei anfügen müssen.
2.  Öffnen Sie die Installationsdatenbank , eine [.msi datei,](windows-installer-file-extensions.md)die das Mergemodul [**mithilfe von OpenDatabase erhält.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-opendatabase) Dieser Schritt ist erforderlich.
3.  Öffnen Sie das Mergemodul , eine [MSM-Datei,](windows-installer-file-extensions.md)die mithilfe von OpenModule in die Datenbank [**zusammengeführt wird.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) Ein Modul muss geöffnet werden, bevor es mit einer Installationsdatenbank zusammengeführt werden kann. Dieser Schritt ist erforderlich.
4.  Führen Sie das Modul mit Merge oder MergeEx in [**der**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) [**Installationsdatenbank zusammen.**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) Beachten Sie, **dass Merge** oder **MergeEx** nur einmal aufgerufen werden können, um eine bestimmte Kombination aus .msi msm-Dateien zusammenführungen. **MergeEx** ist nur verfügbar, wennMergemod.dll [Version 2.0](merge-module-automation.md) oder höher verwendet wird, und nur bei Verwendung der [IMsmMerge2-Schnittstelle.](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) Dieser Schritt ist erforderlich.
5.  Rufen [**Sie get Errors \_ auf,**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) und untersuchen Sie die abgerufene Auflistung von Fehlern auf Mergekonflikte oder andere Fehler. Der Abruf ist nicht destruktiv. Mehrere Instanzen der Fehlersammlung können durch wiederholtes Lesen des Aufrufs get **\_ Errors abgerufen werden.** Sie müssen alle Fehler entsprechend Ihrem Fall beheben.
6.  Ordnen Sie die Komponenten des Mergemoduls allen zusätzlichen Features zu, die mithilfe von mit der Installationsdatenbank zusammengeführt [**wurden Verbinden.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) Das Feature muss bereits vorhanden sein, bevor diese Methode aufruft. Dieser Schritt ist nur erforderlich, wenn Sie über zusätzliche Funktionen verfügen. Weitere Informationen finden Sie unter Verbinden eines [Mergemoduls mit mehreren Funktionen.](connecting-a-merge-module-to-multiple-features.md)
7.  Extrahieren Sie bei Bedarf Quelldateien aus dem Modul, indem Sie eine oder mehrere der folgenden Schritte verwenden.

    Um Dateien aus einer eingebetteten .cab zu extrahieren und dann in ein angegebenes Verzeichnis zu kopieren, verwenden Sie [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) oder [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex). Beachten **Sie, dass ExtractFilesEx** Mergemod.dll [ Version 2.0 oder](merge-module-automation.md) höher erfordert.

    Um Dateien aus einer eingebetteten .cab zu extrahieren und dann in einer angegebenen Datei zu speichern, verwenden Sie [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab).

    Verwenden Sie [**CreateSourceImage,**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage)um Dateien aus einem Modul zu extrahieren und dann nach dem Zusammenführen in ein Quellimage auf dem Datenträger zu kopieren. Beachten **Sie, dass CreateSourceImage** nur mitMergemod.dll [ 2.0 oder höher](merge-module-automation.md) verfügbar ist.

8.  Schließen Sie das aktuelle offene Mergemodul mit [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule). Dieser Schritt ist erforderlich.
9.  Schließen Sie die aktuelle geöffnete Installationsdatenbank [**mit CloseDatabase.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) Dieser Schritt ist erforderlich. Beim Schließen einer Datenbank werden alle Abhängigkeitsinformationen gelöscht, aber es sind keine Fehler betroffen, die nicht abgerufen wurden.
10. Schließen Sie die aktuelle Protokolldatei mit [**CloseLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closelog). Dieser Schritt ist erforderlich, wenn Sie eine Protokolldatei geöffnet haben.

Nachdem das Modul mithilfe vonMergemod.dllmit [](media-table.md) der Datenbank zusammengeführt [wurde, ](merge-module-automation.md)muss die Medientabelle aktualisiert werden, um das gewünschte Quellbildlayout zu beschreiben. Der merge-Prozess von Mergemod.dll aktualisiert die Medientabelle nicht, da der Consumer des Mergemoduls verschiedene Möglichkeiten zum Layout des Quellbilds auswählen kann.

 

 
