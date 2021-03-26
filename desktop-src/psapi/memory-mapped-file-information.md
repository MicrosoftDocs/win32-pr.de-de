---
title: Dateiinformationen Memory-Mapped
description: Eine im Speicher abgebildete Datei (oder Datei Zuordnung) ist das Ergebnis der Zuordnung des Inhalts einer Datei zu einem Teil des virtuellen Adressraums eines Prozesses. Sie kann verwendet werden, um eine Datei oder einen Arbeitsspeicher zwischen zwei oder mehr Prozessen freizugeben.
ms.assetid: b6ec2bc4-c504-4d0b-87f0-39bb1949accd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc6d33e7f3fe6bef36ea6e5a7f355b780d89b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102162"
---
# <a name="memory-mapped-file-information"></a><span data-ttu-id="5b7bd-104">Dateiinformationen Memory-Mapped</span><span class="sxs-lookup"><span data-stu-id="5b7bd-104">Memory-Mapped File Information</span></span>

<span data-ttu-id="5b7bd-105">Eine im *Speicher abgebildete Datei* (oder *Datei Zuordnung*) ist das Ergebnis der Zuordnung des Inhalts einer Datei zu einem Teil des virtuellen Adressraums eines Prozesses.</span><span class="sxs-lookup"><span data-stu-id="5b7bd-105">A *memory-mapped file* (or *file mapping*) is the result of associating a file's contents with a portion of the virtual address space of a process.</span></span> <span data-ttu-id="5b7bd-106">Sie kann verwendet werden, um eine Datei oder einen Arbeitsspeicher zwischen zwei oder mehr Prozessen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="5b7bd-106">It can be used to share a file or memory between two or more processes.</span></span>

<span data-ttu-id="5b7bd-107">Die [**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) -Funktion empfängt ein Prozess handle und einen Zeiger auf eine Adresse als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="5b7bd-107">The [**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) function receives a process handle and a pointer to an address as input.</span></span> <span data-ttu-id="5b7bd-108">Wenn sich die Adresse innerhalb einer Speicher Abbild Datei im virtuellen Adressraum des Prozesses befindet, gibt die Funktion den Namen der Speicher Abbild Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="5b7bd-108">If the address is within a memory-mapped file in the virtual address space of the process, the function returns the name of the memory-mapped file.</span></span> <span data-ttu-id="5b7bd-109">Die von **GetMappedFileName** zurückgegebenen Dateinamen verwenden Geräte Form anstelle von Laufwerk Buchstaben.</span><span class="sxs-lookup"><span data-stu-id="5b7bd-109">The file names returned by **GetMappedFileName** use device form, rather than drive letters.</span></span> <span data-ttu-id="5b7bd-110">Beispielsweise sieht der Dateiname "c: \\ Winnt \\ system32 \\ CType. nls" in Geräte Form wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="5b7bd-110">For example, the file name c:\\winnt\\system32\\ctype.nls would look like this in device form:</span></span>

<span data-ttu-id="5b7bd-111">\\Device \\ Harddisk0 \\ Partition1 \\ Winnt \\ system32 \\ CType. nls</span><span class="sxs-lookup"><span data-stu-id="5b7bd-111">\\Device\\Harddisk0\\Partition1\\WINNT\\System32\\ctype.nls</span></span>

<span data-ttu-id="5b7bd-112">Weitere Informationen zu Speicher Abbild Dateien finden Sie unter [Datei Zuordnung](/windows/desktop/Memory/file-mapping).</span><span class="sxs-lookup"><span data-stu-id="5b7bd-112">For more information about memory-mapped files, see [File Mapping](/windows/desktop/Memory/file-mapping).</span></span> <span data-ttu-id="5b7bd-113">Ein Beispiel für das Konvertieren von Dateinamen in Geräte Form in Laufwerk Buchstaben finden Sie unter Abrufen [eines Datei namens aus einem Datei Handle](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).</span><span class="sxs-lookup"><span data-stu-id="5b7bd-113">For an example that converts file names in device form to drive letters, see [Obtaining a File Name From a File Handle](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).</span></span>

 

 