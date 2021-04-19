---
description: Die Setup Funktionen behandeln Schränke intern. Zum expliziten auflisten und Extrahieren von Dateien aus einer CAB-Datei können Sie die setupiteratecabinet-Funktion aufrufen.
ms.assetid: 14bd925a-e7fe-48a3-9ed6-4e42ce796290
title: Verwenden von CAB-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03467f6591b4503cb13935cca550f8c1ba1dff81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364159"
---
# <a name="using-cabinet-files"></a><span data-ttu-id="e0797-104">Verwenden von CAB-Dateien</span><span class="sxs-lookup"><span data-stu-id="e0797-104">Using Cabinet Files</span></span>

<span data-ttu-id="e0797-105">Die Setup Funktionen behandeln Schränke intern.</span><span class="sxs-lookup"><span data-stu-id="e0797-105">The setup functions handle cabinets internally.</span></span> <span data-ttu-id="e0797-106">Zum expliziten auflisten und Extrahieren von Dateien aus einer CAB-Datei können Sie die [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e0797-106">To explicitly enumerate and extract files from a cabinet, you can call the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function.</span></span>

<span data-ttu-id="e0797-107">Im folgenden Thema wird die interne CAB-Verarbeitung der Setup Funktionen und die Verwendung von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e0797-107">The following topic describes the cabinet processing internal to the setup functions and how to use [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span> <span data-ttu-id="e0797-108">Außerdem werden die von **setupiteratecabinet** gesendeten Benachrichtigungen und das erforderliche Format einer CAB-Rückruf Routine zum Verarbeiten dieser Benachrichtigungen erläutert.</span><span class="sxs-lookup"><span data-stu-id="e0797-108">Also discussed are the notifications sent by **SetupIterateCabinet** and the required format of a cabinet callback routine to process those notifications.</span></span>

-   [<span data-ttu-id="e0797-109">Extrahieren von Dateien aus kabinatendateien</span><span class="sxs-lookup"><span data-stu-id="e0797-109">Extracting Files From Cabinets</span></span>](extracting-files-from-cabinets.md)
-   [<span data-ttu-id="e0797-110">Erstellen einer CAB-Rückruf Routine</span><span class="sxs-lookup"><span data-stu-id="e0797-110">Creating a Cabinet Callback Routine</span></span>](creating-a-cabinet-callback-routine.md)

 

 



