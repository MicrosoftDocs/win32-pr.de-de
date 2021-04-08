---
title: Erfassen von Daten
description: Erfassen von Daten
ms.assetid: de029673-9929-40f9-b29b-2598e1e5c988
keywords:
- capcapturesequence-Makro
- capfilesaveas-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24b2110da9a85faaa991e67efdd1ef48e3d9c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037316"
---
# <a name="capturing-data"></a><span data-ttu-id="11b5e-105">Erfassen von Daten</span><span class="sxs-lookup"><span data-stu-id="11b5e-105">Capturing Data</span></span>

<span data-ttu-id="11b5e-106">Im folgenden Beispiel wird das [**capcapturesequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) -Makro zum Starten der Video Erfassung und das [**capfilesaveas**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) -Makro zum Kopieren der aufgezeichneten Daten aus der Erfassungs Datei in die Datei NEWFILE.AVI verwendet.</span><span class="sxs-lookup"><span data-stu-id="11b5e-106">The following example uses the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro to start video capture and the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro to copy the captured data from the capture file to the file NEWFILE.AVI.</span></span>


```C++
char szNewName[] = "NEWFILE.AVI";

// Set up the capture operation.

capCaptureSequence(hWndC); 

// Capture.

capFileSaveAs(hWndC, szNewName); 
 
```



## <a name="related-topics"></a><span data-ttu-id="11b5e-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="11b5e-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11b5e-108">Verwenden der Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="11b5e-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




