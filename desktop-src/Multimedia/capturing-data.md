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
# <a name="capturing-data"></a>Erfassen von Daten

Im folgenden Beispiel wird das [**capcapturesequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) -Makro zum Starten der Video Erfassung und das [**capfilesaveas**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) -Makro zum Kopieren der aufgezeichneten Daten aus der Erfassungs Datei in die Datei NEWFILE.AVI verwendet.


```C++
char szNewName[] = "NEWFILE.AVI";

// Set up the capture operation.

capCaptureSequence(hWndC); 

// Capture.

capFileSaveAs(hWndC, szNewName); 
 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Video Erfassung](using-video-capture.md)
</dt> </dl>

 

 




