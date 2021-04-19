---
description: Mergemodule stellen eine Standardmethode für Entwickler bereit, um freigegebene Windows Installer Komponenten und Setup Logik für Ihre Anwendungen bereitzustellen.
ms.assetid: 3eb087b1-0f44-40d8-a950-67d489f09408
title: Verwenden der API zum Zusammenführen eines Mergemoduls zu einer Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e68298671045825dda41ad120896fa22c89f068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358594"
---
# <a name="using-the-api-to-merge-a-merge-module-into-a-database"></a>Verwenden der API zum Zusammenführen eines Mergemoduls zu einer Datenbank

[Mergemodule](merge-modules.md) stellen eine Standardmethode für Entwickler bereit, um freigegebene Windows Installer [*Komponenten*](c-gly.md) und Setup Logik für Ihre Anwendungen bereitzustellen. Mergemodule müssen mithilfe eines mergetools in ein Installationspaket zusammengeführt werden. Die beste Alternative besteht darin, ein frei verteiltes Zusammenführungs Tool zu erwerben oder eines der Zusammenführungs Tools zu erwerben, die von unabhängigen Softwareanbietern zur Verfügung stehen. Beispielsweise können Sie die von [Mergemod.dll](merge-module-automation.md)bereitgestellte Funktionalität nutzen.

Führen Sie die folgenden Schritte nacheinander aus, um ein Mergemodul mithilfe der-API von [Mergemod.dll](merge-module-automation.md)in einer Windows Installer-Installations Datenbank zusammenzuführen.

**So führen Sie ein Mergemodul in einer Windows Installer-Installations Datenbank zusammen**

1.  Öffnen Sie mithilfe von [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog)eine Protokolldatei. Dieser Schritt ist nur erforderlich, wenn Sie eine Protokolldatei erstellen oder eine vorhandene Protokolldatei für den Mergeprozess Anfügen müssen.
2.  Öffnen Sie die Installations Datenbank, eine [MSI-Datei](windows-installer-file-extensions.md), die das Mergemodul mithilfe von [**OpenDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-opendatabase)empfängt. Dieser Schritt ist erforderlich.
3.  Öffnen Sie das Mergemodul, eine [MSM-Datei](windows-installer-file-extensions.md), die mit [**OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule)in der Datenbank zusammengeführt wird. Ein Modul muss geöffnet werden, bevor es mit einer Installations Datenbank zusammengeführt werden kann. Dieser Schritt ist erforderlich.
4.  Führen Sie das Modul mithilfe von [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) oder [**mergeex**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex)in der Installations Datenbank zusammen. Beachten Sie, dass **Merge** oder **mergeex** nur einmal aufgerufen werden kann, um eine bestimmte Kombination aus MSI-und MSM-Dateien zusammenzuführen. **Mergeex** ist nur verfügbar, wenn [Mergemod.dll-Version 2,0](merge-module-automation.md) oder höher und nur bei Verwendung der [IMsmMerge2](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) -Schnittstelle verwendet wird. Dieser Schritt ist erforderlich.
5.  Ruft [**get \_ Errors**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) auf und untersucht die abgerufene Auflistung von Fehlern bei Mergekonflikten oder anderen Fehlern. Der Abruf ist nicht destruktiv. Mehrere Instanzen der Fehlersammlung können durch wiederholtes Lesen von get- **\_ Fehlern** abgerufen werden. Sie müssen alle Fehler beheben, die für Ihren Fall geeignet sind.
6.  Ordnen Sie die Komponenten des Mergemoduls allen zusätzlichen Features zu, die mithilfe von [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect)in der Installations Datenbank zusammengeführt wurden oder werden. Die Funktion muss bereits vorhanden sein, bevor diese Methode aufgerufen wird. Dieser Schritt ist nur erforderlich, wenn Sie über zusätzliche Funktionen verfügen. Weitere Informationen finden Sie [unter Verbinden eines Mergemoduls mit mehreren Features](connecting-a-merge-module-to-multiple-features.md) .
7.  Extrahieren Sie ggf. Quelldateien aus dem Modul, indem Sie eine oder mehrere der folgenden Schritte durchgeführt haben.

    Um Dateien aus einer eingebetteten CAB-Datei zu extrahieren und dann in ein bestimmtes Verzeichnis zu kopieren, verwenden Sie [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) oder [**extractfilesex**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex). Beachten Sie, dass **extractfilesex** [Mergemod.dll Version 2,0](merge-module-automation.md) oder höher erfordert.

    Verwenden Sie [**ExtractCab**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab), um Dateien aus einer eingebetteten CAB-Datei zu extrahieren und Sie dann in einer angegebenen Datei zu speichern.

    Verwenden Sie zum Extrahieren von Dateien aus einem Modul und anschließendes Kopieren in ein Quell Abbild auf dem Datenträger nach der Zusammenführung den Befehl " [**kreatesourceimage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage). Beachten Sie, dass " **kreatesourceimage** " nur mit [Mergemod.dll Version 2,0](merge-module-automation.md) oder höher verfügbar ist.

8.  Schließen Sie das aktuelle geöffnete Mergemodul mithilfe von [**closemodule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule). Dieser Schritt ist erforderlich.
9.  Schließen Sie die aktuelle geöffnete Installations Datenbank mithilfe von [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase). Dieser Schritt ist erforderlich. Durch das Schließen einer Datenbank werden alle Abhängigkeitsinformationen gelöscht, aber keine Fehler, die noch nicht abgerufen wurden.
10. Schließen Sie die aktuelle Protokolldatei mit [**closelog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closelog). Dieser Schritt ist erforderlich, wenn Sie eine Protokolldatei geöffnet haben.

Nachdem das Modul mithilfe von [Mergemod.dll](merge-module-automation.md)in der Datenbank zusammengeführt wurde, muss die [Medien Tabelle](media-table.md) aktualisiert werden, damit das gewünschte Layout des Quell Bilds beschrieben wird. Der von Mergemod.dll bereitgestellte Mergeprozess aktualisiert die Medien Tabelle nicht, da der Consumer des Mergemoduls verschiedene Möglichkeiten zum Layout des Quell Bilds auswählen kann.

 

 
