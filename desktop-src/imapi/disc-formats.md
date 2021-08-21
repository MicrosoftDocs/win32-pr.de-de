---
title: Datenträgerformate
description: IMAPI unterstützt die drei Dateisystemformate ISO 9660, Joliet und UDF.
ms.assetid: 9cd782c0-203b-452c-9d04-3464d39453b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af71733ec2747ae227ac412a7b49f0faa73639cf1000f1332db5ec1d1d55db9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758602"
---
# <a name="disc-formats"></a>Datenträgerformate

IMAPI unterstützt drei Dateisystemformate: [ISO 9660](#iso-9660), [Joliet](#joliet)und [UDF](#universal-disk-format-udf).

## <a name="iso-9660"></a>ISO 9660

Das ISO 9660-Format ist das ursprüngliche Standarddateisystem für CD-Datenträger. Das Format wird auf mehreren Betriebssystemen erkannt, einschließlich MSDOS, Mac OS, UNIX und Windows Betriebssystem. Das ISO 9660-Format wird vom Internationale Organisation für Normung (ISO) veröffentlicht.

Das Format beginnt bei Sektor 16 mit dem Volumeheader CD0001; Der Rest des Headers folgt. Andere abgeleitete Formate beginnen ebenfalls bei Sektor 16, verwenden jedoch eine andere Zeichenfolge für den Volumeheader. High Sierra-Datenträger verwenden beispielsweise die Zeichenfolge CD-ROM0001 und das Compact Disc Interactive-Format CD-I0001.

Der Header zeigt auf Bereiche des Datenträgers, in denen die Dateinamen im ISO 9660-Format gespeichert werden. Die Datei- und Verzeichnisbenennungskonvention besteht aus 8 Zeichen, einem Zeitraum und drei mehr Zeichen. Dies ist die gleiche Namenskonvention, die vom MSDOS-Betriebssystem verwendet wird.

Zusätzliche Dateisystemheader für Formate wie Joliet und UDF können auf einem Datenträger vorhanden sein, ohne die Lesbarkeit des ISO 9660-Formats zu beeinträchtigen. Nach den Indizes wird der Datenträger von einer Reihe von Datendateien belegt. Die Indizes für jedes Dateisystem verweisen unabhängig voneinander auf Datendateien auf dem Datenträger.

Die ISO 9660-Spezifikation definiert drei Ebenen des Formats:

-   Ebene 1 definiert Dateinamen für die Verwendung des 8.3-Zeichenformats.
-   Ebene 2 lässt längere Dateinamen zu, wie sie auf DEN Plattformen DOS 6.xx, MacIntosh und UNIX sind.
-   Ebene 3 ermöglicht verleerte Daten und Audiodateien, um die Abrufleistung (Wiedergabe) zu verbessern. Durch diese Ebene wird auch das Dateilimit von 2 GB entfernt. Diese Ebene wird **von der** Imagemastering-API nicht unterstützt.

DVD-Datenträger können auch ISO 9660 verwenden. Das UDF-Dateisystem ist jedoch das häufigste Dateisystem, das mit DVD-Medien verwendet wird.

## <a name="joliet"></a>Joliet

Das Joliet-Format ist eine Ableitung von ISO 9660. Dieses Format schreibt den Joliet-Dateisystemindex zusätzlich zum ISO 9660-Dateisystemindex in das Datenträgerbild.

Der Joliet-Index bietet die folgenden Verbesserungen am Dateisystemindex:

-   Erkennt lange Dateinamen bis zu 32 Zeichen.
-   Unterscheidet zwischen Groß- und Kleinbuchstaben in den Dateinamen.
-   Unterstützt Unicode-Zeichen im Dateinamen.

Der Joliet-Formatheader beginnt bei Sektor 17 des Datenträgers.

Da das Joliet-Format das ISO 9660-Dateisystem auf einem Datenträger beibehalten, wird die Kompatibilität mit ISO 9660-kompatiblen Geräten beibehalten.

## <a name="universal-disk-format-udf"></a>Universal Disk Format (UDF)

Das Universal Disk Format (UDF) ist ein neueres Dateisystem, das von der Optical Storage Technology Association ( UNIVERSE) für optische Medien entwickelt wurde. UdF ist ein portables Format, das von mehreren Betriebssystemen erkannt wird. UdF ersetzt ISO 9660 als neuen Standard, insbesondere durch Lese-/Schreibmedien.

Zu den Features von UDF gehören die folgenden:

-   Unterstützt Medien mit einer Größe von bis zu 2 TB.
-   Unterstützt Flashmedien, Iomega REV-Datenträger und CD-MRW-Datenträger.
-   Speichert Dateien mit einer Länge von weniger als 2 KB im Dateieintragsblock.
-   Unterstützt Dateien bis zu 2 TB mit Dateinamen bis zu 255 Zeichen.
-   Unterstützt einen großen Satz von Dateiattributen, die für verschiedene Betriebssysteme geeignet sind.
-   Unterstützt ein Bridgeformat, bei dem sich die FORMATE ISO 9660, Joliet und UDF alle auf demselben Datenträger befinden. Dies wird in Videoanwendungen wie DVD-Video, DVD+VR und DVD-VR verwendet.
-   Unterstützt benannte Streams und Echtzeitdateien.

 

 




