---
description: Das Erstellen eines bereitgestellten Ordners ist ein zweistufiger Prozess.
ms.assetid: 02ecdf93-1133-48af-a6c9-52142256673f
title: Erstellen von bereitgestellten Ordnern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d64630716be6e85ac323c80e89dda0500ba6c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366223"
---
# <a name="creating-mounted-folders"></a>Erstellen von bereitgestellten Ordnern

Das Erstellen eines bereitgestellten Ordners ist ein zweistufiger Prozess. Nennen Sie zuerst [**getvolumenameforvolumemountpoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) mit dem Bereitstellungspunkt (Laufwerksbuchstaben, VolumeGuid-Pfad oder eingebundenes Ordner) des Volumes, das dem bereitgestellten Ordner zugewiesen werden soll. Verwenden Sie dann die [**setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) -Funktion, um den zurückgegebenen Volume-GUID-Pfad dem gewünschten Verzeichnis auf einem anderen Volume zuzuordnen. Beispielcode finden Sie unter [Erstellen eines eingebundenen Ordners](mounting-a-volume-at-a-mount-point.md).

Die Anwendung kann ein beliebiges leeres Verzeichnis auf einem anderen Volume als dem Stammverzeichnis als bereitgestellter Ordner festlegen. Wenn Sie die [**setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) -Funktion aufrufen, wird dieses Verzeichnis zum bereitgestellten Ordner. Sie können das gleiche Volume mehreren bereitgestellten Ordnern zuweisen.

Nachdem der bereitgestellte Ordner eingerichtet wurde, wird er über Computer Neustarts automatisch verwaltet.

Wenn ein Volume ausfällt, kann auf alle Volumes, die den bereitgestellten Ordnern auf diesem Volume zugewiesen wurden, nicht mehr über diese eingebundenen Ordner zugegriffen werden. Angenommen, Sie verfügen über zwei Volumes: c: und d:, und das Laufwerk d: ist dem bereitgestellten Ordner c: \\ mountd zugeordnet \\ . Wenn das Volume "c:" ausfällt, kann auf Volume "D:" nicht mehr über den Pfad "c: mountd" zugegriffen werden \\ \\ .

Nur NTFS-Dateisystemvolumes können eingebundene Ordner enthalten, aber die Zielvolumes für die bereitgestellten Ordner können nicht-NTFS-Volumes sein.

Eingebundene Ordner werden mithilfe von Analyse Punkten implementiert und unterliegen ihren Einschränkungen. Weitere Informationen finden Sie unter Analyse [Punkte](reparse-points.md). Es ist nicht erforderlich, Analyse Punkte für die Verwendung bereitgestellter Ordner zu manipulieren. Funktionen, wie z. b. [**setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , behandeln alle Analyse Punkt Details für Sie.

Da eingebundene Ordner Verzeichnisse sind, können Sie Sie wie andere Verzeichnisse umbenennen, entfernen, verschieben und anderweitig bearbeiten.

(Hinweis: in der TechNet-Dokumentation wird der Begriff bereitgestellte *Laufwerke* verwendet, um auf bereitgestellte *Ordner* zu verweisen.)

 

 



