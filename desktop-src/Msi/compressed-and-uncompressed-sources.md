---
description: Paketautoren können die Größe ihrer Installationspakete verringern, indem sie die Quelldateien komprimieren und in Schränkdateien einschleieren. Das Quelldateiimage kann komprimiert, unkomprimiert oder eine Mischung aus beiden Typen sein.
ms.assetid: e84c52ca-a1c4-4c81-9c24-31ea435054db
title: Komprimierte und nicht komprimierte Quellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7d35a5723261ab1c62866d185a8402a9607600cad906c2fb66ddc5dc85ac08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144451"
---
# <a name="compressed-and-uncompressed-sources"></a>Komprimierte und nicht komprimierte Quellen

Paketautoren können die Größe ihrer Installationspakete verringern, indem sie die Quelldateien komprimieren und sie in die [Schränkdateien einschleieren.](cabinet-files.md) Das Quelldateiimage kann komprimiert, unkomprimiert oder eine Mischung aus beiden Typen sein.

<dl> <dt>

<span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Komprimierte Quellen
</dt> <dd>

Eine Quelle, die vollständig aus komprimierten Dateien besteht, sollte das komprimierte Flagbit in der Eigenschaft Zusammenfassung der [**Wortanzahl**](word-count-summary.md) enthalten. Die komprimierten Quelldateien müssen in Schränkendateien gespeichert werden, die sich in einem Datenstrom innerhalb der .msi-Datei oder in einer separaten Schränkdatei befinden, die sich im Stammverzeichnis der Quellstruktur befindet. Alle Schränke in der Quelle müssen in der [Media-Tabelle aufgeführt werden.](media-table.md)

</dd> <dt>

<span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Nicht komprimierte Quellen
</dt> <dd>

Eine Quelle, die vollständig aus unkomprimierten Quelldateien besteht, sollte das komprimierte Flagbit aus der Eigenschaft Zusammenfassung der [**Wortanzahl**](word-count-summary.md) weglassen. Alle nicht komprimierten Dateien in der Quelle müssen in der Quellstruktur vorhanden sein, die von der [Directory-Tabelle angegeben wird.](directory-table.md)

</dd> <dt>

<span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Gemischte Quellen 
</dt> <dd>

Um komprimierte und unkomprimierte Quelldateien im gleichen [](word-count-summary.md) Paket zu kombinieren, überschreiben Sie die Eigenschaft Zusammenfassung der Wortanzahl standardmäßig, indem Sie die Bitflags msidbFileAttributesCompressed oder msidbFileAttributesNoncompressed für bestimmte Dateien festlegen. Diese Bitflags werden in der Spalte [](file-table.md) Attribute der File -Tabelle festgelegt, wenn der Komprimierungszustand der Datei nicht mit dem von der Eigenschaft [**Zusammenfassung**](word-count-summary.md) der Wortanzahl angegebenen Standardwert übereinstimmen.

Wenn für die Eigenschaft Zusammenfassung der [**Wortanzahl**](word-count-summary.md) beispielsweise das komprimierte Flagbit festgelegt ist, werden alle Dateien als komprimiert in einem Schränk behandelt. Alle nicht komprimierten Dateien in der Quelle müssen msidbFileAttributesNoncompressed in der Attributes -Spalte der [Dateitabelle enthalten.](file-table.md) Die nicht komprimierten Dateien müssen sich im Stammverzeichnis der Quellstruktur befinden.

Wenn [](word-count-summary.md) für die Eigenschaft Zusammenfassung der Wortanzahl das Flag unkomprimiert festgelegt ist, werden Dateien standardmäßig als unkomprimiert behandelt, und alle komprimierten Dateien müssen msidbFileAttributesCompressed in der Spalte Attribute der Tabelle Datei enthalten. Alle komprimierten Dateien müssen in "cabinet"-Dateien gespeichert werden, die sich in einem Datenstrom innerhalb der .msi-Datei oder in einer separaten Cabinet-Datei befinden, die sich im Stammverzeichnis der Quellstruktur befindet.

Weitere Informationen finden Sie unter [Verwenden von Schränken und komprimierten Quellen.](using-cabinets-and-compressed-sources.md)

</dd> </dl>

 

 



