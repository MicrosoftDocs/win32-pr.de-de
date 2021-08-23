---
description: Die Dateikomprimierung von Dateien, die größtenteils Nullen enthalten, nutzt den Speicherplatz effizient.
ms.assetid: 7326041d-f11e-4b80-ac4e-07173e418ce7
title: Dateien von geringer Dichte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb89a8fd3e8c067d5328756e57d511d4c38d615f2bb19c579208462c3f5bdbf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951049"
---
# <a name="sparse-files"></a>Dateien von geringer Dichte

Eine Datei, in der ein Großteil der Daten Nullen ist, enthält ein *Sparse-Dataset.* Dateien wie diese sind in der Regel sehr groß, z. B. eine Datei, die zu verarbeitende Bilddaten enthält, oder eine Matrix innerhalb einer Hochgeschwindigkeitsdatenbank. Das Problem bei Dateien, die Sparse-DataSets enthalten, besteht darin, dass der Großteil der Datei keine nützlichen Daten enthält, und aus diesem Grund eine ineffiziente Nutzung des Speicherplatzes darstellt.

Die Dateikomprimierung im NTFS-Dateisystem ist eine Teillösung des Problems. Alle Daten in der Datei, die nicht explizit geschrieben werden, werden explizit auf 0 (null) festgelegt. Die Dateikomprimierung komprimiert diese Bereiche von Nullen. Ein Nachteil der Dateikomprimierung ist jedoch, dass die Zugriffszeit aufgrund der Datenkomprimierung und -dekomprimierung erhöht werden kann.

Die Unterstützung für Sparsedateien wird im NTFS-Dateisystem eingeführt, um die Speicherplatznutzung effizienter zu gestalten. Wenn die Funktionalität für Sparsedateien aktiviert ist, ordnet das System einer Datei keinen Festplattenspeicherplatz zu, außer in Regionen, in denen sie Daten ungleich 0 (null) enthält. Wenn ein Schreibvorgang versucht wird, bei dem eine große Menge der Daten im Puffer null ist, werden die Nullen nicht in die Datei geschrieben. Stattdessen erstellt das Dateisystem eine interne Liste mit den Speicherorten der Nullen in der Datei, und diese Liste wird während aller Lesevorgänge abgerufen. Wenn ein Lesevorgang in Bereichen der Datei ausgeführt wird, in denen sich Nullen befanden, gibt das Dateisystem die entsprechende Anzahl von Nullen im Puffer zurück, der für den Lesevorgang zugeordnet ist. Auf diese Weise ist die Wartung der Sparsedatei für alle Prozesse transparent, die darauf zugreifen, und ist effizienter als die Komprimierung für dieses spezielle Szenario.

Der Standarddatenwert einer Sparsedatei ist 0 (null). sie kann jedoch auf andere Werte festgelegt werden.

Weitere Informationen zu Sparsedateien finden Sie in den folgenden Themen.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                     | BESCHREIBUNG                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Dateivorgänge mit geringer Dichte](sparse-file-operations.md)<br/>                           | Bestimmen Sie, ob ein Dateisystem Sparsedateien unterstützt, indem Sie die GetVolumeInformation-Funktion aufrufen.<br/>                                                                                |
| [Abrufen der Größe einer Datei mit geringer Dichte](obtaining-the-size-of-a-sparse-file.md)<br/> | Abrufen der zugeordneten Größe oder der Gesamtgröße für eine Datei mithilfe der [**GetCompressedFileSize-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) oder der [**GetFileSize-Funktion.**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize)<br/> |
| [Dateien mit geringer Dichte und Datenträgerkontingente](sparse-files-and-disk-quota.md)<br/>                | Eine Sparsedatei wirkt sich auf Benutzerkontingente durch die nominale Größe der Datei aus, nicht durch die tatsächlich zugewiesene Menge an Speicherplatz.<br/>                                                                  |



 

 

 




