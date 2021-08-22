---
title: Konfigurieren von Ausstellern und Dekomprimierern
description: Konfigurieren von Ausstellern und Dekomprimierern
ms.assetid: 9cd63470-1591-4de0-b011-d7979539d936
keywords:
- Videokomprimierungs-Manager (VCM), Konfigurieren von Patienten
- VCM (Videokomprimierungs-Manager),Konfigurieren von Patienten
- ICQueryConfigure-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a9ac7eb56c0870d7a08d8ed9fd221a2626bb6be83cc4683cd86c4bfa907db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144923"
---
# <a name="configuring-compressors-and-decompressors"></a>Konfigurieren von Ausstellern und Dekomprimierern

Im folgenden Beispiel wird das [**ICQueryConfigure-Makro**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) verwendet, um zu veranschaulichen, wie getestet wird, ob ein Zeuge das Konfigurationsdialogfeld unterstützt, und um es anzuzeigen, wenn dies der Fall ist.


```C++
// If the compressor handles a configuration dialog box, display it 
// using our application window as the parent window. 

if (ICQueryConfigure(hIC)) ICConfigure(hIC, hwndApp); 
 
```



Das folgende Beispiel zeigt, wie Sie die Zustandsdaten mithilfe des [**ICGetState-Makros**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) abrufen.


```C++
dwStateSize = ICGetStateSize(hIC);    // gets size of buffer required 
h = GlobalAlloc(GHND, dwStateSize);   // allocates buffer 
ICGetState(hIC, (LPVOID)lpData, dwStateSize);  // gets the state data 
 
// Store the state data as required. 
 
```



Das folgende Beispiel zeigt, wie Zustandsdaten mithilfe des [**ICSetState-Makros**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) wiederhergestellt werden. Zustandsdaten, die von Anwendungen wiederhergestellt werden, dürfen keine Änderungen an den Zustandsdaten enthalten, die von einem Treiber abgerufen wurden.


```C++
ICSetState(hIC, (LPVOID)lpData, dwStateSize); // sets new state data 
 
```



 

 




