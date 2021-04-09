---
description: Paket Autoren können die Größe ihrer Installationspakete verringern, indem Sie die Quelldateien komprimieren und in CAB-Dateien einschließen. Das Quelldatei Image kann komprimiert, unkomprimiert oder eine Mischung beider Typen sein.
ms.assetid: e84c52ca-a1c4-4c81-9c24-31ea435054db
title: Komprimierte und nicht komprimierte Quellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dc706a73d52f1dac35c917bd6c178a543ab300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959176"
---
# <a name="compressed-and-uncompressed-sources"></a>Komprimierte und nicht komprimierte Quellen

Paket Autoren können die Größe ihrer Installationspakete verringern, indem Sie die Quelldateien komprimieren und in CAB- [Dateien](cabinet-files.md)einschließen. Das Quelldatei Image kann komprimiert, unkomprimiert oder eine Mischung beider Typen sein.

<dl> <dt>

<span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Komprimierte Quellen
</dt> <dd>

Eine Quelle, die vollständig aus komprimierten Dateien besteht, sollte das komprimierte flagbit in die [**Wort Zählung-Zusammenfassungs**](word-count-summary.md) Eigenschaft einschließen. Die komprimierten Quelldateien müssen in CAB-Dateien gespeichert werden, die sich in einem Datenstream innerhalb der MSI-Datei befinden, oder in einer separaten CAB-Datei, die sich im Stammverzeichnis der Quell Struktur befindet. Alle Schränke in der Quelle müssen in der [Medien Tabelle](media-table.md)aufgeführt werden.

</dd> <dt>

<span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Nicht komprimierte Quellen
</dt> <dd>

Eine Quelle, die ausschließlich aus nicht komprimierten Quelldateien besteht, sollte das komprimierte flagbit aus der Eigenschaft " [**Wort Zähl Zusammenfassung**](word-count-summary.md) " weglassen. Alle nicht komprimierten Dateien in der Quelle müssen in der Quell Struktur vorhanden sein, die in der [Verzeichnis Tabelle](directory-table.md)angegeben ist.

</dd> <dt>

<span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Gemischte Quellen 
</dt> <dd>

Wenn Sie komprimierte und nicht komprimierte Quelldateien im gleichen Paket mischen möchten, überschreiben Sie den Standardwert für die [**Wort Anzahl Zusammenfassungs**](word-count-summary.md) Eigenschaft, indem Sie die Bitflags msidbfileattributescompressed oder msidbfileattributesnoncompressed für bestimmte Dateien festlegen. Diese Bitflags werden in der Spalte Attribute der [Dateitabelle](file-table.md) festgelegt, wenn der Komprimierungs Status der Datei nicht dem Standard entspricht, der von der Eigenschaft [**Wort Anzahl Zusammenfassung**](word-count-summary.md) angegeben wird.

Wenn z. b. für die [**Zusammenfassungs Eigenschaft der Wort Zählung**](word-count-summary.md) das komprimierte flagbit festgelegt ist, werden alle Dateien als komprimiert in eine CAB-Datei behandelt. Alle nicht komprimierten Dateien in der Quelle müssen msidbfileattributesnoncompressed in der Spalte Attribute der [Dateitabelle](file-table.md)enthalten. Die nicht komprimierten Dateien müssen sich im Stammverzeichnis der Quell Struktur befinden.

Wenn für die Eigenschaft für die [**Wort Zähl Zusammenfassung**](word-count-summary.md) das unkomprimierte Flag festgelegt ist, werden Dateien standardmäßig als nicht komprimiert behandelt, und alle komprimierten Dateien müssen msidbfileattributescompressed in der Spalte Attribute der Dateitabelle enthalten. Alle komprimierten Dateien müssen in CAB-Dateien gespeichert werden, die sich in einem Datenstream innerhalb der MSI-Datei befinden, oder in einer separaten CAB-Datei, die sich im Stammverzeichnis der Quell Struktur befindet.

Weitere Informationen finden Sie unter [Verwenden von Schränken und komprimierten Quellen](using-cabinets-and-compressed-sources.md).

</dd> </dl>

 

 



