---
title: Informationen zur Ordner Überwachung
description: Informationen zur Ordner Überwachung
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Windows Media Player, Ordner Überwachung
- Windows Media Player-Objektmodell, Ordner Überwachung
- Objektmodell, Ordner Überwachung
- Windows Media Player ActiveX-Steuerelement, Ordner Überwachung
- ActiveX-Steuerelement, Ordner Überwachung
- Windows Media Player Mobile ActiveX-Steuerelement, Ordner Überwachung
- Windows Media Player Mobile, Ordner Überwachung
- Ordner Überwachung
- Überwachen von Ordnern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3d6af341df706cd85c4158197b27babad09c86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389833"
---
# <a name="about-folder-monitoring"></a>Informationen zur Ordner Überwachung

Windows-Media Player können Ordner überwachen, die digitale Mediendateien enthalten, und die Bibliothek aktualisieren, wenn Dateien hinzugefügt oder entfernt werden. Diese Ordner Überwachungsfunktion wird von der [iwmpfoldermonitorservices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) -Schnittstelle bereitgestellt.

Um die Ordner Überwachungsdienste verwenden zu können, müssen Sie das Player-Objekt in einem Remote Zustand erstellen. Weitere Informationen zum Remoting finden Sie unter [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md). Nachdem Sie eine Remote Instanz des Players erstellt haben, können Sie einen Zeiger auf die **iwmpfoldermonitorservices** -Schnittstelle abrufen, indem Sie **QueryInterface** auf der [iwmpplayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) -Schnittstelle aufrufen.

Windows Media Player eine Liste der überwachten Ordner beibehält. Um eine Liste der überwachten Ordner zu erhalten, verwenden Sie die [iwmpfoldermonitorservices:: get \_ count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) -Methode und die [iwmpfoldermonitorservices:: Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) -Methode. Um der Liste Ordner hinzuzufügen oder Sie aus der Liste zu entfernen, verwenden Sie die [iwmpfoldermonitorservices:: Add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) -Methode bzw. die [Remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) -Methode.

**Starten eines Scans**

Die Überwachung von Ordnern ist normalerweise ein Hintergrundprozess, der nicht explizit aufgerufen werden muss. Wenn Sie einen Ordner aktiv scannen möchten, nennen Sie [iwmpfoldermonitorservices:: StartScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan). Sie können eine laufende Überprüfung mit der [iwmpfoldermonitorservices:: StopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) -Methode beenden.

**Der Ordner Überwachungs Status wird abgerufen.**

**Iwmpfoldermonitorservices** stellt Funktionen zum Abrufen des Status des Ordner Überwachungsprozesses bereit.

Die Ordner Überprüfung erfolgt in zwei Durchläufen. Im ersten Durchlauf scannt der Spieler die Ordner in der Liste der überwachten Ordner nacheinander und erstellt eine Liste der Dateien, die der Bibliothek hinzugefügt werden sollen. Im zweiten Durchlauf durchläuft er die Liste der Dateien und fügt die Dateien der Bibliothek hinzu. Außerdem werden alle Medienelemente aus der Bibliothek entfernt, deren zugehörige physische Dateien aus dem Dateisystem gelöscht wurden.

Das [folderscanstatechange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) -Ereignis wird verwendet, um das Programm zu benachrichtigen, wenn der Player in einen neuen Zustand wechselt. Sie können den aktuellen Status auch abrufen, indem Sie [get \_ ScanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate)aufrufen. Wenn der erste Durchlauf gestartet wird, lautet der aktuelle Zustandswert "wmpfssscan". Während des zweiten Durchlauf wechselt der Status zu "wmpfssupdating". Nachdem der Vorgang abgeschlossen ist, ändert sich der Status in wmpfssbeendet.

Während der Player die überwachten Ordner beim ersten Durchlauf scannt, muss [get \_ scannedfilescount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) aufgerufen werden, um zu überprüfen, wie viele Dateien gescannt wurden. Mit der [get \_ CurrentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) -Methode wird angezeigt, welcher Ordner gerade gescannt wird.

Nachdem der zweite Durchlauf gestartet wurde, können Sie [get \_ addedfilescount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) abrufen, um zu überprüfen, wie viele Dateien der Bibliothek hinzugefügt wurden. Die [get \_ UpdateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) -Methode informiert Sie über den Status des zweiten Durchlauf, als Prozentwert zwischen 0 und 100.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Player-Objektmodell**](about-the-player-object-model.md)
</dt> <dt>

[**Iwmpfoldermonitorservices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 




