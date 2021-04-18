---
description: Durch die Dateikomprimierung von Dateien, die größtenteils Nullen enthalten, wird Speicherplatz effizient genutzt.
ms.assetid: 7326041d-f11e-4b80-ac4e-07173e418ce7
title: Dateien von geringer Dichte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c282ca89c9dc9e44800a2a7fc969c3f883006b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354522"
---
# <a name="sparse-files"></a>Dateien von geringer Dichte

Eine Datei, in *der ein Großteil* der Daten Nullen ist, enthält ein DataSet mit geringer Dichte. Dateien wie diese sind in der Regel sehr groß, z. b. eine Datei mit Abbild Daten, die verarbeitet werden sollen, oder eine Matrix in einer hoch Geschwindigkeits Datenbank. Das Problem bei Dateien, die sparsesdatasets enthalten, besteht darin, dass der Großteil der Datei keine nützlichen Daten enthält und daher eine ineffiziente Nutzung des Speicherplatzes darstellt.

Die Dateikomprimierung im NTFS-Dateisystem ist eine partielle Lösung für das Problem. Alle Daten in der Datei, die nicht explizit geschrieben werden, werden explizit auf 0 (null) festgelegt. Die Dateikomprimierung komprimiert diese Bereiche von Nullen. Ein Nachteil der Dateikomprimierung ist jedoch, dass die Zugriffszeit aufgrund von Datenkomprimierung und-Dekomprimierung erhöht werden kann.

Die Unterstützung für sparsesdateien wird im NTFS-Dateisystem als eine andere Möglichkeit eingeführt, um die Speicherplatz Nutzung effizienter zu gestalten. Wenn die Funktionalität für die Datei mit geringer Dichte aktiviert ist, weist das System keinen Festplatten Speicherplatz zu einer Datei zu, außer in Regionen, in denen Sie Daten enthalten, die nicht NULL sind. Wenn versucht wird, einen Schreibvorgang auszuführen, bei dem eine große Menge an Daten im Puffer Nullen ist, werden die Nullen nicht in die Datei geschrieben. Stattdessen erstellt das Dateisystem eine interne Liste mit den Speicherorten der Nullen in der Datei, und diese Liste wird bei allen Lesevorgängen abgefragt. Wenn ein Lesevorgang in den Bereichen der Datei ausgeführt wird, in der Nullen gefunden wurden, gibt das Dateisystem die entsprechende Anzahl von Nullen im Puffer zurück, der für den Lesevorgang reserviert ist. Auf diese Weise ist die Wartung der sparsedatei für alle Prozesse transparent, die darauf zugreifen, und ist effizienter als die Komprimierung für dieses spezielle Szenario.

Der Standard Datenwert einer sparsedatei ist 0 (null). Sie kann jedoch auf andere Werte festgelegt werden.

Weitere Informationen zu sparsesdateien finden Sie in den folgenden Themen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                     | BESCHREIBUNG                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Vorgänge mit geringer Dichte](sparse-file-operations.md)<br/>                           | Bestimmen Sie, ob ein Dateisystem sparsesdateien unterstützt, indem Sie die GetVolumeInformation-Funktion aufrufen.<br/>                                                                                |
| [Abrufen der Größe einer sparsedatei](obtaining-the-size-of-a-sparse-file.md)<br/> | Rufen Sie die zugeordnete Größe oder die Gesamtgröße für eine Datei mithilfe der [**getcompressedfilesize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) -Funktion oder der [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) -Funktion ab.<br/> |
| [Sparsesdateien und Datenträger Kontingente](sparse-files-and-disk-quota.md)<br/>                | Eine sparsedatei wirkt sich auf Benutzerkontingente durch die nominale Größe der Datei und nicht die tatsächlich zugeordnete Menge an Speicherplatz aus.<br/>                                                                  |



 

 

 




