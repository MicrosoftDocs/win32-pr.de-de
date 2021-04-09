---
description: Die arefileapisansi-Funktion bestimmt, ob die Datei-e/a-Funktionen die ANSI-oder OEM-Zeichensatz-Codepage verwenden.
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: Festlegen der Codepage für den aktuellen Zeichensatz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e180d908605ec423314ef2197829fd95ff51a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865544"
---
# <a name="determining-the-current-character-set-code-page"></a><span data-ttu-id="29c90-103">Festlegen der Codepage für den aktuellen Zeichensatz</span><span class="sxs-lookup"><span data-stu-id="29c90-103">Determining the Current Character Set Code Page</span></span>

<span data-ttu-id="29c90-104">Die [**arefileapisansi**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) -Funktion bestimmt, ob die Datei-e/a-Funktionen die ANSI-oder OEM-Zeichensatz-Codepage verwenden.</span><span class="sxs-lookup"><span data-stu-id="29c90-104">The [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) function determines whether the file I/O functions are using the ANSI or OEM character set code page.</span></span> <span data-ttu-id="29c90-105">Die Funktion [**setfileapistoansi**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) bewirkt, dass die Funktionen die ANSI-Codepage verwenden.</span><span class="sxs-lookup"><span data-stu-id="29c90-105">The [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) function causes the functions to use the ANSI code page.</span></span> <span data-ttu-id="29c90-106">Die [**setfileapistooem**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) -Funktion bewirkt, dass die Funktionen die OEM-Codepage verwenden.</span><span class="sxs-lookup"><span data-stu-id="29c90-106">The [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) function causes the functions to use the OEM code page.</span></span>

<span data-ttu-id="29c90-107">Standardmäßig verwenden Datei-e/a-Funktionen ANSI-Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="29c90-107">By default, file I/O functions use ANSI file names.</span></span> <span data-ttu-id="29c90-108">Die von Kernel32.dll exportierten Funktionen, die Dateinamen akzeptieren oder zurückgeben, sind von der Datei Code Page-Einstellung betroffen.</span><span class="sxs-lookup"><span data-stu-id="29c90-108">Functions exported by Kernel32.dll that accept or return file names are affected by the file code page setting.</span></span>

<span data-ttu-id="29c90-109">Sowohl [**setfileapistoansi**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) als auch [**setfileapistooem**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) legen die Codepage pro Prozess statt pro Thread oder pro Computer fest.</span><span class="sxs-lookup"><span data-stu-id="29c90-109">Both [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) and [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) set the code page per process, rather than per thread or per computer.</span></span>

 

 



