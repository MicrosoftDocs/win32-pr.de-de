---
title: Schreiben in eine Datei
description: Schreiben in eine Datei
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- Avifileschreitedata-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9a6b9a399d8581909c99da615e32ef4487cbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340634"
---
# <a name="writing-to-a-file"></a><span data-ttu-id="0336e-104">Schreiben in eine Datei</span><span class="sxs-lookup"><span data-stu-id="0336e-104">Writing to a File</span></span>

<span data-ttu-id="0336e-105">Sie können zusätzliche Informationen in eine Datei schreiben, die mit Schreibberechtigungen geöffnet wurde, indem Sie die [**avifilewrite tedata**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="0336e-105">You can write supplementary information to a file that has been opened with write privileges by using the [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) function.</span></span> <span data-ttu-id="0336e-106">Diese Funktion kopiert die Informationen aus einem von der Anwendung bereitgestellten Puffer und platziert Sie in einem oder mehreren Blöcken in der Datei.</span><span class="sxs-lookup"><span data-stu-id="0336e-106">This function copies the information from an application-supplied buffer and places it in one or more chunks in the file.</span></span> <span data-ttu-id="0336e-107">Der "Info"-Block ist ein gängiger Riff-Block-Typ, in dem die Funktion ergänzende Informationen speichert.</span><span class="sxs-lookup"><span data-stu-id="0336e-107">The "INFO" chunk is a common RIFF chunk type in which the function stores supplementary information.</span></span> <span data-ttu-id="0336e-108">Eine Beschreibung der Riff-Dateien und der zugehörigen Datenblöcke finden Sie unter [Dienst Format Dienste für den Ressourcenaustausch](resource-interchange-file-format-services.md).</span><span class="sxs-lookup"><span data-stu-id="0336e-108">For a description of RIFF files and their data chunks, see [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span></span>

 

 




