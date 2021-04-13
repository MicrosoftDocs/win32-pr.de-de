---
title: Konfigurieren von Kompressoren und Debug
description: Konfigurieren von Kompressoren und Debug
ms.assetid: 9cd63470-1591-4de0-b011-d7979539d936
keywords:
- Videokomprimierungs-Manager (VCM), Konfigurieren von Kompressoren
- VCM (Videokomprimierungs-Manager), Konfigurieren von Kompressoren
- Icqueryconfigure-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88d388a52047a1aea7936cc494dafc0d1a2d6dec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388232"
---
# <a name="configuring-compressors-and-decompressors"></a><span data-ttu-id="d6d77-106">Konfigurieren von Kompressoren und Debug</span><span class="sxs-lookup"><span data-stu-id="d6d77-106">Configuring Compressors and Decompressors</span></span>

<span data-ttu-id="d6d77-107">Im folgenden Beispiel wird das [**icqueryconfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) -Makro verwendet, um zu veranschaulichen, wie getestet wird, ob ein-Kompressor das Konfigurations Dialogfeld unterstützt, und ob es angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d6d77-107">The following example uses the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro to demonstrate how to test whether a compressor supports the configuration dialog box and to display it if it does.</span></span>


```C++
// If the compressor handles a configuration dialog box, display it 
// using our application window as the parent window. 

if (ICQueryConfigure(hIC)) ICConfigure(hIC, hwndApp); 
 
```



<span data-ttu-id="d6d77-108">Im folgenden Beispiel wird gezeigt, wie die Zustandsdaten mit dem [**icgetstate**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) -Makro abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d6d77-108">The following example shows how to obtain the state data using the [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) macro.</span></span>


```C++
dwStateSize = ICGetStateSize(hIC);    // gets size of buffer required 
h = GlobalAlloc(GHND, dwStateSize);   // allocates buffer 
ICGetState(hIC, (LPVOID)lpData, dwStateSize);  // gets the state data 
 
// Store the state data as required. 
 
```



<span data-ttu-id="d6d77-109">Im folgenden Beispiel wird gezeigt, wie Zustandsdaten mit dem [**icsetstate**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) -Makro wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6d77-109">The following example shows how to restore state data using the [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macro.</span></span> <span data-ttu-id="d6d77-110">Von Anwendungen wiederhergestellte Zustandsdaten sollten keine Änderungen an den Zustandsdaten enthalten, die von einem Treiber abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d6d77-110">State data restored by applications should not contain any changes to the state data obtained from a driver.</span></span>


```C++
ICSetState(hIC, (LPVOID)lpData, dwStateSize); // sets new state data 
 
```



 

 




