---
title: Mit der neuen API können Apps TRIM- und Unmap-Hinweise an Speichermedien senden.
description: Mit der neuen API können Apps \0034 senden. TRIM und Unmap \ 0034; Hinweise zu Speichermedien
ms.assetid: DDBC3592-BD4D-4826-83FE-387564DA07E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d79d47dceb5c8bf2e7575836c9a40ddf0347b7e5c616ab4b7196b547742c97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028828"
---
# <a name="new-api-allows-apps-to-send-trim-and-unmap-hints-to-storage-media"></a>Mit der neuen API können Apps TRIM- und Unmap-Hinweise an Speichermedien senden.

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>Beschreibung

TRIM-Hinweise benachrichtigen das Laufwerk, dass bestimmte Zuvor zugeordnete Sektoren von der App nicht mehr benötigt werden und gelöscht werden können. Dies wird in der Regel verwendet, wenn eine App große Speicherplatzzuweisungen über eine Datei vorzieht und dann die Zuordnungen zur Datei selbst verwaltet (z. B. Virtuelle Festplattendateien).

**Was ist TRIM?**

Solid State Drives (SSDs) sind in der Regel Flashspeicher-basierte Blocklöschgeräte. Dies bedeutet, dass daten, wenn sie auf die SSD geschrieben werden, nicht übergeschrieben werden können und an einen anderen Ort geschrieben werden müssen, bis die Garbage Collection des Blocks möglich ist. Da die SSD über keinen internen Mechanismus verfügt, um zu bestimmen, ob bestimmte Blöcke entfernt werden und andere benötigt werden. Die SSD kann einen Sektor nur dann als "dirty" markieren, wenn er übergeschrieben ist. In anderen Fällen, z. B. beim Löschen einer Datei, behält die SSD diese Sektoren bei, da der Löschvorgang nur als Änderung der Masterdateitabelle (Master File Table, MFT) und nicht als Vorgang für alle Bereiche der Datei erfolgt. In Windows 7 haben wir eine Standard-Methode für die Kommunikation mit SSDs über Sektoren eingeführt, die nicht mehr benötigt werden. Dieser Befehl wird in der [T13-Spezifikation als](https://www.t13.org/Standards/Default.aspx?DocumentType=3) TRIM-Befehl definiert. NTFS sendet den TRIM-Befehl für einige normale Inlinevorgänge wie "deletefile".

**Andere Verwendungsmöglichkeiten von TRIM in der Speicherwelt**

Wie SSDs nutzen Auch Storage Area Networks (SANs) und das neue Windows 8-Feature Software Spaces-Implementierungen TRIM-Befehlshinweise, um ihre Speicherplätze in umgebungen mit schlanker Bereitstellung zu verwalten. SANs und Software Spaces ordnen Speicherbereiche in Größen zu, die größer sind als Sektoren oder Cluster (von 1 MB bis 1 GB). Wenn sie TRIM-Hinweise für die Zuordnungsgröße (oder größer als die Zuordnungsgröße) erhalten, kann das SAN/SSD die Zuordnung einer Region entfernen, um speicherplatz für andere Dateien frei zu machen. Sie übergeben in der Regel alle TRIM-Hinweise an die zugrunde liegenden Medien (SSD oder HDD), damit sie den frei werdenden Speicherplatz nach Belang nutzen können. Sie verschieben Daten in der Regel nicht in Regionen, in denen die Zuordnung wieder aufbewegt wird, und sie verfolgen auch keine TRIM-Bereiche in regionen, deren Zuordnung wieder frei ist (wenn die Region leer ist).

SaNs mit schlanker Speicherbewahrung verwenden die trim-Hinweise, die an sie übergeben werden, um den gesamten physischen Speicherbedarf zu reduzieren und somit die Kosten zu senken. Die [T10-SCSI-Spezifikation](https://www.t10.org) definiert den Befehl "Unmap" (ähnlich wie beim TRIM-Befehl). Hier gilt der Befehl für alle Arten von Speicher, einschließlich HDDs, SSDs und anderen. Der Befehl UnMap hilft, physische Blöcke aus der San-Zuordnung zu entfernen.

## <a name="how-to-use-the-new-api"></a>Verwenden der neuen API


```
#define FSCTL_FILE_LEVEL_TRIM CTL_CODE(FILE_DEVICE_FILE_SYSTEM, 130, METHOD_BUFFERED, FILE_WRITE_DATA)

Where 
typedef struct _EXTENT_PAIR {
    ULONGLONG Offset;
    ULONGLONG Length;
} EXTENT_PAIR, *PEXTENT_PAIR;

typedef struct _FILE_LEVEL_TRIM {
    //
    // A count of how many Offset:Length pairs are given
    //
    DWORD PairCount;
    //
    // All the pairs.
    //
    EXTENT_PAIR Pairs[1];
} FILE_LEVEL_TRIM, *PFILE_LEVEL_TRIM;
```



Datei-TRIM wird nach Möglichkeit über den Puffer oder asynchron (nicht gepuffert) an den Device IOCTL DSM-Befehl TRIM übergeben. Dies wird dem TRIM-Befehl für ATA-Geräte und dem UnMap-Befehl für SCSI-Geräte zugeordnet. Der TRIM-Code der Datei sendet die Regionen 1:1, wie in den obigen Extents angegeben.

Datei-TRIM wartet nicht auf Rückgaben vom Gerät, da die Befehle TRIM und Unmap als Hinweise zu den zugrunde liegenden Speichermedien definiert sind und Rückgabecodes nicht erwartet werden.

**End-to-End-Workflow:**

1.  Datei kürzen aufrufen
    1.  Datei-TRIM überprüft Eingaben auf Fehler
    2.  Datei-TRIM unterbricht die Extent in LCN-Regionen
    3.  Datei-TRIM rundet für falsch ausgerichtete Regionen, die an TRIM übergeben werden, auf und ab.
    4.  Datei-TRIM reiht Einträge im Cache, die sich auf die TRIM-Bereiche beziehen.
    5.  Datei-TRIM übergibt \_ IOCTL-DSM (Trim) pro Region
2.  Trim-Rückgaben oder -Fehler der Datei
    1.  Die Fehlerüberprüfung wird bei der Gültigkeit der Eingabe durchgeführt.
    2.  Wenn nur einige der Extents gültig sind, wird ein Fehler für den vollständigen API-Aufruf zurückgegeben.

**Anwendungsfälle**

**Virtuelle Consumerfestplatte (VHD), die auf einer SSD bereitgestellt ist:**

Die VHD wird zunächst auf "sauberen" nicht verwendeten Medien bereitgestellt. Während die VHD verwendet wird, nutzt die VHD Teile des Speichermediums für Dateien usw. Wenn Dateien auf dem Speichermedium gelöscht werden, werden diese Dateien nicht aus der SSD entfernt, da die vollständige VHD als eine Datei auf der SSD gespeichert wird. Die Hyper-V-Umgebung ruft File TRIM für alle Regionen auf, die gelöscht werden, wenn die Datei in der VHD-Umgebung gelöscht wird. Die \_ Datei-TRIMs werden in die SSD übersetzt, damit die SSD-Leistung optimiert werden kann.

**Consumer-VHD in einem san mit schlanker Bereitstellung bereitgestellt:**

Die VHD wird anfänglich auf einer Mindestgröße einer schlanken bereitgestellten Umgebung bereitgestellt. Wenn Dateien in der VHD gespeichert werden, wächst der Speicherbedarf der VHD in Vielfachen von Slabs. Wenn Dateien in der VHD entfernt werden, ruft Hyper-V File TRIM an das zugrunde liegende, schlanke \_ bereitgestellte SAN auf. Wenn die TRIMs größer als die SLAB-Granularität sind, kann das SAN jetzt eine SLAB entfernen und so den Speicherbedarf der VHD auf diesem SAN verringern.

Wenn sich die VHD auf einem Windows 8-basierten Server befindet, sendet der Storage Optimizer auch TRIMs, um den Speicherbedarf der VHD innerhalb der bereitgestellten VHD zu reduzieren.

## <a name="tests"></a>Tests

In früheren Betriebssystemversionen gibt es keine vergleichbaren APIs. Die tatsächliche API selbst sollte keine Auswirkungen auf die Leistung haben, obwohl die Speichermedien (wenn sie ordnungsgemäß implementiert sind) eine bessere Schreibleistung zeigen können. Die API sollte sehr sorgfältig verwendet werden. es sollten nur Noch-Speicherungen übergeben werden, die nicht mehr benötigt werden, da diese Speicherungen dauerhaft aus den Speichermedien entfernt werden.

## <a name="resources"></a>Ressourcen

-   [T13-Spezifikation](http://www.t13.org/Standards/Default.aspx?DocumentType=3)
-   [T10 SCSI-Spezifikation](https://www.t10.org/)

 

 




