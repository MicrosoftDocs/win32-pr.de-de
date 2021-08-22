---
title: Informationen zur Ordnerüberwachung
description: Informationen zur Ordnerüberwachung
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Windows Media Player,Ordnerüberwachung
- Windows Media Player Objektmodell, Ordnerüberwachung
- Objektmodell,Ordnerüberwachung
- Windows Media Player ActiveX-Steuerelement, Ordnerüberwachung
- ActiveX-Steuerelement, Ordnerüberwachung
- Windows Media Player Mobile ActiveX-Steuerelement, Ordnerüberwachung
- Windows Media Player Mobile, Ordnerüberwachung
- Ordnerüberwachung
- Überwachungsordner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1206defcdc387659567ceedcf7347a3ab99ca45d9926a9bd32c4f75280a8a46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055508"
---
# <a name="about-folder-monitoring"></a>Informationen zur Ordnerüberwachung

Windows Media Player können Ordner überwachen, die digitale Mediendateien enthalten, und die Bibliothek aktualisieren, wenn Dateien hinzugefügt oder entfernt werden. Diese Ordnerüberwachungsfunktion wird von der [IWMPFolderMonitorServices-Schnittstelle](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) bereitgestellt.

Um die Ordnerüberwachungsdienste zu verwenden, müssen Sie das Player-Objekt in einem Remotezustand erstellen. Weitere Informationen zum Remoting finden Sie unter [Remoting des Windows Media Player-Steuerelements.](remoting-the-windows-media-player-control.md) Nachdem Sie eine Remoteinstanz des Players erstellt haben, rufen Sie einen Zeiger auf die **IWMPFolderMonitorServices-Schnittstelle** ab, indem Sie **QueryInterface** für die [IWMPPlayer-Schnittstelle](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) aufrufen.

Windows Media Player führt eine Liste der ordner, die überwacht werden. Um eine Liste der überwachten Ordner abzurufen, verwenden Sie die Methoden [IWMPFolderMonitorServices::get \_ count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) und [IWMPFolderMonitorServices::item.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) Um der Liste Ordner hinzuzufügen oder aus der Liste zu entfernen, verwenden Sie die [Methoden IWMPFolderMonitorServices::add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) bzw. [remove.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove)

**Starten einer Überprüfung**

Die Überwachung von Ordnern ist normalerweise ein Hintergrundprozess, der nicht explizit aufgerufen werden muss. Wenn Sie einen Ordner aktiv überprüfen möchten, rufen [Sie IWMPFolderMonitorServices::startScan auf.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan) Sie können eine laufende Überprüfung mit der [IWMPFolderMonitorServices::stopScan-Methode](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) beenden.

**Abrufen des Ordnerüberwachungsstatus**

**IWMPFolderMonitorServices** bietet Funktionen zum Abrufen des Status des Ordnerüberwachungsprozesses.

Die Ordnerüberprüfung erfolgt in zwei Durchläufen. Im ersten Durchlauf scannt der Player die Ordner, die in der Liste der überwachten Ordner nacheinander benannt sind, und erstellt eine Liste der Dateien, die der Bibliothek hinzugefügt werden sollen. Im zweiten Durchlauf durchläuft er die Liste der Dateien und fügt die Dateien der Bibliothek hinzu und entfernt auch alle Medienelemente aus der Bibliothek, deren entsprechende physische Dateien aus dem Dateisystem gelöscht wurden.

Das [FolderScanStateChange-Ereignis](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) wird verwendet, um Ihr Programm zu benachrichtigen, wenn der Player in einen neuen Zustand wechselt. Sie können den aktuellen Zustand auch abrufen, indem [Sie get \_ scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate)aufrufen. Wenn der erste Durchlauf beginnt, lautet der aktuelle Statuswert wmpfssScanning. Während des zweiten Durchlaufs wechselt der Zustand zu wmpfssUpdating. Nach Abschluss des Prozesses ändert sich der Zustand in wmpfssStopped.

Während der Player die überwachten Ordner im ersten Durchlauf scannt, rufen [Sie get \_ scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) auf, um zu überprüfen, wie viele Dateien gescannt wurden. Die [get \_ currentFolder-Methode](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) teilt Ihnen mit, welcher Ordner gerade überprüft wird.

Nachdem der zweite Durchlauf gestartet wurde, rufen [Sie \_ get addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) auf, um zu überprüfen, wie viele Dateien der Bibliothek hinzugefügt wurden. Die [get \_ updateProgress-Methode](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) teilt Ihnen den Fortschritt des zweiten Durchlaufs als Prozentsatz von 0 bis 100 mit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Playerobjektmodell**](about-the-player-object-model.md)
</dt> <dt>

[**IWMPFolderMonitorServices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 




