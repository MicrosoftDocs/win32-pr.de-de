---
description: Sie können Dateien auf zweierlei Weise aus einer CAB-Datei extrahieren. Die erste und einfachste Möglichkeit besteht darin, die in den Setup Funktionen integrierte automatische CAB-Verarbeitung zu nutzen.
ms.assetid: 113333c8-28d1-4b0e-8da4-0c94389d8038
title: Extrahieren von Dateien aus kabinatendateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94f413b4ad0ee1511dde21af747cd2665a4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350486"
---
# <a name="extracting-files-from-cabinets"></a><span data-ttu-id="26aa4-104">Extrahieren von Dateien aus kabinatendateien</span><span class="sxs-lookup"><span data-stu-id="26aa4-104">Extracting Files from Cabinets</span></span>

<span data-ttu-id="26aa4-105">Sie können Dateien auf zweierlei Weise aus einer CAB-Datei extrahieren.</span><span class="sxs-lookup"><span data-stu-id="26aa4-105">You can extract files from a cabinet in two ways.</span></span> <span data-ttu-id="26aa4-106">Die erste und einfachste Möglichkeit besteht darin, die in den Setup Funktionen integrierte automatische CAB-Verarbeitung zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="26aa4-106">The first and simplest way is to take advantage of the automatic cabinet processing built into the setup functions.</span></span>

<span data-ttu-id="26aa4-107">Die Installationsfunktionen, wie z. b. [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**setupinstallfile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)und [**setupinstallfrominbsection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), überprüfen die Komprimierung der einzelnen Dateien.</span><span class="sxs-lookup"><span data-stu-id="26aa4-107">The installation functions, such as [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), and [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), check the compression on each file.</span></span> <span data-ttu-id="26aa4-108">Wenn sich die Datei in einer CAB-Datei befindet, sucht die Funktion zuerst nach einer Datei mit diesem Namen außerhalb der CAB-Datei.</span><span class="sxs-lookup"><span data-stu-id="26aa4-108">If the file is in a cabinet, the functions first search for a file of that name outside the cabinet.</span></span> <span data-ttu-id="26aa4-109">Wenn Sie gefunden wird, wird die externe Datei von den Funktionen installiert, und die Datei wird im CAB ignoriert.</span><span class="sxs-lookup"><span data-stu-id="26aa4-109">If found, the functions install the external file, ignoring the file inside the cabinet.</span></span> <span data-ttu-id="26aa4-110">Dadurch können Sie eine einzelne Datei innerhalb der CAB-Datei aktualisieren, ohne die CAB-Datei neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="26aa4-110">This enables you to update a single file inside the cabinet without rebuilding the cabinet.</span></span>

<span data-ttu-id="26aa4-111">Die Setup Funktionen verfolgen auch, welche Dateien in einer CAB-Datei abgerufen wurden, sodass eine Datei nur einmal extrahiert wird, auch wenn Sie mehrmals installiert wird.</span><span class="sxs-lookup"><span data-stu-id="26aa4-111">The setup functions also track which files in a cabinet have been retrieved, so that a file is extracted only once, even if it is installed several times.</span></span>

<span data-ttu-id="26aa4-112">Die zweite Möglichkeit zum Extrahieren von Dateien aus einer CAB-Datei ist die Verwendung von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="26aa4-112">The second way to extract files from a cabinet is by using [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span> <span data-ttu-id="26aa4-113">Diese Funktion durchläuft jede Datei in einer CAB-Datei und sendet eine Benachrichtigung an eine Rückruf Routine für jede gefundene Datei.</span><span class="sxs-lookup"><span data-stu-id="26aa4-113">This function iterates through each file in a cabinet, sending a notification to a callback routine for each file found.</span></span> <span data-ttu-id="26aa4-114">Die Rückruf Routine gibt dann einen Wert zurück, der angibt, ob die Datei extrahiert oder übersprungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="26aa4-114">The callback routine then returns a value that indicates whether the file should be extracted or skipped.</span></span>

> [!Note]  
> <span data-ttu-id="26aa4-115">Die Setup-API stellt keine Standard Rückruf Routine zum Verarbeiten von CAB-Benachrichtigungen bereit.</span><span class="sxs-lookup"><span data-stu-id="26aa4-115">The Setup API does not supply a default callback routine to handle cabinet notifications.</span></span> <span data-ttu-id="26aa4-116">Wenn Sie [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) explizit aufrufen, müssen Sie eine Rückruf Routine angeben, um die CAB-Benachrichtigungen zu verarbeiten, die von der Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="26aa4-116">If you call [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) explicitly, you must supply a callback routine to process the cabinet notifications that the function returns.</span></span>

 

 

 



