---
description: Mithilfe bereitgestellter Ordner können Sie unterschiedliche Dateisysteme wie das NTFS-Dateisystem, ein 16-Bit-FAT-Dateisystem und ein ISO-9660-Dateisystem auf einem CD-ROM-Laufwerk in einem logischen Dateisystem auf einem einzelnen NTFS-Volume vereinheitlichen.
ms.assetid: 6de526cd-5537-4411-b43f-3c0bdac70d64
title: Eingebundene Ordner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0f0c937ded5f7a6b78f19b17b4c098178f254f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360630"
---
# <a name="mounted-folders"></a>Eingebundene Ordner

Das NTFS-Dateisystem unterstützt eingebundene Ordner. Ein bereitgestellter *Ordner* ist eine Zuordnung zwischen einem Volume und einem Verzeichnis auf einem anderen Volume. Wenn ein bereitgestellter Ordner erstellt wird, können Benutzer und Anwendungen auf das Ziel Volume zugreifen, indem Sie entweder den Pfad zum eingebundenen Ordner oder den Laufwerk Buchstaben des Volumes verwenden. Beispielsweise kann ein Benutzer einen bereitgestellten Ordner erstellen, um Laufwerk D: dem Ordner c: \\ mnt \\ dDrive auf Laufwerk C zuzuordnen. Nachdem der bereitgestellte Ordner erstellt wurde, kann der Benutzer den Pfad "C: \\ mnt \\ dDrive" verwenden, um auf Laufwerk D: zuzugreifen, als ob es sich um einen Ordner auf Laufwerk "c:" handelt.

Mithilfe bereitgestellter Ordner können Sie unterschiedliche Dateisysteme wie das NTFS-Dateisystem, ein 16-Bit-FAT-Dateisystem und ein ISO-9660-Dateisystem auf einem CD-ROM-Laufwerk in einem logischen Dateisystem auf einem einzelnen NTFS-Volume vereinheitlichen. Weder Benutzer noch Anwendungen benötigen Informationen über das Ziel Volume, auf dem sich eine bestimmte Datei befindet. Alle Informationen, die Sie benötigen, um eine bestimmte Datei zu suchen, sind ein vollständiger Pfad, der einen bereitgestellten Ordner auf dem NTFS-Volume verwendet. Volumes können neu angeordnet, ersetzt oder in viele Volumes unterteilt werden, ohne dass Benutzer oder Anwendungen Einstellungen ändern müssen.

Informationen zu bereitgestellten Ordnern finden Sie in den folgenden Themen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erstellen von bereitgestellten Ordnern](mounting-and-dismounting-a-volume.md)<br/>                                                  | Das Erstellen eines bereitgestellten Ordners ist ein zweistufiger Prozess.<br/>                                                                                                                                                                 |
| [Auflisten eingebundenes Ordner](enumerating-volume-mount-points.md)<br/>                                                 | Funktionen, die zum Auflisten bereitgestellter Ordner auf einem Volume verwendet werden.<br/>                                                                                                                                                       |
| [Bestimmen, ob ein Verzeichnis ein bereitgestellter Ordner ist](determining-whether-a-directory-is-a-volume-mount-point.md)<br/> | Bestimmen, ob ein angegebenes Verzeichnis ein bereitgestellter Ordner ist.<br/>                                                                                                                                              |
| [Zuweisen eines Laufwerk Buchstabens zu einem Volume](assigning-a-drive-letter-to-a-volume.md)<br/>                                   | Sie können einem lokalen Volume einen Laufwerk Buchstaben (z. b. X:) zuweisen \) , indem Sie die [**setvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) -Funktion verwenden, vorausgesetzt, dass diesem Laufwerk Buchstaben nicht bereits ein Volume zugeordnet ist.<br/> |
| [Funktionen für bereitgestellte Ordner](volume-mount-point-functions.md)<br/>                                                       | Funktionen, die zum Verwalten bereitgestellter Ordner verwendet werden.<br/>                                                                                                                                                                        |



 

Beispiele finden Sie unter [Beispiele für eingebundene Ordner](volume-mount-point-examples.md).

 

 




