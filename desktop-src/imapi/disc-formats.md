---
title: Datenträger
description: IMAPI unterstützt die drei Dateisystem Formate ISO 9660, Joliet und UDF.
ms.assetid: 9cd782c0-203b-452c-9d04-3464d39453b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9b4d4c5c5b6aa3e0c4c96598486a531c297b61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310084"
---
# <a name="disc-formats"></a>Datenträger

IMAPI unterstützt drei Dateisystem Formate: [ISO 9660](#iso-9660), [Joliet](#joliet)und [UDF](#universal-disk-format-udf).

## <a name="iso-9660"></a>ISO 9660

Das ISO 9660-Format ist das ursprüngliche Standarddatei System für CD-Datenscheiben. Das Format wird auf verschiedenen Betriebssystemen erkannt, einschließlich MSDOS, der Mac OS, UNIX und des Windows-Betriebssystems. Das ISO 9660-Format wird vom internationale Organisation für Normung (ISO) veröffentlicht.

Das Format beginnt bei Sektor 16 mit dem volumeheader CD0001; der Rest des Headers folgt. Andere abgeleitete Formate beginnen auch bei Sektor 16, aber verwenden eine andere Zeichenfolge für den volumeheader. Beispielsweise verwenden hohe Sierra Disks die Zeichenfolge CD-ROM0001 und das interaktive Format Compact Disc verwendet CD-I0001.

Der-Header verweist auf die Bereiche der Festplatte, die die Dateinamen im ISO 9660-Format speichern. Die Benennungs Konvention für Dateien und Verzeichnisse besteht aus 8 Zeichen, einem Zeitraum und 3 weiteren Zeichen. Dabei handelt es sich um die gleiche Namenskonvention, die vom MSDOS-Betriebssystem verwendet wird.

Weitere Dateisystem Header können für Formate wie Joliet und UDF auf einem Datenträger nebeneinander vorhanden sein, ohne dass sich dies auf die Lesbarkeit des ISO 9660-Formats auswirkt. Nach den Indizes belegt ein Satz von Datendateien die Festplatte. Die Indizes für die einzelnen Dateisysteme verweisen unabhängig auf Datendateien auf der Festplatte.

Die Spezifikation ISO 9660 definiert drei Ebenen des Formats:

-   Ebene 1 definiert Dateinamen, um das 8,3-Zeichenformat zu verwenden.
-   Auf Ebene 2 sind längere Dateinamen zulässig, die auf DOS 6. xx-, Macintosh-und UNIX-Plattformen zu finden sind.
-   Ebene 3 ermöglicht überlappende Daten und Audiodateien, um die Abruf Leistung zu verbessern. Diese Ebene entfernt auch das Limit von 2 GB. Diese Ebene wird von der Image-Mastering-API **nicht** unterstützt.

DVD-CDs können auch ISO 9660 verwenden; das UDF-Dateisystem ist jedoch das gängigste Dateisystem, das mit DVD-Medien verwendet wird.

## <a name="joliet"></a>Joliet

Das Joliet-Format ist eine Ableitung von ISO 9660. Dieses Format schreibt den Joliet-Dateisystem Index zusätzlich zum ISO 9660-Dateisystem Index in das Festplatten Abbild.

Der Joliet-Index bietet die folgenden Verbesserungen am Dateisystem Index:

-   Erkennt lange Dateinamen mit bis zu 32 Zeichen.
-   Unterscheidet zwischen Groß-und Kleinbuchstaben in den Dateinamen.
-   Unterstützt Unicode-Zeichen im Dateinamen.

Der Joliet-Format Header beginnt in Sektor 17 der Festplatte.

Da das Joliet-Format das ISO 9660-Dateisystem auf einem Datenträger beibehält, wird die Kompatibilität mit ISO 9660-kompatiblen Geräten beibehalten.

## <a name="universal-disk-format-udf"></a>Universal Disk Format (UDF)

Das Universal Disk Format (UDF) ist ein neueres Dateisystem, das von der optischen Speichertechnologie Zuordnung (OSTA) für optische Medien entwickelt wurde. UDF ist ein tragbares Format, das von mehreren Betriebssystemen erkannt wird. UDF ersetzt ISO 9660 als neuen Standard, insbesondere bei Lese-/schreibmedien.

UDF bietet folgende Features:

-   Unterstützt Medien mit einer Größe von bis zu 2 TB.
-   Unterstützt Flash Medien, Iomega-und CD-MRW-Scheiben.
-   Speichert Dateien, die kleiner als 2 KB sind, im Datei Eintrags Block.
-   Unterstützt Dateien mit bis zu 2 TB mit Dateinamen, die länger als 255 Zeichen sind.
-   Unterstützt einen umfangreichen Satz von Dateiattributen, die für verschiedene Betriebssysteme geeignet sind.
-   Unterstützt ein Bridge Format, bei dem sich alle Formate von ISO 9660, Joliet und UDF auf derselben Festplatte befinden. Diese wird in Videoanwendungen wie DVD-Video, DVD + VR und DVD-VR verwendet.
-   Unterstützt benannte Streams und "Echt Zeit Dateien".

 

 




