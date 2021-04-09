---
description: Rufen Sie die zugeordnete Größe oder die Gesamtgröße für eine Datei mithilfe der getcompressedfilesize-Funktion oder der GetFileSize-Funktion ab.
ms.assetid: 1894ea01-49ff-41e3-9912-1cd75966bd3f
title: Abrufen der Größe einer sparsedatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93a1c6a33f0d6913e0e6848e4593ea0e0bf0259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863055"
---
# <a name="obtaining-the-size-of-a-sparse-file"></a><span data-ttu-id="731e7-103">Abrufen der Größe einer sparsedatei</span><span class="sxs-lookup"><span data-stu-id="731e7-103">Obtaining the Size of a Sparse File</span></span>

<span data-ttu-id="731e7-104">Verwenden Sie die Funktion [**getcompressedfilesize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) , um die tatsächliche Größe zu ermitteln, die auf dem Datenträger für eine sparsedatei zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="731e7-104">Use the [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) function to obtain the actual size allocated on disk for a sparse file.</span></span> <span data-ttu-id="731e7-105">Diese Summe umfasst nicht die Größe der Regionen, deren Zuordnung aufgehoben wurde, da Sie mit Nullen gefüllt wurden.</span><span class="sxs-lookup"><span data-stu-id="731e7-105">This total does not include the size of the regions which were deallocated because they were filled with zeros.</span></span> <span data-ttu-id="731e7-106">Verwenden Sie die [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) -Funktion, um die Gesamtgröße einer Datei zu bestimmen, einschließlich der Größe der sparsespalten, deren Zuordnung aufgehoben wurde.</span><span class="sxs-lookup"><span data-stu-id="731e7-106">Use the [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function to determine the total size of a file, including the size of the sparse regions that were deallocated.</span></span>

 

 



