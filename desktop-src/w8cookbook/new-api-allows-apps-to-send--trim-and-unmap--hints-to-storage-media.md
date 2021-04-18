---
title: Mit der neuen API können Apps "Trim-und unmap"-Hinweise an Speichermedien senden.
description: Neue API ermöglicht apps das Senden von \ 0034; Trim und unmap \ 0034; Hinweise zu Speichermedien
ms.assetid: DDBC3592-BD4D-4826-83FE-387564DA07E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e043c1188bda790b4ed151e8a79e1f7b4c6f0f9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "106340537"
---
# <a name="new-api-allows-apps-to-send-trim-and-unmap-hints-to-storage-media"></a>Mit der neuen API können Apps "Trim-und unmap"-Hinweise an Speichermedien senden.

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

Mithilfe von Trim-hinweisen wird das Laufwerk benachrichtigt, dass bestimmte zuvor zugewiesene Sektoren von der APP nicht mehr benötigt werden und gelöscht werden können. Dies wird in der Regel verwendet, wenn eine APP große Speicher Belegungen über eine Datei zuweist und die Zuordnungen für die Datei dann selbst verwaltet (z. b. virtuelle Festplatten Dateien).

**Was ist Trim?**

Solid-State-Laufwerke (SSDs) sind in der Regel Flash speicherbasierte Geräte mit Block Löschung. Dies bedeutet, dass beim Schreiben von Daten in den SSD-Daten nicht an Ort und Stelle geschrieben werden dürfen und an einem anderen Ort geschrieben werden müssen, bis der Block in die Garbage Collection aufgenommen werden kann. Da das SSD über keinen internen Mechanismus verfügt, um zu bestimmen, ob bestimmte Blöcke entfernt werden und andere benötigt werden. Der SSD kann die einzige Zeit markieren, die der Bereich "Dirty" ist, wenn er überschrieben wird. In anderen Fällen, z. b. Wenn eine Datei gelöscht wird, behält der SSD diese Sektoren bei, da der Löschvorgang nur als MFT-Änderung (Master File Table) ausgeführt wird und nicht als Vorgang für alle Bereiche der Datei. In Windows 7 haben wir eine Standardmethode für die Kommunikation mit SSDs zu Sektoren eingeführt, die nicht mehr benötigt werden. Dieser Befehl ist in der [T13-Spezifikation](https://www.t13.org/Standards/Default.aspx?DocumentType=3) als Befehl zum kürzen definiert. NTFS sendet den Befehl Trim für einige normale Inline Vorgänge, z. b. "DeleteFile".

**Andere Verwendungsmöglichkeiten von Trim in der Speicher Welt**

Wie SSDs, Storage Area Networks (SANs) und die neuen Implementierungen von Software Spaces für Windows 8-Features verwenden Trim-Befehls Hinweise zum Verwalten Ihrer Leerzeichen in schlank bereitgestellten Umgebungen. Sans und Software Plätze weisen Speicherbereiche zu, die größer sind als Sektoren oder Cluster (von 1 MB bis 1 GB). Wenn Sie für Ihre Zuordnungs Größe (oder höher als die Zuordnungs Größe) Trim-Hinweise erhalten, kann das San/SSD einen Bereich aufheben, um den Speicherplatz für andere Dateien freizugeben. Sie durchlaufen in der Regel alle Trim-Hinweise an das zugrunde liegende Medium (SSD oder HDD), damit Sie den freigegebenen Speicherplatz entsprechend verbrauchen können. In der Regel verschieben Sie Daten nicht, um die Zuordnung von Regionen aufzuheben, und Sie verfolgen auch keine Trim-Bereiche nach den zugewiesenen Regionen (wenn die Region leer ist).

Schlank zugewiesene Sans verwenden die an Sie weiter gegebenen Trim-Hinweise, um den gesamten physischen Speicherbedarf zu verringern und so die Kosten zu senken. Die [T10-SCSI-Spezifikation](https://www.t10.org) definiert den Befehl "unmap" (ähnlich wie der Trim-Befehl). Hier gilt der Befehl für alle Arten von Speicher, einschließlich HDDs, SSDs und anderen. Der unmap-Befehl hilft beim Entfernen physischer Blöcke aus der San-Zuordnung.

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



Die Datei Trim wird über den Puffer, wenn möglich, oder asynchron (nicht gepuffert) an das Gerät ioctl DSM Command Trim übermittelt. Dies wird dem Befehl Trim für ATA-Geräte zugeordnet und der Befehl zum Aufheben der Zuordnung für SCSI-Geräte. Der Code zum Kürzen von Dateien sendet die Regionen nacheinander, wie in den oben aufgeführten Blöcken angegeben.

File Trim wartet nicht auf Rückgabe vom Gerät, da die Befehle Trim und unmap als Hinweise zu den zugrunde liegenden Speichermedien definiert sind und Rückgabecodes nicht erwartet werden.

**End-to-End-Workflow:**

1.  Datei Trim abrufen
    1.  Datei Trim untersucht Eingaben für Fehler
    2.  Durch Datei Trim werden die Blöcke in LCN-Regionen aufgeteilt.
    3.  Die Datei Trim wird für falsch ausgerichtete Bereiche, die an Trim übermittelt werden, auf-und heruntergefahren.
    4.  Durch Datei Trim werden Einträge im Cache gelöscht, die sich auf die Trim-Bereiche beziehen.
    5.  Die Datei Trim übergibt IOCTL \_ DSM (Trim) pro Region.
2.  Datei-Trim-Rückgabe oder-Fehler
    1.  Die Fehlerüberprüfung erfolgt bei der Eingabe Gültigkeit.
    2.  Wenn nur einige der Blöcke gültig sind, wird ein Fehler für den gesamten API-Befehl zurückgegeben.

**Anwendungsfälle**

**Virtuelle Festplatte (Virtual Hard Disk, VHD) auf einem SSD-Laufwerk:**

Die virtuelle Festplatte wird anfänglich auf "sauberen", nicht verwendeten Medien bereitgestellt. Bei Verwendung der VHD verwendet die VHD Teile der Speichermedien für Dateien usw. Wenn Dateien auf dem Speichermedium gelöscht werden, werden diese Dateien nicht aus der SSD entfernt, da die komplette VHD als eine Datei auf dem SSD gespeichert wird. In der Hyper-V-Umgebung wird die Datei Kürzung für alle Regionen aufgerufen, die gelöscht werden, wenn "Delete-File" in der VHD-Umgebung auftritt. Die Datei-Metriken \_ werden in den SSD übersetzt, damit die SSD-Leistung optimiert werden kann.

**In einem dünn bereitgestellten San eingebundene consumervhd:**

Die virtuelle Festplatte wird anfänglich auf einer minimalen Festplatte einer dünn bereitgestellten Umgebung bereitgestellt. Wenn Dateien auf der virtuellen Festplatte gespeichert werden, wächst der Speicherbedarf der virtuellen Festplatte in Vielfachen von Platten. Wenn Dateien in der virtuellen Festplatte entfernt werden, ruft die Hyper-V-Datei in \_ das zugrunde liegende, schlank bereitgestellte San auf. Wenn die Festplatten größer sind als die Granularität der Platte, kann das San nun eine Platte entfernen und somit den Speicherbedarf der VHD auf diesem San verringern.

Wenn sich die virtuelle Festplatte auf einem Windows 8-basierten Server befindet, sendet der Speicher Optimierer auch die drei-MS-Werte, um den Festplatten Speicherplatz der virtuellen Festplatte innerhalb der bereitgestellten VHD zu verringern.

## <a name="tests"></a>Tests

In früheren Betriebssystemversionen gibt es keine vergleichbaren APIs. Die tatsächliche API selbst sollte keine Auswirkung auf die Leistung haben, obwohl das Speichermedium (wenn es korrekt implementiert ist) eine bessere Schreibleistung darstellen kann. Die API sollte sehr sorgfältig verwendet werden. nur Blöcke, die nicht mehr benötigt werden, sollten nach unten weitergegeben werden, da diese Blöcke permanent aus den Speichermedien entfernt werden.

## <a name="resources"></a>Ressourcen

-   [T13-Spezifikation](http://www.t13.org/Standards/Default.aspx?DocumentType=3)
-   [T10-SCSI-Spezifikation](https://www.t10.org/)

 

 




