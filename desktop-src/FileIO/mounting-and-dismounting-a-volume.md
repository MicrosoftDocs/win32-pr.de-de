---
description: Das Erstellen eines bereitgestellten Ordners ist ein zweistufiger Prozess.
ms.assetid: 02ecdf93-1133-48af-a6c9-52142256673f
title: Erstellen von bereitgestellten Ordnern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d3067af38a893085adcc407263711c80a64c3eea1e535f6814db2cd2742f899
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650230"
---
# <a name="creating-mounted-folders"></a>Erstellen von bereitgestellten Ordnern

Das Erstellen eines bereitgestellten Ordners ist ein zweistufiger Prozess. Rufen Sie zunächst [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) mit dem Bereitstellungspunkt (Laufwerkbuchstaben, Volume-GUID-Pfad oder bereitgestellter Ordner) des Volumes auf, das dem bereitgestellten Ordner zugewiesen werden soll. Verwenden Sie dann die [**SetVolumeMountPoint-Funktion,**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) um den zurückgegebenen Volume-GUID-Pfad dem gewünschten Verzeichnis auf einem anderen Volume zu zuordnen. Beispielcode finden Sie unter [Erstellen eines bereitgestellten Ordners.](mounting-a-volume-at-a-mount-point.md)

Ihre Anwendung kann ein beliebiges leeres Verzeichnis auf einem anderen Volume als das Stammverzeichnis als bereitgestellten Ordner festlegen. Wenn Sie die [**SetVolumeMountPoint-Funktion**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) aufrufen, wird dieses Verzeichnis zum bereitgestellten Ordner. Sie können dasselbe Volume mehreren bereitgestellten Ordnern zuweisen.

Nachdem der bereitgestellte Ordner eingerichtet wurde, wird er automatisch durch Computerneustarts verwaltet.

Wenn ein Volume ausfällt, kann auf volumes, die bereitgestellten Ordnern auf diesem Volume zugewiesen wurden, nicht mehr über diese bereitgestellten Ordner zugegriffen werden. Angenommen, Sie verfügen über zwei Volumes: C: und D:, und D: ist dem bereitgestellten Ordner C: \\ MountD \\ zugeordnet. Wenn Volume C: ausfällt, kann auf Volume D: nicht mehr über den Pfad C: \\ MountD zugegriffen \\ werden.

Nur NTFS-Dateisystemvolumes können über bereitgestellte Ordner verfügen, aber die Zielvolumes für die bereitgestellten Ordner können Nicht-NTFS-Volumes sein.

Bereitgestellte Ordner werden mithilfe von Aufbereitungspunkten implementiert und unterliegen deren Einschränkungen. Weitere Informationen finden Sie unter [Reparse Points](reparse-points.md). Für die Verwendung von bereitgestellten Ordnern ist es nicht erforderlich, Aufbereitungspunkte zu bearbeiten. Funktionen wie [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) verarbeiten alle Details des Prüfpunkts für Sie.

Da es sich bei bereitgestellten Ordnern um Verzeichnisse handelt, können Sie sie wie andere Verzeichnisse umbenennen, entfernen, verschieben und anderweitig bearbeiten.

(Hinweis: In der TechNet-Dokumentation wird der Begriff *bereitgestellte Laufwerke* verwendet, um auf *bereitgestellte Ordner zu verweisen.)*

 

 



