---
description: Die Master Dateitabelle (MFT) speichert die Informationen, die erforderlich sind, um Dateien aus einer NTFS-Partition abzurufen.
ms.assetid: 673fb4d0-7b6f-44fe-bfd6-1962e14ccdf5
title: Master Dateitabelle (Entwickler Hinweise)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae8656a44b6dadd7d4ff601ddc64623935f5881
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958167"
---
# <a name="master-file-table"></a>Master Dateitabelle

\[Dieses Dokument gilt nur für Version 3 von NTFS-Volumes.\]

Die Master Dateitabelle (MFT) speichert die Informationen, die erforderlich sind, um Dateien aus einer NTFS-Partition abzurufen.

Eine Datei kann über einen oder mehrere MFT-Einträge verfügen und ein oder mehrere Attribute enthalten. In NTFS ist ein Datei Verweis der MFT-Segment Verweis auf den Basisdatei Daten Satz. Weitere Informationen finden Sie unter [**\_ \_ Referenz zu MFT-Segmenten**](mft-segment-reference.md).

Die MFT enthält Datei Daten Satz Segmente. die ersten 16 dieser sind für spezielle Dateien reserviert, z. b. die folgenden:

-   0: MFT ($MFT)
-   5: Stammverzeichnis ( \\ )
-   6: volumecluster-Zuordnungs Datei ($Bitmap)
-   8: fehlerhafte Cluster Datei ($BadClus)

Jedes Datei Daten Satz Segment beginnt mit einem Datei Daten Satz Segment-Header. Weitere Informationen finden Sie unter [**Header des Datei \_ Daten Satz \_ Segments \_**](file-record-segment-header.md). Auf jedes Datei Daten Satz Segment folgt mindestens ein Attribut. Jedes Attribut beginnt mit einem Attributdaten Satz Header. Weitere Informationen finden Sie unter [**Attribut \_ Daten Satz \_ Header**](attribute-record-header.md). Der Attributdaten Satz enthält den Attributtyp (z. b. $Data oder $Bitmap), einen optionalen Namen und den Attribut Wert. Der Benutzerdaten Strom ist ein Attribut, ebenso wie alle Datenströme. Die Attribut Liste wird mit 0xFFFFFFFF ($End) beendet.

Im folgenden finden Sie einige Beispiel Attribute.

-   Die $MFT Datei enthält ein unbenanntes $Data Attribut, bei dem es sich um die Reihenfolge der MFT-Daten Satz Segmente handelt.
-   Die $MFT Datei enthält ein unbenanntes $Bitmap Attribut, das angibt, welche MFT-Datensätze verwendet werden.
-   Die $Bitmap Datei enthält ein unbenanntes $Data Attribut, das angibt, welche Cluster verwendet werden.
-   Die $BadClus Datei enthält ein $Data Attribut mit dem Namen $Bad, das einen Eintrag enthält, der jedem fehlerhaften Cluster entspricht.

Wenn kein Speicherplatz mehr für das Speichern von Attributen im Datei Daten Satz Segment vorhanden ist, werden zusätzliche Datei Daten Satz Segmente zugeordnet und in das erste (oder Basis-) Datei Daten Satz Segment in einem Attribut eingefügt, das als Attribut Liste bezeichnet wird. Die Attribut Liste gibt an, wo sich die einzelnen Attribute befinden, die der Datei zugeordnet sind. Dies schließt alle Attribute im Basisdatei Daten Satz ein, mit Ausnahme der Attribut Liste selbst. Weitere Informationen finden Sie unter [**Attribut \_ Listen \_ Eintrag**](attribute-list-entry.md).

Zu den zu MFT Gehör Ende Strukturen gehören die folgenden:

-   [**Attribut \_ Listen \_ Eintrag**](attribute-list-entry.md)
-   [**Attribut \_ Daten Satz \_ Header**](attribute-record-header.md)
-   [**\_Dateiname**](file-name.md)
-   [**Header des Datei \_ Daten Satz \_ Segments \_**](file-record-segment-header.md)
-   [**MFT- \_ Segment \_ Verweis**](mft-segment-reference.md)
-   [**\_ \_ multisektorheader**](multi-sector-header.md)
-   [**Standard \_ Informationen**](standard-information.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Technische Referenz zu NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))
</dt> </dl>

 

 
