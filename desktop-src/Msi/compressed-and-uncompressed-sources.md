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
# <a name="compressed-and-uncompressed-sources"></a><span data-ttu-id="b62bf-104">Komprimierte und nicht komprimierte Quellen</span><span class="sxs-lookup"><span data-stu-id="b62bf-104">Compressed and Uncompressed Sources</span></span>

<span data-ttu-id="b62bf-105">Paket Autoren können die Größe ihrer Installationspakete verringern, indem Sie die Quelldateien komprimieren und in CAB- [Dateien](cabinet-files.md)einschließen.</span><span class="sxs-lookup"><span data-stu-id="b62bf-105">Package authors can reduce the size of their installation packages by compressing the source files and including them in [cabinet files](cabinet-files.md).</span></span> <span data-ttu-id="b62bf-106">Das Quelldatei Image kann komprimiert, unkomprimiert oder eine Mischung beider Typen sein.</span><span class="sxs-lookup"><span data-stu-id="b62bf-106">The source file image can be compressed, uncompressed, or a mixture of both types.</span></span>

<dl> <dt>

<span data-ttu-id="b62bf-107"><span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Komprimierte Quellen</span><span class="sxs-lookup"><span data-stu-id="b62bf-107"><span id="_____Compressed_Sources"></span><span id="_____compressed_sources"></span><span id="_____COMPRESSED_SOURCES"></span> Compressed Sources</span></span>
</dt> <dd>

<span data-ttu-id="b62bf-108">Eine Quelle, die vollständig aus komprimierten Dateien besteht, sollte das komprimierte flagbit in die [**Wort Zählung-Zusammenfassungs**](word-count-summary.md) Eigenschaft einschließen.</span><span class="sxs-lookup"><span data-stu-id="b62bf-108">A source consisting entirely of compressed files should include the compressed flag bit in the [**Word Count Summary**](word-count-summary.md) Property.</span></span> <span data-ttu-id="b62bf-109">Die komprimierten Quelldateien müssen in CAB-Dateien gespeichert werden, die sich in einem Datenstream innerhalb der MSI-Datei befinden, oder in einer separaten CAB-Datei, die sich im Stammverzeichnis der Quell Struktur befindet.</span><span class="sxs-lookup"><span data-stu-id="b62bf-109">The compressed source files must be stored in cabinet files located in a data stream inside the .msi file or in a separate cabinet file located at the root of the source tree.</span></span> <span data-ttu-id="b62bf-110">Alle Schränke in der Quelle müssen in der [Medien Tabelle](media-table.md)aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b62bf-110">All of the cabinets in the source must be listed in the [Media table](media-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="b62bf-111"><span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Nicht komprimierte Quellen</span><span class="sxs-lookup"><span data-stu-id="b62bf-111"><span id="Uncompressed_Sources"></span><span id="uncompressed_sources"></span><span id="UNCOMPRESSED_SOURCES"></span>Uncompressed Sources</span></span>
</dt> <dd>

<span data-ttu-id="b62bf-112">Eine Quelle, die ausschließlich aus nicht komprimierten Quelldateien besteht, sollte das komprimierte flagbit aus der Eigenschaft " [**Wort Zähl Zusammenfassung**](word-count-summary.md) " weglassen.</span><span class="sxs-lookup"><span data-stu-id="b62bf-112">A source consisting entirely of uncompressed source files should omit the compressed flag bit from the [**Word Count Summary**](word-count-summary.md) Property.</span></span> <span data-ttu-id="b62bf-113">Alle nicht komprimierten Dateien in der Quelle müssen in der Quell Struktur vorhanden sein, die in der [Verzeichnis Tabelle](directory-table.md)angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="b62bf-113">All of the uncompressed files in the source must exist in the source tree specified by the [Directory table](directory-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="b62bf-114"><span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Gemischte Quellen</span><span class="sxs-lookup"><span data-stu-id="b62bf-114"><span id="Mixed_Sources_____"></span><span id="mixed_sources_____"></span><span id="MIXED_SOURCES_____"></span>Mixed Sources</span></span> 
</dt> <dd>

<span data-ttu-id="b62bf-115">Wenn Sie komprimierte und nicht komprimierte Quelldateien im gleichen Paket mischen möchten, überschreiben Sie den Standardwert für die [**Wort Anzahl Zusammenfassungs**](word-count-summary.md) Eigenschaft, indem Sie die Bitflags msidbfileattributescompressed oder msidbfileattributesnoncompressed für bestimmte Dateien festlegen.</span><span class="sxs-lookup"><span data-stu-id="b62bf-115">To mix compressed and uncompressed source files in the same package, override the [**Word Count Summary**](word-count-summary.md) property default by setting the msidbFileAttributesCompressed or msidbFileAttributesNoncompressed bit flags on particular files.</span></span> <span data-ttu-id="b62bf-116">Diese Bitflags werden in der Spalte Attribute der [Dateitabelle](file-table.md) festgelegt, wenn der Komprimierungs Status der Datei nicht dem Standard entspricht, der von der Eigenschaft [**Wort Anzahl Zusammenfassung**](word-count-summary.md) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b62bf-116">These bit flags are set in the Attributes column of the [File table](file-table.md) if the compression state of the file does not match the default specified by the [**Word Count Summary**](word-count-summary.md) property.</span></span>

<span data-ttu-id="b62bf-117">Wenn z. b. für die [**Zusammenfassungs Eigenschaft der Wort Zählung**](word-count-summary.md) das komprimierte flagbit festgelegt ist, werden alle Dateien als komprimiert in eine CAB-Datei behandelt.</span><span class="sxs-lookup"><span data-stu-id="b62bf-117">For example, if the [**Word Count Summary**](word-count-summary.md) property has the compressed flag bit set, all files are treated as compressed into a cabinet.</span></span> <span data-ttu-id="b62bf-118">Alle nicht komprimierten Dateien in der Quelle müssen msidbfileattributesnoncompressed in der Spalte Attribute der [Dateitabelle](file-table.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="b62bf-118">Any uncompressed files in the source must include msidbFileAttributesNoncompressed in the Attributes column of the [File table](file-table.md).</span></span> <span data-ttu-id="b62bf-119">Die nicht komprimierten Dateien müssen sich im Stammverzeichnis der Quell Struktur befinden.</span><span class="sxs-lookup"><span data-stu-id="b62bf-119">The uncompressed files must be located at the root of the source tree.</span></span>

<span data-ttu-id="b62bf-120">Wenn für die Eigenschaft für die [**Wort Zähl Zusammenfassung**](word-count-summary.md) das unkomprimierte Flag festgelegt ist, werden Dateien standardmäßig als nicht komprimiert behandelt, und alle komprimierten Dateien müssen msidbfileattributescompressed in der Spalte Attribute der Dateitabelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="b62bf-120">If the [**Word Count Summary**](word-count-summary.md) property has the uncompressed flag set, files are treated as uncompressed by default and any compressed files must include msidbFileAttributesCompressed in the Attributes column of the File table.</span></span> <span data-ttu-id="b62bf-121">Alle komprimierten Dateien müssen in CAB-Dateien gespeichert werden, die sich in einem Datenstream innerhalb der MSI-Datei befinden, oder in einer separaten CAB-Datei, die sich im Stammverzeichnis der Quell Struktur befindet.</span><span class="sxs-lookup"><span data-stu-id="b62bf-121">All of the compressed files must be stored in cabinet files located in a data stream inside the .msi file or in a separate cabinet file located at the root of the source tree.</span></span>

<span data-ttu-id="b62bf-122">Weitere Informationen finden Sie unter [Verwenden von Schränken und komprimierten Quellen](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="b62bf-122">For more information, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

</dd> </dl>

 

 



