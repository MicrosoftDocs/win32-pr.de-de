---
title: Erfassen von Daten
description: Erfassen von Daten
ms.assetid: de029673-9929-40f9-b29b-2598e1e5c988
keywords:
- capCaptureSequence-Makro
- capFileSaveAs-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764ff00dedcc044ed5234f8b647b08eaded35ce191bcb56e05cb35f47450677b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941298"
---
# <a name="capturing-data"></a>Erfassen von Daten

Im folgenden Beispiel werden das [**CapCaptureSequence-Makro**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) zum Starten der Videoaufnahme und das [**capFileSaveAs-Makro**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) verwendet, um die erfassten Daten aus der Aufzeichnungsdatei in die Datei NEWFILE.AVI zu kopieren.


```C++
char szNewName[] = "NEWFILE.AVI";

// Set up the capture operation.

capCaptureSequence(hWndC); 

// Capture.

capFileSaveAs(hWndC, szNewName); 
 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Video capture](using-video-capture.md)
</dt> </dl>

 

 




