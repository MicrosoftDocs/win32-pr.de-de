---
description: Alle Informationen zu einer Datei, einschließlich Größe, Zeit- und Datumsstempel, Berechtigungen und Dateninhalt, werden entweder in MFT-Einträgen (Master File Table) oder außerhalb des MFT gespeichert, der von MFT-Einträgen beschrieben wird.
ms.assetid: e0933846-278e-4bc8-8982-c5819c252dad
title: Masterdateitabelle (lokale Dateisysteme)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fefec19906e6e2e2c67bbcabf8bd891ccc032b7e8d0882a3622011c324d11c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525640"
---
# <a name="master-file-table-local-file-systems"></a>Masterdateitabelle (lokale Dateisysteme)

Das NTFS-Dateisystem enthält eine Datei namens *Masterdateitabelle* oder MFT. Es gibt mindestens einen Eintrag im MFT für jede Datei auf einem NTFS-Dateisystemvolume, einschließlich des MFT selbst. Alle Informationen zu einer Datei, einschließlich Größe, Zeit- und Datumsstempel, Berechtigungen und Dateninhalt, werden entweder in MFT-Einträgen oder im Speicherplatz außerhalb des MFT gespeichert, der von MFT-Einträgen beschrieben wird.

Wenn Dateien einem NTFS-Dateisystemvolume hinzugefügt werden, werden dem MFT weitere Einträge hinzugefügt, und die Größe des MFT nimmt zu. Wenn Dateien von einem NTFS-Dateisystemvolume gelöscht werden, werden ihre MFT-Einträge als frei markiert und können wiederverwendet werden. Der Speicherplatz, der für diese Einträge zugeordnet wurde, wird jedoch nicht neu zugeordnet, und die Größe des MFT nimmt nicht ab.

Das NTFS-Dateisystem reserviert Speicherplatz für MFT, um den MFT so zusammenhängend wie möglich zu halten, wenn er wächst. Der vom NTFS-Dateisystem für den MFT auf jedem Volume reservierte Speicherplatz wird als MFT-Zone bezeichnet. Speicherplatz für Dateien und Verzeichnisse wird ebenfalls aus diesem Bereich zugewiesen, jedoch erst, nachdem der gesamte Volumespeicherplatz außerhalb der MFT-Zone zugeordnet wurde.

Abhängig von der durchschnittlichen Dateigröße und anderen Variablen kann entweder die reservierte MFT-Zone oder der nicht reservierte Speicherplatz auf dem Datenträger zuerst zugeordnet werden, wenn der Datenträger die Kapazität ausfüllt. Volumes mit einer kleinen Anzahl relativ großer Dateien weisen zuerst den nicht reservierten Speicherplatz zu, während Volumes mit einer großen Anzahl relativ kleiner Dateien zuerst die MFT-Zone zuordnen. In beiden Fällen beginnt die Fragmentierung des MFT, wenn eine Region oder die andere vollständig zugeordnet wird. Wenn der nicht reservierte Speicherplatz vollständig zugeordnet ist, wird der Speicherplatz für Benutzerdateien und -verzeichnisse aus der MFT-Zone zugeordnet. Wenn die MFT-Zone vollständig zugeordnet ist, wird Speicherplatz für neue MFT-Einträge aus dem nicht reservierten Bereich zugeordnet.

Der MFT selbst kann defragmentiert werden. Um die Wahrscheinlichkeit zu verringern, dass die MFT-Zone vollständig zugeordnet wird, bevor der Defragmentierungsprozess abgeschlossen ist, belassen Sie so viel Speicherplatz wie möglich am Anfang der MFT-Zone, bevor Sie das Volume defragmentieren. Wenn die MFT-Zone vollständig zugeordnet wird, bevor die Defragmentierung abgeschlossen ist, muss außerhalb der MFT-Zone nicht zugeordneter Speicherplatz vorhanden sein.

Die MFT-Standardzone wird vom System berechnet und reserviert, wenn das Volume bereitgestellt wird, und basiert auf der Volumegröße. Sie können die MFT-Zone mithilfe des Registrierungseintrags erhöhen, der in [Microsoft Knowledge Base Artikel 174619](https://support.microsoft.com/kb/174619)beschrieben ist. Sie können die MFT-Standardzone jedoch nicht kleiner als die berechnete Zone machen. Durch erhöhen der MFT-Zone wird der Speicherplatz, den Benutzer für Datendateien verwenden können, nicht verringert.

Um die aktuelle Größe des MFT zu bestimmen, analysieren Sie das NTFS-Dateisystemlaufwerk mit Datenträgerdefragmentierung, und klicken Sie dann auf die Schaltfläche **Bericht anzeigen.** Die Laufwerkstatistiken werden angezeigt, einschließlich der aktuellen MFT-Größe und der Anzahl von Fragmenten. Sie können die Größe des MFT auch mithilfe des [**FSCTL \_ GET \_ NTFS \_ VOLUME \_ DATA-Steuercodes**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data) abrufen.

 

 
