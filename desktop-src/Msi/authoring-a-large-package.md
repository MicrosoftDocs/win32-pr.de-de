---
description: Verwenden Sie diese Richtlinie, um ein Windows Installer-Paket zu erstellen, das mehr als 32767 Dateien enthält.
ms.assetid: 3145629f-cc0a-4216-8549-76bb61070772
title: Erstellen eines großen Pakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca09c427336e4ca8a17fd8ebdf803f52ebe6c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355667"
---
# <a name="authoring-a-large-package"></a><span data-ttu-id="2fa93-103">Erstellen eines großen Pakets</span><span class="sxs-lookup"><span data-stu-id="2fa93-103">Authoring a Large Package</span></span>

<span data-ttu-id="2fa93-104">Verwenden Sie diese Richtlinie, um ein Windows Installer-Paket zu erstellen, das mehr als 32767 Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="2fa93-104">Use this guideline to author a Windows Installer package that contains more than 32767 files.</span></span>

<span data-ttu-id="2fa93-105">Wenn das Windows Installer Paket mehr als 32767 Dateien enthält, müssen Sie das Schema der Datenbank ändern, um den Grenzwert der folgenden Spalten zu erhöhen:</span><span class="sxs-lookup"><span data-stu-id="2fa93-105">If your Windows Installer package contains more than 32767 files, you must change the schema of the database to increase the limit of the following columns:</span></span>

-   <span data-ttu-id="2fa93-106">Die Sequenz Spalte der [Dateitabelle](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="2fa93-106">The Sequence column of the [File table](file-table.md).</span></span>
-   <span data-ttu-id="2fa93-107">Die LastSequence-Spalte der [Medien Tabelle](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="2fa93-107">The LastSequence column of the [Media table](media-table.md).</span></span>
-   <span data-ttu-id="2fa93-108">Die Sequenz Spalte der [patchtabelle](patch-table.md).</span><span class="sxs-lookup"><span data-stu-id="2fa93-108">The Sequence column of the [Patch table](patch-table.md).</span></span>

<span data-ttu-id="2fa93-109">Weitere Informationen finden Sie unter [Column Definition Format](column-definition-format.md).</span><span class="sxs-lookup"><span data-stu-id="2fa93-109">For more information, see [Column Definition Format](column-definition-format.md).</span></span>

<span data-ttu-id="2fa93-110">**So erhöhen Sie die Begrenzung einer Daten Bank Spalte**</span><span class="sxs-lookup"><span data-stu-id="2fa93-110">**To increase the limit of a database column**</span></span>

1.  <span data-ttu-id="2fa93-111">Exportieren Sie die Tabelle in eine IDT-Datei.</span><span class="sxs-lookup"><span data-stu-id="2fa93-111">Export the table to an .idt file.</span></span> <span data-ttu-id="2fa93-112">Weitere Informationen finden Sie unter [Msidb.exe](msidb-exe.md), [Exportieren von Dateien](export-files.md)und [importieren und exportieren](importing-and-exporting.md).</span><span class="sxs-lookup"><span data-stu-id="2fa93-112">For details, see [Msidb.exe](msidb-exe.md), [Export Files](export-files.md), and [Importing and Exporting](importing-and-exporting.md).</span></span>
2.  <span data-ttu-id="2fa93-113">Bearbeiten Sie die IDT-Datei, um den Spaltentyp von i2 in I4 oder von i2 in I4 zu ändern.</span><span class="sxs-lookup"><span data-stu-id="2fa93-113">Edit the .idt file to change the column type from i2 to i4, or from I2 to I4.</span></span>
3.  <span data-ttu-id="2fa93-114">Exportieren Sie die [ \_ Validierungs](-validation-table.md) Tabelle in eine IDT-Datei.</span><span class="sxs-lookup"><span data-stu-id="2fa93-114">Export the [\_Validation](-validation-table.md) table to an .idt file.</span></span>
4.  <span data-ttu-id="2fa93-115">Bearbeiten Sie die IDT-Datei, um die Werte in der Spalte MaxValue der [ \_ Überprüfungs Tabelle so](-validation-table.md) zu ändern, dass Sie die Erhöhung der Spaltenbreite berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="2fa93-115">Edit the .idt file to change the values in the MaxValue column of the [\_Validation](-validation-table.md) table to accommodate the increased column widths.</span></span>
5.  <span data-ttu-id="2fa93-116">Importieren Sie die IDT-Dateien zurück in die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="2fa93-116">Import the .idt files back into the database.</span></span>

<span data-ttu-id="2fa93-117">Beachten Sie, dass Transformationen und Patches nicht zwischen zwei Paketen mit unterschiedlichen Spaltentypen erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="2fa93-117">Note that transforms and patches cannot be created between two packages with different column types.</span></span>

 

 



