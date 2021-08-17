---
description: In der Masterdateitabelle (Master File Table, MFT) werden die Informationen gespeichert, die zum Abrufen von Dateien aus einer NTFS-Partition erforderlich sind.
ms.assetid: 673fb4d0-7b6f-44fe-bfd6-1962e14ccdf5
title: Masterdateitabelle (Entwicklerhinweise)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded28a9655c6d3cbba21449b15bd70cf5a24b17e3864dc1b525cb5f6e4e32fca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955749"
---
# <a name="master-file-table"></a>Masterdateitabelle

\[Dieses Dokument gilt nur für Version 3 von NTFS-Volumes.\]

In der Masterdateitabelle (Master File Table, MFT) werden die Informationen gespeichert, die zum Abrufen von Dateien aus einer NTFS-Partition erforderlich sind.

Eine Datei kann mindestens einen MFT-Datensatz enthalten und ein oder mehrere Attribute enthalten. In NTFS ist ein Dateiverweis der MFT-Segmentverweis des Basisdateidatensatzes. Weitere Informationen finden Sie unter [**MFT \_ SEGMENT \_ REFERENCE**](mft-segment-reference.md).

Der MFT enthält Dateidatensatzsegmente. die ersten 16 davon sind für spezielle Dateien reserviert, z. B.:

-   0: MFT ($Mft)
-   5: Stammverzeichnis ( \\ )
-   6: Volumeclusterzuordnungsdatei ($Bitmap)
-   8: Ungültige Clusterdatei ($BadClus)

Jedes Dateidatensatzsegment beginnt mit einem Dateidatensatzsegmentheader. Weitere Informationen finden Sie unter [**FILE \_ RECORD SEGMENT \_ \_ HEADER**](file-record-segment-header.md). Auf jedes Dateidatensatzsegment folgt mindestens ein Attribut. Jedes Attribut beginnt mit einem Attributdatensatzheader. Weitere Informationen finden Sie unter [**ATTRIBUTE \_ RECORD \_ HEADER**](attribute-record-header.md). Der Attributdatensatz enthält den Attributtyp (z. B. $DATA oder $BITMAP), einen optionalen Namen und den Attributwert. Der Benutzerdatenstrom ist ein Attribut, ebenso wie alle Streams. Die Attributliste wird mit 0xFFFFFFFF ($END) beendet.

Im Folgenden werden einige Beispielattribute beschrieben.

-   Die $Mft-Datei enthält ein unbenanntes $DATA Attribut, das die Sequenz von MFT-Datensatzsegmenten in der angegebenen Reihenfolge ist.
-   Die $Mft-Datei enthält ein unbenanntes $BITMAP Attribut, das angibt, welche MFT-Datensätze verwendet werden.
-   Die $Bitmap-Datei enthält ein unbenanntes $DATA Attribut, das angibt, welche Cluster verwendet werden.
-   Die $BadClus-Datei enthält ein $DATA Attribut namens $BAD, das einen Eintrag enthält, der jedem fehlerhaften Cluster entspricht.

Wenn kein Speicherplatz mehr zum Speichern von Attributen im Dateidatensatzsegment vorhanden ist, werden zusätzliche Dateidatensatzsegmente zugeordnet und im ersten (oder Basis-)Dateidatensatzsegment in einem Attribut namens Attributliste eingefügt. Die Attributliste gibt an, wo jedes der Datei zugeordnete Attribut gefunden werden kann. Dies schließt alle Attribute im Basisdateidatensatz ein, mit Ausnahme der Attributliste selbst. Weitere Informationen finden Sie unter [**ATTRIBUTE \_ LIST \_ ENTRY**](attribute-list-entry.md).

Zu den Strukturen im Zusammenhang mit MFT gehören folgende:

-   [**\_ \_ ATTRIBUTLISTENEINTRAG**](attribute-list-entry.md)
-   [**\_ \_ ATTRIBUTEINTRAGSHEADER**](attribute-record-header.md)
-   [**\_DATEINAME**](file-name.md)
-   [**SEGMENTHEADER FÜR \_ DATEIDATENSATZ \_ \_**](file-record-segment-header.md)
-   [**\_MFT-SEGMENTREFERENZ \_**](mft-segment-reference.md)
-   [**MULTI \_ SECTOR \_ HEADER**](multi-sector-header.md)
-   [**\_STANDARDINFORMATIONEN**](standard-information.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Technische Referenz zu NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))
</dt> </dl>

 

 
