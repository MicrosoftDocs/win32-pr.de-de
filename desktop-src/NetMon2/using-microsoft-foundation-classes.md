---
description: Aufgrund des Speicherplatzes statisch verknüpfter DLLs sollten Sie die Verwendung von Microsoft Foundation Classes (MFCs) vermeiden, um einen Experten zu schreiben.
ms.assetid: 634852fd-d0e0-42a7-90af-e93cc0e4ac84
title: Verwenden von Microsoft Foundation Classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097c4baea2ec109933d52eed420042528e9eea76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757614"
---
# <a name="using-microsoft-foundation-classes"></a><span data-ttu-id="9a07b-103">Verwenden von Microsoft Foundation Classes</span><span class="sxs-lookup"><span data-stu-id="9a07b-103">Using Microsoft Foundation Classes</span></span>

<span data-ttu-id="9a07b-104">Aufgrund des Speicherplatzes statisch verknüpfter DLLs sollten Sie die Verwendung von Microsoft Foundation Classes (MFCs) vermeiden, um einen Experten zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="9a07b-104">Because of the footprint of statically linked DLLs, you should avoid using Microsoft Foundation Classes (MFCs) to write an expert.</span></span> <span data-ttu-id="9a07b-105">Wenn Sie jedoch den MFC verwenden, stellen Sie sicher, dass der Zugriff auf die MFC-DLL-Ressourcen gewährleistet ist, indem Sie den folgenden Code direkt nach dem Eintrag einschließen:</span><span class="sxs-lookup"><span data-stu-id="9a07b-105">However, if you use the MFC, ensure access to any of the MFC DLL resources by including the following code immediately upon entry:</span></span>

``` syntax
#ifdef _AFXDLL
      AFX_MANAGE_STATE(AfxGetStaticModuleState());
#endif
```

 

 



