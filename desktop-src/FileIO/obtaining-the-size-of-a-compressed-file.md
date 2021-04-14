---
description: Verwenden Sie die getcompressedfilesize-Funktion, um die komprimierte Größe einer Datei zu erhalten.
ms.assetid: c6bfd221-f125-48b4-b38b-822a23639c40
title: Abrufen der Größe einer komprimierten Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4954a53184e55341838fef7cd70f01639f13bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527047"
---
# <a name="obtaining-the-size-of-a-compressed-file"></a><span data-ttu-id="1c06e-103">Abrufen der Größe einer komprimierten Datei</span><span class="sxs-lookup"><span data-stu-id="1c06e-103">Obtaining the Size of a Compressed File</span></span>

<span data-ttu-id="1c06e-104">Verwenden Sie die [**getcompressedfilesize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) -Funktion, um die komprimierte Größe einer Datei abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1c06e-104">Use the [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) function to obtain the compressed size of a file.</span></span> <span data-ttu-id="1c06e-105">Wenn die Datei komprimiert ist, ist die komprimierte Größe kleiner als die nicht komprimierte Größe.</span><span class="sxs-lookup"><span data-stu-id="1c06e-105">If the file is compressed, its compressed size will be less than its uncompressed size.</span></span> <span data-ttu-id="1c06e-106">Verwenden Sie die [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) -Funktion, um die unkomprimierte Größe einer Datei zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="1c06e-106">Use the [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function to determine the uncompressed size of a file.</span></span>

 

 



