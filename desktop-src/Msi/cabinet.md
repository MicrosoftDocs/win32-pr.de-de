---
description: Der CAB-Datentyp muss in der CAB-Spalte der Medien Tabelle verwendet werden.
ms.assetid: 149c74ea-4342-45dd-8da4-4dfa7f4317a0
title: KEs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814473ef4d21d5445b5b5319278a5e25a7f5540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864423"
---
# <a name="cabinet"></a><span data-ttu-id="18b10-103">KEs</span><span class="sxs-lookup"><span data-stu-id="18b10-103">Cabinet</span></span>

<span data-ttu-id="18b10-104">Der CAB-Datentyp muss in der CAB-Spalte der [Medien Tabelle](media-table.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18b10-104">The Cabinet data type must be used in the Cabinet column of the [Media table](media-table.md).</span></span>

<span data-ttu-id="18b10-105">Wenn dem CAB-Namen das Nummern Zeichen vorangestellt ist, wird die CAB-Datei als Datenstream innerhalb des Pakets gespeichert.</span><span class="sxs-lookup"><span data-stu-id="18b10-105">If the cabinet name is preceded by the number sign, the cabinet is stored as a data stream inside the package.</span></span> <span data-ttu-id="18b10-106">Die Zeichenfolge, die auf folgt, \# ist ein [Bezeichner](identifier.md) für diesen Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="18b10-106">The character string which follows the \# is an [Identifier](identifier.md) for this data stream.</span></span> <span data-ttu-id="18b10-107">Beachten Sie Folgendes: Wenn die CAB-Datei als Datenstream gespeichert wird, wird bei einem CAB-Namen die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="18b10-107">Note that if the cabinet is stored as a data stream, the name of a cabinet is case-sensitive.</span></span>

<span data-ttu-id="18b10-108">Wenn dem CAB-Namen nicht das Nummern Zeichen vorangestellt ist \# , wird die CAB-Datei in einer separaten Datei gespeichert, die sich im Stammverzeichnis der Quell Struktur befindet, die von der [Verzeichnis Tabelle](directory-table.md)angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="18b10-108">If the cabinet name is not preceded by the number sign \#, the cabinet is stored in a separate file located at the root of the source tree specified by the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="18b10-109">Die CAB-Datei muss die kurze Dateiname-Syntax verwenden, die aus einem acht Zeichennamen, einem Zeitraum und einer Erweiterung mit drei Zeichen besteht.</span><span class="sxs-lookup"><span data-stu-id="18b10-109">The cabinet file must use the short file name syntax consisting of an eight character name, a period, and a three character extension.</span></span> <span data-ttu-id="18b10-110">Der CAB-Datentyp kann die kurze \| CPS-Syntax für Dateinamen nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="18b10-110">The Cabinet data type cannot use the short\|longname syntax for file names.</span></span> <span data-ttu-id="18b10-111">Wenn die CAB-Datei als separate Datei gespeichert wird, wird bei dem Namen der CAB-Datei die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="18b10-111">If the cabinet file is stored as a separate file, the name of the cabinet file is not case-sensitive.</span></span>

<span data-ttu-id="18b10-112">Um Speicherplatz zu sparen, entfernt das Installationsprogramm alle in der MSI-Datei eingebetteten Schränke, bevor das Installationspaket auf dem Computer des Benutzers zwischengespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="18b10-112">To conserve disk space, the installer removes any cabinets embedded in the .msi file before caching the installation package on the user's computer.</span></span>

<span data-ttu-id="18b10-113">Weitere Informationen finden Sie [unter Einschließen einer CAB-Datei in eine Installation](including-a-cabinet-file-in-an-installation.md).</span><span class="sxs-lookup"><span data-stu-id="18b10-113">See [Including a Cabinet File in an Installation](including-a-cabinet-file-in-an-installation.md).</span></span>

 

 



