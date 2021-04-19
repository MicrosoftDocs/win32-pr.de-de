---
description: Alle Informationen zu einer Datei, einschließlich Größe, Zeit-und Datumsstempel, Berechtigungen und Dateninhalt, werden entweder in MFT-Einträgen (Master File Table) oder außerhalb des in der MFT-Einträge beschriebenen Speicherplatzes gespeichert.
ms.assetid: e0933846-278e-4bc8-8982-c5819c252dad
title: Master Dateitabelle (lokale Dateisysteme)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260740c03e7b7e4ebe9c7e8ec90035431f6be649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359511"
---
# <a name="master-file-table-local-file-systems"></a>Master Dateitabelle (lokale Dateisysteme)

Das NTFS-Dateisystem enthält eine Datei mit dem Namen *Master File Table* oder MFT. Es gibt mindestens einen Eintrag in der MFT für jede Datei auf einem NTFS-Dateisystem Volume, einschließlich der MFT selbst. Alle Informationen zu einer Datei, einschließlich Größe, Zeit-und Datumsstempel, Berechtigungen und Dateninhalt, werden entweder in MFT-Einträgen oder außerhalb des durch MFT-Einträge beschriebenen MFT gespeichert.

Wenn Dateien einem NTFS-Dateisystem Volume hinzugefügt werden, werden der MFT weitere Einträge hinzugefügt, und die Größe des MFT vergrößert sich. Wenn Dateien aus einem NTFS-Dateisystem Volume gelöscht werden, werden die MFT-Einträge als frei markiert und können wieder verwendet werden. Der Speicherplatz, der für diese Einträge zugewiesen wurde, wird jedoch nicht neu zugeordnet, und die Größe des MFT wird nicht verringert.

Das NTFS-Dateisystem reserviert Speicherplatz für die MFT, um die MFT so zusammenhängend wie möglich zu halten, wenn Sie wächst. Der vom NTFS-Dateisystem für die MFT in jedem Volume reservierte Speicherplatz wird als MFT-Zone bezeichnet. Der Speicherplatz für Dateien und Verzeichnisse wird ebenfalls von diesem Bereich aus zugewiesen, jedoch erst, nachdem der gesamte volumespeicherplatz außerhalb der MFT-Zone zugeordnet wurde.

Abhängig von der durchschnittlichen Dateigröße und anderen Variablen kann die reservierte MFT-Zone oder der nicht reservierte Speicherplatz auf dem Datenträger zuerst zugewiesen werden, wenn der Datenträger in die Kapazität gefüllt wird. Volumes mit einer kleinen Anzahl von relativ großen Dateien weisen zuerst den nicht reservierten Speicherplatz zu, während Volumes mit einer großen Anzahl von relativ kleinen Dateien zuerst die MFT-Zone zuordnen. In beiden Fällen wird die Fragmentierung der MFT gestartet, wenn eine Region oder die andere vollständig zugeordnet wird. Wenn der nicht reservierte Speicherplatz vollständig zugeordnet ist, wird der Speicherplatz für Benutzer Dateien und Verzeichnisse von der MFT-Zone zugeordnet. Wenn die MFT-Zone vollständig zugeordnet ist, wird Speicherplatz für neue MFT-Einträge aus dem nicht reservierten Speicherplatz zugeordnet.

Die MFT selbst kann zerlegt werden. Um die Wahrscheinlichkeit zu verringern, dass die MFT-Zone vollständig zugewiesen wird, bevor der Defragmentierungs Prozess vollständig ist, sollten Sie so viel Speicherplatz wie möglich am Anfang der MFT-Zone belassen, bevor Sie das Volume defragmentieren. Wenn die MFT-Zone vor dem Abschluss der Defragmentierung vollständig zugewiesen wird, muss außerhalb der MFT-Zone nicht zugewiesener Speicherplatz vorhanden sein.

Die MFT-Standard Zone wird beim Bereitstellen des Volumes berechnet und vom System reserviert. Sie basiert auf der Volumegröße. Sie können die MFT-Zone mithilfe des im [Microsoft Knowledge Base-Artikel 174619](https://support.microsoft.com/kb/174619)beschriebenen Registrierungs Eintrags erhöhen, aber Sie können die MFT-Standard Zone nicht kleiner als die berechnete Spalte machen. Wenn Sie die MFT-Zone vergrößern, verringert sich der Speicherplatz nicht, den Benutzer für Datendateien verwenden können.

Um die aktuelle Größe des MFT zu ermitteln, analysieren Sie das NTFS-Dateisystem Laufwerk mit der Datenträger Defragmentierung, und klicken Sie dann auf die Schaltfläche **Bericht anzeigen** . Die Laufwerks Statistiken werden angezeigt, einschließlich der aktuellen MFT-Größe und der Anzahl der Fragmente. Sie können auch die Größe des MFT abrufen, indem Sie den [**Daten Steuerungs Code FSCTL \_ get \_ NTFS \_ Volume \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data) verwenden.

 

 
