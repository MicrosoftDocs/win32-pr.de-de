---
description: Die GetFileSize-Funktion Ruft die Größe einer Datei ab.
ms.assetid: 4d3a3925-72e8-4350-b46d-e2c25791e862
title: Bestimmen der Größe einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f7205c47fe25b223dbcc12322516ff2b162fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959879"
---
# <a name="determining-the-size-of-a-file"></a><span data-ttu-id="7778e-103">Bestimmen der Größe einer Datei</span><span class="sxs-lookup"><span data-stu-id="7778e-103">Determining the Size of a File</span></span>

<span data-ttu-id="7778e-104">Die [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) -Funktion Ruft die Größe einer Datei ab.</span><span class="sxs-lookup"><span data-stu-id="7778e-104">The [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function retrieves the size of a file.</span></span>

<span data-ttu-id="7778e-105">Da die NTFS-Dateisystem Implementierung von Dateien mehrere Datenströme innerhalb einer Datei zulässt, muss jede Anwendung, die Sie für den Zugriff auf Dateien schreiben, die Möglichkeit berücksichtigen, dass der Ersteller der Datei mehrere Datenströme in die Datei einschließen kann.</span><span class="sxs-lookup"><span data-stu-id="7778e-105">Because the NTFS file system implementation of files allows for multiple streams within a file, any application you write that accesses files must account for the possibility that the creator of the file can include multiple streams in the file.</span></span> <span data-ttu-id="7778e-106">Wenn in einer Datei nicht auf mehrere Datenströme geprüft wird, kann die Anwendung die Gesamtgröße der Datei unterschätzen, unter anderem Fehler.</span><span class="sxs-lookup"><span data-stu-id="7778e-106">If multiple streams are not checked for in a file, the application can underestimate the total size of the file, among other errors.</span></span>

 

 



